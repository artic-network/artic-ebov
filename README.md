# ARTIC-EBOV

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
: [https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V2](https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V2) 

<br />
Ebola virus Nanopore sequencing kit-list:
: > A costed tick-list of equipment, reagents and consumables for a portable Nanopore sequencing lab. 
: Web: [http://artic.network/ebov/ebov-seq-kit.html](/ebov/ebov-seq-kit.html)
: PDF: [ARTIC-EBOV-seqKit-v1.0.0.pdf](documents/ARTIC-EBOV-seqKit-v1.0.0.pdf)

<br />
Ebola virus Nanopore sequencing protocol:
: > A complete step by step protocol that covers primers, amplicon preparation and clean-up, a single-tube protocol to barcode and adaptor ligate the library, and running minION.
: Web: [http://artic.network/ebov/ebov-seq-sop.html](http://artic.network/ebov/ebov-seq-sop.html)
: PDF: [ARTIC-EBOV-seqSOP-v1.0.0.pdf](documents/ARTIC-EBOV-seqSOP-v1.0.0.pdf)

<br />
Setting up the laptop computing environment using Conda:
: > This document describes setting up a laptop with the software and environment needed to undertake off-line Nanopore bioinformatics and phylogenetic analysis.
: Web: [http://artic.network/ebov/ebov-it-setup.html](http://artic.network/ebov/ebov-it-setup.html)
<!-- : PDF: --> 

<br />
Ebola virus Nanopore bioinformatics protocol:
: > A complete bioinformatics protocol to take the output from the [sequencing protocol](http://artic.network/ebov/ebov-seq-sop.html) to consensus genome sequences. Includes basecalling, de-multiplexing, mapping, polishing and consensus generation.
: Web: [http://artic.network/ebov/ebov-bioinformatics-sop.html](http://artic.network/ebov/ebov-bioinformatics-sop.html)
<!-- : PDF: --> 

<br />
Phylogenetic analysis and visualization:
: > An analysis protocol for an initial phylogenetic analysis of consensus genomes. Includes alignment, phylogeny estimation and visualization.
: Web: [http://artic.network/ebov/ebov-phylogenetics-sop.html](http://artic.network/ebov/ebov-phylogenetics-sop.html)
<!-- : PDF: --> 

<hr />
### Data

Ebola virus validation results:
: > Describes validation experiments using this protocol on reference strains of EBOV. MinION 'bulk files' are available to replay the sequencing run.
: [http://artic.network/ebov/ebov-validation.html](http://artic.network/ebov/ebov-validation.html)

<br />
An alignment of 35 complete or nearly-complete genomes spaning 1976-2014.
: > This the reference genome alignment used to create the [pan-Ebola virus primer scheme](https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V2) and are also used in the [phylogenetic protocol](/ebov/ebov-phylogenetics-sop.html).
: [35 EBOV genome alignment - FASTA file.](reference_genomes/ebov-reference-genomes-35.fasta)
: [Maximum likelihood phylogeny - tree file.](reference_genomes/ebov-reference-genomes-35.phyml.tree)
: [Maximum likelihood phylogeny - PNG image.](reference_genomes/ebov-reference-genomes-35.phyml.tree.png)
