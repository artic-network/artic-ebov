---
title: Ebola virus Nanopore sequencing resources
keywords: ebov
last_updated: May 24, 2018
tags: [ebov]
summary: A collection of resources and documents for the genome sequencing of Ebola virus (EBOV) using Oxford Nanopore Technology's MinION platform. Includes a tiled primer scheme, complete lab protocol & equipement/reagent list.
sidebar: artic_sidebar
permalink: ebov/
toc: false
hide_sidebar: true
folder: ebov
---

### Background

The ongoing outbreak of [Ebola virus in the Democratic Republic of Congo](http://www.who.int/emergencies/crises/cod/en/) has highlighted the need for rapid sequencing ability to help with source attribution and to aid epidemiological investigations (including environmental reservoirs).



> These documents and resources are provided in the spirit of Open Science, to foster collaboration and sharing, and to benefit public health response to outbreaks. All written material is provided under the [Creative Commons Attribution (BY) license](http://creativecommons.org/licenses/by/4.0/) which allows unrestricted sharing and modification of the material as long as appropriate credit is given.
>
> We  encourage the modification, improvement and re-purposing of these methods and protocols (under the permissive terms of the CC BY license). We would be happy to host modifications on this website or encourage posting to Open Science platforms such as [http://virological.org/](http://virological.org/).
>
> We also ask that use of this resource is credited in publications or reports to allow us to report this impact to our funding bodies.

### Resources and documents

Pan-Ebola virus primer scheme:
: > The primer scheme used in the sequencing protocol generated using [Primal Scheme](http://http://primal.zibraproject.org).
: [https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V3](https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V3)

<br />
Ebola virus Nanopore sequencing kit-list:
: > A costed tick-list of equipment, reagents and consumables for a portable Nanopore sequencing lab.
: Web: [http://artic.network/ebov/ebov-seq-kit.html](/ebov/ebov-seq-kit.html)
: PDF: [ARTIC-EBOV-seqKit-v2.0.0.pdf](/files/ARTIC-EBOV-seqKit-v2.0.0.pdf)

<br />
Ebola virus Nanopore sequencing protocol:
: > A complete step by step protocol that covers primers, amplicon preparation and clean-up, a single-tube protocol to barcode and adaptor ligate the library, and running minION.
: Web: [http://artic.network/ebov/ebov-seq-sop.html](/ebov/ebov-seq-sop.html)
: PDF: [ARTIC-EBOV-seqSOP-v2.0.0.pdf](/files/ARTIC-EBOV-seqSOP-v2.0.0.pdf)

<br />
Setting up the laptop computing environment using Conda:
: > This document describes setting up a laptop with the software and environment needed to undertake off-line Nanopore bioinformatics and phylogenetic analysis.
: Web: [http://artic.network/ebov/ebov-it-setup.html](/ebov/ebov-it-setup.html)
: PDF: [ARTIC-EBOV-ITSetup-v1.0.0.pdf](/files/ARTIC-EBOV-ITSetup-v1.0.0.pdf)

<br />
Ebola virus Nanopore bioinformatics protocol:
: > A complete bioinformatics protocol to take the output from the [sequencing protocol](/ebov/ebov-seq-sop.html) to consensus genome sequences. Includes basecalling, de-multiplexing, mapping, polishing and consensus generation.
: Web: [http://artic.network/ebov/ebov-bioinformatics-sop.html](/ebov/ebov-bioinformatics-sop.html)
: PDF: [ARTIC-EBOV-bioinformaticsSOP-v1.0.0.pdf](/files/ARTIC-EBOV-bioinformaticsSOP-v1.0.0.pdf)

<br />
Phylogenetic analysis and visualization:
: > An analysis protocol for an initial phylogenetic analysis of consensus genomes. Includes alignment, phylogeny estimation and visualization.
: Web: [http://artic.network/ebov/ebov-phylogenetics-sop.html](/ebov/ebov-phylogenetics-sop.html)
: PDF: [ARTIC-EBOV-phylogeneticsSOP-v1.0.0.pdf](/files/ARTIC-EBOV-phylogeneticsSOP-v1.0.0.pdf)

<hr />
### Data

Ebola virus validation results:
: > Describes validation experiments using this protocol on reference strains of EBOV. MinION 'bulk files' are available to replay the sequencing run.
: [http://artic.network/ebov/ebov-validation.html](/ebov/ebov-validation.html)

<br />
An alignment of 35 complete or nearly-complete genomes spaning 1976-2014.
: > This the reference genome alignment used to create the [pan-Ebola virus primer scheme](https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V2) and are also used in the [phylogenetic protocol](/ebov/ebov-phylogenetics-sop.html).
: [35 EBOV genome alignment - FASTA file.](https://github.com/artic-network/ebov/blob/master/reference_genomes/ebov-reference-genomes-35.fasta)
: [Maximum likelihood phylogeny - tree file.](https://github.com/artic-network/ebov/blob/master/reference_genomes/ebov-reference-genomes-35.phyml.tree)
: {% include image.html prefix="/pages/artic-ebov" file="ebov-reference-genomes-35.phyml.tree.png" caption="Maximum likelihood tree of 35 reference genomes." %}

{% include icon-callout.html
type='default'
file='wellcome-logo-red-small.png'
url='http://wellcome.ac.uk'
width='17%'
title='Funded by the Wellcome Trust'
subtitle='Collaborators Award 206298/Z/17/Z --- <a href="artic.network">ARTIC network</a>'
%}

{% include links.html %}
