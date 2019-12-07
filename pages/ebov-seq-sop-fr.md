---
title: "Protocole de séquençage de virus Ebola par Nanopore | amplicon, barcoding natif"
keywords: protocol
layout: document
last_updated: Dec 06, 2019
tags: [protocol]
summary:
permalink: ebov/ebov-seq-sop-fr.html
folder: ebov
title_text: "Ebola virus sequencing protocol"
subtitle_text: "Nanopore | amplicon | native barcoding"
document_name: "ARTIC-EBOV-seqSOP-fr"
version: v2.0.0
language: fr
creation_date: 2019-12-06
revision_date: 2019-12-06
forked_from: doi:10.1038/nprot.2017.066
author: Luke Meredith, Josh Quick
citation: "Meredith, Quick *et al.* In Prep."
---

{% include callout.html
type='default'
content='**Overview:** Le protocole suivant est adapté de la méthode présentée dans [Quick et al. (2017) *Nature Protocols* **12:** 1261–1276 doi:10.1038/nprot.2017.066](http://doi.org/10.1038/nprot.2017.066) et traite des amorces, de la préparation et purification des amplicons, puis utilise un protocole tube-unique pour ligaturer la librairie avant de séquencer sur minION.'
%}

<br />

Ce document fait partie de la collection sur le protocole de séquençage du virus Ebola par Nanopore :
: [http://artic.network/ebov/](http://artic.network/ebov/)

#### Documents:

Plan des amorces Ebola :
: [https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V3](https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V3)

Protocole de séquençage du virus Ebola par Nanopore :
: [http://artic.network/ebov/ebov-seq-sop.html](http://artic.network/ebov/ebov-seq-sop.html)

Ebola virus Nanopore sequencing kit-list :
: [http://artic.network/ebov/ebov-seq-kit.html](http://artic.network/ebov/ebov-seq-kit.html)

<br /><br /><br />

{% include wellcome-trust.html %}

<div class="pagebreak"> </div>

## Préparation

#### Equipements nécessaires :

   |---:|:---
   |2| Hotte portative de préparation d'acides nucléiques ou équivalent
   |1| vortex 12V
   |1| Centrifugeuse portable Sprout
   |1| Pipette Eppendorf P1000
   |1| Pipette Eppendorf P100 
   |1| Pipette Eppendorf P10
   |1| Support convertible de tubes 1.5mL/0.6mL
   |1| Fluoromètre Quantus
   |1| Machine miniPCR.
   |1| Bloc chauffant
   |1| Support magnétique
{: .compact}

#### Consommables nécessaires :


   |---:|:---
   || Reverse Transcriptase SuperScript IV
   || Q5 Hot Start High-Fidelity 2X Master Mix
   || Amorces Ebola Zaire V3
   || NEBNext Ultra II End Repair/dA-Tailing Module
   || Blunt/TA Ligase Master Mix
   || Aline PCRCLEAN DX 50ml
   || Nanopore Ligation Sequencing Kit 1D
   || Nanopore Native Barcoding Expansion Kit
   || Nanopore R9.4.1 Flow cell
   || Tubes Eppendorf 1.5mL
   || Barettes de 8-tubes 0.2mL 
   || Tubes Falcon 50mL
   || Tubes PCR 0.5ml
   || Système QuantiFluor ONE dsDNA
   || Eau Nuclease-free
   || Ethanol à 70%
   || Cônes de pipette P1000
   || Cônes de pipette P100
   || Cônes de pipette P10 long (long-reach)
   || Papier absorbant
   || Conteneurs de déchets médicaux tranchants
{: .compact}

#### Recommandations de sécurité, de confinement et de contamination

   |---:|:---
   || Robe de laboratoire hydrophobe à nouer dans le dos
   || Gants
   || Stérilisateurs à lumière UV
   || Lingettes de décontamination MediPal
   || Réactifs DNAway and RNAse Zap
{: .compact}

<div class="pagebreak"> </div>

## Protocole

### Partie 1 : Synthèse d'ADNc avec la reverse transcriptase Superscript IV

> **NOTE SUR LA PRÉPARATION DE LA HOTTE :** Pour prévenir les contaminations croisées de l'échantillon ou d'autres réactifs, cette étape doit être effectuée dans la HOTTE DE PRÉPARATION D’ÉCHANTILLONS, qui est pré-stérilisée aux UV et traitée avec des lingettes MediPal, et les réactifs DNAway et RNAseZap. Nettoyer la hotte avec chacun des produits séquentiellement, avec 5 minutes de séchage entre passages. Les pipettes doivent aussi être traitées de la même manière, et exposées aux UV pendant 30 minutes entre chaque préparation de librairies.

1. Préparer la réaction suivante :

    |---|---
    |50&micro;M hexamères aléatoires (random hexamers) | | 1&micro;L   
    |10mM dNTPs mix (10mM chacun)| 1&micro;L   
    |Matrice RNA | 11&micro;L   
    |TOTAL | 12&micro;L

> **NOTE :** L'ARN viral d'origine d'un échantillon clinique doit être compris entre un Ct de 18 à 35. Si le Ct est entre 12 et 15, alors diluer l'échantillon d'un facteur 100 dans l'eau ; si le Ct est entre 15 et 18, alors diluer d'un facteur 10 dans l'eau. Cette dilution réduira le risque d'une inhibition de la PCR.

2. Mélanger doucement (éviter de vortexer) puis centrifuger brièvement le tube pour assurer un contact maximum avec le thermocycleur.
3. Incuber la réaction comme suit :

    |---|---|---
    | Dénaturation | 65&deg;C | 5 mins   
    | Hybridation des amorces | Glace | 1 min 

4. Ajouter ce qui suit à la matrice ADN hybridée :

    |---|---
    |Tampon (Buffer) SSIV | | 4&micro;L   
    |100mM DTT | 1&micro;L   
    |RNaseOUT RNase Inhibitor | 1&micro;L   
    |SSIV Reverse Transcriptase | 1&micro;L  
    |TOTAL | 20&micro;L    

5. Mélanger doucement (éviter de vortexer) puis centrifuger brièvement le tube pour assurer un contact maximum avec le thermocycleur.
6. Incuber la réaction comme suit :

    |---|---|---
    | Extension | 42&deg;C | 90 mins   
    | Inactivation | 70&deg;C | 10 mins

7. L'ADNc est maintenant prêt pour la synthèse des amplicons.

<div class="pagebreak"> </div>

### Partie 2 : Préparation des amplicons d'Ebola

> **NOTE SUR LA PRÉPARATION DE LA HOTTE :** Pour prévenir les contaminations croisées de l’échantillon ou d'autres réactifs, cette étape doit être effectuée dans la HOTTE DE MASTERMIX, qui est pré-stérilisée aux UV et traitée avec des lingettes MediPal, et les réactifs DNAway et RNAseZap. Nettoyer la hotte avec chacun des produits séquentiellement, avec 5 minutes de séchage entre passages. Les pipettes doivent aussi être traitées de la même manière, et exposées aux UV pendant 30 minutes entre chaque préparation de librairies. 

#### Dilution des amorces et préparation

1. Les amorces Ebola de ce protocole ont été préparées grâce à [Primal Scheme](http://primal.zibraproject.org) et génèrent des amplicons chevauchant de 400 nt. Les noms des amorces et leur dilution est listée dans le tableau suivant.

2. Les amorces doivent être préparée et aliquotées AVANT LE DÉPART dans une ENCEINTE PCR STÉRILE. Les amorces ou les réactifs de PCR ne doivent JAMAIS être placés près des matrices ou des amplicons avant usage.

3. Resuspendre les amorces lyophilisées à une concentration de 100&micro;M chacun.

4. Générer les stocks de pool d'amorces en ajoutant 5&micro;L de chaque paire d'amorces dans un tube Eppendorf de 1.5mL étiquetée “Pool 1, 100&micro;M” ou “Pool 2, 100&micro;M”. Le volume total doit être de 505&micro;L pour le Pool 1 et 530&micro;L pour le Pool 2. Ceci est un stock de chaque pool d'amorces à une concentration de 10X.

5. Diluer d'un facteur 10 ce pool d'amorces dans de l'eau de grade moléculaire pour générer les stocks d'amorces à 10&micro;M. Il est recommandé que plusieurs aliquots de chaque pool d'amorces soient préparés afin de tenir compte des risques de dégradation ou de contamination.

<div class="pagebreak"> </div>

  | Nom         | Séquence                         | Nom          | Séquence                 | Mélange | [Stock] |
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

> **NOTE :** Les amorces doivent être utilisées à une concentration finale de 0.015&micro;M par amorce. Ainsi, Pool 1 contient 101 amorces : il est donc nécessaire d'ajouter 3.8&micro;L du Pool 1 à 10&micro;M pour chaque réaction de 25&micro;L. Le pool 2 contient 106 amorces : il est donc nécessaire d'ajouter 4.0&micro;L du Pool 2 à 10&micro;M pour chaque réaction de 25&micro;L. Pour d'autres approches, ajuster le volume de manière appropriée.

6. Préparer les réactions de PCR comme suit dans des tubes PCR à paroi fine de 0.5 mL ou des barettes :

    |Réactif                         |Pool 1       |Pool 2        |
    |--------------------------------|-------------|--------------|
    |NEB Q5 Polymerase 2X MasterMix  |12.5&micro;L |12.5&micro;L  |
    |Pool d'amorces 1 ou 2 (10&micro;M) |3.8&micro;L  |4.0&micro;L   |
    |Eau                           |6.2&micro;L  |6.0&micro;L   |
    |TOTAL                           |22.5&micro;L |22.5&micro;L  |

> **NOTE :** Cette étape doit être faite dans la HOTTE MASTERMIX ; l'ADNc ne doit jamais être emmenée près de cette hotte mastermix.

7. Dans la HOTTE MATRICE ajouter 2.5&micro;L d'ADNc à chaque réaction Pool1 et Pool2 et bien mélanger.

8. Centrifuger brièvement les tubes pour enlever le contenu des couvercles.

9. Préparer les conditions de PCR comme suit :

    |Étape            |Temperature |Temps        |Cycles |
    |----------------|------------|------------|-------|
    |Activation par la chaleur |98&deg;C    |30 secondes  |1      |
    |Dénaturation    |98&deg;C    |15 secondes  |25-35  |
    |Hybridation       |65&deg;C    |300 secondes |25-35  |
    |Maintien            |4&deg;C     |Indéfini  |1      |				

> **NOTE :** Le nombre de cycle doit être de 25 pour des Ct compris entre 18 et 21 jusqu'à un maximum de 35 cycles pour Ct 35.

10. Purifier les amplicons en utilisant le protocole suivant dans la HOTTE MATRICE :

    1. Combiner entièrement le contenu des réactions de PCR “Pool1” et “Pool2” pour chaque échantillon biologique dans un seul tube Eppendorf 1.5mL.

    2. Mélanger délicatement, éviter de vortexer.

    3. S'assurer que les billes Aline sont bien resuspendues en mélangeant vigoureusement avant d'ajouter à l'échantillon. Le mélange doit être d'une couleur brune homogène.

    4. Ajouter un volume équivalent de billes Aline dans le tube et mélanger délicatement soit en pipettant ou en tapotant avec le doigt. Le volume total doit d'environ 50&micro;L, donc ajouter 50&micro;L de billes. 
    
    5. Centrifuger brièvement les tubes pour enlever les billes du couvercle ou des parois du tube.

    6. Incuber 5 mins à température ambiante.

    7. Placer sur un support magnétique et incuber 2 minutes ou jusqu'à ce que les billes aient formée un culot contre l'aimant et que la solution soit complètement transparente.

    8. Enlever et jeter avec précaution la solution, en faisant attention de ne pas toucher le culot de billes.

    9. Ajouter 200&micro;L d'éthanol 70% à température ambiante au culot. 

    10. Enlever et jeter avec précaution l'éthanol, en faisant attention de ne pas toucher le culot de billes.

    11. Répeter les étapes `9` à `10` pour laver à nouveau le culot.

    12. Centrifuger brièvement le culot et enlever avec précaution autant d'éthanol que possible en utilisant un cône de 10&micro;L.

    13. Laisser le culot sécher 1 minute, en éviter de trop le déssecher (si le culot commencer à craqueler, alors il est trop sec).

    14. Resuspendre le culot dans 30&micro;L d'eau, et incuber pour 2 mins.

    15. Placer sur un support magnétique et AVEC PRÉCAUTION enlever l'eau et la transférer dans un tube Eppendorf de 1.5mL propre. ASSUREZ-VOUS qu'aucune bille ne soit transférée dans ce tube. Dans certains cas, une brève centrifugation peut être utile pour culotter les billes résiduelles.
    
    16. Quantifier les mélanges d'amplicons en utilisant le protocole ONE dsDNA du fluoromètre Quantus

<div class="pagebreak"> </div>

### Partie 3 : Quantification Quantus des mélanges d'amplicons

1. Préparer le nombre requis de tubes 0.5mL.

> **NOTE :** N'utiliser que des tubes PCR à paroi fine et transparente de 0.5mL.

2. Annoter le couvercle des tubes. Ne pas annoter les côtés du tube, cela pourrait interférer avec la lecture de l'échantillon.

3. Ajouter 199&micro;L de la solution "ONE dsDNA dye" à chaque tube.

4. Ajouter 1&micro;L de chaque échantillon au tube correspondant.

> **NOTE :**  Utiliser une pipette P2 pour plus de précision.

5. Mélanger chaque échantillon vigoureusement en vortexant pendant 3-5 secondes.

6. Laisser les tubes incuber à température ambiante pendant 2 minutes avant de continuer.

7. Sur l'écran d’accueil du fluoromètre Quantus, sélectionner `Protocol`, puis `ONE DNA` comme type d'analyse.

> **NOTE :** Si vous avez déjà effectué une calibration pour l'analyse sélectionnée, vous pouvez continuer, il n'y a pas besoin de faire des calibrations répétées lors de l'utilisation de la solution ONE DNA pré-diluée. **Si vous souhaitez utiliser une calibration précédente, continuez à l'étape 11**. Dans le cas contraire, continuez avec l'étape 8.

8. Ajouter 200&micro;L de solution "ONE dsDNA Dye" à deux tubes de 0.5mL.

9. Ajouter 1&micro;L d'ADN Lambda standard à 400 ng/&micro;L fourni avec le kit dans l'un des deux tubes. Ces deux tubes sont respectivement le blanc et le standard requis pour effectuer la procédure de calibration à un point. 

10. Sélectionner `Calibrate`, puis `ONE DNA` et placer le blanc dans le lecteur puis sélectionner `Read Blank`. Ensuite placer le standard dans le lecteur et sélectionner `Read Std`.

11. Sur l'écran d’accueil, naviguer sur `Sample Volume` et régler sur 1&micro;L puis sur `Units` et régler sur ng/&micro;L.

12. Placer le premier échantillon dans le lecteur et fermer le couvercle. La concentration est lue automatiquement lors de sa fermeture.

13. Répéter l'étape 12 jusqu'à ce que tous les échantillons aient été lus.

14. La valeur affichée à l'écran est la concentration d'ADN double-brin. **Consigner avec soin tous les résultats** dans un tableur ou un cahier de laboratoire.

<div class="pagebreak"> </div>

### Partie 4: Barcoding et ligation des adapteurs: protocole en tube unique

> **NOTE:** Ceci est un protocole en tube unique pour la préparation de librairies avec ligation de barcode natifs. Nous n'avons observé aucune réduction de performance par rapport aux librairies standards, et peut même être plus rapide si l'on utilise le module Ultra II® ligation, qui est compatible avec le module Ultra II® end repair/dA-tailing en retirant une étape de purification. Si vous avez le temps, on recommande de doubler les temps d'incubation en <span style="color:blue">bleue</span>. Si vous êtes pressés, les temps indiqués en <span style="color:red">rouge</span> sont un bon compromis entre vitesse et efficacité.

1. Préparer la réaction de préparation d'extrémité (End Prep) suivante pour chaque échantillon biologique :

   | ADN (20 ng) | 16.7&micro;L
   | Ultra II End Prep Reaction Buffer | 2.3&micro;L
   | Ultra II End Prep Enzyme Mix | 1&micro;L
   | Total | 20&micro;L  

> **NOTE:** La quantité d'amplicons peut varier de 10-50ng, mais pas au-delà: le molarité de l'ADN serait trop élevée pour un barcoding efficace. Il faut avoir 6 échantillons par chaque librairie barcode natif pour avoir suffisamment de matériel à la fin. 

2. Incuber à température ambiante pendant 20 mins puis à 65&deg;C pendant 10 mins.

3. Placer sur glace pendant 30 secondes.

4. Ajouter directement aux réactions précédentes :

    | NBXX barcode | 2.5&micro;L
    | Ultra II Ligation Master Mix | 22.5&micro;L
    | Ligation Enhancer | 0.7&micro;L
    | Total | 45.7&micro;L

> **NOTE:** N'utiliser qu'UN SEUL barcode par échantillon biologique.

5. Incuber à température ambiante pendant 30 mins, 70&deg;C pendant 10 mins puis placer sur glace.

> **NOTE:** Cette étape vise à inactiver l'ADN ligase pour éviter des croisements entre barcodes.

6. Mélanger tous les fragments barcodés ensemble dans un tube Eppendorf 1.5mL propre.

7. Ajouter 45.7&micro;L de billes Aline par échantillon.

8. Incuber 5 mins.

9. Placer sur un support magnétique et incuber 2 minutes ou jusqu'à transparence.

10. Enlever la solution.

11. Ajouter 200&micro;L d'éthanol à 70%, toujours sur le support magnétique.

12. Enlever et jeter l'éthanol sans toucher le culot.

13.	Répéter les étapes 11 et 12.

15.	Centrifuger brièvement et enlever l'éthanol 70% résiduel puis sécher à l'air libre pendant 1 min.

16.	Resuspendre dans 31&micro;L de tampon EB.

17.	Incuber hors du support magnétique pendant 2 minutes.

18.	Replacer sur le support magnétique.

19. Attendre que la solution devienne transparente puis transférer la solution dans un tube Eppendorf propre de 1.5mL.

20.	Retirer 1&micro;L et mesurer la concentration par Quantus comme décrit au-dessus.

21. Préparer la réaction de ligation d'adaptateur suivante :

    | Mélanges purifiés de pool d'amplicons (~60ng) | 30&micro;L
    | NEBNext Quick Ligation Reaction Buffer (5X) | 10&micro;L
    | AMII adapter mix | 5&micro;L
    | Quick T4 DNA Ligase | 5&micro;L
    | Volume total | 50&micro;L

22. Incuber à température ambiante pendant 30 mins.

23. Ajouter 50&micro;L de billes Aline.

24. Incuber pendant 5 mins.

25. Placer sur un support magnétique jusqu'à transparence.

26. Retirer le surnageant.

27. Ajouter 200&micro;L de SFB et resuspendre en tapotant avec le doigt.

> **ATTENTION :** Ne pas utiliser d'éthanol à 80%.

28. Placer sur le support magnétique jusqu'à transparence.

29. Retirer le surnageant.

30. Répéter le lavage au SFB.

31. Centrifuger brièvement et retirer le SFB résiduel.

32. Ajouter 15&micro;L de tampon EB et resuspendre en tapotant avec le doigt.

33. Incuber à température ambiante pour 2 mins.

34. Placer sur le support magnétique.

35. Transférer avec précaution dans un tube Eppendorf 1.5mL propre.

36. Retirer 1&micro;L et mesurer la concentration avec le fluoromètre Quantus comme décrit au-dessus.

> **NOTE :** Les librairies peuvent être stockées à 4&deg;C si nécessaire, mais pour un meilleur résultat, il est préférable de continuer immédiatement avec le séquençage.

<div class="pagebreak"> </div>

### Partie 5 : Amorçage et chargement sur la flowcell SpotON

1. Dégeler les réactifs suivants à température ambiante avant de les placer sur glace:
   - Sequencing buffer (SQB) [tampon séquençage]
   - Loading beads (LB) [les billes pour le chargement de la flowcell]
   - Flush buffer (FLB) [tampon pour purger a flowcell]
   - Flush tether (FLT)

2. Ajouter 30&micro;L de FLT au tube de FLB et bien mélanger.

3. Retourner le couvercle de la flowcell et faire glisser le couvercle du port d'amorçage au sens des aiguilles d'une montre pour que le port d’amorçage devienne visible. 

> **ATTENTION :** Cette étape doit être faite avec précaution. La matrice des pores doit être constamment couverte par un tampon. Retirer plus que 20-30&micro;L risque d'endommager les pores.

5. Après avoir ouvert le port d'amorçage, vérifier s'il n'y a pas de petites bulles d'air sous le couvercle. Aspirer un petit volume pour enlever toute bulle (quelques &micro;Ls):   
   - Régler une pipette P1000 sur 200&micro;L   
   - Insérer le cône dans le port d'amorçage  
   - Tourner la molette de la pipette jusqu'à ce que le cadran indique 220-230&micro;L, ou jusqu'à ce que vous voyez un petit volume de tampon entrer dans le cône.  

6. Placer 800&micro;L du FLB+FLT dans la flowcell par le port d'amorçage, utilisant la méthode décrite à l'étape 5. Éviter d’introduire des bulles d'air.

7. Attendre 5 minutes.                                            

8. Dans un nouveau tube Eppendorf propre, préparer la dilution de la librairie pour le séquençage :

    | Réactif | Volume
    |---|---
    | SQB | 37.5&micro;L
    | LB | 25.5&micro;L
    | Librairie (~30ng) | 12&micro;L
    | Total | 75&micro;L

9. Soulever doucement le couvercle du port d'échantillon SpotON pour rendre le port accessible.

10. Placer 200&micro;L du mix d'amorçage dans le port d'amorçage (***PAS*** le port d'échantillon SpotON), en évitant l'introduction de bulles d'air.

11. Mélanger doucement la librairie préparée en pipettant de haut et en bas avant de charger la flowcell.

12. Au goutte à goutte, ajouter 75&micro;L de la librairie préparée sur la flowcell par le port d'échantillon SpotON. S'assurer que chaque goutte est bien aspirée dans le port avant ajouter la goutte suivante.

13. Replacer doucement le couvercle du port d'échantillon SpotON, en s'assurant que le bouchon entre bien dans le port SpotON. Fermer le port d’amorçage et replacer le couvercle du MinION.

14. Double-cliquer sur l'icone MinKNOW sur le bureau pour ouvrir l'interface graphique MinKNOW.

15. Si votre MinION été déconnectée de l'ordinateur, le re-connecter maintenant.

16. Choisir le type de flowcell dans la boîte de sélection :

    - `FLO-MIN106` : R9.4.1 flowcell

17. Marquer la flowcell comme `Selected`.

18. Cliquer sur le bouton `New Experiment` en bas à gauche de l'interface graphique.

19. Dans l'écran popup, sélectionner les paramètres pour votre expérience dans les onglets individuels :

    - `Experiment`
    : Nommer le run dans le champ expérience, laisser le champ de l'échantillon vide.

    - `Kit`
    : Selectionner LSK109 comme il n'y a pas d'option pour le kit de barcoding natif (NBD104)

    - `Run Options`
    : Définir la durée du run de sequançage, d'ordinaire 1-2 heures.

    - `Basecalling`
    : Laisser "basecalling" allumé et vérifier que le "HAC" (high accuracy model) est selectionné.

    - `Output`
    : Le nombre de fichiers que MinKNOW écrira dans un seul dossier. Par défaut réglé sur 4000.

20. Cliquer sur `Start run`.

21. Laisser le script se dérouler jusqu'au bout.

22. La page `Experiment` du MinKNOW indiquera la progression du script ; ceci est accessible par l'onglet `Experiment` qui apparaîtra en haut à droite de l'écran.

23. Surveillez le panneau `Message` du côté droit pour les erreurs.
