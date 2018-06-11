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
version: v1.0.0
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
: [https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V2](https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V2) 

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
   |1| Sprout® portable centrifuge
   |1| 1mL Eppendorf pipette
   |1| 0.1mL Eppendorf pipette
   |1| 0.01L Eppendorf pipette
   |1| 1.5mL/0.6mL convertible tube rack
   |1| Qubit 4 Fluorometer (ThermoFisher&trade;)
   |1| miniPCR machine.
   |1| Heat block
   |1| magnetic rack
{: .compact}

#### Consumables required:
 

   |---:|:---
   || Vilo SSIV RT 2x MasterMix
   || Q5 Hotstart HF polymerase 2x Mastermix
   || Ebola Zaire Primers V1
   || NEBNext UltraII End-prep module
   || NEBNext UltraII Ligase module
   || NEBNext FFPE Repair module
   || Agencourt AMPureXP Beads
   || Nanopore Ligation Sequencing Kit 1D
   || Nanopore Native Barcoding Expansion Kit
   || Nanopore R9.4.1 Flow cells
   || 1.5mL eppendorf tubes
   || 0.2mL 8-strip tubes
   || 50mL transfer tubes
   || Qubit Reaction Tubes
   || Qubit 1x dsDNA HS Assay kit
   || Nuclease-free water
   || 70% Ethanol
   || 1mL pipette tips
   || 0.1mL pipette tips
   || 0.01mL pipette tips
   || Paper towelling 
   || Clinical waste sharps containers
{: .compact}

#### Safety, containment and contamination recommendations

   |---:|:---
   || Back-tie hydrophobic lab gown
   || Gloves
   || UV light sterilizers
   || MediPal Decontamination wipes
   || DNAway and RNAse Zap® reagent
{: .compact}

<div class="pagebreak"> </div>

## Protocol

### Part 1: cDNA synthesis with Superscript IV Vilo cDNA kit

> **NOTE ON HOOD PREPARATION:** To prevent cross contamination of both the sample and other reagents, this should be carried out in the SAMPLE PREPARATION HOOD, which is pre-sterilised with UV and treated with MediPal wipes, DNAway and RNAseZap reagent. Wipe down the hood with each sequentially, allowing 5 minutes for drying between each. Pipettes should also be treated in the same way, and UV treated for 30 mins between library preparations. 

1. Recommend aliquoting the Vilo mastermix, to prevent cross contamination and to reduce potential freeze/thaw cycles.
2. Set up the following reaction:

    |---|--- 
    |2x Vilo Master Mix | 5&micro;L   
    |viral RNA | 5&micro;L   
    |TOTAL | 10&micro;L
    
> **NOTE:** Viral RNA input from a clinical sample should be between Ct 18-35. If Ct is between 12-15, then dilute the sample 100-fold in water, if between 15-18 then dilute 10-fold in water. This will reduce the likelihood of PCR-inhibition. 
   
3. Gently mix (avoid vortexing) then pulse spin the tube to ensure maximum contact with the thermal cycler.
4. Incubate the reaction as follows:

    |---|---|--- 
    | Primer annealing | 25&deg;C | 20 mins   
    | Extension | 50&deg;C | 30 mins   
    | Inactivation | 85&deg;C | 10 mins
    
5. cDNA is now ready for amplicon generation.

<div class="pagebreak"> </div>

### Part 2: Ebola Amplicon Preparation

> **NOTE ON HOOD PREPARATION:** To prevent cross contamination of both the sample and other reagents, this should be carried out in the MASTERMIX HOOD, which is pre-sterilised with UV and treated with MediPal wipes, DNAway and RNAseZap reagent. Wipe down the hood with each sequentially, allowing 5 minutes for drying between each. Pipettes should also be treated in the same way, and UV treated for 30 mins between library preparations.

#### Primer dilution and preparation

