# Malagasy-Bible-1865
The **Malagasy Bible** translated in 1835 by [David Griffiths](https://en.wikipedia.org/wiki/David_Griffiths_(missionary)) and revised 1865-66
- David Haslam (text/module developer) - 23 January 2021

## Malagasy ##
Ny Baiboly Malagasy voalohany dia navoaka tamin'ny 1835, nadika avy amin'ny misiônera Welsh David Griffiths (1792-1863) an'ny **London Missionary Society**. Niatrika ny fanitsiana voalohany nataony teo anelanelan'ny 1865 sy 1866.

## Français ##
La première Bible malgache a été éditée en 1835, traduite par le missionnaire gallois David Griffiths (1792-1863) de la [Société missionnaire de Londres](https://fr.wikipedia.org/wiki/Soci%C3%A9t%C3%A9_missionnaire_de_Londres). Elle a subi sa toute première correction entre 1865 et 1866.

## English ##
The first Malagasy Bible was published in 1835, translated by Welsh missionary David Griffiths (1792-1863) of the [London Missionary Society](https://en.wikipedia.org/wiki/London_Missionary_Society). It underwent its first revision between 1865 and 1866.

### Source texts ###
The source text used as the starting point for this project was obtained on 2018-12-18 from the website of [MadaBibliq](https://web.archive.org/web/20181218163116/http://madabibliq.org:80/) that subsequently went AWOL.

- *The original URL is now occupied by a domain squatter, so the above link is to an archived copy on the **Wayback Machine**.*

One of the downloads on the **Concordance** page is particularly useful by being in [Zefania](https://www.zefaniabible.com/) like XML format, which can be downloaded from the following [link](https://web.archive.org/web/20181122034615/http://madabibliq.org/Concordance-malagasy/Linux_Bibliquest_Concordance_Malgache-2.1.0.tar.bz2) as a file in .tar.bz2 Linux compressed format. This contains an XML file called **malgache_malgache.xml** dated 2011-07-27 that was designed for use with [Bibliquest](https://www.bibliquest.net/) Bible software.

The sister website **Madagascar pour Christ** now redirects to [Henoy Ny Baiboly](https://nybaiboly.net/).

This page also has the [Malagasy Bible](https://nybaiboly.net/Bible.htm) available in both **.htm** and **.doc** format, just as the earlier website did.

NB. *I have not yet checked whether any editing changes were made after December 2018.*

It is not known how accurately transcribed the above digitised text source is relative to the corresponding printed edition of the Malagasy Bible.

### Reference work ###

A scanned library copy of the **1887 Edition** of the Malagasy Bible with 1656 pages has been found [here](https://archive.org/details/nysoratramasinad00lond).

This is entitled **Ny Soratra Masina, dia ny Testamenta Taloha sy ny Testamenta Vaovao; Nadika avy tamy ny teny Hebreo sy Grika. (Revision Committee's Version, 1887)**.

This was published in 1889 by the [British and Foreign Bible Society](https://www.biblesociety.org.uk/), is held by the [University of Toronto](https://www.utoronto.ca/), and scanned in 2014. AFAICT, this has not been converted to a usable electronic text. Nevertheless, this may be useful as a reference work to resolve issues with the digitised source text.

### License ###
The Malagasy Bible (1865) is Public Domain.

### Project aims ###
The main aim of this project is to derive an input file in **OSIS** XML format suitable for making a SWORD module for use with Bible study front-end apps associated with the [CrossWire Bible Society](https://crosswire.org/).

#### Text development ####
I did a significant amount of detailed text development during December 2018. 

Many of the details are recorded in my email conversations with this [developer](https://github.com/refdoc).

#### Versification ####
So far, the best fit versification for SWORD is **German** even though the Malagasy Bible was also published as a parallel text edition with a French Bible.

See [La BIBLE Franco-Malgache](https://web.archive.org/web/20181206105212fw_/http://www.madabibliq.org/Bible_franco-malgache/Bible_table_matieres.htm) **En colonnes parallèles côte à côte, la Bible en français (traduction J.N. Darby) et la Bible Malgache.** 

##### Psalm titles #####
The canonical Psalm titles were incorrectly versified in the source XML file. It was necessary to reversify these as verse 1 (sometimes 1-2) and renumber the subsequent verses in such Psalms.

#### Project status ####
Source files and derived files have now been uploaded.

The folder structure is described below.

#### XML
This folder contains the **Bibliquest** XML source text as well as the preprocessed file in which the Psalm titles and versification were adjusted.

#### Merged USFM
This folder contains a single output file in USFM format that then was subsequently split into 66 separate files.

#### USFM
This folder contains the 66 USFM files, one for each Bible book.

#### CMD
This folder contains two Windows CMD files:
1. to assign substitute drive letters (used for analysis)
2. to batch rename the 66 USFM files

#### TextPipe
This folder contains some of my TextPipe filters used for analysis and conversion tasks within this project.
- These are provided "as is" without any commitment to keeping them maintained.
- TextPipe software can be obtained from [DataMystic](https://www.datamystic.com/).
- I have a purchased license to use **TextPipe Standard** and I've been using **TextPipe** since 2001.

NB. The filters were last edited in December 2018 but have been resaved in the new *human readable* JSON format.

#### TextPipe\Lists
This folder contains several tab delimited external **replace lists** called by the main TextPipe filter.

#### OSIS
This folder contains the OSIS XML file made from the USFM files using **adyeths\u2o** Python script.

NB. The OSIS file was further post-processed without a change of filename.

#### SWORD
This folder contains the SWORD module **Mg1865x** made using the module tool called **osis2mod** from CrossWire.

##### Analysis
This folder contains text files relating to module build and testing.
- **osis2mod.log** - this has no entries - which illustrates that **German** v11n is a good match
- **Mg1865x.emptyvss.txt** is the output from Sword utility **emptyvss** - it lists 9 verses absent relative to the **German** v11n.
- **README.md** - observations on versification issues

##### mods.d
This folder contains the module configuration file.

##### modules
This folder contains the module data.

##### Zip
This folder contains an archived copy of the module made using the **Xiphos** maintenance feature.
