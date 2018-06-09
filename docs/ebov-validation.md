---
title: Ebola virus Nanopore validation results
keywords: ebov
last_updated: May 24, 2018
tags: [ebov]
sidebar: artic_sidebar
permalink: ebov/ebov-validation.html
toc: false
hide_sidebar: true
folder: ebov
---

## Background

The ongoing outbreak of Ebola virus in the Democratic Republic of Congo has highlighted
the need for rapid sequencing ability to help with source attribution and aid epidemiological
investigations (including environmental reservoirs).

During real-time sequence surveillance of Ebola in Guinea and Sierra Leone in 2015-2016
we employed a PCR amplicon schemes specifically targeting the Makona strain of Ebola. 
Because this scheme was designed against Makona, we expect that this scheme may not be
optimal due to sequence diversity.

Therefore we devised a new scheme using all available Ebola virus sequences and then
sequenced Zaire Ebolavirus RNAs at Public Health England, Porton Down. We selected viruses
from three separate outbreaks in order to gain confidence in the scheme's ability to sequence
divergent lineages.

This validation acted as a test of our recently published standard operating procedure.

## Primer pairs

Sequence coverage (log scale) at 30 minute and 2 hour time points for three different trains:

![Coverage by primer pair](/images/ebov-validation/coverage.png)

## Results

Phylogenetic tree inference (NJ, HKY performed using Geneious 11) of the three consensus
sequences in context:

### Mayinga strain

![Mayinga tree](/images/ebov-validation/Mayinga-tree.png)

### Makona strain

![Makona tree](/images/ebov-validation/Makona-tree.png)

### Kikwit strain

![Kikwit tree](/images/ebov-validation/Kikwit-tree.png)

Consensus sequences for 2 hour run:

[/artic/ebov-consensus-2h.fasta](https://artic.s3.climb.ac.uk/ebov-consensus-2h.fasta)

## Data availability

Data hosting provided by MRC CLIMB.

30 minute bulk file:

[artic/bulkfiles/nick_W54_55SU1_SUW_20180523_FAH83694_MN21030_sequencing_run_ZEBOV_3samples_NB_87702.fast5](https://artic.s3.climb.ac.uk/bulkfiles/nick_W54_55SU1_SUW_20180523_FAH83694_MN21030_sequencing_run_ZEBOV_3samples_NB_87702.fast5) [4.1Gb]

2 hour bulk file:

[artic/bulkfiles/nick_W54_55SU1_SUW_20180523_FAH83694_MN21030_sequencing_run_ZEBOV_3Samples_NB_58439.fast5](https://artic.s3.climb.ac.uk/bulkfiles/nick_W54_55SU1_SUW_20180523_FAH83694_MN21030_sequencing_run_ZEBOV_3Samples_NB_58439.fast5) [20.5Gb]

## Credits

   - Babak Afrough (Public Health England) for sample preparation, and laboratory and bioinformatics assistance
   - Luke Meredith (University of Cambridge) for sequencing library preparation

## Acknowledgements

We are grateful to Miles Carroll, Steve Pullan, Richard Vipond and Roger Hewson (Public Health England)
for assistance with this validation project and Ben Gannon (RST/Public Health England) for supplying
the flowcell.

{% include icon-callout.html
type='default'
file='wellcome-logo-red-small.png'
url='http://wellcome.ac.uk'
width='17%'
title='Funded by the Wellcome Trust'
subtitle='Collaborators Award 206298/Z/17/Z --- <a href="artic.network">ARTIC network</a>'
%}

{% include links.html %}
