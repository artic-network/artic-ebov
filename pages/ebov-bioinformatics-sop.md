---
title: "Ebola virus Nanopore sequencing bioinformatics protocol | amplicon, native barcoding"
keywords: protocol
layout: document
last_updated: May 18, 2018
tags: [protocol]
summary:
permalink: ebov/ebov-bioinformatics-sop.html
folder: ebov
title_text: "Ebola virus bioinformatics protocol"
subtitle_text: "Nanopore | bioinformatics"
document_name: "ARTIC-EBOV-bioinformaticsSOP"
version: v1.0.0
creation_date: 2018-05-26
revision_date: 
forked_from: 
author: Nick Loman
citation: "Loman *et al.* In Prep."
---

{% include callout.html
type='default'
content='**Overview:** A complete bioinformatics protocol to take the output from the [sequencing protocol](/ebov/ebov-seq-sop.html) to consensus genome sequences. Includes basecalling, de-multiplexing, mapping, polishing and consensus generation.
'
%}

<br />

This document is part of the Ebola virus Nanopore sequencing protocol package:
: [http://artic.network/ebov/](http://artic.network/ebov/)

#### Related documents:

Ebola virus Nanopore sequencing protocol:
: [http://artic.network/ebov/ebov-seq-sop.html](/ebov/ebov-seq-sop.html)

Setting up the laptop computing environment using Conda:
: [http://artic.network/ebov/ebov-it-setup.html](http://artic.network/ebov/ebov-it-setup.html)

Phylogenetic analysis and visualization:
: [http://artic.network/ebov/ebov-phylogenetics-sop.html](http://artic.network/ebov/ebov-phylogenetics-sop.html)


<br /><br /><br />

{% include wellcome-trust.html %}

<div class="pagebreak"> </div>

## Preparation

Set up the computing environment as described here in this document: [ebov-it-setup](ebov-it-setup.html). This should be done and tested prior to sequencing, particularly if this will be done in an environment without internet access or where this is slow or unreliable. Once this is done, the bioinformatics can be performed largely off-line. 

## Nanopore Bioinformatics

Activate the ARTIC environment:

```bash
source activate artic-ebov
```

### Basecalling with Albacore (MinION on laptop)

Run the Albacore basecaller on the new MinION run folder:

```bash
read_fast5_basecaller.py -c r94_450bps_linear.cfg -i /path/to/reads -s run_name -o fastq -t 4 -r --barcoding
````

You need to substitute `/path/to/reads` to the folder where the FAST5 files from your
run are. Common locations are:

   - Mac: ```/Library/MinKNOW/data/reads/run_name```
   - Linux: ```/var/lib/MinKNOW/data/reads```
   - Windows ```c:/data/reads```
   
This will create a folder called `run_name` with the base-called reads in it.

### Consensus sequence generation

Gather up the FASTQ output from Albacore:

```bash
artic gather --min-length 400 --max-length 700 --prefix run_name basecalled_reads
```

Here `basecalled_reads` should be the folder in which Albacore put the base-called reads (i.e., `run_name` from the command above).

We use a length filter here of between 400 and 700 to remove obviously chimeric reads.

> **Basecalling using MinIT or GridION**
> 
> If running on MinIT or GridION and you have used Guppy to basecall through Dogfish, instead you can do:
> 
> ```bash
> artic gather --guppy --min-length 400 --max-length 700 --prefix run_name /data/basecalled/path/to/reads
> ```

You will now have a file called: ``run_name_all.fastq``
and a file called ``run_name_sequencing_summary.txt``, 
as well as individual files for each barcode (if previously demultiplexed).

### Demultiplex with Porechop with stringent settings

This stage is obligatory, even if you have already demultiplexed with Albacore, due to
significant barcoding misassignments that can confound results:

```bash
artic demultiplex --threads 4 run_name_all.fastq
```

Now you will have new files called:

```bash
run_name_all_BC01.fastq
run_name_all_BC02.fastq
run_name_all_BC03.fastq
```

### Create the nanopolish index (once per sequencing run, not per sample)

```bash
nanopolish index -s run_name_sequencing_summary.txt -d /path/to/reads run_name_all.fastq
```

Again, alter ``/path/to/reads`` to point to the original location of the FAST5 files.

## Run the MinION pipeline

For each barcode you wish to process:

```bash
artic minion --normalise 200 --threads 4 --scheme-directory artic-ebov/primer-schemes --read-file run_name_final_NB01.fastq --nanopolish-read-file run_name_all.fastq ZaireEbola/V2 samplename
```

Replace ``samplename`` as appropriate:

## Output files

   * ``samplename.primertrimmed.bam`` - BAM file for visualisation after primer-binding site trimming
   * ``samplename.vcf`` - detected variants in VCF format
   * ``samplename.variants.tab`` - detected variants
   * ``samplename.consensus.fasta`` - consensus sequence