1. Ebola primers for this protocol were designed using [Primal Scheme](http://primal.zibraproject.org) and generate 400nt amplicons with 75nt overlaps. Primer names and dilutions are listed in the table below. 

2. Primers should be prepped and aliquoted PRIOR TO DEPARTURE in a STERILE PCR CABINET. At NO stage should primers or PCR reagents be anywhere near the template or amplicons until use. 

3. Resuspend lyophilised primers at a concentration of 100&micro;M each

4. Generate primer pool stocks by adding 20&micro;L of each primer pair to a 1.5mL Eppendorf labelled “Pool 1, 100&micro;M” or “Pool 2, 100&micro;M”. Total volume should be 480&micro;L of Pool 1 and 460&micro;L of Pool 2. This is a 10x stock of each primer pool. 

5. Dilute this primer pool 1:10 in molecular grade water, to generate 10&micro;M primer stocks. Recommend that at least 1mL of each primer pool is taken in 100&micro;L aliquots, to account for any risks of degradation of contamination. 

<div class="pagebreak"> </div>

   | NAME         | Sequence                         | NAME          | Sequence                 | Pool | [Stock] |
   |-------------:|----------------------------------|--------------:|--------------------------|------|---------|
   | EBOV_1_LEFT | `TGTGTGCGAATAACTATGAGGAAGAT` | EBOV_1_RIGHT | `TCAGATTCAGTGAGACTCGGCG` | 1    | 100&micro;M   |
   | EBOV_2_LEFT | `AAAGACAAATTGCTCGGAATCACAA` | EBOV_2_RIGHT | `CAAAGGAGAGAAACTGACCGGC` | 2    | 100&micro;M   |
   | EBOV_3_LEFT | `AAGAGAACACTTGCTGCCATGC` | EBOV_3_RIGHT | `CATACTCTCCATGCTTGGCCAG` | 1    | 100&micro;M   |
   | EBOV_4_LEFT | `AGTTCGTCTCCATCCTCTTGCA` | EBOV_4_RIGHT | `TCCTGGAAAGGGAATGTCGTCA` | 2    | 100&micro;M   |
   | EBOV_5_LEFT | `GAAGCTATCACTGCTGCGTCAC` | EBOV_5_RIGHT | `TAATTGGTGTCAGCATGCGAGG` | 1    | 100&micro;M   |
   | EBOV_6_LEFT | `CCTCACAGAACAATCCACCACG` | EBOV_6_RIGHT | `TCTTTTTCAGTGAGCCATGGTGG` | 2    | 100&micro;M   |
   | EBOV_7_LEFT | `CAGTGATGGCAAAGAGTACACGT` | EBOV_7_RIGHT | `AATGTTGGGCAGGCTAGTAGGT` | 1    | 100&micro;M   |
   | EBOV_8_LEFT | `CCACAGTTATAGCCATAATTGTAACTCAAT` | EBOV_8_RIGHT | `TGATTGCAAATTGGGTCCGTTTG` | 2    | 100&micro;M   |
   | EBOV_9_LEFT | `ACGCATCCCAAATGCAACAAAC` | EBOV_9_RIGHT | `GCCGAAATGTCAGGTTTCCCAA` | 1    | 100&micro;M   |
   | EBOV_10_LEFT | `TGAGACCGTCCCTCAAAGTGTT` | EBOV_10_RIGHT | `GAGGGAAGGGAGATTGGCTCAA` | 2    | 100&micro;M   |
   | EBOV_11_LEFT | `CATCGCCCAAGATTGATCGAGG` | EBOV_11_RIGHT | `AGGAAGCCTGTATTGCTGTTGC` | 1    | 100&micro;M   |
   | EBOV_12_LEFT | `TTGCCTACTGCTCCTCCTGAAT` | EBOV_12_RIGHT | `GGAAGAACGAACTCCTGGAGGA` | 2    | 100&micro;M   |
   | EBOV_13_LEFT | `CTTGTCAGAGTCAATCGGCTGG` | EBOV_13_RIGHT | `GTCCAACCCAATGTACTTTGGCA` | 1    | 100&micro;M   |
   | EBOV_14_LEFT | `TCCACAAGCTGACCGGTAAGAA` | EBOV_14_RIGHT | `AGCATGCAGGCAATTTGAGGAT` | 2    | 100&micro;M   |
   | EBOV_15_LEFT | `ACGGTGATTCAAATGTTAATCTTTCTCAT` | EBOV_15_RIGHT | `AGTTTGTCGACATCACTAACCTGT` | 1    | 100&micro;M   |
   | EBOV_16_LEFT | `AGAACATTTTCCATCCCACTTGGA` | EBOV_16_RIGHT | `TTGGGGCAGTATCAGAAATGCA` | 2    | 100&micro;M   |
   | EBOV_17_LEFT | `TGATCGACTTGCTTCCACAGTT` | EBOV_17_RIGHT | `CCGGACTCTGACCACTGATGTT` | 1    | 100&micro;M   |
   | EBOV_18_LEFT | `ACCTCACTAGAAAAATTCGCAGTGA` | EBOV_18_RIGHT | `TTTTGGGGACTTGTTGTGGTGG` | 2    | 100&micro;M   |
   | EBOV_19_LEFT | `CCCCAAAAGCAGAGAACACCAA` | EBOV_19_RIGHT | `CGGTTGAGGATTGAAAAGGTGC` | 1    | 100&micro;M   |
   | EBOV_20_LEFT | `CCAACGAGACGACTCAAGCTCT` | EBOV_20_RIGHT | `TGGCTATGTTTAAAGCTCCAGTGT` | 2    | 100&micro;M   |
   | EBOV_21_LEFT | `AGCCTCAAATCAATGAAACCAGGA` | EBOV_21_RIGHT | `TGGTCGTGTCCATCCCTTGAAT` | 1    | 100&micro;M   |
   | EBOV_22_LEFT | `GCTTCATATGAGAGAGGACGCC` | EBOV_22_RIGHT | `GGTTCTGATGTCTTGTCTCGCC` | 2    | 100&micro;M   |
   | EBOV_23_LEFT | `ATCCAACGGCTGATGATTTCCAG` | EBOV_23_RIGHT | `ACCCTCATCAGACCATGAGCAT` | 1    | 100&micro;M   |
   | EBOV_24_LEFT | `CTGCTGTCGTTGTTTCAGGGTT` | EBOV_24_RIGHT | `ACACCTCCTCCACAGCTTGAAG` | 2    | 100&micro;M   |
   | EBOV_25_LEFT | `GCAACGATCCATCCCATCAAAAA` | EBOV_25_RIGHT | `TTTCAGCCAATGGAGTTGACCTG` | 1    | 100&micro;M   |
   | EBOV_26_LEFT | `GGGGCAATAATATCTAATTGAACTTAGCC` | EBOV_26_RIGHT | `AGAGATTCCTTGTTATTGACCATGCAG` | 2    | 100&micro;M   |
   | EBOV_27_LEFT | `GTGACTCACAAAGGAATGGCCC` | EBOV_27_RIGHT | `CGATTTGTCGGGTTCTTGGAGC` | 1    | 100&micro;M   |
   | EBOV_28_LEFT | `CGGATTGTTGAGCAGTATTGAAATTGG` | EBOV_28_RIGHT | `AGCAATTCTATGATGTTGTCTTGGAATCT` | 2    | 100&micro;M   |
   | EBOV_29_LEFT | `TCCTCACTGTAAGCCAGCTTCC` | EBOV_29_RIGHT | `TTTCGGGAGTTTACAGTTGCGT` | 1    | 100&micro;M   |
   | EBOV_30_LEFT | `CTAGTCACTAGAGCTTGCGGGT` | EBOV_30_RIGHT | `AGTCCCCATAGCCTAAGATGTCT` | 2    | 100&micro;M   |
   | EBOV_31_LEFT | `CTGGCTATTTTAACTCGAAGGGGT` | EBOV_31_RIGHT | `AAGAATCGGCCCTTCCTCTCAG` | 1    | 100&micro;M   |
   | EBOV_32_LEFT | `AAGTTCCTCGAACCATTGTGCTT` | EBOV_32_RIGHT | `TCATTGGCAACGGAGGGAATTG` | 2    | 100&micro;M   |
   | EBOV_33_LEFT | `TGATAGTCAAGGATCTTGGTACAGTGT` | EBOV_33_RIGHT | `AGCAAGACCATCAGCTAACAGAG` | 1    | 100&micro;M   |
   | EBOV_34_LEFT | `AATTGCCTTATCCGACTCGCAA` | EBOV_34_RIGHT | `TGAGCACATGAAATACTTGTCCAGA` | 2    | 100&micro;M   |
   | EBOV_35_LEFT | `AAGGGCCTAGTTCATACAGGGG` | EBOV_35_RIGHT | `CTGCAAGGAAAGATATGTCGTGTCT` | 1    | 100&micro;M   |
   | EBOV_36_LEFT | `ATCTTCAAGGGACCCTGGCTAG` | EBOV_36_RIGHT | `CTTAGGGTGATGGTCCTGCGTA` | 2    | 100&micro;M   |
   | EBOV_37_LEFT | `GCGGATTAAATGTCCCTGGGTC` | EBOV_37_RIGHT | `TGGCTCCAATAAGAGGTCTTCCC` | 1    | 100&micro;M   |
   | EBOV_38_LEFT | `GCGGAGGCTTTAACCCAAATAACT` | EBOV_38_RIGHT | `TTCCTGAGTAATGTGAAGGGGTCA` | 2    | 100&micro;M   |
   | EBOV_39_LEFT | `GCAGTTCGAACAGTGACTTGCT` | EBOV_39_RIGHT | `ATGAGATATTGCAATTGAGTCCTCCT` | 1    | 100&micro;M   |
   | EBOV_40_LEFT | `TAACAAGATACCGAGAAAACGAATTGATT` | EBOV_40_RIGHT | `TGAGGATCAATACTCATTAACCGTGAC` | 2    | 100&micro;M   |
   | EBOV_41_LEFT | `GCTCATTGCGAATACTTAAGCCAAC` | EBOV_41_RIGHT | `TGTGCTTGATCCAGTTGAAGAGT` | 1    | 100&micro;M   |
   | EBOV_42_LEFT | `CATGCATCATTGGCGTACTGGA` | EBOV_42_RIGHT | `CGGATCTCAATTGCCGTAAGTACT` | 2    | 100&micro;M   |
   | EBOV_43_LEFT | `GGGACACGCCAATTAACGTCAT` | EBOV_43_RIGHT | `TCTGTTGTCTCTGCATCCATGG` | 1    | 100&micro;M   |
   | EBOV_44_LEFT | `AGACCAAAGAGCAAGGCTACCT` | EBOV_44_RIGHT | `CCTGTGGTATAGTACTTTCTCTAATGATGG` | 2    | 100&micro;M   |
   | EBOV_45_LEFT | `ACTCAGTATGCTGACTGTGAGTTACA` | EBOV_45_RIGHT | `TAAACTCAGAAGCCCTGTCAGC` | 1    | 100&micro;M   |
   | EBOV_46_LEFT | `AGATTGCAATTGTGAAGAACGTTTCT` | EBOV_46_RIGHT | `TCAACCAAAACACTATTCCATCTGACA` | 2    | 100&micro;M   |
   | EBOV_47_LEFT | `GCCGCAATGAATTTAACGCAACA` | EBOV_47_RIGHT | `TGTGTGCGACCATTTTTCCAGG` | 1    | 100&micro;M   |
{: .compact}

> **NOTE:** Primers need to be used at a final concentration of 0.015&micro;M per primer. In this case, Pool 1 has 48 primers in it so the requirement is 1.8&micro;L of 10&micro;M primer Pool 1 per 25&micro;L reaction. Pool 2 has 46 primers so needs 1.72&micro;L of primer Pool 2 per 25&micro;L reaction. For other schemes, adjust the volume added appropriately. 

6. Set up the amplicon PCR reactions as follows in 0.5mL thin-walled PCR or strip-tubes:

    |Reagent |POOL 1 |POOL 2 |
    |--------|-------|-------|
    |NEB Q5® Polymerase 2X MasterMix |12.5&micro;L |12.5&micro;L |
    |Primer Pool 1 or 2 (10&micro;M) |1.8&micro;L |1.72&micro;L |
    |Water |6.7&micro;L |6.78&micro;L |
    |TOTAL |21&micro;L |21&micro;L |
    
> **NOTE:** This should be carried out in the mastermix hood and cDNA should not be taken anywhere near the mastermix hood at any stage.

7. In the TEMPLATE HOOD add 4&micro;L of cDNA to each Pool1 and Pool2 reaction mix and mix well.

8. Pulse centrifuge the tubes to remove any contents from the lid.

9. Set up the cycling conditions as follows:

    |                |Temperature |Time        |Cycles |
    |----------------|------------|------------|-------| 
    |Heat Activation |98&deg;C        |30 seconds  |1      |
    |Denaturation    |98&deg;C        |15 seconds  |35     |
    |Annealing       |65&deg;C        |300 seconds  |.      |
    |Hold            |4&deg;C         |Indefinite  |1      |				

10. Clean-up the amplicons using the following protocol in the TEMPLATE HOOD:
  
    1. Combine the entire contents of “Pool1” and “Pool2” PCR reactions for each biological sample into to a single 1.5mL Eppendorf tube. 
   
    2. Mix sample gently, avoid vortexing.
      
    3. Ensure AmpureXP beads are well resuspended by thoroughly mixing prior to addition to the sample. Mixture should be a homogenous brown colour. 
      
    4. Add an equal volume of AmpureXP beads to the tube and mix gently by either flicking or pipetting. This should be approximately 50&micro;L, so add 50&micro;L of beads.
      
    5. Pulse centrifuge the tubes to remove any beads or solution from the lid or side of the tube. 
    
    6. Incubate for 2 mins at 25&deg;C.
     
    7. Place on magnetic rack and incubate for 2 mins or until the beads have pelleted against the magnet and the solution is completely clear. 
     
    8. Carefully remove and discard the solution, being careful not to displace the bead pellet. 
    
    9. Add 200&micro;L of room-temperature 70% ethanol to the pellet. 
      
    10. Remove from magnet and mix by gently flicking the tube. 
     
    11. Pulse centrifuge the tube to make sure all the mixture is out of the lid following flicking, then place back onto the magnet. 
     
    12. Incubate for 2 mins or until the beads have pelleted against the magnet and the solution is completely clear. 
     
    13. Carefully remove and discard ethanol, being careful not to displace the bead pellet.
      
    14. Repeat steps `h` to `m` to wash the pellet again. 
      
    15. Briefly pulse centrifuge the pellet and carefully remove as much ethanol as possible using a 10&micro;L tip. 
      
    16. Allow the pellet to dry for 2 mins, being careful not to overdry (if the pellet is cracking, then it is too dry).
      
    17. Resuspend pellet in 30&micro;L of water, and incubate for 2 mins. 
      
    18. Place on magnet and CAREFULLY remove water and transfer to a clean 1.5mL Eppendorf tube. MAKE SURE that no beads are transferred into this tube. In some cases a pulse centrifugation can be used to pellet residual beads.  
      
    19. Quantify the amplicon library using Qubit4&trade; following the dsDNA protocol.
    
<div class="pagebreak"> </div>

### Part 3: Qubit Quantification of Nucleic Acid: dsDNA

1. Set up the required number of 0.5mL tubes for standards and samples. The Qubit&trade; 1X dsDNA HS Assay requires 2 standards. 

> **NOTE:** Use only thin-wall, clear, 0.5mL PCR tubes. Acceptable tubes include Qubit&trade; assay tubes (Cat. No. Q32856) 
   
2. Label the tube lids. Do not label the side of the tube as this could interfere with the sample read. Label the lid of each standard tube correctly. Calibration of the Qubit&trade; Fluorometer requires the standards to be inserted into the instrument in the right order

3. Add 10&micro;L of each Qubit&trade; standard to the appropriate tube. 

4. Add 1–20&micro;L of each user sample to the appropriate tube. 

> **NOTE:**  If you are adding 1–2&micro;L of sample, use a P-2 pipette for best results.  

5. Add the Qubit&trade; 1X dsDNA 1X buffer to each tube such that the final volume is 200&micro;L. 
   
> **NOTE:**  The final volume in each tube must be 200&micro;L. Each standard tube requires 190&micro;L of Qubit&trade; working solution, and each sample tube requires anywhere from 180–199&micro;L. Ensure that you have sufficient Qubit&trade; working solution to accommodate all standards and samples. 
   
> **NOTE:**  To avoid any cross-contamination, we recommend that you remove the total amount of working solution required for your samples and standards from the working solution bottle and then add the required volume to the appropriate tubes instead of pipetting directly from the bottle to each tube. 

6. Mix each sample vigorously by vortexing for 3–5 seconds. 

7. Allow all tubes to incubate at room temperature for 2 minutes, then proceed to “Read standards and samples”. 

8. On the Home screen of the Qubit&trade; 4 Fluorometer, press DNA, then select `1X dsDNA HS` as the assay type. The `Read standards` screen is displayed. Press `Read Standards` to proceed. 

> **NOTE:** If you have already performed a calibration for the selected assay, the instrument prompts you to choose between reading new standards and running samples using the previous calibration. **If you want to use the previous calibration, skip to step 11**. Otherwise, continue with step 9. 

9. Insert the tube containing Standard #1 into the sample chamber, close the lid, then press Read standard. When the reading is complete (~3 seconds), remove Standard #1. 

10. Insert the tube containing Standard #2 into the sample chamber, close the lid, then press Read standard. When the reading is complete, remove Standard #2. 

11. The instrument displays the results on the Read standard screen. For information on interpreting the calibration results, refer to the Qubit&trade; Fluorometer User Guide, available for download at thermofisher.com/qubit. 

12. Press `Run samples`. 

13. On the assay screen, select the sample volume and units: 

    - Press the `+` or `–` buttons on the wheel, or anywhere on the wheel itself, to select the sample volume added to the assay tube (from 1–20&micro;L). 
    
    - From the unit dropdown menu, select the units for the output sample concentration. 

14. Insert a sample tube into the sample chamber, close the lid, then press `Read tube`. When the reading is complete (~3 seconds), remove the sample tube. 

15. **The top value (in large font) is the concentration of the original sample and the bottom value is the dilution concentration**. For information on interpreting the sample results, refer to the Qubit&trade; Fluorometer User Guide. 

16. Repeat step 14 until all samples have been read.

17. Carefully **record all results** and store run file from the Qubit on a memory stick. 

<div class="pagebreak"> </div>

### Part 4: Barocoding and adaptor ligation: One-pot protocol.
 
> **NOTE:** This is a ‘one-pot ligation’ protocol for native barcoded ligation libraries. We have seen no reduction in performance compared to standard libraries, and is made faster by using the Ultra II® ligation module which is compatible with the Ultra II® end repair/dA-tailing module removing a clean-up step. If you have the time I would recommend using the double incubation times in <span style="color:blue">blue</span>, if you are in a hurry the times in <span style="color:red">red</span> are a good compromise between speed and efficiency.

1. Set up the following end-prep reaction for each biological sample:

   | DNA (500 ng) | 25&micro;L
   | Ultra II End Prep Reaction Buffer | 3.5&micro;L
   | Ultra II End Prep Enzyme Mix | 1.5&micro;L
   | Total | 30&micro;L  
    
> **NOTE:** Amount of RNA can vary from 250-1000ng, less than this and the coverage and depth may be sub-optimal. 
    
2. Incubate at RT for <span style="color:red">5 mins</span> or <span style="color:blue">10 mins</span> then 65&deg;C for <span style="color:red">5 mins</span> or <span style="color:blue">10 mins</span>

3. Place on ice for 30 secs

4. Add the following directly to the previous reactions:

    | NBXX barcode | 2.5&micro;L
    | Ultra II Ligation Master Mix | 20&micro;L 
    | Ligation Enhancer | 1&micro;L
    | Total | 53.5&micro;L
   
> **NOTE:** Use a SINGLE barcode per biological sample. 

5. Incubate at RT for <span style="color:red">10 mins</span> or <span style="color:blue">20 mins</span>, 70&deg;C for 5 mins then place on ice.

6. Pool all barcoded fragments together into a clean 1.5 ml Eppendorf tube

7. Add 53&micro;L Ampure XP beads per sample.

8. Incubate for <span style="color:red">5 mins</span> or <span style="color:blue">10 mins</span>.

9. Place on a magnet rack until clear.

10. Remove solution. 

11. Add 200&micro;L 80% ethanol to the tube still on the magnetic rack.

12. Incubate 30 secs.

13. Remove solution.

14.	Repeat last three steps (11-13).

15.	Spin down and remove residual 70% ethanol and air dry for 1 min.

16.	Resuspend in 31&micro;L EB.

17.	Incubate off the magnetic rack for <span style="color:red">5 mins</span> or <span style="color:blue">10 mins</span> mins.

18.	Replace on magnetic rack.

19. Incubate for 2 mins at room temperature and then carefully remove solution and transfer to a clean 1.5mL Eppendorf tube. 

20.	Remove 1&micro;L and assess concentration by Qubit as described in previous section. 

21. Set up the following adapter ligation reaction:

    | Cleaned-up barcoded fragments (~3&micro;g) | 30.0&micro;L
    | BAM 1D | 20.0&micro;L
    | Ultra II Ligation module | 40.0&micro;L
    | Ultra II Ligation enhancer | 1.0&micro;L
    | Total volume | 91.0&micro;L

22. Incubate at RT for <span style="color:red">10 mins</span> or <span style="color:blue">20 mins</span>.

23. Add 45.5&micro;L Ampure XP beads

24. Incubate for <span style="color:red">5 mins</span> or <span style="color:blue">10 mins</span> mins

25. Place on a magnetic rack until clear

26. Remove supernatant 

27. Add 150&micro;L ABB and resuspend by flicking 

> **CAUTION:** do not use 80% ethanol

28. Place on magnetic rack until clear

29. Remove supernatant

30. Repeat ABB wash

31. Spin down and remove residual ABB

32. Add 12&micro;L ELB and resuspend by flicking

33. Incubate at RT for <span style="color:red">5 mins</span> or <span style="color:blue">10 mins</span>

34. Place on magnetic rack

35. Carefully transfer solution to a clean 1.5mL Eppendorf tube. 

36. Remove 1&micro;L and assess concentration by Qubit (wait until beads have settled before measuring).

> **NOTE:** Library can be now be stored at -20oC if required, but for best results it would be best to proceed immediately to sequencing. 

<div class="pagebreak"> </div>

### Part 5: Priming and loading the SpotON flow cell 

1. Thaw the following:
   - ABB Buffer (ABB) at RT 
   - Library loading beads (LLB) at RT   
   - Running Buffer with Fuel Mix (RBF) on ice 

2. Thoroughly mix the contents of the RBF and LLB tubes by pipetting.

3. Flip back the MinION lid and slide the priming port cover clockwise so that the priming port is visible.

> **IMPORTANT:** Care must be taken when drawing back buffer from the flow cell. The array of pores must be covered by buffer at all times. Removing more than 20-30&micro;L risks damaging the pores in the array.

5. After opening the priming port, check for small bubble under the cover. Draw back a small volume to remove any bubble (a few&micro;Ls):   
   - Set a P1000 pipette to 200&micro;L   
   - Insert the tip into the priming port   
   - Turn the wheel until the dial shows 220-230&micro;L, or until you can see a small volume of buffer entering the pipette tip.  
    
6. Prepare the flow cell priming mix in a clean 1.5 ml Eppendorf tube. Avoid introducing bubbles at this stage to ease the next step. 

    | RBF | 576&micro;L 
    | Nuclease-free water | 624&micro;L 
   
7. Load 800&micro;L of the priming mix into the flow cell via the priming port, using the dial-down method described in step 5, avoiding the introduction of air bubbles. 

8. Wait for 5 minutes.                                            

9. In a new tube prepare the library dilution for sequencing:

    | Reagent | Volume
    |---|--- 
    | RBF | 35&micro;L
    | Nuclease-free water | 3.5&micro;L
    | LLB | 25.5&micro;L
    | Library | 11&micro;L
    | Total | 75&micro;L 

10. Gently lift the SpotON sample port cover to make the SpotON sample port accessible.

11. Load 200&micro;L of the priming mix into the flow cell via the priming port (**NOT** the SpotON sample port), avoiding the introduction of air bubbles.

12.  Mix the prepared library gently by pipetting up and down just prior to loading.

13. Add 75&micro;L of sample to the flow cell via the SpotON sample port in a dropwise fashion. Ensure each drop flows into the port before adding the next.

14. Gently replace the SpotON sample port cover, making sure the bung enters the SpotON port, close the priming port and replace the MinION lid.

15. Double–click the MinKNOW icon located on the desktop to open the MinKNOW GUI. 

16. If your MinION was disconnected from the computer, plug it back in.

17. Choose the flow cell type from the selector box:
 
    - `FLO-MIN106` : R9.4.1 flowcells
   
    - `FLO-MIN107` : R9.5.1 flowcells

18. Then mark the flow cell as `Selected`. 

19. Click the `New Experiment` button at the bottom left of the GUI.

20. On the New experiment popup screen, select the running parameters for your experiment from the individual tabs:
   
    - `Output settings - FASTQ`
    : The number of basecalls that MinKNOW will write in a single file. By default this is set to 4000
    
    - `Output settings - FAST5`
    : The number of files that MinKNOW will write to a single folder. By default this is set to 4000
   
21. Click `Begin Experiment`.

22. Allow the script to run to completion.

23. The MinKNOW Experiment page will indicate the progression of the script; this can be accessed through the `Experiment` tab that will appear at the top right of the screen

24. Monitor messages in the Message panel in the MinKNOW GUI
