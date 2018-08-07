---
title: "Ebola virus Nanopore sequencing kit-list | Nanopore, amplicon, native barcoding"
keywords: kit-list
layout: document
last_updated: May 18, 2018
tags: [kit-list]
summary:
permalink: ebov/ebov-seq-kit.html
folder: ebov
title_text: "Ebola virus sequencing kit-list"
subtitle_text: "Nanopore | amplicon | native barcoding"
document_name: "ARTIC-EBOV-seqKit"
version: v1.0.0
creation_date: 2018-05-21
revision_date: 2018-05-21
forked_from: doi:10.1038/nprot.2017.066
author: Luke Meredith
citation: "Meredith, Quick *et al.* In Prep."
---

{% include callout.html
type='default'
content='**Overview:** The following protocol is adapted from the methods of [Quick et al. (2017) *Nature Protocols* **12:** 1261–1276 doi:10.1038/nprot.2017.066](http://doi.org/10.1038/nprot.2017.066) and covers primers, amplicon preparation and clean-up, then uses a single-tube protocol to barcode and adaptor ligate the library, before running minION.'
%}

This document is part of the Ebola virus Nanopore sequencing protocol package:
: [http://artic.network/ebov/](http://artic.network/ebov/)

#### Related documents:

Ebola primer scheme:
: [https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V2](https://github.com/artic-network/primer-schemes/tree/master/ZaireEbola/V2) 

Ebola virus Nanopore sequencing protocol:
: [http://artic.network/ebov/ebov-seq-sop.html](http://artic.network/ebov/ebov-seq-sop.html)

Ebola virus Nanopore sequencing kit-list:
: [http://artic.network/ebov/ebov-seq-kit.html](http://artic.network/ebov/ebov-seq-kit.html)

{% include icon-callout.html
type='default'
file='wellcome-logo-black-small.png'
url='http://wellcome.ac.uk'
title='Funded by the Wellcome Trust'
subtitle='Collaborators Award 206298/Z/17/Z --- <a href="artic.network">ARTIC network</a>'
%}

<div class="pagebreak"> </div>

### Library Preparation and Sequencing Reagents:

   | Product | Supplier | Cat No. | Unit Cost | # Req | Cost
   |-----------------------------------------|------------------|---|---|---|---
   | Vilo SSIV RT | Thermo | 11756050 | £793 | 1 | £793 | <span class="checkbox">&nbsp;</span>
   | Q5&reg; Hot Start HF Polymerase (2xMM)  | NEB | M0494L | £611 | 1 | £611 | <span class="checkbox">&nbsp;</span>
   | NEBNext&reg; UltraII&trade; End-prep | NEB | E7546L | £722 | 1 | £722 | <span class="checkbox">&nbsp; </span>
   | Ebola Zaire V2 Primers* | Thermo |  | £240 | 1 | £220 | <span class="checkbox">&nbsp;</span>
   | NEBNext&reg; UltraII&trade; Ligation Module | NEB | E7595L | £1,204 | 1 | £1,204 | <span class="checkbox">&nbsp;</span>
   | NEBNext&reg; FFPE Repair Module | NEB | M6630L | £539 | 1 | £539 | <span class="checkbox">&nbsp;</span>
   | Agencourt&reg; AmpureXP&trade; Beads (60mL) | FisherSci | 10453438 | £620 | 1 | £620 | <span class="checkbox">&nbsp;</span>
   | Ligation Sequencing Kit 1D | Nanopore | SQK-LSK108 | £450 | 4 | £1,800 | <span class="checkbox">&nbsp;</span>
   | Low Input by PCR Barcoding Kit | Nanopore | SQK-LWB001 | £500 | 2 | £1,000 | <span class="checkbox">&nbsp;</span>
   | Native Barcoding Expansion Kit | Nanopore | EXP-NBD103 | £250 | 4 | £1,000 | <span class="checkbox">&nbsp;</span>
   | R9.4.1 flow cells | Nanopore |  | £375 | 12 | £4,500 | <span class="checkbox">&nbsp;</span>
   | Qubit&reg; dsDNA HS Assay Kit | Thermo | Q32851 | £185 | 2 | £370 | <span class="checkbox">&nbsp;</span>
   | **TOTAL COST** | | | | | **£13,379**
               
               
<div class="pagebreak"></div>

### Equipment and Containment

   | Product | Supplier | Cat No. | Unit Cost | # Req | Cost
   |---|---|---|---|---|---
   | 1000&micro;L pipettes | Gilson | 10387322 | £210 | 2 | £420 | <span class="checkbox">&nbsp;</span>  
   | 100&micro;L pipettes | Gilson | 10442412 | £210 | 2 | £420 | <span class="checkbox">&nbsp;</span>  
   | 10&micro;L pipettes | Gilson | 10236072 | £210 | 2 | £420 | <span class="checkbox">&nbsp;</span>  
   | Sprout Microfuge (12V) | PhilipHarris | B8R04574 | £170 | 2 | £340 | <span class="checkbox">&nbsp;</span>  
   | PV-1 Mini Vortex | WolfLabs | PV-1 | £150 | 2 | £300 | <span class="checkbox">&nbsp;</span>  
   | Portable Heat Block | Mobitec | Pad3-H-CB | £310 | 1 | £310 | <span class="checkbox">&nbsp;</span>  
   | DynaMag-2 magnetic rack | Thermo | 12321D | £540 | 1 | £540 | <span class="checkbox">&nbsp;</span>  
   | MiniPCR&trade; Mini8 | Cambio | MPQP100001 | £535 | 4 | £2,140 | <span class="checkbox">&nbsp;</span>  
   | MyGo&reg; Mini qPCR | IT-IS  | SKU7642 | £6,500 | 1 | £6,500 | <span class="checkbox">&nbsp;</span>  
   | Qubit4&reg; spectrophotometer | Thermo | Q33228 | £2,578 | 1 | £2,578 | <span class="checkbox">&nbsp;</span>  
   | Collapsible Tube racks (small x5) | FisherSci | 11770045 | £50 | 1 | £50 | <span class="checkbox">&nbsp;</span>  
   | Collapsible Tube racks (large x5) | FisherSci | 11710634 | £50 | 1 | £50 | <span class="checkbox">&nbsp;</span>  
   | Cold Racks (0.2-0.5mL) | Sigma | Z606634-1EA | £50 | 2 | £100 | <span class="checkbox">&nbsp;</span>  
   | Lab Mats | StarLab | E3860-0061 | £25 | 2 | £50 | <span class="checkbox">&nbsp;</span>  
   | USB Lights | Amazon | Jebsen-T05 | £20 | 2 | £40 | <span class="checkbox">&nbsp;</span>  
   | Portable UV Lamps | Amazon | B078LSR3MG | £20 | 2 | £40 | <span class="checkbox">&nbsp;</span> 
   | Portable glove box | Amazon | B01B1MGRR0 | £70 | 2 | £40 | <span class="checkbox">&nbsp;</span>  
   | TOTAL COST |  |  |  |  | £14,438 | 
 
 
### Consumables and Disposables
 
   | Product (Number) | Supplier | Cat No. | Unit Cost | # Req | Cost | 
   |---|---|---|---|---|---
   | Stacked 1000&micro;L Filter Tips (500) | FisherSci | 11977724 | £70 | 2 | £140 | <span class="checkbox">&nbsp;</span>  
   | Stacked 100&micro;L Filter Tips (1000) | FisherSci | 11947724 | £60 | 1 | £60 | <span class="checkbox">&nbsp;</span>  
   | Stacked 10&micro;L Filter Tips (1000) | FisherSci | 11907724 | £60 | 1 | £60 | <span class="checkbox">&nbsp;</span>  
   | 1.5mL Eppendorf Tubes (500) | StarLab | I1415-5500 | £20 | 2 | £40 | <span class="checkbox">&nbsp;</span>  
   | 0.6mL Eppendorf Tubes (500) | StarLab | I1405-1500 | £20 | 1 | £20 | <span class="checkbox">&nbsp;</span>  
   | 0.2mL 8-strip tubes (1000) | StarLab | I1402-3600 | £60 | 1 | £60 | <span class="checkbox">&nbsp;</span>  
   | Qubit Reaction Tubes (500) | Thermo | Q32856 | £50 | 1 | £50 | <span class="checkbox">&nbsp;</span>  
   | MyGo PCR Tubes (500) | IT-IS  | SKU7688 | £85 | 1 | £85 | <span class="checkbox">&nbsp;</span>  
   | BioBIn&reg; Disposal Bins (100) | FisherSci | 10394373 | £121 | 1 | £121 | <span class="checkbox">&nbsp;</span>  
   | Gloves (Large, 100) | StarLab | SG-P-L | £5 | 2 | £10 | <span class="checkbox">&nbsp;</span>  
   | Gloves (Small, 100) | StarLab | SG-P-S | £5 | 2 | £10 | <span class="checkbox">&nbsp;</span>  
   | Paper Towels | Generic |  |  | 4 | N/A | <span class="checkbox">&nbsp;</span>  
   | Decon Wipes (240) | MediPal | PMC6038 | £6 | 2 | £12 | <span class="checkbox">&nbsp;</span>  
   | Back-tie Lab Gowns (45G) | VWR | 113-8316 | £56 | 10 | £56 | <span class="checkbox">&nbsp;</span>  
   | RNAse Away (250mL) | Thermo | 10328011 | £60 | 2 | £120 | <span class="checkbox">&nbsp;</span>  
   | DNA Away (250mL) | Thermo | 7010PK | £20 | 2 | £40 | <span class="checkbox">&nbsp;</span>  
   | **TOTAL COST** |  |  |  |  | **£884** | 
 
 
### Cold Chain, Power and Storage

   | Product (Number) | Supplier | Cat No. | Unit Cost | # Req | Cost | 
   |---|---|---|---|---|---
   | Flat dehydrated cold sheets (ThermaFreeze) | Amazon | B003ET2G74 | £15 | 10 | £150 | <span class="checkbox">&nbsp;</span>  
   | Thermos Radiance Cooler Bag | Amazon | B00BHW5B4U | £10 | 4 | £40 | <span class="checkbox">&nbsp;</span>  
   | Portable Fridge Bag | Amazon | B008N5UU3G | £70 | 1 | £70 | <span class="checkbox">&nbsp;</span>  
   | Credo Cube Series 20M 4L | Pelican  | Contact Supp. |  |  | N/A | <span class="checkbox">&nbsp;</span>  
   | PowerAdd Pilot Pro2 85Wh LiION 9-20V | Amazon | B013HXKZYW | £80 | 2 | £160 | <span class="checkbox">&nbsp;</span>  
   | Solar Charger, 85Wh, LiION 5-20V | Amazon | B00AE9FBCO | £85 | 2 | £170 | <span class="checkbox">&nbsp;</span>  
   | Goal Zero Yeti 150 Portable Power Station | GoalZero | SKU22004 | £200 | 1 | £200 | <span class="checkbox">&nbsp;</span>  
   | Goal Zero Nomad 28 Plus Solar Panel | Goal Zero | SKU11805 | £250 | 1 | £250 | <span class="checkbox">&nbsp;</span>  
   | Surge Protector Extension (4-plug) | Belkin | B0002AG0F2 | £6 | 3 | £18 | <span class="checkbox">&nbsp;</span>  
   | SKROSS Universal Mini Travel Adaptor | Amazon | B00OHSWG6C | £10 | 2 | £20 | <span class="checkbox">&nbsp;</span>  
   | Peli Air 1615 Waterproof Equipment Case | R&S Comp. | 121-8893 | £550 | 1 | £550 | <span class="checkbox">&nbsp;</span>  
   | Eagle Creek Cargo Hauler, 120L | Amazon | B01HIGO3OC | £150 | 1 | £150 | <span class="checkbox">&nbsp;</span>  
   | BESTEK 200W Power Inverter DC 12V | Amazon | B01N2P9V64 | £30 | 1 | £30 | <span class="checkbox">&nbsp;</span>  
   | Samsung Portable SSD T5 1TB | Amazon | B074M774TW | £320 | 2 | £640 | <span class="checkbox">&nbsp;</span>  
   | Seagate&reg; 5TB External HD  | Amazon | B01M058Q39 | £119 | 2 | £238 | <span class="checkbox">&nbsp;</span>  
   | **TOTAL COST** |  |  |  |  | **£2,686** | 
 
 
 <!--IT Requirements-->
 
