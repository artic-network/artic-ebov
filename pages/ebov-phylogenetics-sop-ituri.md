---
title: "Ebola virus real-time phylogenetics"
keywords: protocol
layout: document
last_updated: Dec 12, 2019
tags: [protocol]
summary:
permalink: ebov/ebov-phylogenetics-sop.html
folder: ebov
title_text: "Ebola virus phylogenetic analysis protocol"
subtitle_text: "Nanopore | bioinformatics"
document_name: "ARTIC-IturiEBOV-phylogeneticsSOP"
version: v1.0.0
creation_date: 2019-12-12
forked_from: 
author: Andrew Rambaut
citation: "Loman *et al.* In Prep."
---

{% include callout.html
type='default'
content='**Overview:** An analysis protocol for an initial phylogenetic analysis of consensus genomes. Includes alignment, phylogeny estimation and visualization.'
%}

<br />

This document is part of the Ebola virus Nanopore sequencing protocol package:
: [http://artic.network/ebov/](http://artic.network/ebov/)

#### Related documents:

Ebola virus Nanopore sequencing protocol:
: [http://artic.network/ebov/ebov-seq-sop.html](/ebov/ebov-seq-sop.html)

Setting up the laptop computing environment using Conda:
: [http://artic.network/ebov/ebov-it-setup.html](http://artic.network/ebov/ebov-it-setup.html)

Ebola virus Nanopore bioinformatics protocol:
: [http://artic.network/ebov/ebov-bioinformatics-sop.html](http://artic.network/ebov/ebov-bioinformatics-sop.html)

<br /><br /><br />

{% include wellcome-trust.html %}

<div class="pagebreak"> </div>

## Preparation

Set up the computing environment as described in this document: [ebov-it-setup](ebov-it-setup.html)

This protocol also assumes that the setup and installation of the bioinformatics protocol has been performed as described in this document: [ebov-bioinformatics-sop](ebov-bioinformatics-sop.html) .

### Installing software

Activate the ARTIC Conda environment:

```bash
source activate artic-ebov
```

### Reference genomes

`genomes_462_2019-12-09.aln.fasta` - An alignment of 462 complete or largely-complete genomes from North Kivu and Ituri of DRC. 

[This data is provided by the INRB on their GitHub.](https://github.com/inrb-drc/ebola-nord-kivu)

This is a FASTA format file which contains a multiple alignment of the 462 genomes. 

## Building a multiple alignment

Use [MUSCLE](http://www.drive5.com/muscle/) multiple alignment software to align the new genome consensus sequences to the existing reference genome alignment:

```bash
muscle -profile -in1 genomes_462_2019-12-09.aln.fasta -in2 new_genomes.fasta -fastaout new_genomes.aligned.fasta
```

This methods keeps the existing alignment and pair-wise aligns the new sequence to it.   

> **Note:** The `profile` option is much quicker than doing a full multiple alignment but could be problematic if the new genome is divergent from all the reference genomes. It may be worth doing a full re-alignment.
 
- Optional step -- To re-align an existing alignment:
```bash
muscle -in new_genomes.aligned.fasta -out new_genomes.re-aligned.fasta -refine
```

## Inferring a phylogenetic tree

We will infer a phylogenetic tree using maximum likelihood (ML) with [iqTree](http://www.iqtree.org). 
This will use the default nucleotide model (HKY with gamma distributed site rate heterogeneity):

```bash
iqtree -m HKY+G -pre new_genomes.iqtree -s new_genomes.aligned.fasta
```
   
The `-pre new_genomes.iqtree` option defines what the output files will be called. 
The output goes into six files with various extensions, but the tree will be in : `new_genomes.iqtree.treefile`. 
The `-fast` option will produce a tree much faster but it will be more approximate.

## View the phylogenetic tree

We suggest using [FigTree](https://github.com/rambaut/figtree/) for interactive tree viewing and interpretation.

The lastest version can be downloaded from here:

```bash
wget https://github.com/rambaut/figtree/releases/download/v1.4.4/FigTree_v1.4.4.tgz
tar xfz FigTree_v1.4.4.tgz
```

To open the tree in FigTree:

```bash
java -jar FigTree_v1.4.4/lib/figtree.jar new_genomes.iqtree.treefile
```

