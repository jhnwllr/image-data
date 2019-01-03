
# GBIF image data

**Basis of record** tells us roughly whether an image was collected in situ (**human observation** like with a phone) or was collected or digitized by a museum (**preserved specimen**). Plants are often collected by museums as **preserved specimens** aka "herbarium sheets". For simplicity I have ignored other types of basis of record, since [there are very few images with other types of basis of record](https://www.gbif.org/occurrence/search?basis_of_record=FOSSIL_SPECIMEN&basis_of_record=LIVING_SPECIMEN&basis_of_record=UNKNOWN&basis_of_record=LITERATURE&basis_of_record=MATERIAL_SAMPLE&basis_of_record=MACHINE_OBSERVATION&basis_of_record=OBSERVATION&media_type=StillImage).

# Licenses 

There are many types of licenses. I have mostly broken things down into **non-commercial** and **commercial**. **Non-commerical** meaning anyone normal private citizen can use the photo not for profit. And **commercial** meaning a business could use the image to make a profit. 

# Image counts 

Below I look at raw image counts on GBIF. 

## Images counts by kingdom, basisofrecord, and license

Two things to notice here: 

* There are a lot of "herbarium sheets" (preserved specimens) for plants.
* There are very few human observations available for commercial use. 

![](https://raw.githubusercontent.com/jhnwllr/image-data/master/plots/kingdomBORBarplot.png)

## Here I have images broken down by class, basisofrecord, and license

At a lower taxonomic level we see that **flowering plants (magnoliopsida, liliopsida)** have many many images. Many are probably "herbarium sheets" (preserved specimens), but there are still millions of human observations. Again however **commercial use** might be difficult for many groups.

![](https://raw.githubusercontent.com/jhnwllr/image-data/master/plots/classBORBarplot.png)

# Species Counts 

The total number of images is less interesting than the total number of species. Now I want to look at **species counts with >10 images** rather than total image counts. 

## Species counts with >10 images 

In the plot I am only showing classes with more than >1000 species with >10 images.

![](https://raw.githubusercontent.com/jhnwllr/image-data/master/plots/classSpeBarplot.png)

# Percent coverage

Here I look at what is the percentage coverage in a group. 

**Percent coverage = num. sp. >10 img/total num. sp. in class**

## Percent coverage of species with >10 images

**Percent coverage (num. sp. >10 img/total num. sp. in taxonomic class)**. Here we see that global image coverage is quite poor for most groups with the exception of maybe **Aves** (birds) and a few plant classes (**Pinopsida**, **Lycopodiopsida**, **Polypodiopsida**), although many of these plant classes are "preserved specimens" aka probably herbarium sheets. Other groups have very poor global image coverage even considering preserved museum specimens. 

The global look for images for commercial use is even worse, although there is reasonable non-commercial image coverage. 

**Species counts** were taken from **GBIF backbone** and probably should be interpreted with caution. Duplicates might explain why we see >100% in some cases. A better measure might be the total number of species for which we have **at least 1 occurrence**. Still this graph  shows us that **regional breakdowns** are probably necessary for an image dataset with good coverage. 

![](https://raw.githubusercontent.com/jhnwllr/image-data/master/plots/percentageCoverageBarplot.png)

# Good regional image datasets

Below is a table of potentially good regional image datasets. 

An interactive version of this table can be found [here](https://jhnwllr.github.io/charts/percentCoverageTable). csv [here](https://github.com/jhnwllr/image-data/blob/master/data/percentCoverageTable.csv).

**PercentCoverage** = **totalSpeciesWith10Images** (or more) / **totalSpeciesInCountry**.  I have counted species as being in a country by including it if it at least has one occurrence record in that country. For example, 2773 of 3450 species of birds in the US have >10 images on GBIF, meaning there are 3450 bird species with >1 occurrence record in the US. This differs from the above graph because those totals were taken directly from the backbone. 

It might be possible to breakdown these categories even more. For example, certain insect groups like butterflies or dragonflies might have better regional coverage in some areas. 


| percentCoverage  | basisofrecord      | country            | class           | countryCode | totalSpeciesWith10Images | totalSpeciesInCountry | 
|------------------|--------------------|--------------------|-----------------|-------------|--------------------------|-----------------------| 
| 96.1699164345404 | HUMAN_OBSERVATION  | Australia          | Aves            | AU          | 1381                     | 1436                  | 
| 90.4347826086957 | HUMAN_OBSERVATION  | Mexico             | Aves            | MX          | 1560                     | 1725                  | 
| 80.3768115942029 | HUMAN_OBSERVATION  | United States      | Aves            | US          | 2773                     | 3450                  | 
| 77.1799628942486 | PRESERVED_SPECIMEN | Brazil             | Polypodiopsida  | BR          | 1664                     | 2156                  | 
| 73.2623208325152 | PRESERVED_SPECIMEN | Brazil             | Magnoliopsida   | BR          | 29850                    | 40744                 | 
| 70.2799410650389 | PRESERVED_SPECIMEN | United States      | Liliopsida      | US          | 6678                     | 9502                  | 
| 62.6786353498362 | PRESERVED_SPECIMEN | United States      | Magnoliopsida   | US          | 22763                    | 36317                 | 
| 60.5712409717663 | PRESERVED_SPECIMEN | Estonia            | Magnoliopsida   | EE          | 1845                     | 3046                  | 
| 51.3939393939394 | PRESERVED_SPECIMEN | Russia             | Liliopsida      | RU          | 1272                     | 2475                  | 
| 48.8372093023256 | PRESERVED_SPECIMEN | United States      | Lecanoromycetes | US          | 2373                     | 4859                  | 
| 48.254828871569  | PRESERVED_SPECIMEN | United States      | Bryopsida       | US          | 1424                     | 2951                  | 
| 48.2040229885057 | PRESERVED_SPECIMEN | Canada             | Liliopsida      | CA          | 1342                     | 2784                  | 
| 45.7916102841678 | HUMAN_OBSERVATION  | Denmark            | Agaricomycetes  | DK          | 1692                     | 3695                  | 
| 42.757030889811  | PRESERVED_SPECIMEN | Russia             | Magnoliopsida   | RU          | 4637                     | 10845                 | 
| 41.806125670982  | PRESERVED_SPECIMEN | Brazil             | Liliopsida      | BR          | 5296                     | 12668                 | 
| 41.0839160839161 | PRESERVED_SPECIMEN | Ukraine            | Magnoliopsida   | UA          | 1410                     | 3432                  | 
| 36.8472267272138 | PRESERVED_SPECIMEN | Puerto Rico        | Magnoliopsida   | PR          | 1136                     | 3083                  | 
| 35.6159548182139 | HUMAN_OBSERVATION  | United States      | Reptilia        | US          | 1009                     | 2833                  | 
| 34.6922246220302 | PRESERVED_SPECIMEN | New Caledonia      | Magnoliopsida   | NC          | 1285                     | 3704                  | 
| 34.4232278315459 | PRESERVED_SPECIMEN | Kazakhstan         | Magnoliopsida   | KZ          | 1316                     | 3823                  | 
| 33.4196106506595 | HUMAN_OBSERVATION  | United States      | Magnoliopsida   | US          | 12137                    | 36317                 | 
| 29.7960237541957 | HUMAN_OBSERVATION  | Norway             | Magnoliopsida   | NO          | 1154                     | 3873                  | 
| 29.2334724357566 | PRESERVED_SPECIMEN | Canada             | Magnoliopsida   | CA          | 2662                     | 9106                  | 
| 29.0909090909091 | HUMAN_OBSERVATION  | Norway             | Agaricomycetes  | NO          | 1136                     | 3905                  | 
| 28.9601554907677 | PRESERVED_SPECIMEN | Dominican Republic | Magnoliopsida   | DO          | 1192                     | 4116                  | 
| 28.3259911894273 | HUMAN_OBSERVATION  | New Zealand        | Magnoliopsida   | NZ          | 1929                     | 6810                  | 
| 25.8262747051985 | HUMAN_OBSERVATION  | South Africa       | Liliopsida      | ZA          | 1555                     | 6021                  | 
| 24.6855041610219 | PRESERVED_SPECIMEN | Madagascar         | Magnoliopsida   | MG          | 2551                     | 10334                 | 
| 24.656309377445  | PRESERVED_SPECIMEN | United States      | Agaricomycetes  | US          | 2206                     | 8947                  | 
| 23.7002736266049 | HUMAN_OBSERVATION  | United States      | Liliopsida      | US          | 2252                     | 9502                  | 
| 23.2820187271862 | PRESERVED_SPECIMEN | Cuba               | Magnoliopsida   | CU          | 1467                     | 6301                  | 
| 22.1834652228238 | HUMAN_OBSERVATION  | South Africa       | Magnoliopsida   | ZA          | 4261                     | 19208                 | 
| 20.9455683469319 | HUMAN_OBSERVATION  | United States      | Agaricomycetes  | US          | 1874                     | 8947                  | 
| 19.9099494838568 | HUMAN_OBSERVATION  | Canada             | Magnoliopsida   | CA          | 1813                     | 9106                  | 
| 18.3071161048689 | PRESERVED_SPECIMEN | Cameroon           | Magnoliopsida   | CM          | 1222                     | 6675                  | 
| 17.7177671661452 | PRESERVED_SPECIMEN | Angola             | Magnoliopsida   | AO          | 1076                     | 6073                  | 
| 17.1399045322573 | PRESERVED_SPECIMEN | Peru               | Magnoliopsida   | PE          | 3483                     | 20321                 | 
| 16.5469672189433 | PRESERVED_SPECIMEN | France             | Magnoliopsida   | FR          | 2327                     | 14063                 | 
| 16.266325691844  | PRESERVED_SPECIMEN | Estonia            | Insecta         | EE          | 1781                     | 10949                 | 
| 16.0236657216813 | PRESERVED_SPECIMEN | Taiwan             | Insecta         | TW          | 1300                     | 8113                  | 
| 15.9836993434458 | PRESERVED_SPECIMEN | Turkey             | Magnoliopsida   | TR          | 1412                     | 8834                  | 
| 14.6154350534391 | HUMAN_OBSERVATION  | Norway             | Insecta         | NO          | 2229                     | 15251                 | 
| 14.5991270388238 | PRESERVED_SPECIMEN | Mexico             | Magnoliopsida   | MX          | 3813                     | 26118                 | 
| 12.9522431259045 | PRESERVED_SPECIMEN | Venezuela          | Magnoliopsida   | VE          | 1790                     | 13820                 | 
| 11.6480231873556 | PRESERVED_SPECIMEN | Colombia           | Magnoliopsida   | CO          | 2572                     | 22081                 | 
| 10.9752802917736 | PRESERVED_SPECIMEN | Ecuador            | Magnoliopsida   | EC          | 1625                     | 14806                 | 
| 10.2330434782609 | PRESERVED_SPECIMEN | Spain              | Magnoliopsida   | ES          | 1471                     | 14375                 | 
| 9.40695776731517 | HUMAN_OBSERVATION  | United States      | Insecta         | US          | 8012                     | 85171                 | 
| 9.25902008899743 | PRESERVED_SPECIMEN | United States      | Insecta         | US          | 7886                     | 85171                 | 
| 9.08185925415422 | HUMAN_OBSERVATION  | Mexico             | Magnoliopsida   | MX          | 2372                     | 26118                 | 
| 8.32282471626734 | PRESERVED_SPECIMEN | Bolivia            | Magnoliopsida   | BO          | 1254                     | 15067                 | 
| 7.57327388367976 | PRESERVED_SPECIMEN | Norway             | Insecta         | NO          | 1155                     | 15251                 | 
| 7.51416270111036 | HUMAN_OBSERVATION  | Australia          | Magnoliopsida   | AU          | 1658                     | 22065                 | 
| 7.17878993881713 | PRESERVED_SPECIMEN | Australia          | Magnoliopsida   | AU          | 1584                     | 22065                 | 
| 7.10923953430765 | HUMAN_OBSERVATION  | Australia          | Insecta         | AU          | 2296                     | 32296                 | 
| 6.77214431259739 | HUMAN_OBSERVATION  | Canada             | Insecta         | CA          | 1695                     | 25029                 | 
| 6.74445547831844 | PRESERVED_SPECIMEN | China              | Magnoliopsida   | CN          | 1630                     | 24168                 | 
| 5.41961682632237 | PRESERVED_SPECIMEN | South Africa       | Magnoliopsida   | ZA          | 1041                     | 19208                 | 
| 5.32105577619232 | HUMAN_OBSERVATION  | Mexico             | Insecta         | MX          | 1514                     | 28453                 | 
| 5.22593791202205 | PRESERVED_SPECIMEN | Canada             | Insecta         | CA          | 1308                     | 25029                 | 
| 4.66311617537776 | PRESERVED_SPECIMEN | Australia          | Insecta         | AU          | 1506                     | 32296                 | 
| 3.99606368397006 | PRESERVED_SPECIMEN | Mexico             | Insecta         | MX          | 1137                     | 28453                 | 












