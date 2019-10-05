---
title: "Ebola virus Nanopore sequencing protocol | amplicon, native barcoding"
keywords: protocol
layout: document
last_updated: October 5, 2019
tags: [protocol] 
permalink: ebov/ebov-it-setup.html
folder: ebov
title_text: "Ebola virus bioinformatics environment setup"
subtitle_text: "Nanopore | bioinformatics"
document_name: "ARTIC-EBOV-ITSetup"
version: v2.0.0
creation_date: 2019-10-05
forked_from: 
author: Nick Loman, Andrew Rambaut
citation: "Loman *et al.* In Prep."
---

{% include callout.html
type='default'
content='**Overview:** Instructions for setting up the laptop computing environment for running the MinION sequencer and performing the bioinformatics and downstream phylogenetic analyses.'
%}

<br />

This document is part of the Ebola virus Nanopore sequencing protocol package:
: [http://artic.network/ebov/](http://artic.network/ebov/)

#### Related documents:

Ebola virus Nanopore bioinformatics protocol:
: [http://artic.network/ebov/ebov-bioinformatics-sop.html](http://artic.network/ebov/ebov-bioinformatics-sop.html)

Phylogenetic analysis and visualization:
: [http://artic.network/ebov/ebov-phylogenetics-sop.html](http://artic.network/ebov/ebov-phylogenetics-sop.html)


<br /><br /><br />

{% include wellcome-trust.html %}

<div class="pagebreak"> </div>

## Preparation

#### Equipment required:

Laptop requirements for MinION:
: Intel i7 or Xeon processor
: 16GB RAM
: 1TB SSD hard drive
: USB 3
: Full Oxford Nanopore Technologies [lab and computing requirements are here](https://nanoporetech.com/sites/default/files/s3/MinION-Computer-Requirements-March-17_Final.pdf).

Optional:
: sNVIDIA CUDA compatible GPU

## Software Setup

These protocols instructions assume a 64-bit UNIX, Linux or similar environment. This could be Mac OS X (Yosemite or later), Linux (e.g., Ubuntu 16 or later), or Windows 10  Subsystem for Linux. It assumes familiarity with a UNIX-like *bash* command-line. 

The steps in this document should be done and tested prior to sequencing, particularly if this will be done in an environment without internet access or where this is slow or unreliable. Once this is done, the bioinformatics and phylogenetics protocols can be performed largely off-line. 

### Conda

Software will be installed using [Conda](https://conda.io/) -- a cross-platform package and dependency installer.
 
For Conda installation instructions for your operating system go to: [https://conda.io/docs/user-guide/install/](https://conda.io/docs/user-guide/install/). We suggest installing the `Miniconda` version which is relatively small and quick to install. 

> *NOTE:* Install the `64-bit Python 3.7` version of Miniconda

### Installing ARTIC Ebola virus specific data and software

Install the ARTIC Ebola virus data and software repository:

```bash
git clone https://github.com/artic-network/artic-ebov.git
```

Create a custom Conda environment for running software. Although not strictly necessary this will prevent any conflicts with other similar software installed and can be readily removed. This may take some time as it will install the required packages and all their dependencies.

```bash
conda env create -f artic-ebov/environment.yml
```

> *NOTE:* This command can take a while depending on the speed of the internet connection.

You can use this command to activate the environment: 

```
conda activate artic-ebov
```

and then deactivate it again using this:

```bash
conda deactivate
```

The artic environment can be removed using this:

```bash
conda remove --name artic-ebov --all
```

### Installing Oxford Nanopore MinKNOW and basecalling software

The software for running the MinION and basecalling can be downloaded from the [Oxford Nanopore Technologies Community site](https://community.nanoporetech.com). Log in to find the `Software Downloads` button. Download `MinION Software` (currently v19.06.8) and `Guppy` (currently v2.3.1) appropriate to the system being used. Follow the `Installation guide` for each package.

`MinKNOW` is a graphical user-interface programme that will be installed in the application area of the system.

`Guppy` is a set of command-line programs that will be available on your path once installed. 
