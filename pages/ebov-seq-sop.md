---
title: "Ebola virus Nanopore sequencing protocol | amplicon, native barcoding"
keywords: protocol
layout: document
last_updated: May 18, 2018
tags: [protocol]
summary:
permalink: ebov/ebov-seq-sop.html
folder: ebov
title_text: "Ebola virus sequencing protocol"
subtitle_text: "Nanopore | amplicon | native barcoding"
document_name: "ARTIC-EBOV-seqSOP"
version: v2.0.0
creation_date: 2018-05-17
revision_date: 2018-05-27
forked_from: doi:10.1038/nprot.2017.066
author: Luke Meredith
citation: "Meredith, Quick *et al.* In Prep."
---

{% include callout.html
type='default'
content='**Overview:** The following protocol is adapted from the methods of [Quick et al. (2017) *Nature Protocols* **12:** 1261–1276 doi:10.1038/nprot.2017.066](http://doi.org/10.1038/nprot.2017.066) and covers primers, amplicon preparation and clean-up, then uses a single-tube protocol to barcode and adaptor ligate the library, before running minION.'
%}

<br />

This document is part of the Ebola virus Nanopore sequencing protocol package:
: [http://artic.network/ebov/](http://artic.network/ebov/)

#### Related documents:

Ebola primer scheme:
: [https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V3](https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V3)

Ebola virus Nanopore sequencing protocol:
: [http://artic.network/ebov/ebov-seq-sop.html](http://artic.network/ebov/ebov-seq-sop.html)

Ebola virus Nanopore sequencing kit-list:
: [http://artic.network/ebov/ebov-seq-kit.html](http://artic.network/ebov/ebov-seq-kit.html)

<br /><br /><br />

{% include wellcome-trust.html %}

<div class="pagebreak"> </div>

## Preparation

#### Equipment required:

   |---:|:---
   |2| Portable nucleic acid preparation hood or equivalent
   |1| 12V vortex
   |1| Sprout portable centrifuge
   |1| P1000 Eppendorf pipette
   |1| P100 Eppendorf pipette
   |1| P10 Eppendorf pipette
   |1| 1.5mL/0.6mL convertible tube rack
   |1| Quantus Fluorometer
   |1| miniPCR machine.
   |1| Heat block
   |1| Magnetic rack
{: .compact}

#### Consumables required:


   |---:|:---
   || SuperScript IV Reverse Transcriptase
   || Q5 Hot Start High-Fidelity 2X Master Mix
   || Ebola Zaire Primers V3
   || NEBNext Ultra II End Repair/dA-Tailing Module
   || Blunt/TA Ligase Master Mix
   || Aline PCRCLEAN DX 50ml
   || Nanopore Ligation Sequencing Kit 1D
   || Nanopore Native Barcoding Expansion Kit
   || Nanopore R9.4.1 Flow cell
   || 1.5mL Eppendorf Tubes
   || 0.2mL 8-strip Tubes
   || 50mL Falcon Tubes
   || 0.5ml PCR Tubes
   || QuantiFluor ONE dsDNA System
   || Nuclease-free water
   || 70% Ethanol
   || P1000 pipette tips
   || P100 pipette tips
   || P10 long-reach pipette tips
   || Paper towelling
   || Clinical waste sharps containers
{: .compact}

#### Safety, containment and contamination recommendations

   |---:|:---
   || Back-tie hydrophobic lab gown
   || Gloves
   || UV light sterilizers
   || MediPal Decontamination wipes
   || DNAway and RNAse Zap reagent
{: .compact}

<div class="pagebreak"> </div>

## Protocol

### Part 1: cDNA synthesis with Superscript IV reverse transcriptase

> **NOTE ON HOOD PREPARATION:** To prevent cross contamination of both the sample and other reagents, this should be carried out in the SAMPLE PREPARATION HOOD, which is pre-sterilised with UV and treated with MediPal wipes, DNAway and RNAseZap reagent. Wipe down the hood with each sequentially, allowing 5 minutes for drying between each. Pipettes should also be treated in the same way, and UV treated for 30 mins between library preparations.

1. Set up the following reaction:

    |---|---
    |50&micro;M random hexamers | | 1&micro;L   
    |10mM dNTPs mix (10mM each)| 1&micro;L   
    |Template RNA | 11&micro;L   
    |TOTAL | 12&micro;L

> **NOTE:** Viral RNA input from a clinical sample should be between Ct 18-35. If Ct is between 12-15, then dilute the sample 100-fold in water, if between 15-18 then dilute 10-fold in water. This will reduce the likelihood of PCR-inhibition.

2. Gently mix (avoid vortexing) then pulse spin the tube to ensure maximum contact with the thermal cycler.
3. Incubate the reaction as follows:

    |---|---|---
    | Denaturation | 65&deg;C | 5 mins   
    | Primer annealing | Ice | 1 mins   

4. Add the following to the annealed template RNA:

    |---|---
    |SSIV Buffer | | 4&micro;L   
    |100mM DTT | 1&micro;L   
    |RNaseOUT RNase Inhibitor | 1&micro;L   
    |SSIV Reverse Transcriptase | 1&micro;L  
    |TOTAL | 20&micro;L    

5. Gently mix (avoid vortexing) then pulse spin the tube to ensure maximum contact with the thermal cycler.
6. Incubate the reaction as follows:

    |---|---|---
    | Extension | 42&deg;C | 90 mins   
    | Inactivation | 70&deg;C | 10 mins

7. cDNA is now ready for amplicon generation.

<div class="pagebreak"> </div>

### Part 2: Ebola Amplicon Preparation

> **NOTE ON HOOD PREPARATION:** To prevent cross contamination of both the sample and other reagents, this should be carried out in the MASTERMIX HOOD, which is pre-sterilised with UV and treated with MediPal wipes, DNAway and RNAseZap reagent. Wipe down the hood with each sequentially, allowing 5 minutes for drying between each. Pipettes should also be treated in the same way, and UV treated for 30 mins between library preparations.

#### Primer dilution and preparation

1. Ebola primers for this protocol were designed using [Primal Scheme](http://primal.zibraproject.org) and generate overlapping 400nt amplicons. Primer names and dilutions are listed in the table below.

2. Primers should be prepped and aliquoted PRIOR TO DEPARTURE in a STERILE PCR CABINET. At NO stage should primers or PCR reagents be anywhere near the template or amplicons until use.

3. Resuspend lyophilised primers at a concentration of 100&micro;M each

4. Generate primer pool stocks by adding 5&micro;L of each primer pair to a 1.5mL Eppendorf labelled “Pool 1, 100&micro;M” or “Pool 2, 100&micro;M”. Total volume should be 505&micro;L of Pool 1 and 530&micro;L of Pool 2. This is a 10x stock of each primer pool.

5. Dilute this primer pool 1:10 in molecular grade water, to generate 10&micro;M primer stocks. Recommend that multiple aliquots of each primer pool are made to account for any risks of degradation of contamination.

<div class="pagebreak"> </div>

  | Name         | Sequence                         | Name          | Sequence                 | Pool | [Stock] |
  |-------------:|----------------------------------|--------------:|--------------------------|------|---------|
  | Ebov-10-Pan_1_LEFT | `TGTGTGCGAATAACTATGAGGAAGA` | Ebov-10-Pan_1_RIGHT | `TTTCCAATGTTTTACCCCAAGCTTT` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_1_RIGHT_alt1 | `TTTCCAATGCTTTACCCCAAGCTTT` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_1_RIGHT_alt2 | `TTTCCAATGTTTTACCCCAAGTTTT` | 1 | 100&micro;M |
  | Ebov-10-Pan_2_LEFT | `CAAGCAAGATTGAGAATTAACCTTGGT` | Ebov-10-Pan_2_RIGHT | `ATCTCCCTGGTACGCATGATGA` | 2 | 100&micro;M |
  | Ebov-10-Pan_2_LEFT_alt1 | `CAAGCAAGATTGAGAATTAACCTTGAT` | Ebov-10-Pan_2_RIGHT_alt1 | `ATCTCCTTGGTACGCATGATGA` | 2 | 100&micro;M |
  | Ebov-10-Pan_3_LEFT | `GGCCTTTGAAGCAGGTGTTGAT` | Ebov-10-Pan_3_RIGHT | `TCAGTCCTTGCTCTGCATGTAC` | 1 | 100&micro;M |
  | Ebov-10-Pan_4_LEFT | `CCTTTGCAAGTCTATTCCTTCCGA` | Ebov-10-Pan_4_RIGHT | `CTGAGTGCAGCCTTAAAGGAGT` | 2 | 100&micro;M |
  | Ebov-10-Pan_4_LEFT_alt1 | `CTTTTGCAAGTCTATTCCTTCCGA` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_5_LEFT | `AGTTCGTCTCCATCCTCTTGCA` | Ebov-10-Pan_5_RIGHT | `CTGGAAGCTGATTTCGTTCTTTTTCT` | 1 | 100&micro;M |
  | Ebov-10-Pan_6_LEFT | `GAGTCTCGCGAACTTGACCATC` | Ebov-10-Pan_6_RIGHT | `TCCTCGTCGTCCTCGTCTAGAT` | 2 | 100&micro;M |
  | Ebov-10-Pan_6_LEFT_alt1 | `GAATCTCGCGAACTTGACCATC` | Ebov-10-Pan_6_RIGHT_alt1 | `TCCTCATCGTCCTCGTCTAGAT` | 2 | 100&micro;M |
  | Ebov-10-Pan_7_LEFT | `AGCTACGGCGAATACCAGAGTT` | Ebov-10-Pan_7_RIGHT | `GTCCCTGTCCTGCTCTTCATCA` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_7_RIGHT_alt1 | `GTCCCTGTCCTGTTCTTCATCA` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_7_RIGHT_alt2 | `GTCCCTGTCCTGTTCTTCATCG` | 1 | 100&micro;M |
  | Ebov-10-Pan_8_LEFT | `TTAACGAAGAGGCAGACCCACT` | Ebov-10-Pan_8_RIGHT | `TTCCTCTTCAAGGGAGTCTGGA` | 2 | 100&micro;M |
  | Ebov-10-Pan_8_LEFT_alt1 | `TCAACGAAGAGGCAGACCCACT` | Ebov-10-Pan_8_RIGHT_alt1 | `TTCCTCTTCAAGGGAGTCCGGA` | 2 | 100&micro;M |
  | Ebov-10-Pan_9_LEFT | `GTGACAACACCCAGTCAGAACA` | Ebov-10-Pan_9_RIGHT | `TCTTCCTGTTTTCGTTCCTTGACT` | 1 | 100&micro;M |
  | Ebov-10-Pan_9_LEFT_alt1 | `GTGACAACACCCAGCCAGAACA` | Ebov-10-Pan_9_RIGHT_alt1 | `TCTTCCTGTTTGCGTTCCTTGACT` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_9_RIGHT_alt2 | `TCTTCCTGTTTGCGTTTCTTGACT` | 1 | 100&micro;M |
  | Ebov-10-Pan_10_LEFT | `ACAATGGGATGATTCAACCGACA` | Ebov-10-Pan_10_RIGHT | `TCGAGTGCTAGAGAATTCAATTGACG` | 2 | 100&micro;M |
  | Ebov-10-Pan_10_LEFT_alt1 | `ATAATGGGATGATTTAACCGACA` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_11_LEFT | `ACCTACTAGCCTGCCCAACATT` | Ebov-10-Pan_11_RIGHT | `AATTGGGTCCGTTTGGGTTTGA` | 1 | 100&micro;M |
  | Ebov-10-Pan_11_LEFT_alt1 | `ACCTACTAGCCTACCCAACATT` | Ebov-10-Pan_11_RIGHT_alt1 | `AATTGGATCCGTTTGGGTTTGA` | 1 | 100&micro;M |
  | Ebov-10-Pan_12_LEFT | `CCCAAATGCAACAAACGAAGCC` | Ebov-10-Pan_12_RIGHT | `TCAATCTTACCCCGAATCGCAC` | 2 | 100&micro;M |
  | Ebov-10-Pan_12_LEFT_alt1 | `CCCAAATGCAACAAACAAAGCC` | Ebov-10-Pan_12_RIGHT_alt1 | `TCAATCTTACCCCGAATTGCAC` | 2 | 100&micro;M |
  | Ebov-10-Pan_13_LEFT | `TATTGGGCCGAACATGGTCAAC` | Ebov-10-Pan_13_RIGHT | `TGACAGGTGGAGCAGCATCTTG` | 1 | 100&micro;M |
  | Ebov-10-Pan_13_LEFT_alt1 | `TATTGGGCTGAACATGGTCAAC` |  |  | 1 | 100&micro;M |
  | Ebov-10-Pan_14_LEFT | `CATTCATGCTGAGTTCCAGGCC` | Ebov-10-Pan_14_RIGHT | `GCGAGATATGAACAATTTTATCTTGGTCG` | 2 | 100&micro;M |
  |  |  | Ebov-10-Pan_14_RIGHT_alt1 | `GCGAGATAAGGACAATTTTATCTTGGTCG` | 2 | 100&micro;M |
  |  |  | Ebov-10-Pan_14_RIGHT_alt2 | `GCGAGATAAGAACAATTTTATCTTGGTCG` | 2 | 100&micro;M |
  | Ebov-10-Pan_15_LEFT | `TGAGTATCAGCCCTGGATAATATAAGTCA` | Ebov-10-Pan_15_RIGHT | `TCGATGGAGTGTCCCCATTGAC` | 1 | 100&micro;M |
  | Ebov-10-Pan_15_LEFT_alt1 | `TGAGTATCAGCCCTAGATAATATAAGTCA` | Ebov-10-Pan_15_RIGHT_alt1 | `TCGATGGAGTGTCTCCATTGAC` | 1 | 100&micro;M |
  | Ebov-10-Pan_16_LEFT | `GCAACAGCAATACAGGCTTCCT` | Ebov-10-Pan_16_RIGHT | `GAAAGCCTGGTTTCCAATTCGC` | 2 | 100&micro;M |
  | Ebov-10-Pan_16_LEFT_alt1 | `GCAACAACAATACAGGCTTCCT` | Ebov-10-Pan_16_RIGHT_alt1 | `GAAGGCCTGGTTTCCAATTCGC` | 2 | 100&micro;M |
  | Ebov-10-Pan_17_LEFT | `CCACTTGTCAGAGTCAATCGGC` | Ebov-10-Pan_17_RIGHT | `GTTTCTGGCACTTCGATTCCCA` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_17_RIGHT_alt1 | `GTTTCTGGCACTTCGATACCCA` | 1 | 100&micro;M |
  | Ebov-10-Pan_18_LEFT | `AAAATCCAAGCAATAATGACTTCACTCC` | Ebov-10-Pan_18_RIGHT | `TTGATCAATTAAAAGTGTCTCCTCTAATGG` | 2 | 100&micro;M |
  |  |  | Ebov-10-Pan_18_RIGHT_alt1 | `TCGATCAATTTAAAGTATCTCCTCTAATGG` | 2 | 100&micro;M |
  |  |  | Ebov-10-Pan_18_RIGHT_alt2 | `TTGATCAATTAAAAGTATCTCCTCTAATAG` | 2 | 100&micro;M |
  | Ebov-10-Pan_19_LEFT | `AGATCCAGTTTTATAGAATCTTCTCAGGGA` | Ebov-10-Pan_19_RIGHT | `AGAAGGGCAATGTCTGTACTTGG` | 1 | 100&micro;M |
  | Ebov-10-Pan_19_LEFT_alt1 | `AGATCCAGTTTTACAGAATCTTCTCAGGGA` | Ebov-10-Pan_19_RIGHT_alt1 | `AGAAGGGCGATGTCTGTGCTTGG` | 1 | 100&micro;M |
  | Ebov-10-Pan_20_LEFT | `AGCCAGTGTGACTTGGATTGGA` | Ebov-10-Pan_20_RIGHT | `AGTTTGTCGACATCACTAACCTGT` | 2 | 100&micro;M |
  |  |  | Ebov-10-Pan_20_RIGHT_alt1 | `AGTTTGTCGACATCACTAACTTGT` | 2 | 100&micro;M |
  | Ebov-10-Pan_21_LEFT | `AGAACATTTTCCATCCCACTTGGA` | Ebov-10-Pan_21_RIGHT | `AAGCACCCTCTTTATGGAAGGC` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_21_RIGHT_alt1 | `AAGCACCCTCTTTGTGGAAGGC` | 1 | 100&micro;M |
  | Ebov-10-Pan_22_LEFT | `TGCCGGTATGTGCACAAAGTAT` | Ebov-10-Pan_22_RIGHT | `ATATATTGTCTCATTCAGCTGGAGCA` | 2 | 100&micro;M |
  | Ebov-10-Pan_23_LEFT | `CGAGGTTGACAATTTGACCTACGT` | Ebov-10-Pan_23_RIGHT | `GCAAGGGTTGTTAGATGCGACA` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_23_RIGHT_alt1 | `GCAAGGGTTGTCAGATGCGACA` | 1 | 100&micro;M |
  | Ebov-10-Pan_24_LEFT | `TGCAATGGTTCAAGTGCACAGT` | Ebov-10-Pan_24_RIGHT | `CTGGCACTCTCTTCTCCGGTAT` | 2 | 100&micro;M |
  | Ebov-10-Pan_24_LEFT_alt1 | `TGCAATGGTTCAAGTGCACAAT` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_25_LEFT | `ACCACAACAAGTCCCCAAAACC` | Ebov-10-Pan_25_RIGHT | `TAGCTCAGTTGTGGCTCTCAGG` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_25_RIGHT_alt1 | `TAGCTCGGTTGTGGCTCTCAGG` | 1 | 100&micro;M |
  | Ebov-10-Pan_26_LEFT | `ATCTGTGGGTTGAGACAGCTGG` | Ebov-10-Pan_26_RIGHT | `GCTTTTCCATGAAGCAATCTGAAGA` | 2 | 100&micro;M |
  | Ebov-10-Pan_26_LEFT_alt1 | `ATCTGTGGATTGAGGCAGCTGG` | Ebov-10-Pan_26_RIGHT_alt1 | `GCTTTGCCATGAAGCAATCTGAAGA` | 2 | 100&micro;M |
  | Ebov-10-Pan_26_LEFT_alt2 | `ATCTGTGGGTTGAGGCAGCTGG` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_27_LEFT | `TGGAGTTACAGGCGTTATAATTGCA` | Ebov-10-Pan_27_RIGHT | `AAAGGCTTCTTTCCCTTGTCACT` | 1 | 100&micro;M |
  | Ebov-10-Pan_28_LEFT | `TCATCCTTGATTCTACAATCATGACAGT` | Ebov-10-Pan_28_RIGHT | `AGGTGCTGGAGGAACTGTTAATG` | 2 | 100&micro;M |
  | Ebov-10-Pan_28_LEFT_alt1 | `TCATCCTTGATTCTACAATCATAACAGT` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_29_LEFT | `GAGTACCGTCAATCAAGGAGCG` | Ebov-10-Pan_29_RIGHT | `CACAGCACATAGAGTCAACAATGC` | 1 | 100&micro;M |
  | Ebov-10-Pan_30_LEFT | `GATCAAGACGGCAGAACACTGG` | Ebov-10-Pan_30_RIGHT | `ATCAGACCATGAGCATGTCCCC` | 2 | 100&micro;M |
  | Ebov-10-Pan_31_LEFT | `CTGCTGTCGTTGTTTCAGGGTT` | Ebov-10-Pan_31_RIGHT | `ATGGGATGGATCGTTGCTACCT` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_31_RIGHT_alt1 | `ATGGGATGGATCGTTGCTGCCT` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_31_RIGHT_alt2 | `ATGAGATGGATCGTTGCTACCT` | 1 | 100&micro;M |
  | Ebov-10-Pan_32_LEFT | `GCCAAGCATACCTCTTGCACAA` | Ebov-10-Pan_32_RIGHT | `TGGACTACCCTGAAATAGTACTTTGC` | 2 | 100&micro;M |
  | Ebov-10-Pan_33_LEFT | `TGCGGAGGTCTGATAAGAATAAACC` | Ebov-10-Pan_33_RIGHT | `TTCAACCTTGAAACCTTGCGCT` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_33_RIGHT_alt1 | `TTCAACTTTGAAACCTTGCGCT` | 1 | 100&micro;M |
  | Ebov-10-Pan_34_LEFT | `GCTGAAAAGAAGCTTACCTACAACG` | Ebov-10-Pan_34_RIGHT | `TCCTTGTCATTGACCATGCAGG` | 2 | 100&micro;M |
  | Ebov-10-Pan_34_LEFT_alt1 | `GTTGAAAAAAGGCCTACCTACAACG` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_34_LEFT_alt2 | `GCTGAAAAGAAGCCCACCTACAACG` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_35_LEFT | `GTGACTCACAAAGGAATGGCCC` | Ebov-10-Pan_35_RIGHT | `ACAATCCGTTGTAGTTCACGACA` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_35_RIGHT_alt1 | `ACAACCCGTTGTAGTTCACGACA` | 1 | 100&micro;M |
  | Ebov-10-Pan_36_LEFT | `TGCTGTCGTTGATTCGATCCAA` | Ebov-10-Pan_36_RIGHT | `AGCAGAGATGTCAAGATAACTATTGAGT` | 2 | 100&micro;M |
  | Ebov-10-Pan_37_LEFT | `ACACGAATGCAAAGTTTGATTCTTGA` | Ebov-10-Pan_37_RIGHT | `TGAAACCTAACACATGTGACCTGC` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_37_RIGHT_alt1 | `TGAAACCTAACACACGTGACCTGC` | 1 | 100&micro;M |
  | Ebov-10-Pan_38_LEFT | `CCCTCAAACAAGAGATTCCAAGACA` | Ebov-10-Pan_38_RIGHT | `ACAGTTGCGTAGTTGCGGATTA` | 2 | 100&micro;M |
  | Ebov-10-Pan_38_LEFT_alt1 | `CCCTCAAATAAGAGATTCCAAGACA` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_38_LEFT_alt2 | `TCCTCAAATAAGAGATTCCAAGACA` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_39_LEFT | `ACCTAGTCACTAGAGCTTGCGG` | Ebov-10-Pan_39_RIGHT | `ACATTTGATGTAAAAATTCATTGCCCTG` | 1 | 100&micro;M |
  | Ebov-10-Pan_40_LEFT | `GTGGGTGCTCAAGAAGACTGTG` | Ebov-10-Pan_40_RIGHT | `TGAGATTAGAGTTGTGTTGAATCGACA` | 2 | 100&micro;M |
  | Ebov-10-Pan_40_LEFT_alt1 | `GTGGGTGCTCAAGAGGACTGTG` | Ebov-10-Pan_40_RIGHT_alt1 | `TGAGATTAGAGTCGTGTTGAATCGACA` | 2 | 100&micro;M |
  | Ebov-10-Pan_41_LEFT | `AAGAAGCGGTTCAAGGGCATAC` | Ebov-10-Pan_41_RIGHT | `CTATGGAATTCACGGATCTTTTGAGC` | 1 | 100&micro;M |
  | Ebov-10-Pan_41_LEFT_alt1 | `AAGAAGCAGTTCAAGGGCATAC` | Ebov-10-Pan_41_RIGHT_alt1 | `CTATGGAATTCACGGATCTTTTGATC` | 1 | 100&micro;M |
  | Ebov-10-Pan_42_LEFT | `TGCATTTAGCTGTAAATCACACCCT` | Ebov-10-Pan_42_RIGHT | `AATCATTGGCAACGGAGGGAAT` | 2 | 100&micro;M |
  |  |  | Ebov-10-Pan_42_RIGHT_alt1 | `AATCATTGGCAACGGGGGGAAT` | 2 | 100&micro;M |
  | Ebov-10-Pan_43_LEFT | `GTCAAGGATCTTGGTACAGTGTTACT` | Ebov-10-Pan_43_RIGHT | `TGAGAAAGAAAAGTTCCGATATTGTGGT` | 1 | 100&micro;M |
  | Ebov-10-Pan_43_LEFT_alt1 | `GCCAAGGGTCTTGGTACAGTGTTACT` | Ebov-10-Pan_43_RIGHT_alt1 | `TGAGAAAGAAAAATTCCGGTATTGTGGT` | 1 | 100&micro;M |
  | Ebov-10-Pan_43_LEFT_alt2 | `GTCAAGGGTCTTGGTACAGTGTTACT` | Ebov-10-Pan_43_RIGHT_alt2 | `TGAGAAAGAAAAATTCCGATATTGTGGT` | 1 | 100&micro;M |
  | Ebov-10-Pan_44_LEFT | `TTGAGAATGTTCTTTCCTACGCACA` | Ebov-10-Pan_44_RIGHT | `ACGGTTGCAATATTCTATAAAAGGTGC` | 2 | 100&micro;M |
  | Ebov-10-Pan_44_LEFT_alt1 | `TTGAGAATGTTCTTTCCTACGCGCA` | Ebov-10-Pan_44_RIGHT_alt1 | `ACGGTTGCAATATTCGATAAAAGGTGC` | 2 | 100&micro;M |
  |  |  | Ebov-10-Pan_44_RIGHT_alt2 | `ACGGTTACAATATTCTATAAAAGGTGC` | 2 | 100&micro;M |
  | Ebov-10-Pan_45_LEFT | `CCACAGTTAGAGGGAGTAGCTTTG` | Ebov-10-Pan_45_RIGHT | `GCTCGTCTGCGTCAGTCTCTAA` | 1 | 100&micro;M |
  | Ebov-10-Pan_45_LEFT_alt1 | `CCACAGTTAGAGGGAGTAGTTTTG` |  |  | 1 | 100&micro;M |
  | Ebov-10-Pan_46_LEFT | `AAGTTACGCTCAGCTGTGATGG` | Ebov-10-Pan_46_RIGHT | `ATGGAAAGCTGCGGTTATCCTG` | 2 | 100&micro;M |
  | Ebov-10-Pan_47_LEFT | `TAGGCACTGCTTTTGAGCGATC` | Ebov-10-Pan_47_RIGHT | `CACAAAGTCAATGGCAGTGCAG` | 1 | 100&micro;M |
  | Ebov-10-Pan_47_LEFT_alt1 | `TAGGCACCGCTTTTGAGCGGTC` |  |  | 1 | 100&micro;M |
  | Ebov-10-Pan_47_LEFT_alt2 | `TAGGCACTGCTTTTGAACGATC` |  |  | 1 | 100&micro;M |
  | Ebov-10-Pan_48_LEFT | `TCTCCGAATGATTGAGATGGATGATT` | Ebov-10-Pan_48_RIGHT | `CTCAGTCTGTCCAAAACCGGTG` | 2 | 100&micro;M |
  | Ebov-10-Pan_48_LEFT_alt1 | `TCTCCGAATGATTGGGATGGATGATT` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_49_LEFT | `GATATCTTTTCACGCACGCCGA` | Ebov-10-Pan_49_RIGHT | `CCACCTGGTTGCTTTGCATTTG` | 1 | 100&micro;M |
  | Ebov-10-Pan_49_LEFT_alt1 | `GATATCTTTTCACGCACGCCCA` | Ebov-10-Pan_49_RIGHT_alt1 | `CCACCAGGTTGCTTTGCATTTG` | 1 | 100&micro;M |
  | Ebov-10-Pan_50_LEFT | `TCAAAGTGTTTTGGCTGAAACCCT` | Ebov-10-Pan_50_RIGHT | `TCCTGAGTAATGTGAAGGGGTCA` | 2 | 100&micro;M |
  | Ebov-10-Pan_50_LEFT_alt1 | `TCAAAGTGGTTTGGCTGAAACCCT` | Ebov-10-Pan_50_RIGHT_alt1 | `TCCTGAGTAATGTGAAGGAGTCA` | 2 | 100&micro;M |
  | Ebov-10-Pan_51_LEFT | `AACAGTGACTTGCTAATAAAACCATTTTTG` | Ebov-10-Pan_51_RIGHT | `AAATACTGAGCTGGTACTTCCCG` | 1 | 100&micro;M |
  | Ebov-10-Pan_51_LEFT_alt1 | `AACAGTGACTTGCTAATAAAGCCATTTTTG` |  |  | 1 | 100&micro;M |
  | Ebov-10-Pan_51_LEFT_alt2 | `AACAGTGATTTGCTAATAAAACCATTTTTG` |  |  | 1 | 100&micro;M |
  | Ebov-10-Pan_52_LEFT | `AATCGTGCTCACCTTCATCTAACT` | Ebov-10-Pan_52_RIGHT | `CCCAAAACTGTACAGAAGTCCTATCT` | 2 | 100&micro;M |
  | Ebov-10-Pan_53_LEFT | `ACAGACCCAATTAGCAGTGGAGA` | Ebov-10-Pan_53_RIGHT | `ACAATTGTTCCGCGATTAATTATCCAT` | 1 | 100&micro;M |
  | Ebov-10-Pan_53_LEFT_alt1 | `ACAGACCCAATTAGCAGCGGAGA` | Ebov-10-Pan_53_RIGHT_alt1 | `ACAATTGTTCCGCGATTAATTATCCACT` | 1 | 100&micro;M |
  | Ebov-10-Pan_54_LEFT | `TCTCAGATGCGGCCAGGTTATT` | Ebov-10-Pan_54_RIGHT | `TGACCATCACTGTTGTTTGTGCT` | 2 | 100&micro;M |
  | Ebov-10-Pan_54_LEFT_alt1 | `TCTCAGATGCGGCCAGATTATT` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_55_LEFT | `TGGAGGAGCAGACACAGAAACA` | Ebov-10-Pan_55_RIGHT | `ATGACGTTAATTGGCGTGTCCC` | 1 | 100&micro;M |
  | Ebov-10-Pan_55_LEFT_alt1 | `TGGAGGAGCAGGCACAGAAACA` | Ebov-10-Pan_55_RIGHT_alt1 | `ATGACGTCAATTGGCGTGTCCC` | 1 | 100&micro;M |
  | Ebov-10-Pan_55_LEFT_alt2 | `TGGAGAAGCAGGCACAGAAACA` | Ebov-10-Pan_55_RIGHT_alt2 | `ATGACGTTAATTGGCGCGTCCC` | 1 | 100&micro;M |
  | Ebov-10-Pan_56_LEFT | `CTCACACCGTCTAGTCCTACCT` | Ebov-10-Pan_56_RIGHT | `TTTGACATAACAGGTAGAAGCATCCT` | 2 | 100&micro;M |
  | Ebov-10-Pan_56_LEFT_alt1 | `CTCGCACCGTCTAGTCCTACCT` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_56_LEFT_alt2 | `CTCACATCGTCTAGTCCTACCT` |  |  | 2 | 100&micro;M |
  | Ebov-10-Pan_57_LEFT | `ACACGCTAGCTACTGAGTCCAG` | Ebov-10-Pan_57_RIGHT | `ATTGGCTTAATTAAATAACCAGTGGCA` | 1 | 100&micro;M |
  | Ebov-10-Pan_58_LEFT | `TGAAAGCAGTGGTCCTTAAAGTCT` | Ebov-10-Pan_58_RIGHT | `TGCTCTAAGATGTGCTAAGTGCTG` | 2 | 100&micro;M |
  |  |  | Ebov-10-Pan_58_RIGHT_alt1 | `TGCTCTAAGATGTGCCAAGTGCTG` | 2 | 100&micro;M |
  | Ebov-10-Pan_59_LEFT | `CGTCGATTCAAAAAGAGGTCCACT` | Ebov-10-Pan_59_RIGHT | `TCAGAAGCCCTGTCAGCCTTTC` | 1 | 100&micro;M |
  | Ebov-10-Pan_60_LEFT | `AGATTGCAATTGTGAAGAACGTTTCT` | Ebov-10-Pan_60_RIGHT | `AGAGTGCAGAGTTTATTATGTTGCGT` | 2 | 100&micro;M |
  | Ebov-10-Pan_61_LEFT | `TCACAATGCAGCATGTGTGACA` | Ebov-10-Pan_61_RIGHT | `AGGTATTTCTGATTTTACAGTCCTGCC` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_61_RIGHT_alt1 | `AGGTATTTATGATTTTACAGTCCTGCC` | 1 | 100&micro;M |
  |  |  | Ebov-10-Pan_61_RIGHT_alt2 | `AGGTATTTCTGATTTTACAGTCATGCC` | 1 | 100&micro;M |
  | Ebov-10-Pan_62_LEFT | `CCTGTCAGATGGAATAGTGTTTTGGT` | Ebov-10-Pan_62_RIGHT | `AATTTTTGTGTGCGACCATTTTTCC` | 2 | 100&micro;M |
{: .compact}

> **NOTE:** Primers need to be used at a final concentration of 0.015&micro;M per primer. In this case, Pool 1 has 101 primers in it so the requirement is 3.8&micro;L of 10&micro;M primers Pool 1 per 25&micro;L reaction. Pool 2 has 106 primers so needs 4.0&micro;L of 10&micro;M primers Pool 2 per 25&micro;L reaction. For other schemes, adjust the volume added appropriately.

6. Set up the amplicon PCR reactions as follows in 0.5mL thin-walled PCR or strip-tubes:

    |Reagent                         |Pool 1       |Pool 2        |
    |--------------------------------|-------------|--------------|
    |NEB Q5 Polymerase 2X MasterMix  |12.5&micro;L |12.5&micro;L  |
    |Primer Pool 1 or 2 (10&micro;M) |3.8&micro;L  |4.0&micro;L   |
    |Water                           |6.2&micro;L  |6.0&micro;L   |
    |TOTAL                           |22.5&micro;L |22.5&micro;L  |

> **NOTE:** This should be carried out in the mastermix hood and cDNA should not be taken anywhere near the mastermix hood at any stage.

7. In the TEMPLATE HOOD add 2.5&micro;L of cDNA to each Pool1 and Pool2 reaction mix and mix well.

8. Pulse centrifuge the tubes to remove any contents from the lid.

9. Set up the cycling conditions as follows:

    |Step            |Temperature |Time        |Cycles |
    |----------------|------------|------------|-------|
    |Heat Activation |98&deg;C    |30 seconds  |1      |
    |Denaturation    |98&deg;C    |15 seconds  |25-35  |
    |Annealing       |65&deg;C    |300 seconds |25-35  |
    |Hold            |4&deg;C     |Indefinite  |1      |				

> **NOTE:** Cycle number should be 25 for Ct18-21 up to a maximum of 35 cycles for Ct 35

10. Clean-up the amplicons using the following protocol in the TEMPLATE HOOD:

    1. Combine the entire contents of “Pool1” and “Pool2” PCR reactions for each biological sample into to a single 1.5mL Eppendorf tube.

    2. Mix sample gently, avoid vortexing.

    3. Ensure Aline beads are well resuspended by thoroughly mixing prior to addition to the sample. Mixture should be a homogenous brown colour.

    4. Add an equal volume of Aline beads to the tube and mix gently by either flicking or pipetting. This should be approximately 50&micro;L, so add 50&micro;L of beads.

    5. Pulse centrifuge the tubes to remove any beads or solution from the lid or side of the tube.

    6. Incubate for 5 mins at RT.

    7. Place on magnetic rack and incubate for 2 mins or until the beads have pelleted against the magnet and the solution is completely clear.

    8. Carefully remove and discard the solution, being careful not to displace the bead pellet.

    9. Add 200&micro;L of room-temperature 70% ethanol to the pellet.

    10. Carefully remove and discard ethanol, being careful not to displace the bead pellet.

    11. Repeat steps `i` to `j` to wash the pellet again.

    12. Briefly pulse centrifuge the pellet and carefully remove as much ethanol as possible using a 10&micro;L tip.

    13. Allow the pellet to dry for 1 mins, being careful not to overdry (if the pellet starts to crack then it is too dry).

    14. Resuspend pellet in 30&micro;L of water, and incubate for 2 mins.

    15. Place on magnet and CAREFULLY remove water and transfer to a clean 1.5mL Eppendorf tube. MAKE SURE that no beads are transferred into this tube. In some cases a pulse centrifugation can be used to pellet residual beads.  

    16. Quantify the amplicons pools using the Quantus Fluorometer following ONE dsDNA protocol.

<div class="pagebreak"> </div>

### Part 3: Quantus Quantification of Amplicon Pools

1. Set up the required number of 0.5mL tubes samples.

> **NOTE:** Use only thin-wall, clear, 0.5mL PCR tubes.

2. Label the tube lids. Do not label the side of the tube as this could interfere with the sample reading.

3. Add 199&micro;L ONE dsDNA dye solution to each tube.

4. Add 1&micro;L of each user sample to the appropriate tube.

> **NOTE:**  Use a P2 pipette for highest accuracy.

5. Mix each sample vigorously by vortexing for 3–5 seconds.

6. Allow all tubes to incubate at room temperature for 2 minutes before proceeding.

7. On the Home screen of the Quantus Fluorometer, select `Protocol`, then select `ONE DNA` as the assay type.

> **NOTE:** If you have already performed a calibration for the selected assay you can continue, there is no need to perform repeat calibrations when using ONE DNA pre diluted dye solution. **If you want to use the previous calibration, skip to step 11**. Otherwise, continue with step 9.

8. Add 200&micro;L ONE dsDNA Dye solution to two 0.5mL tubes.

9. Add 1&micro;L Lambda DNA standard 400 ng/&micro;L provided in the kit to one of the tube. These two tubes are the blank sample and standard required to perform the single point calibration procedure.

10. Selection 'Calibrate' then 'ONE DNA' then place the blank sample in the reader then select 'Read Blank'. Now place the standard in the reader and select 'Read Std'.

11. On the home screen navigate to 'Sample Volume' and set it to 1 ul then 'Units' and set it to ng/&micro;L.

12. Load the first sample into the reader and close the lid. The sample concentration is automatically read when you close the lid.

13. Repeat step 12 until all samples have been read.

14. The value displayed on the screen is the dsDNA concentration, carefully **record all results** in a spreadsheet or laboratory notebook.

<div class="pagebreak"> </div>

### Part 4: Barocoding and adaptor ligation: One-pot protocol.

> **NOTE:** This is a ‘one-pot ligation’ protocol for native barcoded ligation libraries. We have seen no reduction in performance compared to standard libraries, and is made faster by using the Ultra II® ligation module which is compatible with the Ultra II® end repair/dA-tailing module removing a clean-up step. If you have the time I would recommend using the double incubation times in <span style="color:blue">blue</span>, if you are in a hurry the times in <span style="color:red">red</span> are a good compromise between speed and efficiency.

1. Set up the following end-prep reaction for each biological sample:

   | DNA (20 ng) | 16.7&micro;L
   | Ultra II End Prep Reaction Buffer | 2.3&micro;L
   | Ultra II End Prep Enzyme Mix | 1&micro;L
   | Total | 20&micro;L  

> **NOTE:** Quantity of amplicons can vary from 10-50ng, any more than this and the molarity of DNA ends will be too high for efficient barcoding. You need to have 6 samples per native barcoded library to have sufficient material at the end.

2. Incubate at RT for 20 mins then 65&deg;C for 10 mins

3. Place on ice for 30 secs

4. Add the following directly to the previous reactions:

    | NBXX barcode | 2.5&micro;L
    | Ultra II Ligation Master Mix | 22.5&micro;L
    | Ligation Enhancer | 0.7&micro;L
    | Total | 45.7&micro;L

> **NOTE:** Use a SINGLE barcode per biological sample.

5. Incubate at RT for 30 mins, 70&deg;C for 10 mins then place on ice.

**NOTE:** This is to inactivate the DNA ligase to prevent barcode crossover.

6. Pool all barcoded fragments together into a clean 1.5 ml Eppendorf tube

7. Add 45.7&micro;L Aline beads per sample.

8. Incubate for 5 mins.

9. Place on a magnet rack for 2 mins or until clear.

10. Remove solution.

11. Add 200&micro;L 70% ethanol to the tube still on the magnetic rack.

12. Remove and discard ethanol without disturbing the pellet.

13.	Repeat steps 11 and 12.

15.	Spin down and remove residual 70% ethanol and air dry for 1 min.

16.	Resuspend in 31&micro;L EB.

17.	Incubate off the magnetic rack for 2 mins.

18.	Replace on magnetic rack.

19. Wait until clear and then carefully remove solution and transfer to a clean 1.5mL Eppendorf tube.

20.	Remove 1&micro;L and assess concentration by Quantus as described in previous section.

21. Set up the following adapter ligation reaction:

    | Cleaned-up barcoded amplicon pools (~60ng) | 30&micro;L
    | NEBNext Quick Ligation Reaction Buffer (5X) | 10&micro;L
    | AMII adapter mix | 5&micro;L
    | Quick T4 DNA Ligase | 5&micro;L
    | Total volume | 50&micro;L

22. Incubate at RT for 30 mins.

23. Add 50&micro;L Aline beads

24. Incubate for 5 mins

25. Place on a magnetic rack until clear

26. Remove supernatant

27. Add 200&micro;L SFB and resuspend by flicking

> **CAUTION:** do not use 80% ethanol

28. Place on magnetic rack until clear

29. Remove supernatant

30. Repeat SFB wash

31. Spin down and remove residual SFB

32. Add 15&micro;L EB and resuspend by flicking

33. Incubate at RT for 2 mins.

34. Place on magnetic rack.

35. Carefully transfer solution to a clean 1.5mL Eppendorf tube.

36. Remove 1&micro;L and assess concentration by Quantus (wait until beads have settled before measuring).

> **NOTE:** Library can be now be stored at 4&deg;C if required, but for best results it would be best to proceed immediately to sequencing.

<div class="pagebreak"> </div>

### Part 5: Priming and loading the SpotON flow cell

1. Thaw the following at RT before placing on ice:
   - Sequencing buffer (SQB)
   - Loading beads (LB)
   - Flush buffer (FLB)
   - Flush tether (FLT)

2. Add 30 ul FLT to the tube of FLB and mix well.

3. Flip back the MinION lid and slide the priming port cover clockwise so that the priming port is visible.

> **IMPORTANT:** Care must be taken when drawing back buffer from the flow cell. The array of pores must be covered by buffer at all times. Removing more than 20-30&micro;L risks damaging the pores in the array.

5. After opening the priming port, check for small bubble under the cover. Draw back a small volume to remove any bubble (a few&micro;Ls):   
   - Set a P1000 pipette to 200&micro;L   
   - Insert the tip into the priming port   
   - Turn the wheel until the dial shows 220-230&micro;L, or until you can see a small volume of buffer entering the pipette tip.  

6. Load 800&micro;L of FLB plus FLT into the flow cell via the priming port, using the dial-down method described in step 5, avoiding the introduction of air bubbles.

7. Wait for 5 minutes.                                            

8. In a new tube prepare the library dilution for sequencing:

    | Reagent | Volume
    |---|---
    | SQB | 37.5&micro;L
    | LB | 25.5&micro;L
    | Library (~30ng) | 12&micro;L
    | Total | 75&micro;L

9. Gently lift the SpotON sample port cover to make the SpotON sample port accessible.

10. Load 200&micro;L of the priming mix into the flow cell via the priming port (**NOT** the SpotON sample port), avoiding the introduction of air bubbles.

11.  Mix the prepared library gently by pipetting up and down just prior to loading.

12. Add 75&micro;L of the prepared library to the flow cell via the SpotON sample port in a dropwise fashion. Ensure each drop siphons into the port before adding the next.

13. Gently replace the SpotON sample port cover, making sure the bung enters the SpotON port, close the priming port and replace the MinION lid.

14. Double–click the MinKNOW icon located on the desktop to open the MinKNOW GUI.

15. If your MinION was disconnected from the computer, plug it back in.

16. Choose the following flow cell type from the selector box:

    - `FLO-MIN106` : R9.4.1 flowcell

17. Then mark the flow cell as `Selected`.

18. Click the `New Experiment` button at the bottom left of the GUI.

19. On the New experiment popup screen, select the running parameters for your experiment from the individual tabs:

    - `Experiment`
    : Name the run in the experiment field, leave the sample field blank.

    - `Kit`
    : Selection LSK109 as there is no option for native barcoding (NBD104)

    - `Run Options`
    : Set the run length, usually 1-2 hours.

    - `Basecalling`
    : Leave basecalling turned on and check the HAC (high accuracy model) is selected

    - `Output`
    : The number of files that MinKNOW will write to a single folder. By default this is set to 4000

20. Click `Start run`.

21. Allow the script to run to completion.

22. The MinKNOW Experiment page will indicate the progression of the script; this can be accessed through the `Experiment` tab that will appear at the top right of the screen

23. Monitor the Message panel on the right hand side for errors.
