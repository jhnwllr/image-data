
# GBIF image data

**Basis of record** tells us roughly whether an image was collected in situ (**human observation** like with a phone) or was collected or digitized by a museum (**preserved specimen**). Plants are often collected by museums as **preserved specimens** aka "herbarium sheets". For simplicity I have ignored other types of basis of record, since [there are very few images with other types of basis of record](https://www.gbif.org/occurrence/search?basis_of_record=FOSSIL_SPECIMEN&basis_of_record=LIVING_SPECIMEN&basis_of_record=UNKNOWN&basis_of_record=LITERATURE&basis_of_record=MATERIAL_SAMPLE&basis_of_record=MACHINE_OBSERVATION&basis_of_record=OBSERVATION&media_type=StillImage).

# Licenses 

There are many types of licenses. I have mostly broken things down into **non-commercial** and **commercial**. **Non-commerical** meaning any normal private citizen can use the photo not for profit. And **commercial** meaning a business could use the image to make a profit. 

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

| percentCoverage    | basisofrecord      | country                          | class             | totalSpeciesInCountry | totalSpeciesWith10Images | license         | 
|--------------------|--------------------|----------------------------------|-------------------|-----------------------|--------------------------|-----------------| 
| 111.111111111111   | PRESERVED_SPECIMEN | Estonia                          | Polypodiopsida    | 36                    | 40                       | total           | 
| 111.111111111111   | PRESERVED_SPECIMEN | Estonia                          | Polypodiopsida    | 36                    | 40                       | non-commercial  | 
| 102.941176470588   | HUMAN_OBSERVATION  | South Korea                      | Amphibia          | 34                    | 35                       | total           | 
| 102.941176470588   | HUMAN_OBSERVATION  | South Korea                      | Amphibia          | 34                    | 35                       | non-commercial  | 
| 101.41592920354    | PRESERVED_SPECIMEN | Estonia                          | Liliopsida        | 565                   | 573                      | non-commercial  | 
| 101.41592920354    | PRESERVED_SPECIMEN | Estonia                          | Liliopsida        | 565                   | 573                      | total           | 
| 100                | PRESERVED_SPECIMEN | Canada                           | Equisetopsida     | 33                    | 33                       | total           | 
| 96.6666666666667   | PRESERVED_SPECIMEN | French Southern Territories      | Polypodiopsida    | 30                    | 29                       | total           | 
| 96.3712491277041   | HUMAN_OBSERVATION  | Australia                        | Aves              | 1433                  | 1381                     | total           | 
| 94.2857142857143   | PRESERVED_SPECIMEN | United States                    | Psilotopsida      | 70                    | 66                       | total           | 
| 90.4872389791183   | HUMAN_OBSERVATION  | Mexico                           | Aves              | 1724                  | 1560                     | total           | 
| 89.5953757225434   | PRESERVED_SPECIMEN | Cameroon                         | Polypodiopsida    | 346                   | 310                      | total           | 
| 86.25              | PRESERVED_SPECIMEN | New Caledonia                    | Pinopsida         | 80                    | 69                       | total           | 
| 85                 | PRESERVED_SPECIMEN | New Caledonia                    | Pinopsida         | 80                    | 68                       | non-commercial  | 
| 80.3768115942029   | HUMAN_OBSERVATION  | United States                    | Aves              | 3450                  | 2773                     | total           | 
| 77.6223776223776   | HUMAN_OBSERVATION  | Norway                           | Aves              | 715                   | 555                      | total           | 
| 77.6119402985075   | HUMAN_OBSERVATION  | New Zealand                      | Aves              | 536                   | 416                      | total           | 
| 77.2516248839369   | PRESERVED_SPECIMEN | Brazil                           | Polypodiopsida    | 2154                  | 1664                     | total           | 
| 75.754060324826    | HUMAN_OBSERVATION  | Mexico                           | Aves              | 1724                  | 1306                     | non-commercial  | 
| 73.2569268903232   | PRESERVED_SPECIMEN | Brazil                           | Magnoliopsida     | 40747                 | 29850                    | total           | 
| 72.4137931034483   | HUMAN_OBSERVATION  | New Zealand                      | Lycopodiopsida    | 29                    | 21                       | total           | 
| 72.4137931034483   | HUMAN_OBSERVATION  | New Zealand                      | Lycopodiopsida    | 29                    | 21                       | non-commercial  | 
| 71.4285714285714   | PRESERVED_SPECIMEN | Turkey                           | Pinopsida         | 35                    | 25                       | total           | 
| 71.4285714285714   | PRESERVED_SPECIMEN | Turkey                           | Pinopsida         | 35                    | 25                       | non-commercial  | 
| 70.8888888888889   | HUMAN_OBSERVATION  | New Zealand                      | Polypodiopsida    | 450                   | 319                      | total           | 
| 70.8888888888889   | HUMAN_OBSERVATION  | New Zealand                      | Polypodiopsida    | 450                   | 319                      | non-commercial  | 
| 70.1492537313433   | PRESERVED_SPECIMEN | United States                    | Equisetopsida     | 67                    | 47                       | total           | 
| 70.117597648047    | PRESERVED_SPECIMEN | United States                    | Liliopsida        | 9524                  | 6678                     | total           | 
| 68.6274509803922   | PRESERVED_SPECIMEN | Palau                            | Reptilia          | 51                    | 35                       | open commercial | 
| 68.6274509803922   | PRESERVED_SPECIMEN | Palau                            | Reptilia          | 51                    | 35                       | non-commercial  | 
| 68.6274509803922   | PRESERVED_SPECIMEN | Palau                            | Reptilia          | 51                    | 35                       | total           | 
| 66.6666666666667   | PRESERVED_SPECIMEN | United States                    | Charophyceae      | 99                    | 66                       | total           | 
| 66.4179104477612   | HUMAN_OBSERVATION  | New Zealand                      | Aves              | 536                   | 356                      | non-commercial  | 
| 65.9090909090909   | HUMAN_OBSERVATION  | South Africa                     | Aves              | 1276                  | 841                      | total           | 
| 65.6565656565657   | PRESERVED_SPECIMEN | United States                    | Charophyceae      | 99                    | 65                       | open commercial | 
| 65.6565656565657   | PRESERVED_SPECIMEN | United States                    | Charophyceae      | 99                    | 65                       | non-commercial  | 
| 65.4782608695652   | HUMAN_OBSERVATION  | United States                    | Aves              | 3450                  | 2259                     | non-commercial  | 
| 65.1851851851852   | PRESERVED_SPECIMEN | United States                    | Sphagnopsida      | 135                   | 88                       | total           | 
| 65.0943396226415   | HUMAN_OBSERVATION  | Denmark                          | Aves              | 636                   | 414                      | non-commercial  | 
| 65.0943396226415   | HUMAN_OBSERVATION  | Denmark                          | Aves              | 636                   | 414                      | total           | 
| 63.2326820603908   | HUMAN_OBSERVATION  | Estonia                          | Aves              | 563                   | 356                      | total           | 
| 62.9666011787819   | HUMAN_OBSERVATION  | Canada                           | Aves              | 1018                  | 641                      | total           | 
| 62.5993454885461   | PRESERVED_SPECIMEN | United States                    | Magnoliopsida     | 36363                 | 22763                    | total           | 
| 62.5222024866785   | HUMAN_OBSERVATION  | Estonia                          | Aves              | 563                   | 352                      | non-commercial  | 
| 62.5               | PRESERVED_SPECIMEN | Brazil                           | Lycopodiopsida    | 280                   | 175                      | total           | 
| 61.8860510805501   | HUMAN_OBSERVATION  | Canada                           | Aves              | 1018                  | 630                      | non-commercial  | 
| 61.4420062695925   | HUMAN_OBSERVATION  | South Africa                     | Aves              | 1276                  | 784                      | non-commercial  | 
| 60.5513619954053   | PRESERVED_SPECIMEN | Estonia                          | Magnoliopsida     | 3047                  | 1845                     | total           | 
| 60.5513619954053   | PRESERVED_SPECIMEN | Estonia                          | Magnoliopsida     | 3047                  | 1845                     | non-commercial  | 
| 60.2941176470588   | HUMAN_OBSERVATION  | Norway                           | Pinopsida         | 68                    | 41                       | total           | 
| 60.2739726027397   | HUMAN_OBSERVATION  | Norway                           | Polypodiopsida    | 73                    | 44                       | total           | 
| 60                 | PRESERVED_SPECIMEN | United States                    | Marchantiopsida   | 140                   | 84                       | total           | 
| 60                 | HUMAN_OBSERVATION  | Italy                            | Amphibia          | 60                    | 36                       | total           | 
| 60                 | PRESERVED_SPECIMEN | New Caledonia                    | Pinopsida         | 80                    | 48                       | open commercial | 
| 59.1916558018253   | HUMAN_OBSERVATION  | United States                    | Amphibia          | 767                   | 454                      | total           | 
| 59.1549295774648   | PRESERVED_SPECIMEN | Russia                           | Sphagnopsida      | 71                    | 42                       | total           | 
| 58.4615384615385   | PRESERVED_SPECIMEN | United States                    | Lycopodiopsida    | 325                   | 190                      | total           | 
| 57.780612244898    | PRESERVED_SPECIMEN | United States                    | Polypodiopsida    | 1568                  | 906                      | total           | 
| 57.7464788732394   | PRESERVED_SPECIMEN | Russia                           | Sphagnopsida      | 71                    | 41                       | non-commercial  | 
| 57.7464788732394   | PRESERVED_SPECIMEN | Russia                           | Sphagnopsida      | 71                    | 41                       | open commercial | 
| 57.2649572649573   | HUMAN_OBSERVATION  | Norway                           | Mammalia          | 117                   | 67                       | total           | 
| 55.8139534883721   | PRESERVED_SPECIMEN | Puerto Rico                      | Lycopodiopsida    | 43                    | 24                       | total           | 
| 55.5555555555556   | PRESERVED_SPECIMEN | Sweden                           | Charophyceae      | 54                    | 30                       | total           | 
| 55.5555555555556   | PRESERVED_SPECIMEN | Sweden                           | Charophyceae      | 54                    | 30                       | open commercial | 
| 55.5555555555556   | PRESERVED_SPECIMEN | Sweden                           | Charophyceae      | 54                    | 30                       | non-commercial  | 
| 55.3191489361702   | PRESERVED_SPECIMEN | Russia                           | Lycopodiopsida    | 47                    | 26                       | total           | 
| 54.9295774647887   | PRESERVED_SPECIMEN | United States                    | Taphrinomycetes   | 71                    | 39                       | non-commercial  | 
| 54.9295774647887   | PRESERVED_SPECIMEN | United States                    | Taphrinomycetes   | 71                    | 39                       | total           | 
| 54.9295774647887   | PRESERVED_SPECIMEN | United States                    | Taphrinomycetes   | 71                    | 39                       | open commercial | 
| 54.5454545454545   | PRESERVED_SPECIMEN | Philippines                      | Amphibia          | 165                   | 90                       | non-commercial  | 
| 54.5454545454545   | PRESERVED_SPECIMEN | Philippines                      | Amphibia          | 165                   | 90                       | total           | 
| 53.9765319426336   | HUMAN_OBSERVATION  | United States                    | Amphibia          | 767                   | 414                      | non-commercial  | 
| 53.9393939393939   | PRESERVED_SPECIMEN | Philippines                      | Amphibia          | 165                   | 89                       | open commercial | 
| 53.6231884057971   | PRESERVED_SPECIMEN | Guatemala                        | Lycopodiopsida    | 69                    | 37                       | total           | 
| 53.3333333333333   | HUMAN_OBSERVATION  | Italy                            | Amphibia          | 60                    | 32                       | non-commercial  | 
| 53.2110091743119   | HUMAN_OBSERVATION  | Canada                           | Amphibia          | 109                   | 58                       | total           | 
| 52.3232323232323   | PRESERVED_SPECIMEN | Puerto Rico                      | Polypodiopsida    | 495                   | 259                      | total           | 
| 51.3524424707307   | PRESERVED_SPECIMEN | Russia                           | Liliopsida        | 2477                  | 1272                     | total           | 
| 51.1450381679389   | HUMAN_OBSERVATION  | New Zealand                      | Mammalia          | 131                   | 67                       | total           | 
| 50.4587155963303   | HUMAN_OBSERVATION  | Canada                           | Amphibia          | 109                   | 55                       | non-commercial  | 
| 50.2403846153846   | PRESERVED_SPECIMEN | Philippines                      | Reptilia          | 416                   | 209                      | total           | 
| 50                 | PRESERVED_SPECIMEN | Dominican Republic               | Reptilia          | 178                   | 89                       | total           | 
| 50                 | HUMAN_OBSERVATION  | South Korea                      | Reptilia          | 58                    | 29                       | total           | 
| 50                 | HUMAN_OBSERVATION  | South Korea                      | Reptilia          | 58                    | 29                       | non-commercial  | 
| 50                 | PRESERVED_SPECIMEN | Philippines                      | Reptilia          | 416                   | 208                      | non-commercial  | 
| 48.9920201595968   | PRESERVED_SPECIMEN | United States                    | Liliopsida        | 9524                  | 4666                     | non-commercial  | 
| 48.936170212766    | PRESERVED_SPECIMEN | Russia                           | Lycopodiopsida    | 47                    | 23                       | open commercial | 
| 48.936170212766    | PRESERVED_SPECIMEN | Russia                           | Lycopodiopsida    | 47                    | 23                       | non-commercial  | 
| 48.7769784172662   | PRESERVED_SPECIMEN | United States                    | Lecanoromycetes   | 4865                  | 2373                     | total           | 
| 48.271186440678    | PRESERVED_SPECIMEN | United States                    | Bryopsida         | 2950                  | 1424                     | total           | 
| 48.1283422459893   | PRESERVED_SPECIMEN | Madagascar                       | Polypodiopsida    | 748                   | 360                      | total           | 
| 48.0486931614751   | PRESERVED_SPECIMEN | Canada                           | Liliopsida        | 2793                  | 1342                     | total           | 
| 47.752808988764    | PRESERVED_SPECIMEN | Dominican Republic               | Reptilia          | 178                   | 85                       | non-commercial  | 
| 47.5234270414993   | PRESERVED_SPECIMEN | Cuba                             | Polypodiopsida    | 747                   | 355                      | total           | 
| 47.4576271186441   | PRESERVED_SPECIMEN | Madagascar                       | Lycopodiopsida    | 59                    | 28                       | total           | 
| 47.0402525651144   | PRESERVED_SPECIMEN | Malaysia                         | Polypodiopsida    | 1267                  | 596                      | total           | 
| 46.9598965071151   | PRESERVED_SPECIMEN | United States                    | Pinopsida         | 773                   | 363                      | total           | 
| 46.9115865966895   | PRESERVED_SPECIMEN | Russia                           | Liliopsida        | 2477                  | 1162                     | non-commercial  | 
| 46.8085106382979   | PRESERVED_SPECIMEN | United States                    | Gnetopsida        | 47                    | 22                       | total           | 
| 46.6289866774324   | PRESERVED_SPECIMEN | Russia                           | Liliopsida        | 2477                  | 1155                     | open commercial | 
| 46.5753424657534   | PRESERVED_SPECIMEN | Norway                           | Polypodiopsida    | 73                    | 34                       | total           | 
| 46.4336661911555   | PRESERVED_SPECIMEN | Russia                           | Bryopsida         | 1402                  | 651                      | total           | 
| 46                 | PRESERVED_SPECIMEN | Canada                           | Lycopodiopsida    | 100                   | 46                       | total           | 
| 45.945945945946    | PRESERVED_SPECIMEN | Brazil                           | Phaeophyceae      | 111                   | 51                       | total           | 
| 45.8015267175573   | HUMAN_OBSERVATION  | New Zealand                      | Mammalia          | 131                   | 60                       | non-commercial  | 
| 45.7916102841678   | HUMAN_OBSERVATION  | Denmark                          | Agaricomycetes    | 3695                  | 1692                     | total           | 
| 45.7317073170732   | PRESERVED_SPECIMEN | Haiti                            | Reptilia          | 164                   | 75                       | total           | 
| 45.6953642384106   | HUMAN_OBSERVATION  | Armenia                          | Aves              | 302                   | 138                      | non-commercial  | 
| 45.6953642384106   | HUMAN_OBSERVATION  | Armenia                          | Aves              | 302                   | 138                      | total           | 
| 45.6490727532097   | PRESERVED_SPECIMEN | Russia                           | Bryopsida         | 1402                  | 640                      | non-commercial  | 
| 45.6490727532097   | PRESERVED_SPECIMEN | Russia                           | Bryopsida         | 1402                  | 640                      | open commercial | 
| 45.6140350877193   | PRESERVED_SPECIMEN | United Kingdom                   | Sarcopterygii     | 57                    | 26                       | non-commercial  | 
| 45.6140350877193   | PRESERVED_SPECIMEN | United Kingdom                   | Sarcopterygii     | 57                    | 26                       | open commercial | 
| 45.6140350877193   | PRESERVED_SPECIMEN | United Kingdom                   | Sarcopterygii     | 57                    | 26                       | total           | 
| 45.4326923076923   | PRESERVED_SPECIMEN | Philippines                      | Reptilia          | 416                   | 189                      | open commercial | 
| 45.3125            | HUMAN_OBSERVATION  | Taiwan                           | Amphibia          | 64                    | 29                       | total           | 
| 45.3125            | HUMAN_OBSERVATION  | Taiwan                           | Amphibia          | 64                    | 29                       | non-commercial  | 
| 44.7761194029851   | HUMAN_OBSERVATION  | United States                    | Equisetopsida     | 67                    | 30                       | total           | 
| 44.7080291970803   | HUMAN_OBSERVATION  | South Korea                      | Aves              | 548                   | 245                      | total           | 
| 44.7019867549669   | HUMAN_OBSERVATION  | Armenia                          | Aves              | 302                   | 135                      | open commercial | 
| 44.6083995459705   | PRESERVED_SPECIMEN | Norway                           | Liliopsida        | 881                   | 393                      | total           | 
| 44.5019404915912   | HUMAN_OBSERVATION  | United States                    | Pinopsida         | 773                   | 344                      | total           | 
| 44.48              | HUMAN_OBSERVATION  | Italy                            | Aves              | 625                   | 278                      | total           | 
| 44.3965517241379   | PRESERVED_SPECIMEN | China                            | Pinopsida         | 232                   | 103                      | total           | 
| 44.1666666666667   | PRESERVED_SPECIMEN | Philippines                      | Lycopodiopsida    | 120                   | 53                       | total           | 
| 43.978102189781    | HUMAN_OBSERVATION  | South Korea                      | Aves              | 548                   | 241                      | non-commercial  | 
| 43.75              | PRESERVED_SPECIMEN | Japan                            | Amphibia          | 96                    | 42                       | total           | 
| 43.5691318327974   | PRESERVED_SPECIMEN | Dominican Republic               | Polypodiopsida    | 622                   | 271                      | total           | 
| 43.2648401826484   | PRESERVED_SPECIMEN | Jamaica                          | Polypodiopsida    | 876                   | 379                      | total           | 
| 43.1011826544021   | PRESERVED_SPECIMEN | Ukraine                          | Liliopsida        | 761                   | 328                      | total           | 
| 42.9697766097241   | PRESERVED_SPECIMEN | Ukraine                          | Liliopsida        | 761                   | 327                      | open commercial | 
| 42.9697766097241   | PRESERVED_SPECIMEN | Ukraine                          | Liliopsida        | 761                   | 327                      | non-commercial  | 
| 42.8571428571429   | PRESERVED_SPECIMEN | Norway                           | Myxomycetes       | 301                   | 129                      | total           | 
| 42.7638844577515   | PRESERVED_SPECIMEN | Brazil                           | Magnoliopsida     | 40747                 | 17425                    | non-commercial  | 
| 42.7215772986917   | PRESERVED_SPECIMEN | Russia                           | Magnoliopsida     | 10854                 | 4637                     | total           | 
| 42.3580786026201   | PRESERVED_SPECIMEN | United Kingdom                   | Elasmobranchii    | 229                   | 97                       | open commercial | 
| 42.3580786026201   | PRESERVED_SPECIMEN | United Kingdom                   | Elasmobranchii    | 229                   | 97                       | non-commercial  | 
| 42.3580786026201   | PRESERVED_SPECIMEN | United Kingdom                   | Elasmobranchii    | 229                   | 97                       | total           | 
| 41.8589946253557   | PRESERVED_SPECIMEN | Brazil                           | Liliopsida        | 12652                 | 5296                     | total           | 
| 41.7910447761194   | HUMAN_OBSERVATION  | United States                    | Equisetopsida     | 67                    | 28                       | non-commercial  | 
| 41.6608513607816   | HUMAN_OBSERVATION  | Australia                        | Aves              | 1433                  | 597                      | non-commercial  | 
| 41.6558861578267   | HUMAN_OBSERVATION  | United States                    | Pinopsida         | 773                   | 322                      | non-commercial  | 
| 41.5584415584416   | PRESERVED_SPECIMEN | Estonia                          | Mammalia          | 77                    | 32                       | non-commercial  | 
| 41.5584415584416   | PRESERVED_SPECIMEN | Estonia                          | Mammalia          | 77                    | 32                       | total           | 
| 41.4187643020595   | PRESERVED_SPECIMEN | Philippines                      | Polypodiopsida    | 1311                  | 543                      | total           | 
| 41.28              | HUMAN_OBSERVATION  | Italy                            | Aves              | 625                   | 258                      | non-commercial  | 
| 41.2006578947368   | PRESERVED_SPECIMEN | United States                    | Jungermanniopsida | 1216                  | 501                      | total           | 
| 41.1290322580645   | PRESERVED_SPECIMEN | Costa Rica                       | Lycopodiopsida    | 124                   | 51                       | total           | 
| 41.1198600174978   | PRESERVED_SPECIMEN | Ukraine                          | Magnoliopsida     | 3429                  | 1410                     | total           | 
| 41.0615339749198   | PRESERVED_SPECIMEN | Ukraine                          | Magnoliopsida     | 3429                  | 1408                     | non-commercial  | 
| 40.9157188684748   | PRESERVED_SPECIMEN | Ukraine                          | Magnoliopsida     | 3429                  | 1403                     | open commercial | 
| 40.9090909090909   | PRESERVED_SPECIMEN | Papua New Guinea                 | Pinopsida         | 66                    | 27                       | total           | 
| 40.8973650267183   | PRESERVED_SPECIMEN | Russia                           | Magnoliopsida     | 10854                 | 4439                     | non-commercial  | 
| 40.8542246982358   | PRESERVED_SPECIMEN | Brazil                           | Polypodiopsida    | 2154                  | 880                      | non-commercial  | 
| 40.7608695652174   | PRESERVED_SPECIMEN | Mexico                           | Pinopsida         | 184                   | 75                       | total           | 
| 40.625             | PRESERVED_SPECIMEN | Japan                            | Amphibia          | 96                    | 39                       | non-commercial  | 
| 40.5405405405405   | PRESERVED_SPECIMEN | Canada                           | Sphagnopsida      | 111                   | 45                       | total           | 
| 40.2439024390244   | PRESERVED_SPECIMEN | Haiti                            | Reptilia          | 164                   | 66                       | non-commercial  | 
| 40.2432283029298   | PRESERVED_SPECIMEN | Russia                           | Magnoliopsida     | 10854                 | 4368                     | open commercial | 
| 40.2298850574713   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Reptilia          | 87                    | 35                       | total           | 
| 40.1578458681523   | PRESERVED_SPECIMEN | Brazil                           | Polypodiopsida    | 2154                  | 865                      | open commercial | 
| 40.1015228426396   | HUMAN_OBSERVATION  | Russia                           | Aves              | 985                   | 395                      | total           | 
| 39.9598393574297   | PRESERVED_SPECIMEN | United Kingdom                   | Florideophyceae   | 498                   | 199                      | non-commercial  | 
| 39.9598393574297   | PRESERVED_SPECIMEN | United Kingdom                   | Florideophyceae   | 498                   | 199                      | total           | 
| 39.7887323943662   | HUMAN_OBSERVATION  | Mexico                           | Reptilia          | 1136                  | 452                      | total           | 
| 39.3034825870647   | PRESERVED_SPECIMEN | Russia                           | Polypodiopsida    | 201                   | 79                       | total           | 
| 39.2452830188679   | PRESERVED_SPECIMEN | Guatemala                        | Polypodiopsida    | 795                   | 312                      | total           | 
| 39.1878172588832   | HUMAN_OBSERVATION  | Russia                           | Aves              | 985                   | 386                      | non-commercial  | 
| 39.0804597701149   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Reptilia          | 87                    | 34                       | non-commercial  | 
| 39.0625            | PRESERVED_SPECIMEN | United Kingdom                   | Holocephali       | 64                    | 25                       | open commercial | 
| 39.0625            | PRESERVED_SPECIMEN | United Kingdom                   | Holocephali       | 64                    | 25                       | non-commercial  | 
| 39.0625            | PRESERVED_SPECIMEN | United Kingdom                   | Holocephali       | 64                    | 25                       | total           | 
| 38.9830508474576   | PRESERVED_SPECIMEN | Madagascar                       | Lycopodiopsida    | 59                    | 23                       | open commercial | 
| 38.9830508474576   | PRESERVED_SPECIMEN | Madagascar                       | Lycopodiopsida    | 59                    | 23                       | non-commercial  | 
| 38.5925085130533   | HUMAN_OBSERVATION  | Norway                           | Liliopsida        | 881                   | 340                      | total           | 
| 38.5721648219501   | PRESERVED_SPECIMEN | Brazil                           | Magnoliopsida     | 40747                 | 15717                    | open commercial | 
| 38.5518590998043   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Insecta           | 2044                  | 788                      | total           | 
| 38.5416666666667   | PRESERVED_SPECIMEN | Japan                            | Amphibia          | 96                    | 37                       | open commercial | 
| 38.454011741683    | HUMAN_OBSERVATION  | Hong Kong SAR China              | Insecta           | 2044                  | 786                      | non-commercial  | 
| 38.3791024782317   | PRESERVED_SPECIMEN | Papua New Guinea                 | Polypodiopsida    | 1493                  | 573                      | total           | 
| 38.2922535211268   | HUMAN_OBSERVATION  | Mexico                           | Reptilia          | 1136                  | 435                      | non-commercial  | 
| 38.2001836547291   | PRESERVED_SPECIMEN | United Kingdom                   | Actinopterygii    | 1089                  | 416                      | total           | 
| 38.2001836547291   | PRESERVED_SPECIMEN | United Kingdom                   | Actinopterygii    | 1089                  | 416                      | open commercial | 
| 38.2001836547291   | PRESERVED_SPECIMEN | United Kingdom                   | Actinopterygii    | 1089                  | 416                      | non-commercial  | 
| 38.1016042780749   | PRESERVED_SPECIMEN | Madagascar                       | Polypodiopsida    | 748                   | 285                      | open commercial | 
| 38.1016042780749   | PRESERVED_SPECIMEN | Madagascar                       | Polypodiopsida    | 748                   | 285                      | non-commercial  | 
| 37.8058405682715   | PRESERVED_SPECIMEN | Malaysia                         | Polypodiopsida    | 1267                  | 479                      | open commercial | 
| 37.8058405682715   | PRESERVED_SPECIMEN | Malaysia                         | Polypodiopsida    | 1267                  | 479                      | non-commercial  | 
| 37.5436147941382   | PRESERVED_SPECIMEN | Costa Rica                       | Polypodiopsida    | 1433                  | 538                      | total           | 
| 37.4738311235171   | PRESERVED_SPECIMEN | Australia                        | Aves              | 1433                  | 537                      | total           | 
| 37.3786541264472   | PRESERVED_SPECIMEN | United States                    | Magnoliopsida     | 36363                 | 13592                    | non-commercial  | 
| 37.171052631579    | PRESERVED_SPECIMEN | Canada                           | Polypodiopsida    | 304                   | 113                      | total           | 
| 37.1681415929204   | PRESERVED_SPECIMEN | Spain                            | Polypodiopsida    | 339                   | 126                      | total           | 
| 36.8421052631579   | PRESERVED_SPECIMEN | Georgia                          | Polypodiopsida    | 57                    | 21                       | non-commercial  | 
| 36.8421052631579   | PRESERVED_SPECIMEN | Georgia                          | Polypodiopsida    | 57                    | 21                       | total           | 
| 36.8421052631579   | PRESERVED_SPECIMEN | Georgia                          | Polypodiopsida    | 57                    | 21                       | open commercial | 
| 36.8233387358185   | PRESERVED_SPECIMEN | Puerto Rico                      | Magnoliopsida     | 3085                  | 1136                     | total           | 
| 36.81592039801     | PRESERVED_SPECIMEN | Russia                           | Polypodiopsida    | 201                   | 74                       | open commercial | 
| 36.81592039801     | PRESERVED_SPECIMEN | Russia                           | Polypodiopsida    | 201                   | 74                       | non-commercial  | 
| 36.7647058823529   | HUMAN_OBSERVATION  | Spain                            | Amphibia          | 68                    | 25                       | total           | 
| 35.8778625954198   | PRESERVED_SPECIMEN | Malaysia                         | Lycopodiopsida    | 131                   | 47                       | total           | 
| 35.7615894039735   | PRESERVED_SPECIMEN | Colombia                         | Leotiomycetes     | 151                   | 54                       | total           | 
| 35.7615894039735   | PRESERVED_SPECIMEN | Colombia                         | Leotiomycetes     | 151                   | 54                       | non-commercial  | 
| 35.7615894039735   | PRESERVED_SPECIMEN | Colombia                         | Leotiomycetes     | 151                   | 54                       | open commercial | 
| 35.6594556873692   | PRESERVED_SPECIMEN | Australia                        | Aves              | 1433                  | 511                      | non-commercial  | 
| 35.6285310734463   | HUMAN_OBSERVATION  | United States                    | Reptilia          | 2832                  | 1009                     | total           | 
| 35.5769230769231   | PRESERVED_SPECIMEN | Cuba                             | Reptilia          | 208                   | 74                       | total           | 
| 35.3932584269663   | PRESERVED_SPECIMEN | Kenya                            | Amphibia          | 178                   | 63                       | total           | 
| 35.2941176470588   | PRESERVED_SPECIMEN | French Southern Territories      | Magnoliopsida     | 102                   | 36                       | total           | 
| 35.2407536636427   | PRESERVED_SPECIMEN | Australia                        | Aves              | 1433                  | 505                      | open commercial | 
| 35                 | PRESERVED_SPECIMEN | Bahamas                          | Phaeophyceae      | 60                    | 21                       | total           | 
| 34.7222222222222   | PRESERVED_SPECIMEN | United States                    | Anopla            | 72                    | 25                       | total           | 
| 34.7109670448406   | PRESERVED_SPECIMEN | New Caledonia                    | Magnoliopsida     | 3702                  | 1285                     | total           | 
| 34.3782654127482   | PRESERVED_SPECIMEN | Kazakhstan                       | Magnoliopsida     | 3828                  | 1316                     | total           | 
| 34.375             | PRESERVED_SPECIMEN | Taiwan                           | Amphibia          | 64                    | 22                       | total           | 
| 34.375             | PRESERVED_SPECIMEN | Taiwan                           | Amphibia          | 64                    | 22                       | non-commercial  | 
| 34.3521421107628   | PRESERVED_SPECIMEN | Kazakhstan                       | Magnoliopsida     | 3828                  | 1315                     | open commercial | 
| 34.3521421107628   | PRESERVED_SPECIMEN | Kazakhstan                       | Magnoliopsida     | 3828                  | 1315                     | non-commercial  | 
| 34.2857142857143   | PRESERVED_SPECIMEN | United States                    | Marchantiopsida   | 140                   | 48                       | non-commercial  | 
| 34.1935483870968   | HUMAN_OBSERVATION  | Italy                            | Reptilia          | 155                   | 53                       | total           | 
| 33.7522441651706   | PRESERVED_SPECIMEN | Mongolia                         | Liliopsida        | 557                   | 188                      | total           | 
| 33.7209302325581   | PRESERVED_SPECIMEN | United Kingdom                   | Echinoidea        | 172                   | 58                       | total           | 
| 33.7209302325581   | PRESERVED_SPECIMEN | United Kingdom                   | Echinoidea        | 172                   | 58                       | open commercial | 
| 33.7209302325581   | PRESERVED_SPECIMEN | United Kingdom                   | Echinoidea        | 172                   | 58                       | non-commercial  | 
| 33.7078651685393   | PRESERVED_SPECIMEN | Kenya                            | Amphibia          | 178                   | 60                       | non-commercial  | 
| 33.6633663366337   | HUMAN_OBSERVATION  | South Africa                     | Amphibia          | 202                   | 68                       | total           | 
| 33.5714285714286   | PRESERVED_SPECIMEN | Brazil                           | Lycopodiopsida    | 280                   | 94                       | non-commercial  | 
| 33.3773341033468   | HUMAN_OBSERVATION  | United States                    | Magnoliopsida     | 36363                 | 12137                    | total           | 
| 33.3333333333333   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Arachnida         | 156                   | 52                       | non-commercial  | 
| 33.3333333333333   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Arachnida         | 156                   | 52                       | total           | 
| 33.1683168316832   | HUMAN_OBSERVATION  | South Africa                     | Amphibia          | 202                   | 67                       | non-commercial  | 
| 32.8571428571429   | PRESERVED_SPECIMEN | United States                    | Marchantiopsida   | 140                   | 46                       | open commercial | 
| 32.8571428571429   | PRESERVED_SPECIMEN | Brazil                           | Lycopodiopsida    | 280                   | 92                       | open commercial | 
| 32.8571428571429   | PRESERVED_SPECIMEN | United States                    | Psilotopsida      | 70                    | 23                       | non-commercial  | 
| 32.8125            | PRESERVED_SPECIMEN | Taiwan                           | Amphibia          | 64                    | 21                       | open commercial | 
| 32.6750448833034   | PRESERVED_SPECIMEN | Mongolia                         | Liliopsida        | 557                   | 182                      | open commercial | 
| 32.6750448833034   | PRESERVED_SPECIMEN | Mongolia                         | Liliopsida        | 557                   | 182                      | non-commercial  | 
| 32.5842696629214   | PRESERVED_SPECIMEN | Kenya                            | Amphibia          | 178                   | 58                       | open commercial | 
| 32.2869955156951   | PRESERVED_SPECIMEN | Brazil                           | Ulvophyceae       | 223                   | 72                       | total           | 
| 32.2839919624916   | PRESERVED_SPECIMEN | Papua New Guinea                 | Polypodiopsida    | 1493                  | 482                      | non-commercial  | 
| 32.2387005649718   | HUMAN_OBSERVATION  | United States                    | Reptilia          | 2832                  | 913                      | non-commercial  | 
| 32.2115384615385   | PRESERVED_SPECIMEN | Cuba                             | Reptilia          | 208                   | 67                       | non-commercial  | 
| 32.0158102766798   | PRESERVED_SPECIMEN | United Kingdom                   | Reptilia          | 506                   | 162                      | open commercial | 
| 32.0158102766798   | PRESERVED_SPECIMEN | United Kingdom                   | Reptilia          | 506                   | 162                      | total           | 
| 32.0158102766798   | PRESERVED_SPECIMEN | United Kingdom                   | Reptilia          | 506                   | 162                      | non-commercial  | 
| 31.8965517241379   | PRESERVED_SPECIMEN | China                            | Pinopsida         | 232                   | 74                       | non-commercial  | 
| 31.8206374932469   | PRESERVED_SPECIMEN | New Caledonia                    | Magnoliopsida     | 3702                  | 1178                     | non-commercial  | 
| 31.7848410757946   | PRESERVED_SPECIMEN | Kazakhstan                       | Liliopsida        | 818                   | 260                      | total           | 
| 31.7073170731707   | PRESERVED_SPECIMEN | Guam                             | Polypodiopsida    | 82                    | 26                       | total           | 
| 31.6855753646677   | PRESERVED_SPECIMEN | New Caledonia                    | Magnoliopsida     | 3702                  | 1173                     | open commercial | 
| 31.6811788345613   | PRESERVED_SPECIMEN | Papua New Guinea                 | Polypodiopsida    | 1493                  | 473                      | open commercial | 
| 31.6420537359404   | HUMAN_OBSERVATION  | United States                    | Magnoliopsida     | 36363                 | 11506                    | non-commercial  | 
| 31.5789473684211   | PRESERVED_SPECIMEN | Brazil                           | Sphagnopsida      | 133                   | 42                       | total           | 
| 31.547619047619    | PRESERVED_SPECIMEN | Liberia                          | Polypodiopsida    | 168                   | 53                       | total           | 
| 31.4415437003405   | PRESERVED_SPECIMEN | Norway                           | Liliopsida        | 881                   | 277                      | non-commercial  | 
| 31.4285714285714   | HUMAN_OBSERVATION  | United States                    | Psilotopsida      | 70                    | 22                       | non-commercial  | 
| 31.4285714285714   | HUMAN_OBSERVATION  | United States                    | Psilotopsida      | 70                    | 22                       | total           | 
| 31.3253012048193   | PRESERVED_SPECIMEN | Australia                        | Charophyceae      | 83                    | 26                       | total           | 
| 31.3253012048193   | PRESERVED_SPECIMEN | Australia                        | Charophyceae      | 83                    | 26                       | non-commercial  | 
| 31.3253012048193   | PRESERVED_SPECIMEN | Australia                        | Charophyceae      | 83                    | 26                       | open commercial | 
| 31.3253012048193   | PRESERVED_SPECIMEN | Puerto Rico                      | Phaeophyceae      | 83                    | 26                       | non-commercial  | 
| 31.3253012048193   | PRESERVED_SPECIMEN | Puerto Rico                      | Phaeophyceae      | 83                    | 26                       | open commercial | 
| 31.3253012048193   | PRESERVED_SPECIMEN | Puerto Rico                      | Phaeophyceae      | 83                    | 26                       | total           | 
| 30.9290953545232   | PRESERVED_SPECIMEN | Kazakhstan                       | Liliopsida        | 818                   | 253                      | non-commercial  | 
| 30.9290953545232   | PRESERVED_SPECIMEN | Kazakhstan                       | Liliopsida        | 818                   | 253                      | open commercial | 
| 30.8403361344538   | PRESERVED_SPECIMEN | Mongolia                         | Magnoliopsida     | 2380                  | 734                      | total           | 
| 30.7983193277311   | PRESERVED_SPECIMEN | Mongolia                         | Magnoliopsida     | 2380                  | 733                      | non-commercial  | 
| 30.7983193277311   | PRESERVED_SPECIMEN | Mongolia                         | Magnoliopsida     | 2380                  | 733                      | open commercial | 
| 30.6748466257669   | PRESERVED_SPECIMEN | Mexico                           | Lycopodiopsida    | 163                   | 50                       | total           | 
| 30.6569343065693   | PRESERVED_SPECIMEN | Venezuela                        | Leotiomycetes     | 137                   | 42                       | total           | 
| 30.6569343065693   | PRESERVED_SPECIMEN | Venezuela                        | Leotiomycetes     | 137                   | 42                       | non-commercial  | 
| 30.6569343065693   | PRESERVED_SPECIMEN | Venezuela                        | Leotiomycetes     | 137                   | 42                       | open commercial | 
| 30.6312769010043   | PRESERVED_SPECIMEN | Mexico                           | Polypodiopsida    | 1394                  | 427                      | total           | 
| 30.5343511450382   | PRESERVED_SPECIMEN | Malaysia                         | Lycopodiopsida    | 131                   | 40                       | non-commercial  | 
| 30.5343511450382   | PRESERVED_SPECIMEN | Malaysia                         | Lycopodiopsida    | 131                   | 40                       | open commercial | 
| 30.3030303030303   | PRESERVED_SPECIMEN | Saudi Arabia                     | Reptilia          | 132                   | 40                       | non-commercial  | 
| 30.3030303030303   | PRESERVED_SPECIMEN | Saudi Arabia                     | Reptilia          | 132                   | 40                       | total           | 
| 30.1261829652997   | HUMAN_OBSERVATION  | South Africa                     | Mammalia          | 634                   | 191                      | total           | 
| 30                 | PRESERVED_SPECIMEN | United Kingdom                   | Branchiopoda      | 120                   | 36                       | total           | 
| 30                 | PRESERVED_SPECIMEN | United Kingdom                   | Branchiopoda      | 120                   | 36                       | non-commercial  | 
| 30                 | PRESERVED_SPECIMEN | United Kingdom                   | Branchiopoda      | 120                   | 36                       | open commercial | 
| 29.7729618163055   | HUMAN_OBSERVATION  | Norway                           | Magnoliopsida     | 3876                  | 1154                     | total           | 
| 29.6296296296296   | PRESERVED_SPECIMEN | United States                    | Sphagnopsida      | 135                   | 40                       | non-commercial  | 
| 29.5238095238095   | PRESERVED_SPECIMEN | Estonia                          | Pinopsida         | 105                   | 31                       | total           | 
| 29.5238095238095   | PRESERVED_SPECIMEN | Estonia                          | Pinopsida         | 105                   | 31                       | non-commercial  | 
| 29.4975688816856   | PRESERVED_SPECIMEN | Puerto Rico                      | Magnoliopsida     | 3085                  | 910                      | non-commercial  | 
| 29.4871794871795   | PRESERVED_SPECIMEN | French Southern Territories      | Liliopsida        | 78                    | 23                       | total           | 
| 29.3375394321767   | HUMAN_OBSERVATION  | South Africa                     | Mammalia          | 634                   | 186                      | non-commercial  | 
| 29.3333333333333   | PRESERVED_SPECIMEN | Uganda                           | Actinopterygii    | 300                   | 88                       | non-commercial  | 
| 29.3333333333333   | PRESERVED_SPECIMEN | Uganda                           | Actinopterygii    | 300                   | 88                       | total           | 
| 29.3274531422271   | HUMAN_OBSERVATION  | Spain                            | Aves              | 907                   | 266                      | total           | 
| 29.2763157894737   | PRESERVED_SPECIMEN | Chile                            | Polypodiopsida    | 304                   | 89                       | total           | 
| 29.2382495948136   | PRESERVED_SPECIMEN | Puerto Rico                      | Magnoliopsida     | 3085                  | 902                      | open commercial | 
| 29.1497975708502   | PRESERVED_SPECIMEN | Canada                           | Jungermanniopsida | 494                   | 144                      | total           | 
| 29.1438581125465   | PRESERVED_SPECIMEN | Canada                           | Magnoliopsida     | 9134                  | 2662                     | total           | 
| 29.0537084398977   | HUMAN_OBSERVATION  | Norway                           | Agaricomycetes    | 3910                  | 1136                     | total           | 
| 28.9780077619664   | PRESERVED_SPECIMEN | United States                    | Pinopsida         | 773                   | 224                      | non-commercial  | 
| 28.9390628793396   | PRESERVED_SPECIMEN | Dominican Republic               | Magnoliopsida     | 4119                  | 1192                     | total           | 
| 28.9294665234515   | PRESERVED_SPECIMEN | Canada                           | Liliopsida        | 2793                  | 808                      | non-commercial  | 
| 28.8973384030418   | PRESERVED_SPECIMEN | United Kingdom                   | Hydrozoa          | 263                   | 76                       | open commercial | 
| 28.8973384030418   | PRESERVED_SPECIMEN | United Kingdom                   | Hydrozoa          | 263                   | 76                       | non-commercial  | 
| 28.8973384030418   | PRESERVED_SPECIMEN | United Kingdom                   | Hydrozoa          | 263                   | 76                       | total           | 
| 28.7162162162162   | PRESERVED_SPECIMEN | Puerto Rico                      | Florideophyceae   | 296                   | 85                       | non-commercial  | 
| 28.7162162162162   | PRESERVED_SPECIMEN | Puerto Rico                      | Florideophyceae   | 296                   | 85                       | open commercial | 
| 28.7162162162162   | PRESERVED_SPECIMEN | Puerto Rico                      | Florideophyceae   | 296                   | 85                       | total           | 
| 28.6496350364964   | HUMAN_OBSERVATION  | South Korea                      | Aves              | 548                   | 157                      | open commercial | 
| 28.4347826086957   | PRESERVED_SPECIMEN | United States                    | Aves              | 3450                  | 981                      | total           | 
| 28.4132841328413   | PRESERVED_SPECIMEN | Greenland                        | Liliopsida        | 271                   | 77                       | total           | 
| 28.3870967741935   | HUMAN_OBSERVATION  | Italy                            | Reptilia          | 155                   | 44                       | non-commercial  | 
| 28.3731688511951   | PRESERVED_SPECIMEN | Bahamas                          | Magnoliopsida     | 1297                  | 368                      | total           | 
| 28.3176746917205   | HUMAN_OBSERVATION  | New Zealand                      | Magnoliopsida     | 6812                  | 1929                     | total           | 
| 28.2883147386964   | HUMAN_OBSERVATION  | New Zealand                      | Magnoliopsida     | 6812                  | 1927                     | non-commercial  | 
| 28                 | PRESERVED_SPECIMEN | Uganda                           | Actinopterygii    | 300                   | 84                       | open commercial | 
| 28                 | HUMAN_OBSERVATION  | New Zealand                      | Polypodiopsida    | 450                   | 126                      | open commercial | 
| 27.9906176700547   | HUMAN_OBSERVATION  | United Kingdom                   | Aves              | 1279                  | 358                      | total           | 
| 27.9503105590062   | PRESERVED_SPECIMEN | Puerto Rico                      | Ulvophyceae       | 161                   | 45                       | open commercial | 
| 27.9503105590062   | PRESERVED_SPECIMEN | Puerto Rico                      | Ulvophyceae       | 161                   | 45                       | non-commercial  | 
| 27.9503105590062   | PRESERVED_SPECIMEN | Puerto Rico                      | Ulvophyceae       | 161                   | 45                       | total           | 
| 27.906976744186    | PRESERVED_SPECIMEN | United States                    | Ustilaginomycetes | 215                   | 60                       | non-commercial  | 
| 27.906976744186    | PRESERVED_SPECIMEN | United States                    | Ustilaginomycetes | 215                   | 60                       | total           | 
| 27.906976744186    | PRESERVED_SPECIMEN | United States                    | Ustilaginomycetes | 215                   | 60                       | open commercial | 
| 27.906976744186    | PRESERVED_SPECIMEN | Mayotte                          | Polypodiopsida    | 86                    | 24                       | total           | 
| 27.8947368421053   | PRESERVED_SPECIMEN | Jamaica                          | Demospongiae      | 190                   | 53                       | open commercial | 
| 27.8947368421053   | PRESERVED_SPECIMEN | Jamaica                          | Demospongiae      | 190                   | 53                       | non-commercial  | 
| 27.8947368421053   | PRESERVED_SPECIMEN | Jamaica                          | Demospongiae      | 190                   | 53                       | total           | 
| 27.7777777777778   | PRESERVED_SPECIMEN | Afghanistan                      | Reptilia          | 108                   | 30                       | non-commercial  | 
| 27.7777777777778   | PRESERVED_SPECIMEN | Afghanistan                      | Reptilia          | 108                   | 30                       | total           | 
| 27.7777777777778   | PRESERVED_SPECIMEN | Afghanistan                      | Reptilia          | 108                   | 30                       | open commercial | 
| 27.7173913043478   | HUMAN_OBSERVATION  | Mexico                           | Pinopsida         | 184                   | 51                       | non-commercial  | 
| 27.7173913043478   | HUMAN_OBSERVATION  | Mexico                           | Pinopsida         | 184                   | 51                       | total           | 
| 27.5418776782236   | PRESERVED_SPECIMEN | Spain                            | Liliopsida        | 2567                  | 707                      | total           | 
| 27.2887323943662   | PRESERVED_SPECIMEN | Mexico                           | Reptilia          | 1136                  | 310                      | total           | 
| 27.2727272727273   | PRESERVED_SPECIMEN | Saudi Arabia                     | Reptilia          | 132                   | 36                       | open commercial | 
| 27.2727272727273   | PRESERVED_SPECIMEN | France                           | Phaeophyceae      | 264                   | 72                       | total           | 
| 27.2381985892566   | PRESERVED_SPECIMEN | Canada                           | Bryopsida         | 1843                  | 502                      | total           | 
| 27.2206303724928   | HUMAN_OBSERVATION  | Madagascar                       | Aves              | 349                   | 95                       | non-commercial  | 
| 27.2206303724928   | HUMAN_OBSERVATION  | Madagascar                       | Aves              | 349                   | 95                       | total           | 
| 27.1084337349398   | PRESERVED_SPECIMEN | United States                    | Phaeophyceae      | 498                   | 135                      | total           | 
| 26.9076305220884   | PRESERVED_SPECIMEN | United States                    | Phaeophyceae      | 498                   | 134                      | open commercial | 
| 26.9076305220884   | PRESERVED_SPECIMEN | United States                    | Phaeophyceae      | 498                   | 134                      | non-commercial  | 
| 26.7441860465116   | PRESERVED_SPECIMEN | Mayotte                          | Polypodiopsida    | 86                    | 23                       | non-commercial  | 
| 26.7441860465116   | PRESERVED_SPECIMEN | Mayotte                          | Polypodiopsida    | 86                    | 23                       | open commercial | 
| 26.6895761741123   | PRESERVED_SPECIMEN | Mayotte                          | Magnoliopsida     | 873                   | 233                      | total           | 
| 26.4705882352941   | PRESERVED_SPECIMEN | Puerto Rico                      | Liliopsida        | 1088                  | 288                      | total           | 
| 26.4604810996564   | PRESERVED_SPECIMEN | Mayotte                          | Magnoliopsida     | 873                   | 231                      | non-commercial  | 
| 26.4604810996564   | PRESERVED_SPECIMEN | Mayotte                          | Magnoliopsida     | 873                   | 231                      | open commercial | 
| 26.4456437933693   | PRESERVED_SPECIMEN | Bahamas                          | Magnoliopsida     | 1297                  | 343                      | non-commercial  | 
| 26.4367816091954   | PRESERVED_SPECIMEN | Jamaica                          | Reptilia          | 87                    | 23                       | non-commercial  | 
| 26.4367816091954   | PRESERVED_SPECIMEN | Jamaica                          | Reptilia          | 87                    | 23                       | total           | 
| 26.2899262899263   | PRESERVED_SPECIMEN | Fiji                             | Polypodiopsida    | 407                   | 107                      | total           | 
| 26.1744966442953   | HUMAN_OBSERVATION  | New Zealand                      | Phaeophyceae      | 149                   | 39                       | total           | 
| 26.1744966442953   | HUMAN_OBSERVATION  | New Zealand                      | Phaeophyceae      | 149                   | 39                       | non-commercial  | 
| 25.8219860511458   | HUMAN_OBSERVATION  | South Africa                     | Liliopsida        | 6022                  | 1555                     | total           | 
| 25.7894736842105   | PRESERVED_SPECIMEN | Australia                        | Demospongiae      | 1140                  | 294                      | total           | 
| 25.7861635220126   | HUMAN_OBSERVATION  | Australia                        | Amphibia          | 318                   | 82                       | total           | 
| 25.6844850065189   | PRESERVED_SPECIMEN | United States                    | Amphibia          | 767                   | 197                      | total           | 
| 25.6578947368421   | HUMAN_OBSERVATION  | Canada                           | Polypodiopsida    | 304                   | 78                       | total           | 
| 25.4932912391476   | HUMAN_OBSERVATION  | Australia                        | Reptilia          | 1267                  | 323                      | total           | 
| 25.4901960784314   | PRESERVED_SPECIMEN | French Southern Territories      | Magnoliopsida     | 102                   | 26                       | open commercial | 
| 25.4901960784314   | PRESERVED_SPECIMEN | French Southern Territories      | Magnoliopsida     | 102                   | 26                       | non-commercial  | 
| 25.3947368421053   | HUMAN_OBSERVATION  | Australia                        | Mammalia          | 760                   | 193                      | total           | 
| 25.354609929078    | PRESERVED_SPECIMEN | Indonesia                        | Polypodiopsida    | 2256                  | 572                      | total           | 
| 25.0863060989643   | PRESERVED_SPECIMEN | New Caledonia                    | Liliopsida        | 869                   | 218                      | total           | 
| 25.03259452412     | PRESERVED_SPECIMEN | United States                    | Amphibia          | 767                   | 192                      | non-commercial  | 
| 25.0268528464017   | HUMAN_OBSERVATION  | New Zealand                      | Liliopsida        | 1862                  | 466                      | total           | 
| 24.9762883338603   | PRESERVED_SPECIMEN | Brazil                           | Liliopsida        | 12652                 | 3160                     | non-commercial  | 
| 24.9731471535983   | HUMAN_OBSERVATION  | New Zealand                      | Liliopsida        | 1862                  | 465                      | non-commercial  | 
| 24.9119718309859   | PRESERVED_SPECIMEN | Mexico                           | Reptilia          | 1136                  | 283                      | non-commercial  | 
| 24.8381877022654   | HUMAN_OBSERVATION  | Costa Rica                       | Aves              | 1236                  | 307                      | total           | 
| 24.8366013071895   | PRESERVED_SPECIMEN | Bahamas                          | Ulvophyceae       | 153                   | 38                       | total           | 
| 24.8265227447957   | PRESERVED_SPECIMEN | Bahamas                          | Magnoliopsida     | 1297                  | 322                      | open commercial | 
| 24.6902826171119   | PRESERVED_SPECIMEN | Madagascar                       | Magnoliopsida     | 10332                 | 2551                     | total           | 
| 24.6783756572324   | PRESERVED_SPECIMEN | United States                    | Agaricomycetes    | 8939                  | 2206                     | total           | 
| 24.6736292428198   | HUMAN_OBSERVATION  | South Africa                     | Reptilia          | 766                   | 189                      | total           | 
| 24.6710526315789   | HUMAN_OBSERVATION  | Canada                           | Polypodiopsida    | 304                   | 75                       | non-commercial  | 
| 24.5430809399478   | HUMAN_OBSERVATION  | South Africa                     | Reptilia          | 766                   | 188                      | non-commercial  | 
| 24.5145631067961   | HUMAN_OBSERVATION  | Costa Rica                       | Aves              | 1236                  | 303                      | non-commercial  | 
| 24.5059288537549   | PRESERVED_SPECIMEN | Canada                           | Pinopsida         | 253                   | 62                       | total           | 
| 24.4565217391304   | PRESERVED_SPECIMEN | Mexico                           | Pinopsida         | 184                   | 45                       | non-commercial  | 
| 24.3243243243243   | HUMAN_OBSERVATION  | South Africa                     | Agaricomycetes    | 407                   | 99                       | total           | 
| 24.3243243243243   | HUMAN_OBSERVATION  | South Africa                     | Agaricomycetes    | 407                   | 99                       | non-commercial  | 
| 24.0673411318369   | PRESERVED_SPECIMEN | Brazil                           | Liliopsida        | 12652                 | 3045                     | open commercial | 
| 24.0584166026134   | PRESERVED_SPECIMEN | Brazil                           | Jungermanniopsida | 1301                  | 313                      | total           | 
| 23.7505249895002   | PRESERVED_SPECIMEN | United States                    | Liliopsida        | 9524                  | 2262                     | open commercial | 
| 23.7037037037037   | PRESERVED_SPECIMEN | United States                    | Sphagnopsida      | 135                   | 32                       | open commercial | 
| 23.6842105263158   | PRESERVED_SPECIMEN | United Kingdom                   | Mammalia          | 532                   | 126                      | open commercial | 
| 23.6842105263158   | PRESERVED_SPECIMEN | United Kingdom                   | Mammalia          | 532                   | 126                      | non-commercial  | 
| 23.6842105263158   | PRESERVED_SPECIMEN | United Kingdom                   | Mammalia          | 532                   | 126                      | total           | 
| 23.6677115987461   | PRESERVED_SPECIMEN | South Africa                     | Aves              | 1276                  | 302                      | total           | 
| 23.6455270894582   | HUMAN_OBSERVATION  | United States                    | Liliopsida        | 9524                  | 2252                     | total           | 
| 23.590333716916    | PRESERVED_SPECIMEN | New Caledonia                    | Liliopsida        | 869                   | 205                      | non-commercial  | 
| 23.590333716916    | PRESERVED_SPECIMEN | New Caledonia                    | Liliopsida        | 869                   | 205                      | open commercial | 
| 23.5772357723577   | PRESERVED_SPECIMEN | Colombia                         | Lycopodiopsida    | 246                   | 58                       | total           | 
| 23.5342353423534   | PRESERVED_SPECIMEN | Brazil                           | Bryopsida         | 2439                  | 574                      | total           | 
| 23.4848484848485   | PRESERVED_SPECIMEN | United Kingdom                   | Crinoidea         | 132                   | 31                       | non-commercial  | 
| 23.4848484848485   | PRESERVED_SPECIMEN | United Kingdom                   | Crinoidea         | 132                   | 31                       | total           | 
| 23.4848484848485   | PRESERVED_SPECIMEN | United Kingdom                   | Crinoidea         | 132                   | 31                       | open commercial | 
| 23.4726688102894   | PRESERVED_SPECIMEN | Dominican Republic               | Polypodiopsida    | 622                   | 146                      | non-commercial  | 
| 23.4726688102894   | PRESERVED_SPECIMEN | Dominican Republic               | Polypodiopsida    | 622                   | 146                      | open commercial | 
| 23.4680573663625   | PRESERVED_SPECIMEN | United States                    | Amphibia          | 767                   | 180                      | open commercial | 
| 23.4597156398104   | PRESERVED_SPECIMEN | United States                    | Arthoniomycetes   | 422                   | 99                       | total           | 
| 23.4522942461763   | PRESERVED_SPECIMEN | Dominican Republic               | Magnoliopsida     | 4119                  | 966                      | non-commercial  | 
| 23.4042553191489   | PRESERVED_SPECIMEN | Dominica                         | Polypodiopsida    | 235                   | 55                       | total           | 
| 23.3333333333333   | PRESERVED_SPECIMEN | Brazil                           | Florideophyceae   | 600                   | 140                      | total           | 
| 23.2635585156993   | PRESERVED_SPECIMEN | Cuba                             | Magnoliopsida     | 6306                  | 1467                     | total           | 
| 23.1548480463097   | PRESERVED_SPECIMEN | France                           | Florideophyceae   | 691                   | 160                      | total           | 
| 22.9910172371935   | PRESERVED_SPECIMEN | Dominican Republic               | Magnoliopsida     | 4119                  | 947                      | open commercial | 
| 22.9623824451411   | PRESERVED_SPECIMEN | South Africa                     | Aves              | 1276                  | 293                      | open commercial | 
| 22.9623824451411   | PRESERVED_SPECIMEN | South Africa                     | Aves              | 1276                  | 293                      | non-commercial  | 
| 22.8125            | HUMAN_OBSERVATION  | New Zealand                      | Arachnida         | 640                   | 146                      | total           | 
| 22.7848101265823   | PRESERVED_SPECIMEN | Japan                            | Pinopsida         | 158                   | 36                       | total           | 
| 22.766217870257    | PRESERVED_SPECIMEN | Peru                             | Polypodiopsida    | 1634                  | 372                      | total           | 
| 22.7513227513227   | PRESERVED_SPECIMEN | Spain                            | Pinopsida         | 189                   | 43                       | total           | 
| 22.7272727272727   | HUMAN_OBSERVATION  | Singapore                        | Aves              | 528                   | 120                      | total           | 
| 22.680412371134    | HUMAN_OBSERVATION  | New Zealand                      | Maxillopoda       | 97                    | 22                       | non-commercial  | 
| 22.680412371134    | HUMAN_OBSERVATION  | New Zealand                      | Maxillopoda       | 97                    | 22                       | total           | 
| 22.585048299034    | HUMAN_OBSERVATION  | United States                    | Liliopsida        | 9524                  | 2151                     | non-commercial  | 
| 22.4137931034483   | PRESERVED_SPECIMEN | United Kingdom                   | Ostracoda         | 986                   | 221                      | total           | 
| 22.4137931034483   | PRESERVED_SPECIMEN | United Kingdom                   | Ostracoda         | 986                   | 221                      | non-commercial  | 
| 22.4137931034483   | PRESERVED_SPECIMEN | United Kingdom                   | Ostracoda         | 986                   | 221                      | open commercial | 
| 22.3484848484848   | HUMAN_OBSERVATION  | Singapore                        | Aves              | 528                   | 118                      | non-commercial  | 
| 22.2222222222222   | PRESERVED_SPECIMEN | New Zealand                      | Polypodiopsida    | 450                   | 100                      | total           | 
| 22.2222222222222   | PRESERVED_SPECIMEN | Puerto Rico                      | Polypodiopsida    | 495                   | 110                      | non-commercial  | 
| 22.2185320491531   | HUMAN_OBSERVATION  | South Africa                     | Liliopsida        | 6022                  | 1338                     | non-commercial  | 
| 22.2104144527099   | HUMAN_OBSERVATION  | Japan                            | Aves              | 941                   | 209                      | total           | 
| 22.1841834988018   | PRESERVED_SPECIMEN | Madagascar                       | Liliopsida        | 2921                  | 648                      | total           | 
| 22.1830985915493   | PRESERVED_SPECIMEN | Mexico                           | Reptilia          | 1136                  | 252                      | open commercial | 
| 22.1742298084929   | HUMAN_OBSERVATION  | South Africa                     | Magnoliopsida     | 19216                 | 4261                     | total           | 
| 22.1649484536082   | HUMAN_OBSERVATION  | Martinique                       | Aves              | 194                   | 43                       | total           | 
| 22.1649484536082   | HUMAN_OBSERVATION  | Martinique                       | Aves              | 194                   | 43                       | non-commercial  | 
| 22.03125           | HUMAN_OBSERVATION  | New Zealand                      | Arachnida         | 640                   | 141                      | non-commercial  | 
| 22.020202020202    | PRESERVED_SPECIMEN | Puerto Rico                      | Polypodiopsida    | 495                   | 109                      | open commercial | 
| 21.9178835629624   | PRESERVED_SPECIMEN | United States                    | Magnoliopsida     | 36363                 | 7970                     | open commercial | 
| 21.8045112781955   | PRESERVED_SPECIMEN | United States                    | Exobasidiomycetes | 133                   | 29                       | open commercial | 
| 21.8045112781955   | PRESERVED_SPECIMEN | United States                    | Exobasidiomycetes | 133                   | 29                       | total           | 
| 21.8045112781955   | PRESERVED_SPECIMEN | United States                    | Exobasidiomycetes | 133                   | 29                       | non-commercial  | 
| 21.7006661115737   | HUMAN_OBSERVATION  | South Africa                     | Magnoliopsida     | 19216                 | 4170                     | non-commercial  | 
| 21.634121274409    | PRESERVED_SPECIMEN | Colombia                         | Polypodiopsida    | 1946                  | 421                      | total           | 
| 21.6326530612245   | PRESERVED_SPECIMEN | Equatorial Guinea                | Polypodiopsida    | 245                   | 53                       | total           | 
| 21.5909090909091   | PRESERVED_SPECIMEN | France                           | Phaeophyceae      | 264                   | 57                       | open commercial | 
| 21.5909090909091   | PRESERVED_SPECIMEN | France                           | Phaeophyceae      | 264                   | 57                       | non-commercial  | 
| 21.5384615384615   | PRESERVED_SPECIMEN | United States                    | Lycopodiopsida    | 325                   | 70                       | non-commercial  | 
| 21.4467005076142   | PRESERVED_SPECIMEN | France                           | Liliopsida        | 3152                  | 676                      | total           | 
| 21.4322250639386   | PRESERVED_SPECIMEN | Norway                           | Agaricomycetes    | 3910                  | 838                      | total           | 
| 21.3367609254499   | PRESERVED_SPECIMEN | French Polynesia                 | Polypodiopsida    | 389                   | 83                       | total           | 
| 21.3235294117647   | PRESERVED_SPECIMEN | Puerto Rico                      | Liliopsida        | 1088                  | 232                      | non-commercial  | 
| 21.2355212355212   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Aves              | 518                   | 110                      | total           | 
| 21.1204481792717   | PRESERVED_SPECIMEN | Cuba                             | Liliopsida        | 1785                  | 377                      | total           | 
| 21.0710128055879   | PRESERVED_SPECIMEN | United States                    | Florideophyceae   | 1718                  | 362                      | total           | 
| 21.0666666666667   | HUMAN_OBSERVATION  | Denmark                          | Pezizomycetes     | 375                   | 79                       | total           | 
| 21.048321048321    | PRESERVED_SPECIMEN | Dominican Republic               | Liliopsida        | 1221                  | 257                      | total           | 
| 21.0477941176471   | PRESERVED_SPECIMEN | Puerto Rico                      | Liliopsida        | 1088                  | 229                      | open commercial | 
| 21.042471042471    | HUMAN_OBSERVATION  | Hong Kong SAR China              | Aves              | 518                   | 109                      | non-commercial  | 
| 20.9643136816199   | HUMAN_OBSERVATION  | United States                    | Agaricomycetes    | 8939                  | 1874                     | total           | 
| 20.9486166007905   | HUMAN_OBSERVATION  | Canada                           | Pinopsida         | 253                   | 53                       | total           | 
| 20.9109730848861   | PRESERVED_SPECIMEN | United States                    | Ulvophyceae       | 483                   | 101                      | open commercial | 
| 20.9109730848861   | PRESERVED_SPECIMEN | United States                    | Ulvophyceae       | 483                   | 101                      | non-commercial  | 
| 20.9109730848861   | PRESERVED_SPECIMEN | United States                    | Ulvophyceae       | 483                   | 101                      | total           | 
| 20.8978328173375   | PRESERVED_SPECIMEN | Norway                           | Magnoliopsida     | 3876                  | 810                      | total           | 
| 20.8115942028986   | HUMAN_OBSERVATION  | United States                    | Aves              | 3450                  | 718                      | open commercial | 
| 20.7920792079208   | PRESERVED_SPECIMEN | Bahamas                          | Florideophyceae   | 202                   | 42                       | total           | 
| 20.7270408163265   | PRESERVED_SPECIMEN | United States                    | Polypodiopsida    | 1568                  | 325                      | non-commercial  | 
| 20.7198443579767   | HUMAN_OBSERVATION  | France                           | Aves              | 1028                  | 213                      | total           | 
| 20.7194244604317   | PRESERVED_SPECIMEN | United States                    | Lecanoromycetes   | 4865                  | 1008                     | non-commercial  | 
| 20.6063318044524   | HUMAN_OBSERVATION  | United States                    | Agaricomycetes    | 8939                  | 1842                     | non-commercial  | 
| 20.5533596837945   | HUMAN_OBSERVATION  | Canada                           | Pinopsida         | 253                   | 52                       | non-commercial  | 
| 20.5252918287938   | HUMAN_OBSERVATION  | France                           | Aves              | 1028                  | 211                      | non-commercial  | 
| 20.4255319148936   | PRESERVED_SPECIMEN | Portugal                         | Polypodiopsida    | 235                   | 48                       | total           | 
| 20.3980099502488   | PRESERVED_SPECIMEN | Ecuador                          | Lycopodiopsida    | 201                   | 41                       | total           | 
| 20.2626641651032   | HUMAN_OBSERVATION  | Mexico                           | Amphibia          | 533                   | 108                      | total           | 
| 20.2614379084967   | PRESERVED_SPECIMEN | Bahamas                          | Ulvophyceae       | 153                   | 31                       | open commercial | 
| 20.2614379084967   | PRESERVED_SPECIMEN | Bahamas                          | Ulvophyceae       | 153                   | 31                       | non-commercial  | 
| 20.2586206896552   | HUMAN_OBSERVATION  | Benin                            | Mammalia          | 232                   | 47                       | total           | 
| 20.2586206896552   | HUMAN_OBSERVATION  | Benin                            | Mammalia          | 232                   | 47                       | non-commercial  | 
| 20.2337472607743   | HUMAN_OBSERVATION  | Argentina                        | Aves              | 1369                  | 277                      | total           | 
| 20.2054794520548   | HUMAN_OBSERVATION  | New Zealand                      | Pinopsida         | 292                   | 59                       | total           | 
| 20.0832365466512   | PRESERVED_SPECIMEN | Madagascar                       | Magnoliopsida     | 10332                 | 2075                     | non-commercial  | 
| 20                 | PRESERVED_SPECIMEN | Bermuda                          | Florideophyceae   | 275                   | 55                       | total           | 
| 20                 | PRESERVED_SPECIMEN | Bermuda                          | Florideophyceae   | 275                   | 55                       | non-commercial  | 
| 20                 | PRESERVED_SPECIMEN | Bermuda                          | Florideophyceae   | 275                   | 55                       | open commercial | 
| 20                 | HUMAN_OBSERVATION  | Costa Rica                       | Reptilia          | 350                   | 70                       | non-commercial  | 
| 20                 | HUMAN_OBSERVATION  | Costa Rica                       | Reptilia          | 350                   | 70                       | total           | 
| 19.8979591836735   | HUMAN_OBSERVATION  | United States                    | Polypodiopsida    | 1568                  | 312                      | total           | 
| 19.8630136986301   | HUMAN_OBSERVATION  | New Zealand                      | Pinopsida         | 292                   | 58                       | non-commercial  | 
| 19.8489161375082   | HUMAN_OBSERVATION  | Canada                           | Magnoliopsida     | 9134                  | 1813                     | total           | 
| 19.7954711468225   | HUMAN_OBSERVATION  | Argentina                        | Aves              | 1369                  | 271                      | non-commercial  | 
| 19.790454016298    | PRESERVED_SPECIMEN | United States                    | Florideophyceae   | 1718                  | 340                      | non-commercial  | 
| 19.790454016298    | PRESERVED_SPECIMEN | United States                    | Florideophyceae   | 1718                  | 340                      | open commercial | 
| 19.7080291970803   | PRESERVED_SPECIMEN | Mayotte                          | Insecta           | 137                   | 27                       | total           | 
| 19.7014925373134   | PRESERVED_SPECIMEN | Germany                          | Actinopterygii    | 670                   | 132                      | total           | 
| 19.656283566058    | HUMAN_OBSERVATION  | Canada                           | Liliopsida        | 2793                  | 549                      | total           | 
| 19.6476964769648   | PRESERVED_SPECIMEN | Madagascar                       | Magnoliopsida     | 10332                 | 2030                     | open commercial | 
| 19.6428571428571   | PRESERVED_SPECIMEN | Ghana                            | Amphibia          | 112                   | 22                       | non-commercial  | 
| 19.6428571428571   | PRESERVED_SPECIMEN | Ghana                            | Amphibia          | 112                   | 22                       | open commercial | 
| 19.6428571428571   | PRESERVED_SPECIMEN | Ghana                            | Amphibia          | 112                   | 22                       | total           | 
| 19.4395796847636   | PRESERVED_SPECIMEN | Mexico                           | Bryopsida         | 1713                  | 333                      | total           | 
| 19.4328881103569   | HUMAN_OBSERVATION  | Canada                           | Magnoliopsida     | 9134                  | 1775                     | non-commercial  | 
| 19.4148936170213   | PRESERVED_SPECIMEN | Indonesia                        | Polypodiopsida    | 2256                  | 438                      | non-commercial  | 
| 19.3895870736086   | PRESERVED_SPECIMEN | Japan                            | Polypodiopsida    | 1114                  | 216                      | total           | 
| 19.3814432989691   | PRESERVED_SPECIMEN | Canada                           | Lecanoromycetes   | 2425                  | 470                      | total           | 
| 19.3466539803362   | PRESERVED_SPECIMEN | Cuba                             | Magnoliopsida     | 6306                  | 1220                     | non-commercial  | 
| 19.3340494092374   | HUMAN_OBSERVATION  | Canada                           | Liliopsida        | 2793                  | 540                      | non-commercial  | 
| 19.3181818181818   | PRESERVED_SPECIMEN | Peru                             | Lycopodiopsida    | 176                   | 34                       | total           | 
| 19.3069306930693   | PRESERVED_SPECIMEN | Bahamas                          | Florideophyceae   | 202                   | 39                       | open commercial | 
| 19.3069306930693   | PRESERVED_SPECIMEN | Bahamas                          | Florideophyceae   | 202                   | 39                       | non-commercial  | 
| 19.2660550458716   | HUMAN_OBSERVATION  | Mexico                           | Pezizomycetes     | 109                   | 21                       | non-commercial  | 
| 19.2660550458716   | HUMAN_OBSERVATION  | Mexico                           | Pezizomycetes     | 109                   | 21                       | total           | 
| 19.2513368983957   | PRESERVED_SPECIMEN | Puerto Rico                      | Pucciniomycetes   | 187                   | 36                       | open commercial | 
| 19.2513368983957   | PRESERVED_SPECIMEN | Puerto Rico                      | Pucciniomycetes   | 187                   | 36                       | non-commercial  | 
| 19.2513368983957   | PRESERVED_SPECIMEN | Puerto Rico                      | Pucciniomycetes   | 187                   | 36                       | total           | 
| 19.2488262910798   | HUMAN_OBSERVATION  | Botswana                         | Mammalia          | 213                   | 41                       | total           | 
| 19.2356485886457   | PRESERVED_SPECIMEN | Cuba                             | Magnoliopsida     | 6306                  | 1213                     | open commercial | 
| 19.2272309107636   | PRESERVED_SPECIMEN | Panama                           | Polypodiopsida    | 1087                  | 209                      | total           | 
| 19.1964285714286   | HUMAN_OBSERVATION  | United States                    | Polypodiopsida    | 1568                  | 301                      | non-commercial  | 
| 19.1829484902309   | PRESERVED_SPECIMEN | Estonia                          | Aves              | 563                   | 108                      | non-commercial  | 
| 19.1829484902309   | PRESERVED_SPECIMEN | Estonia                          | Aves              | 563                   | 108                      | total           | 
| 19.1489361702128   | HUMAN_OBSERVATION  | New Zealand                      | Reptilia          | 141                   | 27                       | total           | 
| 19.1489361702128   | HUMAN_OBSERVATION  | New Zealand                      | Reptilia          | 141                   | 27                       | non-commercial  | 
| 19.0159574468085   | PRESERVED_SPECIMEN | Indonesia                        | Polypodiopsida    | 2256                  | 429                      | open commercial | 
| 18.9931350114416   | PRESERVED_SPECIMEN | Philippines                      | Polypodiopsida    | 1311                  | 249                      | non-commercial  | 
| 18.9636163175303   | HUMAN_OBSERVATION  | Spain                            | Aves              | 907                   | 172                      | non-commercial  | 
| 18.9493433395872   | HUMAN_OBSERVATION  | Mexico                           | Amphibia          | 533                   | 101                      | non-commercial  | 
| 18.8524590163934   | PRESERVED_SPECIMEN | Canada                           | Cyanophyceae      | 122                   | 23                       | total           | 
| 18.8343994314144   | PRESERVED_SPECIMEN | United States                    | Pucciniomycetes   | 1407                  | 265                      | open commercial | 
| 18.8343994314144   | PRESERVED_SPECIMEN | United States                    | Pucciniomycetes   | 1407                  | 265                      | non-commercial  | 
| 18.8343994314144   | PRESERVED_SPECIMEN | United States                    | Pucciniomycetes   | 1407                  | 265                      | total           | 
| 18.7643020594966   | PRESERVED_SPECIMEN | Philippines                      | Polypodiopsida    | 1311                  | 246                      | open commercial | 
| 18.75              | HUMAN_OBSERVATION  | Niger                            | Mammalia          | 144                   | 27                       | total           | 
| 18.75              | HUMAN_OBSERVATION  | Niger                            | Mammalia          | 144                   | 27                       | non-commercial  | 
| 18.7134502923977   | PRESERVED_SPECIMEN | Micronesia (Federated States of) | Polypodiopsida    | 171                   | 32                       | total           | 
| 18.7035069075452   | HUMAN_OBSERVATION  | Japan                            | Aves              | 941                   | 176                      | non-commercial  | 
| 18.6590436590437   | HUMAN_OBSERVATION  | Norway                           | Lecanoromycetes   | 1924                  | 359                      | total           | 
| 18.6150576127084   | PRESERVED_SPECIMEN | United States                    | Agaricomycetes    | 8939                  | 1664                     | non-commercial  | 
| 18.5606060606061   | HUMAN_OBSERVATION  | Israel                           | Aves              | 528                   | 98                       | non-commercial  | 
| 18.5606060606061   | HUMAN_OBSERVATION  | Israel                           | Aves              | 528                   | 98                       | total           | 
| 18.5011709601874   | PRESERVED_SPECIMEN | Bahamas                          | Liliopsida        | 427                   | 79                       | total           | 
| 18.4971098265896   | PRESERVED_SPECIMEN | Cameroon                         | Polypodiopsida    | 346                   | 64                       | non-commercial  | 
| 18.4738955823293   | PRESERVED_SPECIMEN | Cuba                             | Polypodiopsida    | 747                   | 138                      | open commercial | 
| 18.4738955823293   | PRESERVED_SPECIMEN | Cuba                             | Polypodiopsida    | 747                   | 138                      | non-commercial  | 
| 18.4726522187822   | PRESERVED_SPECIMEN | Norway                           | Magnoliopsida     | 3876                  | 716                      | non-commercial  | 
| 18.3913189394787   | PRESERVED_SPECIMEN | United States                    | Agaricomycetes    | 8939                  | 1644                     | open commercial | 
| 18.3456183456183   | PRESERVED_SPECIMEN | Dominican Republic               | Liliopsida        | 1221                  | 224                      | non-commercial  | 
| 18.3043738765728   | PRESERVED_SPECIMEN | Cameroon                         | Magnoliopsida     | 6676                  | 1222                     | total           | 
| 18.2965299684543   | HUMAN_OBSERVATION  | Mexico                           | Mammalia          | 951                   | 174                      | total           | 
| 18.2089552238806   | PRESERVED_SPECIMEN | Germany                          | Actinopterygii    | 670                   | 122                      | non-commercial  | 
| 18.1483752299203   | HUMAN_OBSERVATION  | Singapore                        | Insecta           | 1631                  | 296                      | non-commercial  | 
| 18.1483752299203   | HUMAN_OBSERVATION  | Singapore                        | Insecta           | 1631                  | 296                      | total           | 
| 18.0904522613065   | PRESERVED_SPECIMEN | Russia                           | Pinopsida         | 199                   | 36                       | open commercial | 
| 18.0904522613065   | PRESERVED_SPECIMEN | Russia                           | Pinopsida         | 199                   | 36                       | non-commercial  | 
| 18.0904522613065   | PRESERVED_SPECIMEN | Russia                           | Pinopsida         | 199                   | 36                       | total           | 
| 17.9012345679012   | HUMAN_OBSERVATION  | Denmark                          | Myxomycetes       | 162                   | 29                       | total           | 
| 17.8832116788321   | PRESERVED_SPECIMEN | Cameroon                         | Amphibia          | 274                   | 49                       | total           | 
| 17.8754578754579   | PRESERVED_SPECIMEN | Venezuela                        | Polypodiopsida    | 1365                  | 244                      | total           | 
| 17.8711484593838   | PRESERVED_SPECIMEN | Cuba                             | Liliopsida        | 1785                  | 319                      | non-commercial  | 
| 17.7985948477752   | PRESERVED_SPECIMEN | Bahamas                          | Liliopsida        | 427                   | 76                       | non-commercial  | 
| 17.7723177723178   | PRESERVED_SPECIMEN | Dominican Republic               | Liliopsida        | 1221                  | 217                      | open commercial | 
| 17.7177671661452   | PRESERVED_SPECIMEN | Angola                           | Magnoliopsida     | 6073                  | 1076                     | total           | 
| 17.703081232493    | PRESERVED_SPECIMEN | Cuba                             | Liliopsida        | 1785                  | 316                      | open commercial | 
| 17.6724137931034   | PRESERVED_SPECIMEN | China                            | Pinopsida         | 232                   | 41                       | open commercial | 
| 17.6711767117671   | PRESERVED_SPECIMEN | Brazil                           | Bryopsida         | 2439                  | 431                      | non-commercial  | 
| 17.6711767117671   | PRESERVED_SPECIMEN | Brazil                           | Bryopsida         | 2439                  | 431                      | open commercial | 
| 17.6470588235294   | HUMAN_OBSERVATION  | Denmark                          | Pucciniomycetes   | 221                   | 39                       | total           | 
| 17.6300578034682   | HUMAN_OBSERVATION  | Norway                           | Actinopterygii    | 346                   | 61                       | total           | 
| 17.6100628930818   | PRESERVED_SPECIMEN | Germany                          | Arthoniomycetes   | 159                   | 28                       | total           | 
| 17.5675675675676   | HUMAN_OBSERVATION  | Taiwan                           | Reptilia          | 148                   | 26                       | total           | 
| 17.5675675675676   | HUMAN_OBSERVATION  | Taiwan                           | Reptilia          | 148                   | 26                       | non-commercial  | 
| 17.5221238938053   | HUMAN_OBSERVATION  | Greece                           | Aves              | 565                   | 99                       | total           | 
| 17.5221238938053   | HUMAN_OBSERVATION  | Greece                           | Aves              | 565                   | 99                       | non-commercial  | 
| 17.5               | PRESERVED_SPECIMEN | Philippines                      | Lycopodiopsida    | 120                   | 21                       | non-commercial  | 
| 17.4915254237288   | PRESERVED_SPECIMEN | United States                    | Bryopsida         | 2950                  | 516                      | non-commercial  | 
| 17.4757281553398   | PRESERVED_SPECIMEN | New Caledonia                    | Polypodiopsida    | 412                   | 72                       | total           | 
| 17.4074074074074   | PRESERVED_SPECIMEN | United Kingdom                   | Phaeophyceae      | 270                   | 47                       | non-commercial  | 
| 17.4074074074074   | PRESERVED_SPECIMEN | United Kingdom                   | Phaeophyceae      | 270                   | 47                       | total           | 
| 17.3507462686567   | HUMAN_OBSERVATION  | New Zealand                      | Aves              | 536                   | 93                       | open commercial | 
| 17.3501577287066   | HUMAN_OBSERVATION  | Mexico                           | Mammalia          | 951                   | 165                      | non-commercial  | 
| 17.3333333333333   | PRESERVED_SPECIMEN | Bermuda                          | Ulvophyceae       | 150                   | 26                       | open commercial | 
| 17.3333333333333   | PRESERVED_SPECIMEN | Bermuda                          | Ulvophyceae       | 150                   | 26                       | total           | 
| 17.3333333333333   | PRESERVED_SPECIMEN | Bermuda                          | Ulvophyceae       | 150                   | 26                       | non-commercial  | 
| 17.2791243158718   | HUMAN_OBSERVATION  | United Kingdom                   | Aves              | 1279                  | 221                      | non-commercial  | 
| 17.2789896670494   | PRESERVED_SPECIMEN | Turkey                           | Liliopsida        | 1742                  | 301                      | total           | 
| 17.2554347826087   | HUMAN_OBSERVATION  | Taiwan                           | Aves              | 736                   | 127                      | total           | 
| 17.2554347826087   | HUMAN_OBSERVATION  | Taiwan                           | Aves              | 736                   | 127                      | non-commercial  | 
| 17.1641791044776   | HUMAN_OBSERVATION  | Burkina Faso                     | Mammalia          | 134                   | 23                       | total           | 
| 17.1641791044776   | HUMAN_OBSERVATION  | Burkina Faso                     | Mammalia          | 134                   | 23                       | non-commercial  | 
| 17.1641791044776   | PRESERVED_SPECIMEN | Haiti                            | Polypodiopsida    | 536                   | 92                       | total           | 
| 17.1532846715328   | PRESERVED_SPECIMEN | Cameroon                         | Amphibia          | 274                   | 47                       | non-commercial  | 
| 17.1373745325723   | PRESERVED_SPECIMEN | Peru                             | Magnoliopsida     | 20324                 | 3483                     | total           | 
| 17.1021377672209   | HUMAN_OBSERVATION  | Mexico                           | Agaricomycetes    | 2526                  | 432                      | total           | 
| 17.0625494853523   | HUMAN_OBSERVATION  | Mexico                           | Agaricomycetes    | 2526                  | 431                      | non-commercial  | 
| 16.988416988417    | PRESERVED_SPECIMEN | Brazil                           | Demospongiae      | 259                   | 44                       | non-commercial  | 
| 16.988416988417    | PRESERVED_SPECIMEN | Brazil                           | Demospongiae      | 259                   | 44                       | open commercial | 
| 16.988416988417    | PRESERVED_SPECIMEN | Brazil                           | Demospongiae      | 259                   | 44                       | total           | 
| 16.9811320754717   | PRESERVED_SPECIMEN | Germany                          | Arthoniomycetes   | 159                   | 27                       | non-commercial  | 
| 16.7883211678832   | PRESERVED_SPECIMEN | Mayotte                          | Insecta           | 137                   | 23                       | non-commercial  | 
| 16.7465548232475   | PRESERVED_SPECIMEN | Cameroon                         | Magnoliopsida     | 6676                  | 1118                     | non-commercial  | 
| 16.6994106090373   | HUMAN_OBSERVATION  | Canada                           | Aves              | 1018                  | 170                      | open commercial | 
| 16.6666666666667   | PRESERVED_SPECIMEN | Iraq                             | Actinopterygii    | 126                   | 21                       | total           | 
| 16.6666666666667   | PRESERVED_SPECIMEN | Iraq                             | Actinopterygii    | 126                   | 21                       | non-commercial  | 
| 16.6666666666667   | PRESERVED_SPECIMEN | Comoros                          | Polypodiopsida    | 216                   | 36                       | non-commercial  | 
| 16.6666666666667   | PRESERVED_SPECIMEN | Comoros                          | Polypodiopsida    | 216                   | 36                       | total           | 
| 16.6153846153846   | HUMAN_OBSERVATION  | United States                    | Lycopodiopsida    | 325                   | 54                       | total           | 
| 16.5967645296585   | PRESERVED_SPECIMEN | Cameroon                         | Magnoliopsida     | 6676                  | 1108                     | open commercial | 
| 16.5926395939086   | PRESERVED_SPECIMEN | France                           | Liliopsida        | 3152                  | 523                      | non-commercial  | 
| 16.5919282511211   | PRESERVED_SPECIMEN | Papua New Guinea                 | Reptilia          | 446                   | 74                       | total           | 
| 16.5413533834586   | PRESERVED_SPECIMEN | Brazil                           | Sphagnopsida      | 133                   | 22                       | open commercial | 
| 16.5413533834586   | PRESERVED_SPECIMEN | Brazil                           | Sphagnopsida      | 133                   | 22                       | non-commercial  | 
| 16.539910441396    | PRESERVED_SPECIMEN | France                           | Magnoliopsida     | 14069                 | 2327                     | total           | 
| 16.5394402035623   | HUMAN_OBSERVATION  | Italy                            | Mammalia          | 393                   | 65                       | total           | 
| 16.5371809100999   | HUMAN_OBSERVATION  | Canada                           | Mammalia          | 901                   | 149                      | total           | 
| 16.532721010333    | PRESERVED_SPECIMEN | Turkey                           | Liliopsida        | 1742                  | 288                      | non-commercial  | 
| 16.5212649945474   | PRESERVED_SPECIMEN | United States                    | Leotiomycetes     | 1834                  | 303                      | total           | 
| 16.5               | PRESERVED_SPECIMEN | Japan                            | Reptilia          | 200                   | 33                       | total           | 
| 16.4657360406091   | PRESERVED_SPECIMEN | France                           | Liliopsida        | 3152                  | 519                      | open commercial | 
| 16.4319248826291   | HUMAN_OBSERVATION  | Botswana                         | Mammalia          | 213                   | 35                       | non-commercial  | 
| 16.3677130044843   | PRESERVED_SPECIMEN | Papua New Guinea                 | Reptilia          | 446                   | 73                       | non-commercial  | 
| 16.3651315789474   | PRESERVED_SPECIMEN | United States                    | Jungermanniopsida | 1216                  | 199                      | open commercial | 
| 16.3651315789474   | PRESERVED_SPECIMEN | United States                    | Jungermanniopsida | 1216                  | 199                      | non-commercial  | 
| 16.3076923076923   | HUMAN_OBSERVATION  | United States                    | Lycopodiopsida    | 325                   | 53                       | non-commercial  | 
| 16.304347826087    | PRESERVED_SPECIMEN | Venezuela                        | Lycopodiopsida    | 184                   | 30                       | total           | 
| 16.266325691844    | PRESERVED_SPECIMEN | Estonia                          | Insecta           | 10949                 | 1781                     | total           | 
| 16.266325691844    | PRESERVED_SPECIMEN | Estonia                          | Insecta           | 10949                 | 1781                     | non-commercial  | 
| 16.2087912087912   | HUMAN_OBSERVATION  | Canada                           | Reptilia          | 364                   | 59                       | total           | 
| 16.2037037037037   | PRESERVED_SPECIMEN | Comoros                          | Polypodiopsida    | 216                   | 35                       | open commercial | 
| 16.1849710982659   | PRESERVED_SPECIMEN | Cameroon                         | Polypodiopsida    | 346                   | 56                       | open commercial | 
| 16.1832946635731   | HUMAN_OBSERVATION  | Mexico                           | Aves              | 1724                  | 279                      | open commercial | 
| 16.0762942779292   | PRESERVED_SPECIMEN | French Guiana                    | Polypodiopsida    | 367                   | 59                       | total           | 
| 16.0561451557686   | PRESERVED_SPECIMEN | Madagascar                       | Liliopsida        | 2921                  | 469                      | non-commercial  | 
| 16.0561451557686   | PRESERVED_SPECIMEN | Madagascar                       | Liliopsida        | 2921                  | 469                      | open commercial | 
| 16.0493827160494   | PRESERVED_SPECIMEN | Australia                        | Calcarea          | 162                   | 26                       | total           | 
| 16                 | PRESERVED_SPECIMEN | Japan                            | Reptilia          | 200                   | 32                       | non-commercial  | 
| 16                 | PRESERVED_SPECIMEN | Japan                            | Reptilia          | 200                   | 32                       | open commercial | 
| 15.9957627118644   | PRESERVED_SPECIMEN | United States                    | Reptilia          | 2832                  | 453                      | total           | 
| 15.9921269528847   | PRESERVED_SPECIMEN | Taiwan                           | Insecta           | 8129                  | 1300                     | total           | 
| 15.972850678733    | PRESERVED_SPECIMEN | Turkey                           | Magnoliopsida     | 8840                  | 1412                     | total           | 
| 15.9513904094592   | PRESERVED_SPECIMEN | Canada                           | Magnoliopsida     | 9134                  | 1457                     | non-commercial  | 
| 15.9340659340659   | HUMAN_OBSERVATION  | Canada                           | Reptilia          | 364                   | 58                       | non-commercial  | 
| 15.9250585480094   | PRESERVED_SPECIMEN | Bahamas                          | Liliopsida        | 427                   | 68                       | open commercial | 
| 15.8345221112696   | PRESERVED_SPECIMEN | French Guiana                    | Liliopsida        | 1402                  | 222                      | total           | 
| 15.8307210031348   | PRESERVED_SPECIMEN | Guyana                           | Polypodiopsida    | 638                   | 101                      | total           | 
| 15.8031674208145   | PRESERVED_SPECIMEN | Turkey                           | Magnoliopsida     | 8840                  | 1397                     | non-commercial  | 
| 15.7894736842105   | PRESERVED_SPECIMEN | Germany                          | Zygnematophyceae  | 475                   | 75                       | total           | 
| 15.7760814249364   | HUMAN_OBSERVATION  | Italy                            | Mammalia          | 393                   | 62                       | non-commercial  | 
| 15.7407407407407   | PRESERVED_SPECIMEN | Mayotte                          | Liliopsida        | 216                   | 34                       | non-commercial  | 
| 15.7407407407407   | PRESERVED_SPECIMEN | Mayotte                          | Liliopsida        | 216                   | 34                       | total           | 
| 15.7407407407407   | PRESERVED_SPECIMEN | Mayotte                          | Liliopsida        | 216                   | 34                       | open commercial | 
| 15.702479338843    | HUMAN_OBSERVATION  | Norway                           | Arachnida         | 968                   | 152                      | total           | 
| 15.6094084105488   | PRESERVED_SPECIMEN | United Kingdom                   | Malacostraca      | 1403                  | 219                      | total           | 
| 15.5911973144349   | HUMAN_OBSERVATION  | Brazil                           | Aves              | 2681                  | 418                      | total           | 
| 15.5722326454034   | PRESERVED_SPECIMEN | Mexico                           | Amphibia          | 533                   | 83                       | total           | 
| 15.5642023346303   | HUMAN_OBSERVATION  | Costa Rica                       | Amphibia          | 257                   | 40                       | non-commercial  | 
| 15.5642023346303   | HUMAN_OBSERVATION  | Costa Rica                       | Amphibia          | 257                   | 40                       | total           | 
| 15.5405405405405   | PRESERVED_SPECIMEN | Taiwan                           | Reptilia          | 148                   | 23                       | total           | 
| 15.5405405405405   | PRESERVED_SPECIMEN | Taiwan                           | Reptilia          | 148                   | 23                       | open commercial | 
| 15.5405405405405   | PRESERVED_SPECIMEN | Taiwan                           | Reptilia          | 148                   | 23                       | non-commercial  | 
| 15.4668567355666   | PRESERVED_SPECIMEN | United Kingdom                   | Malacostraca      | 1403                  | 217                      | non-commercial  | 
| 15.4668567355666   | PRESERVED_SPECIMEN | United Kingdom                   | Malacostraca      | 1403                  | 217                      | open commercial | 
| 15.3262518968134   | PRESERVED_SPECIMEN | Honduras                         | Polypodiopsida    | 659                   | 101                      | total           | 
| 15.2958152958153   | PRESERVED_SPECIMEN | United States                    | Pezizomycetes     | 693                   | 106                      | total           | 
| 15.2948044366608   | PRESERVED_SPECIMEN | Mexico                           | Bryopsida         | 1713                  | 262                      | open commercial | 
| 15.2948044366608   | PRESERVED_SPECIMEN | Mexico                           | Bryopsida         | 1713                  | 262                      | non-commercial  | 
| 15.2173913043478   | PRESERVED_SPECIMEN | Kenya                            | Reptilia          | 368                   | 56                       | non-commercial  | 
| 15.2173913043478   | PRESERVED_SPECIMEN | Kenya                            | Reptilia          | 368                   | 56                       | total           | 
| 15.1212553495007   | PRESERVED_SPECIMEN | French Guiana                    | Liliopsida        | 1402                  | 212                      | non-commercial  | 
| 15.1212553495007   | PRESERVED_SPECIMEN | French Guiana                    | Liliopsida        | 1402                  | 212                      | open commercial | 
| 15.0793650793651   | PRESERVED_SPECIMEN | United Kingdom                   | Gymnolaemata      | 504                   | 76                       | total           | 
| 15.0793650793651   | PRESERVED_SPECIMEN | United Kingdom                   | Gymnolaemata      | 504                   | 76                       | open commercial | 
| 15.0793650793651   | PRESERVED_SPECIMEN | United Kingdom                   | Gymnolaemata      | 504                   | 76                       | non-commercial  | 
| 15.0568181818182   | PRESERVED_SPECIMEN | Papua New Guinea                 | Amphibia          | 352                   | 53                       | total           | 
| 15.0568181818182   | PRESERVED_SPECIMEN | Papua New Guinea                 | Amphibia          | 352                   | 53                       | non-commercial  | 
| 14.9833518312986   | HUMAN_OBSERVATION  | Canada                           | Mammalia          | 901                   | 135                      | non-commercial  | 
| 14.8471615720524   | PRESERVED_SPECIMEN | Indonesia                        | Lycopodiopsida    | 229                   | 34                       | total           | 
| 14.8014440433213   | PRESERVED_SPECIMEN | Cameroon                         | Bryopsida         | 554                   | 82                       | total           | 
| 14.765625          | HUMAN_OBSERVATION  | Colombia                         | Aves              | 2560                  | 378                      | total           | 
| 14.7186147186147   | HUMAN_OBSERVATION  | United States                    | Pezizomycetes     | 693                   | 102                      | total           | 
| 14.7058823529412   | PRESERVED_SPECIMEN | Tanzania                         | Mammalia          | 578                   | 85                       | total           | 
| 14.7058823529412   | PRESERVED_SPECIMEN | Tanzania                         | Mammalia          | 578                   | 85                       | non-commercial  | 
| 14.6810146041507   | PRESERVED_SPECIMEN | Brazil                           | Jungermanniopsida | 1301                  | 191                      | non-commercial  | 
| 14.6810146041507   | PRESERVED_SPECIMEN | Brazil                           | Jungermanniopsida | 1301                  | 191                      | open commercial | 
| 14.6739130434783   | PRESERVED_SPECIMEN | Bahamas                          | Demospongiae      | 184                   | 27                       | open commercial | 
| 14.6739130434783   | PRESERVED_SPECIMEN | Bahamas                          | Demospongiae      | 184                   | 27                       | total           | 
| 14.6739130434783   | PRESERVED_SPECIMEN | Bahamas                          | Demospongiae      | 184                   | 27                       | non-commercial  | 
| 14.6684831970936   | HUMAN_OBSERVATION  | Ecuador                          | Aves              | 2202                  | 323                      | total           | 
| 14.6586345381526   | HUMAN_OBSERVATION  | United States                    | Phaeophyceae      | 498                   | 73                       | total           | 
| 14.6209386281588   | PRESERVED_SPECIMEN | Cameroon                         | Bryopsida         | 554                   | 81                       | non-commercial  | 
| 14.6209386281588   | PRESERVED_SPECIMEN | Cameroon                         | Bryopsida         | 554                   | 81                       | open commercial | 
| 14.6183699870634   | HUMAN_OBSERVATION  | United States                    | Pinopsida         | 773                   | 113                      | open commercial | 
| 14.5851662012776   | PRESERVED_SPECIMEN | Mexico                           | Magnoliopsida     | 26143                 | 3813                     | total           | 
| 14.5743145743146   | HUMAN_OBSERVATION  | United States                    | Pezizomycetes     | 693                   | 101                      | non-commercial  | 
| 14.5283957637359   | PRESERVED_SPECIMEN | France                           | Magnoliopsida     | 14069                 | 2044                     | non-commercial  | 
| 14.5161290322581   | PRESERVED_SPECIMEN | Saudi Arabia                     | Insecta           | 372                   | 54                       | total           | 
| 14.4890038809832   | HUMAN_OBSERVATION  | New Zealand                      | Agaricomycetes    | 2319                  | 336                      | total           | 
| 14.4868301544051   | HUMAN_OBSERVATION  | Ecuador                          | Aves              | 2202                  | 319                      | non-commercial  | 
| 14.4571280321702   | HUMAN_OBSERVATION  | Norway                           | Insecta           | 15418                 | 2229                     | total           | 
| 14.453125          | PRESERVED_SPECIMEN | Gabon                            | Magnoliopsida     | 4608                  | 666                      | total           | 
| 14.4522144522145   | PRESERVED_SPECIMEN | Mauritius                        | Insecta           | 429                   | 62                       | total           | 
| 14.4465290806754   | PRESERVED_SPECIMEN | Mexico                           | Amphibia          | 533                   | 77                       | non-commercial  | 
| 14.402759810263    | HUMAN_OBSERVATION  | New Zealand                      | Agaricomycetes    | 2319                  | 334                      | non-commercial  | 
| 14.3791314236975   | PRESERVED_SPECIMEN | France                           | Magnoliopsida     | 14069                 | 2023                     | open commercial | 
| 14.3714689265537   | PRESERVED_SPECIMEN | United States                    | Reptilia          | 2832                  | 407                      | non-commercial  | 
| 14.3504531722054   | PRESERVED_SPECIMEN | Kyrgyzstan                       | Magnoliopsida     | 2648                  | 380                      | open commercial | 
| 14.3504531722054   | PRESERVED_SPECIMEN | Kyrgyzstan                       | Magnoliopsida     | 2648                  | 380                      | non-commercial  | 
| 14.3504531722054   | PRESERVED_SPECIMEN | Kyrgyzstan                       | Magnoliopsida     | 2648                  | 380                      | total           | 
| 14.321608040201    | HUMAN_OBSERVATION  | Australia                        | Elasmobranchii    | 398                   | 57                       | total           | 
| 14.0808344198175   | HUMAN_OBSERVATION  | United States                    | Amphibia          | 767                   | 108                      | open commercial | 
| 14.0712945590994   | PRESERVED_SPECIMEN | Ecuador                          | Reptilia          | 533                   | 75                       | total           | 
| 14.0694568121104   | PRESERVED_SPECIMEN | India                            | Polypodiopsida    | 1123                  | 158                      | total           | 
| 14.0676117775354   | PRESERVED_SPECIMEN | United States                    | Leotiomycetes     | 1834                  | 258                      | non-commercial  | 
| 14.0591204037491   | HUMAN_OBSERVATION  | Tanzania                         | Aves              | 1387                  | 195                      | total           | 
| 14.0566359604231   | PRESERVED_SPECIMEN | Thailand                         | Liliopsida        | 2931                  | 412                      | total           | 
| 13.9784946236559   | PRESERVED_SPECIMEN | Saudi Arabia                     | Insecta           | 372                   | 52                       | non-commercial  | 
| 13.9283683911313   | HUMAN_OBSERVATION  | Germany                          | Aves              | 1759                  | 245                      | total           | 
| 13.9269406392694   | PRESERVED_SPECIMEN | Jamaica                          | Polypodiopsida    | 876                   | 122                      | non-commercial  | 
| 13.914924297044    | HUMAN_OBSERVATION  | Tanzania                         | Aves              | 1387                  | 193                      | non-commercial  | 
| 13.8983050847458   | PRESERVED_SPECIMEN | United States                    | Bryopsida         | 2950                  | 410                      | open commercial | 
| 13.8790035587189   | PRESERVED_SPECIMEN | Jamaica                          | Agaricomycetes    | 562                   | 78                       | non-commercial  | 
| 13.8790035587189   | PRESERVED_SPECIMEN | Jamaica                          | Agaricomycetes    | 562                   | 78                       | open commercial | 
| 13.8790035587189   | PRESERVED_SPECIMEN | Jamaica                          | Agaricomycetes    | 562                   | 78                       | total           | 
| 13.8557637705849   | PRESERVED_SPECIMEN | Germany                          | Lecanoromycetes   | 1761                  | 244                      | total           | 
| 13.8398622470943   | PRESERVED_SPECIMEN | French Guiana                    | Magnoliopsida     | 4646                  | 643                      | total           | 
| 13.8314785373609   | PRESERVED_SPECIMEN | Mali                             | Liliopsida        | 629                   | 87                       | total           | 
| 13.8314785373609   | PRESERVED_SPECIMEN | Mali                             | Liliopsida        | 629                   | 87                       | non-commercial  | 
| 13.8314785373609   | PRESERVED_SPECIMEN | Mali                             | Liliopsida        | 629                   | 87                       | open commercial | 
| 13.8202649480845   | PRESERVED_SPECIMEN | Canada                           | Liliopsida        | 2793                  | 386                      | open commercial | 
| 13.8127853881279   | PRESERVED_SPECIMEN | Jamaica                          | Polypodiopsida    | 876                   | 121                      | open commercial | 
| 13.757816941444    | HUMAN_OBSERVATION  | Germany                          | Aves              | 1759                  | 242                      | non-commercial  | 
| 13.7533274179237   | HUMAN_OBSERVATION  | Norway                           | Bryopsida         | 1127                  | 155                      | total           | 
| 13.7404580152672   | PRESERVED_SPECIMEN | United States                    | Leotiomycetes     | 1834                  | 252                      | open commercial | 
| 13.6960600375235   | PRESERVED_SPECIMEN | Mexico                           | Amphibia          | 533                   | 73                       | open commercial | 
| 13.6854060193072   | PRESERVED_SPECIMEN | Germany                          | Lecanoromycetes   | 1761                  | 241                      | non-commercial  | 
| 13.6678200692042   | HUMAN_OBSERVATION  | Tanzania                         | Mammalia          | 578                   | 79                       | total           | 
| 13.6531365313653   | PRESERVED_SPECIMEN | Greenland                        | Liliopsida        | 271                   | 37                       | non-commercial  | 
| 13.6531365313653   | PRESERVED_SPECIMEN | Greenland                        | Liliopsida        | 271                   | 37                       | open commercial | 
| 13.5546875         | HUMAN_OBSERVATION  | Colombia                         | Aves              | 2560                  | 347                      | non-commercial  | 
| 13.5467980295567   | HUMAN_OBSERVATION  | Zimbabwe                         | Aves              | 812                   | 110                      | total           | 
| 13.5467980295567   | HUMAN_OBSERVATION  | Zimbabwe                         | Aves              | 812                   | 110                      | non-commercial  | 
| 13.4782608695652   | PRESERVED_SPECIMEN | Tanzania                         | Polypodiopsida    | 460                   | 62                       | total           | 
| 13.4387351778656   | PRESERVED_SPECIMEN | Canada                           | Pinopsida         | 253                   | 34                       | non-commercial  | 
| 13.3603238866397   | PRESERVED_SPECIMEN | France                           | Polypodiopsida    | 494                   | 66                       | total           | 
| 13.3522727272727   | PRESERVED_SPECIMEN | Papua New Guinea                 | Amphibia          | 352                   | 47                       | open commercial | 
| 13.3333333333333   | HUMAN_OBSERVATION  | Singapore                        | Reptilia          | 180                   | 24                       | total           | 
| 13.2971506105834   | HUMAN_OBSERVATION  | Chile                            | Aves              | 737                   | 98                       | non-commercial  | 
| 13.2971506105834   | HUMAN_OBSERVATION  | Chile                            | Aves              | 737                   | 98                       | total           | 
| 13.2387706855792   | PRESERVED_SPECIMEN | Turkmenistan                     | Liliopsida        | 423                   | 56                       | total           | 
| 13.2286995515695   | PRESERVED_SPECIMEN | Papua New Guinea                 | Reptilia          | 446                   | 59                       | open commercial | 
| 13.1301289566237   | HUMAN_OBSERVATION  | Denmark                          | Lecanoromycetes   | 853                   | 112                      | total           | 
| 13.0330945069942   | PRESERVED_SPECIMEN | Thailand                         | Liliopsida        | 2931                  | 382                      | non-commercial  | 
| 13.0246020260492   | PRESERVED_SPECIMEN | France                           | Florideophyceae   | 691                   | 90                       | open commercial | 
| 13.0246020260492   | PRESERVED_SPECIMEN | France                           | Florideophyceae   | 691                   | 90                       | non-commercial  | 
| 13                 | HUMAN_OBSERVATION  | Malaysia                         | Aves              | 1100                  | 143                      | total           | 
| 12.987012987013    | HUMAN_OBSERVATION  | Netherlands                      | Aves              | 1001                  | 130                      | total           | 
| 12.960235640648    | PRESERVED_SPECIMEN | Guadeloupe                       | Liliopsida        | 679                   | 88                       | total           | 
| 12.9503689769932   | PRESERVED_SPECIMEN | Venezuela                        | Magnoliopsida     | 13822                 | 1790                     | total           | 
| 12.9449838187702   | HUMAN_OBSERVATION  | United States                    | Polyplacophora    | 309                   | 40                       | total           | 
| 12.9032258064516   | HUMAN_OBSERVATION  | Svalbard & Jan Mayen             | Aves              | 527                   | 68                       | total           | 
| 12.8947368421053   | HUMAN_OBSERVATION  | Australia                        | Mammalia          | 760                   | 98                       | non-commercial  | 
| 12.8939828080229   | PRESERVED_SPECIMEN | United States                    | Eurotiomycetes    | 1047                  | 135                      | total           | 
| 12.874442319949    | PRESERVED_SPECIMEN | Mali                             | Magnoliopsida     | 1569                  | 202                      | non-commercial  | 
| 12.874442319949    | PRESERVED_SPECIMEN | Mali                             | Magnoliopsida     | 1569                  | 202                      | open commercial | 
| 12.874442319949    | PRESERVED_SPECIMEN | Mali                             | Magnoliopsida     | 1569                  | 202                      | total           | 
| 12.8712871287129   | PRESERVED_SPECIMEN | South Africa                     | Amphibia          | 202                   | 26                       | total           | 
| 12.8205128205128   | HUMAN_OBSERVATION  | Spain                            | Reptilia          | 312                   | 40                       | total           | 
| 12.7777777777778   | HUMAN_OBSERVATION  | Singapore                        | Reptilia          | 180                   | 23                       | non-commercial  | 
| 12.7717391304348   | PRESERVED_SPECIMEN | Kenya                            | Reptilia          | 368                   | 47                       | open commercial | 
| 12.7659574468085   | PRESERVED_SPECIMEN | Turkmenistan                     | Liliopsida        | 423                   | 54                       | non-commercial  | 
| 12.7659574468085   | PRESERVED_SPECIMEN | Turkmenistan                     | Liliopsida        | 423                   | 54                       | open commercial | 
| 12.753036437247    | PRESERVED_SPECIMEN | Canada                           | Jungermanniopsida | 494                   | 63                       | non-commercial  | 
| 12.753036437247    | PRESERVED_SPECIMEN | Canada                           | Jungermanniopsida | 494                   | 63                       | open commercial | 
| 12.6637554585153   | PRESERVED_SPECIMEN | Comoros                          | Magnoliopsida     | 916                   | 116                      | total           | 
| 12.6637554585153   | PRESERVED_SPECIMEN | Comoros                          | Magnoliopsida     | 916                   | 116                      | non-commercial  | 
| 12.6506024096386   | HUMAN_OBSERVATION  | United States                    | Phaeophyceae      | 498                   | 63                       | non-commercial  | 
| 12.5925925925926   | PRESERVED_SPECIMEN | Iran                             | Reptilia          | 270                   | 34                       | total           | 
| 12.5643666323378   | PRESERVED_SPECIMEN | Guinea                           | Liliopsida        | 971                   | 122                      | total           | 
| 12.5545851528384   | PRESERVED_SPECIMEN | Comoros                          | Magnoliopsida     | 916                   | 115                      | open commercial | 
| 12.5490196078431   | HUMAN_OBSERVATION  | Norway                           | Pucciniomycetes   | 255                   | 32                       | total           | 
| 12.5256673511294   | HUMAN_OBSERVATION  | Madagascar                       | Reptilia          | 487                   | 61                       | non-commercial  | 
| 12.5256673511294   | HUMAN_OBSERVATION  | Madagascar                       | Reptilia          | 487                   | 61                       | total           | 
| 12.5               | PRESERVED_SPECIMEN | Micronesia (Federated States of) | Magnoliopsida     | 880                   | 110                      | total           | 
| 12.4877089478859   | PRESERVED_SPECIMEN | United States                    | Demospongiae      | 1017                  | 127                      | total           | 
| 12.4189696349369   | PRESERVED_SPECIMEN | Thailand                         | Liliopsida        | 2931                  | 364                      | open commercial | 
| 12.3827392120075   | PRESERVED_SPECIMEN | Ecuador                          | Reptilia          | 533                   | 66                       | non-commercial  | 
| 12.3417721518987   | PRESERVED_SPECIMEN | United Kingdom                   | Demospongiae      | 316                   | 39                       | total           | 
| 12.3417721518987   | PRESERVED_SPECIMEN | United Kingdom                   | Demospongiae      | 316                   | 39                       | open commercial | 
| 12.3417721518987   | PRESERVED_SPECIMEN | United Kingdom                   | Demospongiae      | 316                   | 39                       | non-commercial  | 
| 12.3091603053435   | PRESERVED_SPECIMEN | Madagascar                       | Bryopsida         | 1048                  | 129                      | total           | 
| 12.3088399850802   | HUMAN_OBSERVATION  | Brazil                           | Aves              | 2681                  | 330                      | non-commercial  | 
| 12.291052114061    | PRESERVED_SPECIMEN | United States                    | Demospongiae      | 1017                  | 125                      | non-commercial  | 
| 12.291052114061    | PRESERVED_SPECIMEN | United States                    | Demospongiae      | 1017                  | 125                      | open commercial | 
| 12.1999020088192   | HUMAN_OBSERVATION  | India                            | Aves              | 2041                  | 249                      | total           | 
| 12.1951219512195   | PRESERVED_SPECIMEN | Ecuador                          | Polypodiopsida    | 1722                  | 210                      | total           | 
| 12.1317157712305   | PRESERVED_SPECIMEN | Oman                             | Magnoliopsida     | 1154                  | 140                      | non-commercial  | 
| 12.1317157712305   | PRESERVED_SPECIMEN | Oman                             | Magnoliopsida     | 1154                  | 140                      | total           | 
| 12.1167883211679   | PRESERVED_SPECIMEN | Cuba                             | Agaricomycetes    | 685                   | 83                       | total           | 
| 12.1167883211679   | PRESERVED_SPECIMEN | Cuba                             | Agaricomycetes    | 685                   | 83                       | open commercial | 
| 12.1167883211679   | PRESERVED_SPECIMEN | Cuba                             | Agaricomycetes    | 685                   | 83                       | non-commercial  | 
| 12.1091529277999   | PRESERVED_SPECIMEN | Cameroon                         | Liliopsida        | 1759                  | 213                      | total           | 
| 12.1076233183857   | PRESERVED_SPECIMEN | Brazil                           | Ulvophyceae       | 223                   | 27                       | open commercial | 
| 12.1076233183857   | PRESERVED_SPECIMEN | Brazil                           | Ulvophyceae       | 223                   | 27                       | non-commercial  | 
| 12.0915032679739   | HUMAN_OBSERVATION  | Costa Rica                       | Mammalia          | 306                   | 37                       | total           | 
| 12.085308056872    | HUMAN_OBSERVATION  | Algeria                          | Aves              | 422                   | 51                       | total           | 
| 12.085308056872    | HUMAN_OBSERVATION  | Algeria                          | Aves              | 422                   | 51                       | non-commercial  | 
| 12.0665742024965   | HUMAN_OBSERVATION  | Portugal                         | Aves              | 721                   | 87                       | total           | 
| 12.0665742024965   | HUMAN_OBSERVATION  | Portugal                         | Aves              | 721                   | 87                       | non-commercial  | 
| 12.0486815415821   | PRESERVED_SPECIMEN | Vietnam                          | Liliopsida        | 2465                  | 297                      | total           | 
| 12.0409604519774   | PRESERVED_SPECIMEN | United States                    | Reptilia          | 2832                  | 341                      | open commercial | 
| 11.9728320960354   | PRESERVED_SPECIMEN | Chile                            | Magnoliopsida     | 6331                  | 758                      | total           | 
| 11.9377162629758   | HUMAN_OBSERVATION  | Tanzania                         | Mammalia          | 578                   | 69                       | non-commercial  | 
| 11.9269776876268   | PRESERVED_SPECIMEN | Vietnam                          | Liliopsida        | 2465                  | 294                      | non-commercial  | 
| 11.9089316987741   | PRESERVED_SPECIMEN | Portugal                         | Liliopsida        | 1142                  | 136                      | total           | 
| 11.8811881188119   | PRESERVED_SPECIMEN | South Africa                     | Amphibia          | 202                   | 24                       | non-commercial  | 
| 11.8632240055827   | HUMAN_OBSERVATION  | Australia                        | Aves              | 1433                  | 170                      | open commercial | 
| 11.854103343465    | PRESERVED_SPECIMEN | Mauritius                        | Bryopsida         | 329                   | 39                       | total           | 
| 11.854103343465    | PRESERVED_SPECIMEN | Mauritius                        | Bryopsida         | 329                   | 39                       | non-commercial  | 
| 11.854103343465    | PRESERVED_SPECIMEN | Mauritius                        | Bryopsida         | 329                   | 39                       | open commercial | 
| 11.8518518518519   | PRESERVED_SPECIMEN | Iran                             | Reptilia          | 270                   | 32                       | non-commercial  | 
| 11.8389897395422   | HUMAN_OBSERVATION  | Australia                        | Reptilia          | 1267                  | 150                      | non-commercial  | 
| 11.8110236220472   | PRESERVED_SPECIMEN | Guadeloupe                       | Polypodiopsida    | 381                   | 45                       | total           | 
| 11.8090452261307   | HUMAN_OBSERVATION  | Australia                        | Elasmobranchii    | 398                   | 47                       | non-commercial  | 
| 11.8086696562033   | HUMAN_OBSERVATION  | Botswana                         | Aves              | 669                   | 79                       | non-commercial  | 
| 11.8086696562033   | HUMAN_OBSERVATION  | Botswana                         | Aves              | 669                   | 79                       | total           | 
| 11.7977528089888   | PRESERVED_SPECIMEN | Mauritius                        | Florideophyceae   | 178                   | 21                       | open commercial | 
| 11.7977528089888   | PRESERVED_SPECIMEN | Mauritius                        | Florideophyceae   | 178                   | 21                       | non-commercial  | 
| 11.7977528089888   | PRESERVED_SPECIMEN | Mauritius                        | Florideophyceae   | 178                   | 21                       | total           | 
| 11.7363344051447   | PRESERVED_SPECIMEN | Azerbaijan                       | Liliopsida        | 622                   | 73                       | open commercial | 
| 11.7363344051447   | PRESERVED_SPECIMEN | Azerbaijan                       | Liliopsida        | 622                   | 73                       | total           | 
| 11.7363344051447   | PRESERVED_SPECIMEN | Azerbaijan                       | Liliopsida        | 622                   | 73                       | non-commercial  | 
| 11.7241379310345   | PRESERVED_SPECIMEN | Vietnam                          | Liliopsida        | 2465                  | 289                      | open commercial | 
| 11.6883116883117   | HUMAN_OBSERVATION  | Netherlands                      | Aves              | 1001                  | 117                      | non-commercial  | 
| 11.6751269035533   | PRESERVED_SPECIMEN | Guinea                           | Polypodiopsida    | 197                   | 23                       | total           | 
| 11.6453862175134   | PRESERVED_SPECIMEN | Colombia                         | Magnoliopsida     | 22086                 | 2572                     | total           | 
| 11.6279069767442   | HUMAN_OBSERVATION  | Norway                           | Myxomycetes       | 301                   | 35                       | total           | 
| 11.504264198875    | HUMAN_OBSERVATION  | United States                    | Mammalia          | 5511                  | 634                      | total           | 
| 11.437908496732    | HUMAN_OBSERVATION  | Costa Rica                       | Mammalia          | 306                   | 35                       | non-commercial  | 
| 11.4152591729761   | PRESERVED_SPECIMEN | Georgia                          | Magnoliopsida     | 3434                  | 392                      | total           | 
| 11.4130434782609   | PRESERVED_SPECIMEN | Mexico                           | Pinopsida         | 184                   | 21                       | open commercial | 
| 11.3636363636364   | PRESERVED_SPECIMEN | Brunei                           | Polypodiopsida    | 264                   | 30                       | total           | 
| 11.3636363636364   | PRESERVED_SPECIMEN | Brunei                           | Polypodiopsida    | 264                   | 30                       | non-commercial  | 
| 11.3636363636364   | PRESERVED_SPECIMEN | Brunei                           | Polypodiopsida    | 264                   | 30                       | open commercial | 
| 11.3207547169811   | HUMAN_OBSERVATION  | Australia                        | Amphibia          | 318                   | 36                       | non-commercial  | 
| 11.3079019073569   | HUMAN_OBSERVATION  | Australia                        | Polypodiopsida    | 734                   | 83                       | total           | 
| 11.2696563774024   | PRESERVED_SPECIMEN | Georgia                          | Magnoliopsida     | 3434                  | 387                      | open commercial | 
| 11.2696563774024   | PRESERVED_SPECIMEN | Georgia                          | Magnoliopsida     | 3434                  | 387                      | non-commercial  | 
| 11.2685337726524   | HUMAN_OBSERVATION  | New Zealand                      | Insecta           | 6070                  | 684                      | total           | 
| 11.2412177985948   | PRESERVED_SPECIMEN | Puerto Rico                      | Sordariomycetes   | 427                   | 48                       | total           | 
| 11.2412177985948   | PRESERVED_SPECIMEN | Puerto Rico                      | Sordariomycetes   | 427                   | 48                       | open commercial | 
| 11.2412177985948   | PRESERVED_SPECIMEN | Puerto Rico                      | Sordariomycetes   | 427                   | 48                       | non-commercial  | 
| 11.2171837708831   | PRESERVED_SPECIMEN | Puerto Rico                      | Agaricomycetes    | 419                   | 47                       | non-commercial  | 
| 11.2171837708831   | PRESERVED_SPECIMEN | Puerto Rico                      | Agaricomycetes    | 419                   | 47                       | open commercial | 
| 11.2171837708831   | PRESERVED_SPECIMEN | Puerto Rico                      | Agaricomycetes    | 419                   | 47                       | total           | 
| 11.2121212121212   | PRESERVED_SPECIMEN | Guatemala                        | Reptilia          | 330                   | 37                       | total           | 
| 11.1929307805596   | PRESERVED_SPECIMEN | Guadeloupe                       | Liliopsida        | 679                   | 76                       | open commercial | 
| 11.1929307805596   | PRESERVED_SPECIMEN | Guadeloupe                       | Liliopsida        | 679                   | 76                       | non-commercial  | 
| 11.1904761904762   | PRESERVED_SPECIMEN | Trinidad & Tobago                | Polypodiopsida    | 420                   | 47                       | total           | 
| 11.1724137931034   | PRESERVED_SPECIMEN | Georgia                          | Liliopsida        | 725                   | 81                       | total           | 
| 11.1625678696902   | PRESERVED_SPECIMEN | Guyana                           | Magnoliopsida     | 6262                  | 699                      | total           | 
| 11.1516414799375   | PRESERVED_SPECIMEN | China                            | Polypodiopsida    | 1919                  | 214                      | total           | 
| 11.142061281337    | HUMAN_OBSERVATION  | Norway                           | Jungermanniopsida | 359                   | 40                       | total           | 
| 11.1372549019608   | PRESERVED_SPECIMEN | U.S. Virgin Islands              | Magnoliopsida     | 1275                  | 142                      | total           | 
| 11.1368909512761   | HUMAN_OBSERVATION  | South Africa                     | Polypodiopsida    | 431                   | 48                       | non-commercial  | 
| 11.1368909512761   | HUMAN_OBSERVATION  | South Africa                     | Polypodiopsida    | 431                   | 48                       | total           | 
| 11.1111111111111   | HUMAN_OBSERVATION  | Spain                            | Pinopsida         | 189                   | 21                       | total           | 
| 11.1111111111111   | PRESERVED_SPECIMEN | Trinidad & Tobago                | Arachnida         | 252                   | 28                       | total           | 
| 11.1111111111111   | PRESERVED_SPECIMEN | Trinidad & Tobago                | Arachnida         | 252                   | 28                       | non-commercial  | 
| 11.0655737704918   | PRESERVED_SPECIMEN | Canada                           | Phaeophyceae      | 244                   | 27                       | open commercial | 
| 11.0655737704918   | PRESERVED_SPECIMEN | Canada                           | Phaeophyceae      | 244                   | 27                       | non-commercial  | 
| 11.0655737704918   | PRESERVED_SPECIMEN | Canada                           | Phaeophyceae      | 244                   | 27                       | total           | 
| 11.0599078341014   | HUMAN_OBSERVATION  | United States                    | Maxillopoda       | 434                   | 48                       | total           | 
| 11.0032362459547   | HUMAN_OBSERVATION  | United States                    | Polyplacophora    | 309                   | 34                       | non-commercial  | 
| 10.9987085665088   | PRESERVED_SPECIMEN | French Guiana                    | Magnoliopsida     | 4646                  | 511                      | non-commercial  | 
| 10.9987085665088   | PRESERVED_SPECIMEN | French Guiana                    | Magnoliopsida     | 4646                  | 511                      | open commercial | 
| 10.9737979470556   | PRESERVED_SPECIMEN | Ecuador                          | Magnoliopsida     | 14808                 | 1625                     | total           | 
| 10.958904109589    | PRESERVED_SPECIMEN | New Zealand                      | Pinopsida         | 292                   | 32                       | total           | 
| 10.9195402298851   | PRESERVED_SPECIMEN | Russia                           | Jungermanniopsida | 522                   | 57                       | total           | 
| 10.9152927799886   | PRESERVED_SPECIMEN | Cameroon                         | Liliopsida        | 1759                  | 192                      | non-commercial  | 
| 10.8974358974359   | HUMAN_OBSERVATION  | Spain                            | Reptilia          | 312                   | 34                       | non-commercial  | 
| 10.8731466227348   | HUMAN_OBSERVATION  | New Zealand                      | Insecta           | 6070                  | 660                      | non-commercial  | 
| 10.8667529107374   | PRESERVED_SPECIMEN | United States                    | Pinopsida         | 773                   | 84                       | open commercial | 
| 10.8552631578947   | PRESERVED_SPECIMEN | Canada                           | Polypodiopsida    | 304                   | 33                       | non-commercial  | 
| 10.8433734939759   | PRESERVED_SPECIMEN | Papua New Guinea                 | Insecta           | 3901                  | 423                      | total           | 
| 10.8208955223881   | PRESERVED_SPECIMEN | New Zealand                      | Aves              | 536                   | 58                       | total           | 
| 10.8173076923077   | PRESERVED_SPECIMEN | Germany                          | Myxomycetes       | 416                   | 45                       | total           | 
| 10.8173076923077   | PRESERVED_SPECIMEN | Germany                          | Myxomycetes       | 416                   | 45                       | non-commercial  | 
| 10.7638888888889   | HUMAN_OBSERVATION  | Switzerland                      | Aves              | 576                   | 62                       | non-commercial  | 
| 10.7638888888889   | HUMAN_OBSERVATION  | Switzerland                      | Aves              | 576                   | 62                       | total           | 
| 10.7447413303013   | PRESERVED_SPECIMEN | Cameroon                         | Liliopsida        | 1759                  | 189                      | open commercial | 
| 10.7226107226107   | PRESERVED_SPECIMEN | Mauritius                        | Insecta           | 429                   | 46                       | non-commercial  | 
| 10.6918238993711   | PRESERVED_SPECIMEN | Comoros                          | Liliopsida        | 318                   | 34                       | total           | 
| 10.6918238993711   | PRESERVED_SPECIMEN | Comoros                          | Liliopsida        | 318                   | 34                       | open commercial | 
| 10.6918238993711   | PRESERVED_SPECIMEN | Comoros                          | Liliopsida        | 318                   | 34                       | non-commercial  | 
| 10.6870229007634   | PRESERVED_SPECIMEN | Madagascar                       | Bryopsida         | 1048                  | 112                      | open commercial | 
| 10.6870229007634   | PRESERVED_SPECIMEN | Madagascar                       | Bryopsida         | 1048                  | 112                      | non-commercial  | 
| 10.6870229007634   | HUMAN_OBSERVATION  | Zimbabwe                         | Mammalia          | 262                   | 28                       | non-commercial  | 
| 10.6870229007634   | HUMAN_OBSERVATION  | Zimbabwe                         | Mammalia          | 262                   | 28                       | total           | 
| 10.6274007682458   | PRESERVED_SPECIMEN | Haiti                            | Insecta           | 781                   | 83                       | total           | 
| 10.6060606060606   | PRESERVED_SPECIMEN | Guatemala                        | Amphibia          | 198                   | 21                       | total           | 
| 10.6               | PRESERVED_SPECIMEN | Malawi                           | Actinopterygii    | 500                   | 53                       | total           | 
| 10.6               | PRESERVED_SPECIMEN | Malawi                           | Actinopterygii    | 500                   | 53                       | open commercial | 
| 10.6               | PRESERVED_SPECIMEN | Malawi                           | Actinopterygii    | 500                   | 53                       | non-commercial  | 
| 10.5475927967659   | HUMAN_OBSERVATION  | Australia                        | Actinopterygii    | 5442                  | 574                      | total           | 
| 10.4166666666667   | PRESERVED_SPECIMEN | Germany                          | Liliopsida        | 2448                  | 255                      | total           | 
| 10.3887826641173   | HUMAN_OBSERVATION  | Mali                             | Magnoliopsida     | 1569                  | 163                      | total           | 
| 10.3799185888738   | PRESERVED_SPECIMEN | Bolivia                          | Polypodiopsida    | 1474                  | 153                      | total           | 
| 10.377358490566    | PRESERVED_SPECIMEN | Australia                        | Amphibia          | 318                   | 33                       | total           | 
| 10.3703703703704   | PRESERVED_SPECIMEN | United Kingdom                   | Phaeophyceae      | 270                   | 28                       | open commercial | 
| 10.36866359447     | HUMAN_OBSERVATION  | United States                    | Maxillopoda       | 434                   | 45                       | non-commercial  | 
| 10.3673955079578   | HUMAN_OBSERVATION  | United States                    | Actinopterygii    | 6723                  | 697                      | total           | 
| 10.3618421052632   | PRESERVED_SPECIMEN | Kyrgyzstan                       | Liliopsida        | 608                   | 63                       | total           | 
| 10.3585657370518   | PRESERVED_SPECIMEN | Canada                           | Demospongiae      | 251                   | 26                       | non-commercial  | 
| 10.3585657370518   | PRESERVED_SPECIMEN | Canada                           | Demospongiae      | 251                   | 26                       | open commercial | 
| 10.3585657370518   | PRESERVED_SPECIMEN | Canada                           | Demospongiae      | 251                   | 26                       | total           | 
| 10.3448275862069   | PRESERVED_SPECIMEN | Russia                           | Jungermanniopsida | 522                   | 54                       | open commercial | 
| 10.3448275862069   | PRESERVED_SPECIMEN | Russia                           | Jungermanniopsida | 522                   | 54                       | non-commercial  | 
| 10.3380695737384   | HUMAN_OBSERVATION  | India                            | Aves              | 2041                  | 211                      | non-commercial  | 
| 10.3221337028057   | PRESERVED_SPECIMEN | Azerbaijan                       | Magnoliopsida     | 2887                  | 298                      | total           | 
| 10.3221337028057   | PRESERVED_SPECIMEN | Azerbaijan                       | Magnoliopsida     | 2887                  | 298                      | non-commercial  | 
| 10.3194103194103   | PRESERVED_SPECIMEN | Fiji                             | Polypodiopsida    | 407                   | 42                       | non-commercial  | 
| 10.3182256509161   | PRESERVED_SPECIMEN | Turkmenistan                     | Magnoliopsida     | 2074                  | 214                      | open commercial | 
| 10.3182256509161   | PRESERVED_SPECIMEN | Turkmenistan                     | Magnoliopsida     | 2074                  | 214                      | non-commercial  | 
| 10.3182256509161   | PRESERVED_SPECIMEN | Turkmenistan                     | Magnoliopsida     | 2074                  | 214                      | total           | 
| 10.2874956702459   | PRESERVED_SPECIMEN | Azerbaijan                       | Magnoliopsida     | 2887                  | 297                      | open commercial | 
| 10.2867203219316   | PRESERVED_SPECIMEN | Nigeria                          | Magnoliopsida     | 3976                  | 409                      | total           | 
| 10.2756892230576   | HUMAN_OBSERVATION  | Cuba                             | Aves              | 399                   | 41                       | non-commercial  | 
| 10.2756892230576   | HUMAN_OBSERVATION  | Cuba                             | Aves              | 399                   | 41                       | total           | 
| 10.2649006622517   | PRESERVED_SPECIMEN | Comoros                          | Insecta           | 302                   | 31                       | total           | 
| 10.2639296187683   | PRESERVED_SPECIMEN | Vanuatu                          | Polypodiopsida    | 341                   | 35                       | open commercial | 
| 10.2639296187683   | PRESERVED_SPECIMEN | Vanuatu                          | Polypodiopsida    | 341                   | 35                       | non-commercial  | 
| 10.2639296187683   | PRESERVED_SPECIMEN | Vanuatu                          | Polypodiopsida    | 341                   | 35                       | total           | 
| 10.2409638554217   | PRESERVED_SPECIMEN | United Kingdom                   | Florideophyceae   | 498                   | 51                       | open commercial | 
| 10.2301968147994   | PRESERVED_SPECIMEN | Spain                            | Magnoliopsida     | 14379                 | 1471                     | total           | 
| 10.2228047182176   | HUMAN_OBSERVATION  | Sweden                           | Aves              | 763                   | 78                       | total           | 
| 10.2173913043478   | PRESERVED_SPECIMEN | Tanzania                         | Polypodiopsida    | 460                   | 47                       | non-commercial  | 
| 10.2088167053364   | PRESERVED_SPECIMEN | Seychelles                       | Insecta           | 431                   | 44                       | total           | 
| 10.2040816326531   | PRESERVED_SPECIMEN | Norway                           | Bryopsida         | 1127                  | 115                      | total           | 
| 10.1503759398496   | HUMAN_OBSERVATION  | Madagascar                       | Mammalia          | 266                   | 27                       | total           | 
| 10.1503759398496   | HUMAN_OBSERVATION  | Madagascar                       | Mammalia          | 266                   | 27                       | non-commercial  | 
| 10.10919337795     | HUMAN_OBSERVATION  | Australia                        | Agaricomycetes    | 2839                  | 287                      | total           | 
| 10.1075268817204   | PRESERVED_SPECIMEN | French Polynesia                 | Liliopsida        | 465                   | 47                       | total           | 
| 10.0917431192661   | HUMAN_OBSERVATION  | Sweden                           | Aves              | 763                   | 77                       | non-commercial  | 
| 10.0737100737101   | PRESERVED_SPECIMEN | Fiji                             | Polypodiopsida    | 407                   | 41                       | open commercial | 
| 10.0609756097561   | HUMAN_OBSERVATION  | Dominican Republic               | Aves              | 328                   | 33                       | total           | 
| 10.0609756097561   | HUMAN_OBSERVATION  | Dominican Republic               | Aves              | 328                   | 33                       | non-commercial  | 
| 10.0591715976331   | HUMAN_OBSERVATION  | Serbia                           | Agaricomycetes    | 338                   | 34                       | total           | 
| 10.0591715976331   | HUMAN_OBSERVATION  | Serbia                           | Agaricomycetes    | 338                   | 34                       | non-commercial  | 
| 10.0520405368392   | PRESERVED_SPECIMEN | United States                    | Sordariomycetes   | 3651                  | 367                      | total           | 
| 10.0436681222707   | PRESERVED_SPECIMEN | Indonesia                        | Lycopodiopsida    | 229                   | 23                       | non-commercial  | 
| 10.0436681222707   | PRESERVED_SPECIMEN | Indonesia                        | Lycopodiopsida    | 229                   | 23                       | open commercial | 
| 10                 | HUMAN_OBSERVATION  | Iceland                          | Aves              | 600                   | 60                       | total           | 
| 10                 | HUMAN_OBSERVATION  | Iceland                          | Aves              | 600                   | 60                       | non-commercial  | 
| 9.96189439303212   | HUMAN_OBSERVATION  | United States                    | Mammalia          | 5511                  | 549                      | non-commercial  | 
| 9.9609375          | PRESERVED_SPECIMEN | Martinique                       | Liliopsida        | 512                   | 51                       | total           | 
| 9.95670995670996   | HUMAN_OBSERVATION  | Norway                           | Pezizomycetes     | 462                   | 46                       | total           | 
| 9.9537037037037    | PRESERVED_SPECIMEN | Greenland                        | Magnoliopsida     | 432                   | 43                       | total           | 
| 9.86031224322103   | PRESERVED_SPECIMEN | United States                    | Sordariomycetes   | 3651                  | 360                      | non-commercial  | 
| 9.83292248698987   | PRESERVED_SPECIMEN | United States                    | Sordariomycetes   | 3651                  | 359                      | open commercial | 
| 9.81963927855711   | PRESERVED_SPECIMEN | Brazil                           | Amphibia          | 998                   | 98                       | total           | 
| 9.7944377267231    | HUMAN_OBSERVATION  | Denmark                          | Leotiomycetes     | 827                   | 81                       | total           | 
| 9.78260869565217   | PRESERVED_SPECIMEN | Tanzania                         | Polypodiopsida    | 460                   | 45                       | open commercial | 
| 9.77242302543507   | HUMAN_OBSERVATION  | Kenya                            | Mammalia          | 747                   | 73                       | total           | 
| 9.765625           | PRESERVED_SPECIMEN | Martinique                       | Liliopsida        | 512                   | 50                       | non-commercial  | 
| 9.765625           | PRESERVED_SPECIMEN | Martinique                       | Liliopsida        | 512                   | 50                       | open commercial | 
| 9.76331360946746   | PRESERVED_SPECIMEN | Estonia                          | Pezizomycetes     | 338                   | 33                       | total           | 
| 9.76331360946746   | PRESERVED_SPECIMEN | Estonia                          | Pezizomycetes     | 338                   | 33                       | non-commercial  | 
| 9.75609756097561   | PRESERVED_SPECIMEN | Puerto Rico                      | Cyanophyceae      | 287                   | 28                       | total           | 
| 9.75               | HUMAN_OBSERVATION  | Puerto Rico                      | Aves              | 400                   | 39                       | total           | 
| 9.75               | HUMAN_OBSERVATION  | Puerto Rico                      | Aves              | 400                   | 39                       | non-commercial  | 
| 9.74842767295597   | PRESERVED_SPECIMEN | Australia                        | Amphibia          | 318                   | 31                       | non-commercial  | 
| 9.74124809741248   | HUMAN_OBSERVATION  | Belize                           | Aves              | 657                   | 64                       | total           | 
| 9.74124809741248   | HUMAN_OBSERVATION  | Belize                           | Aves              | 657                   | 64                       | non-commercial  | 
| 9.72222222222222   | PRESERVED_SPECIMEN | Oman                             | Liliopsida        | 288                   | 28                       | total           | 
| 9.72222222222222   | PRESERVED_SPECIMEN | Oman                             | Liliopsida        | 288                   | 28                       | non-commercial  | 
| 9.71302428256071   | PRESERVED_SPECIMEN | Philippines                      | Agaricomycetes    | 453                   | 44                       | non-commercial  | 
| 9.71302428256071   | PRESERVED_SPECIMEN | Philippines                      | Agaricomycetes    | 453                   | 44                       | total           | 
| 9.71302428256071   | PRESERVED_SPECIMEN | Philippines                      | Agaricomycetes    | 453                   | 44                       | open commercial | 
| 9.68992248062016   | PRESERVED_SPECIMEN | Comoros                          | Bryopsida         | 258                   | 25                       | total           | 
| 9.68992248062016   | PRESERVED_SPECIMEN | Comoros                          | Bryopsida         | 258                   | 25                       | non-commercial  | 
| 9.68992248062016   | PRESERVED_SPECIMEN | Comoros                          | Bryopsida         | 258                   | 25                       | open commercial | 
| 9.6745027124774    | PRESERVED_SPECIMEN | United Kingdom                   | Liliopsida        | 2212                  | 214                      | total           | 
| 9.62962962962963   | PRESERVED_SPECIMEN | Iran                             | Reptilia          | 270                   | 26                       | open commercial | 
| 9.60264900662252   | PRESERVED_SPECIMEN | Comoros                          | Insecta           | 302                   | 29                       | non-commercial  | 
| 9.59420289855072   | PRESERVED_SPECIMEN | United States                    | Aves              | 3450                  | 331                      | non-commercial  | 
| 9.56175298804781   | PRESERVED_SPECIMEN | Malaysia                         | Amphibia          | 251                   | 24                       | total           | 
| 9.53947368421053   | PRESERVED_SPECIMEN | Chile                            | Polypodiopsida    | 304                   | 29                       | non-commercial  | 
| 9.53288846520496   | PRESERVED_SPECIMEN | Gabon                            | Liliopsida        | 1049                  | 100                      | total           | 
| 9.52577319587629   | PRESERVED_SPECIMEN | Canada                           | Lecanoromycetes   | 2425                  | 231                      | non-commercial  | 
| 9.51724137931034   | PRESERVED_SPECIMEN | Georgia                          | Liliopsida        | 725                   | 69                       | non-commercial  | 
| 9.51724137931034   | PRESERVED_SPECIMEN | Georgia                          | Liliopsida        | 725                   | 69                       | open commercial | 
| 9.51276102088167   | HUMAN_OBSERVATION  | Denmark                          | Sordariomycetes   | 862                   | 82                       | total           | 
| 9.4995303904468    | PRESERVED_SPECIMEN | Vietnam                          | Magnoliopsida     | 7453                  | 708                      | total           | 
| 9.46372239747634   | HUMAN_OBSERVATION  | Lithuania                        | Agaricomycetes    | 317                   | 30                       | non-commercial  | 
| 9.46372239747634   | HUMAN_OBSERVATION  | Lithuania                        | Agaricomycetes    | 317                   | 30                       | total           | 
| 9.39393939393939   | PRESERVED_SPECIMEN | Guatemala                        | Reptilia          | 330                   | 31                       | non-commercial  | 
| 9.38887912345462   | HUMAN_OBSERVATION  | United States                    | Insecta           | 85335                 | 8012                     | total           | 
| 9.3841642228739    | PRESERVED_SPECIMEN | Réunion                          | Polypodiopsida    | 341                   | 32                       | total           | 
| 9.37944102321175   | PRESERVED_SPECIMEN | Sweden                           | Lecanoromycetes   | 2111                  | 198                      | total           | 
| 9.37866354044549   | PRESERVED_SPECIMEN | Japan                            | Liliopsida        | 2559                  | 240                      | total           | 
| 9.375              | PRESERVED_SPECIMEN | Kyrgyzstan                       | Liliopsida        | 608                   | 57                       | open commercial | 
| 9.375              | PRESERVED_SPECIMEN | Kyrgyzstan                       | Liliopsida        | 608                   | 57                       | non-commercial  | 
| 9.35193881658392   | PRESERVED_SPECIMEN | Vietnam                          | Magnoliopsida     | 7453                  | 697                      | non-commercial  | 
| 9.33416303671437   | PRESERVED_SPECIMEN | French Polynesia                 | Magnoliopsida     | 1607                  | 150                      | total           | 
| 9.3320701089531    | PRESERVED_SPECIMEN | Sweden                           | Lecanoromycetes   | 2111                  | 197                      | non-commercial  | 
| 9.32642487046632   | PRESERVED_SPECIMEN | United States                    | Rhabditophora     | 386                   | 36                       | total           | 
| 9.32203389830508   | PRESERVED_SPECIMEN | India                            | Bryopsida         | 1888                  | 176                      | total           | 
| 9.28074245939675   | PRESERVED_SPECIMEN | Seychelles                       | Insecta           | 431                   | 40                       | non-commercial  | 
| 9.27143432174963   | PRESERVED_SPECIMEN | Vietnam                          | Magnoliopsida     | 7453                  | 691                      | open commercial | 
| 9.24807903402854   | PRESERVED_SPECIMEN | Sri Lanka                        | Magnoliopsida     | 3644                  | 337                      | total           | 
| 9.24528301886792   | HUMAN_OBSERVATION  | Iran                             | Aves              | 530                   | 49                       | non-commercial  | 
| 9.24528301886792   | HUMAN_OBSERVATION  | Iran                             | Aves              | 530                   | 49                       | total           | 
| 9.24122575730943   | PRESERVED_SPECIMEN | United States                    | Insecta           | 85335                 | 7886                     | total           | 
| 9.23076923076923   | HUMAN_OBSERVATION  | Poland                           | Aves              | 650                   | 60                       | total           | 
| 9.22330097087379   | PRESERVED_SPECIMEN | New Caledonia                    | Polypodiopsida    | 412                   | 38                       | open commercial | 
| 9.22330097087379   | PRESERVED_SPECIMEN | New Caledonia                    | Polypodiopsida    | 412                   | 38                       | non-commercial  | 
| 9.18097754293263   | HUMAN_OBSERVATION  | United States                    | Arachnida         | 6056                  | 556                      | total           | 
| 9.16905444126074   | PRESERVED_SPECIMEN | Madagascar                       | Aves              | 349                   | 32                       | total           | 
| 9.16313559322034   | PRESERVED_SPECIMEN | India                            | Bryopsida         | 1888                  | 173                      | non-commercial  | 
| 9.16313559322034   | PRESERVED_SPECIMEN | India                            | Bryopsida         | 1888                  | 173                      | open commercial | 
| 9.14285714285714   | PRESERVED_SPECIMEN | Peru                             | Reptilia          | 525                   | 48                       | total           | 
| 9.12806539509537   | PRESERVED_SPECIMEN | Australia                        | Polypodiopsida    | 734                   | 67                       | total           | 
| 9.12017167381974   | PRESERVED_SPECIMEN | United States                    | Clitellata        | 932                   | 85                       | total           | 
| 9.07317446352752   | HUMAN_OBSERVATION  | Mexico                           | Magnoliopsida     | 26143                 | 2372                     | total           | 
| 9.04872389791183   | PRESERVED_SPECIMEN | South Africa                     | Polypodiopsida    | 431                   | 39                       | total           | 
| 9.03010033444816   | PRESERVED_SPECIMEN | Australia                        | Pinopsida         | 299                   | 27                       | total           | 
| 9.02727307501052   | HUMAN_OBSERVATION  | Mexico                           | Magnoliopsida     | 26143                 | 2360                     | non-commercial  | 
| 9.02527075812274   | PRESERVED_SPECIMEN | Canada                           | Arachnida         | 1662                  | 150                      | non-commercial  | 
| 9.02527075812274   | PRESERVED_SPECIMEN | Canada                           | Arachnida         | 1662                  | 150                      | total           | 
| 8.98617511520737   | PRESERVED_SPECIMEN | United States                    | Maxillopoda       | 434                   | 39                       | total           | 
| 8.97097625329815   | PRESERVED_SPECIMEN | United States                    | Chlorophyceae     | 379                   | 34                       | open commercial | 
| 8.97097625329815   | PRESERVED_SPECIMEN | United States                    | Chlorophyceae     | 379                   | 34                       | total           | 
| 8.97097625329815   | PRESERVED_SPECIMEN | United States                    | Chlorophyceae     | 379                   | 34                       | non-commercial  | 
| 8.96797153024911   | PRESERVED_SPECIMEN | Ecuador                          | Bryopsida         | 1405                  | 126                      | non-commercial  | 
| 8.96797153024911   | PRESERVED_SPECIMEN | Ecuador                          | Bryopsida         | 1405                  | 126                      | total           | 
| 8.96797153024911   | PRESERVED_SPECIMEN | Ecuador                          | Bryopsida         | 1405                  | 126                      | open commercial | 
| 8.9126559714795    | HUMAN_OBSERVATION  | United States                    | Asteroidea        | 561                   | 50                       | total           | 
| 8.87230514096186   | PRESERVED_SPECIMEN | South Africa                     | Bryopsida         | 1206                  | 107                      | total           | 
| 8.84146341463415   | HUMAN_OBSERVATION  | Zambia                           | Mammalia          | 328                   | 29                       | total           | 
| 8.83693677857854   | HUMAN_OBSERVATION  | United States                    | Insecta           | 85335                 | 7541                     | non-commercial  | 
| 8.8348271446863    | PRESERVED_SPECIMEN | Haiti                            | Insecta           | 781                   | 69                       | non-commercial  | 
| 8.81818181818182   | HUMAN_OBSERVATION  | Malaysia                         | Aves              | 1100                  | 97                       | non-commercial  | 
| 8.79541108986616   | PRESERVED_SPECIMEN | Australia                        | Florideophyceae   | 1046                  | 92                       | total           | 
| 8.79541108986616   | PRESERVED_SPECIMEN | Australia                        | Florideophyceae   | 1046                  | 92                       | open commercial | 
| 8.79541108986616   | PRESERVED_SPECIMEN | Australia                        | Florideophyceae   | 1046                  | 92                       | non-commercial  | 
| 8.7893864013267    | PRESERVED_SPECIMEN | South Africa                     | Bryopsida         | 1206                  | 106                      | non-commercial  | 
| 8.7893864013267    | PRESERVED_SPECIMEN | South Africa                     | Bryopsida         | 1206                  | 106                      | open commercial | 
| 8.78787878787879   | PRESERVED_SPECIMEN | Guatemala                        | Reptilia          | 330                   | 29                       | open commercial | 
| 8.76565295169946   | HUMAN_OBSERVATION  | United States                    | Elasmobranchii    | 559                   | 49                       | total           | 
| 8.76288659793814   | HUMAN_OBSERVATION  | Benin                            | Aves              | 582                   | 51                       | non-commercial  | 
| 8.76288659793814   | HUMAN_OBSERVATION  | Benin                            | Aves              | 582                   | 51                       | total           | 
| 8.76288659793814   | PRESERVED_SPECIMEN | United Kingdom                   | Strophomenata     | 388                   | 34                       | total           | 
| 8.76288659793814   | PRESERVED_SPECIMEN | United Kingdom                   | Strophomenata     | 388                   | 34                       | open commercial | 
| 8.76288659793814   | PRESERVED_SPECIMEN | United Kingdom                   | Strophomenata     | 388                   | 34                       | non-commercial  | 
| 8.75486381322957   | PRESERVED_SPECIMEN | France                           | Aves              | 1028                  | 90                       | total           | 
| 8.75               | PRESERVED_SPECIMEN | France                           | Ulvophyceae       | 240                   | 21                       | total           | 
| 8.70147255689424   | HUMAN_OBSERVATION  | Kenya                            | Mammalia          | 747                   | 65                       | non-commercial  | 
| 8.69165747886806   | HUMAN_OBSERVATION  | Australia                        | Actinopterygii    | 5442                  | 473                      | non-commercial  | 
| 8.68055555555556   | PRESERVED_SPECIMEN | United Kingdom                   | Trematoda         | 288                   | 25                       | non-commercial  | 
| 8.68055555555556   | PRESERVED_SPECIMEN | United Kingdom                   | Trematoda         | 288                   | 25                       | total           | 
| 8.68055555555556   | PRESERVED_SPECIMEN | United Kingdom                   | Trematoda         | 288                   | 25                       | open commercial | 
| 8.67208672086721   | PRESERVED_SPECIMEN | Panama                           | Reptilia          | 369                   | 32                       | total           | 
| 8.67208672086721   | PRESERVED_SPECIMEN | Panama                           | Reptilia          | 369                   | 32                       | non-commercial  | 
| 8.64584967833046   | PRESERVED_SPECIMEN | Mexico                           | Liliopsida        | 6373                  | 551                      | total           | 
| 8.62710099657891   | HUMAN_OBSERVATION  | United States                    | Actinopterygii    | 6723                  | 580                      | non-commercial  | 
| 8.61423220973783   | HUMAN_OBSERVATION  | Bulgaria                         | Aves              | 534                   | 46                       | total           | 
| 8.61423220973783   | HUMAN_OBSERVATION  | Bulgaria                         | Aves              | 534                   | 46                       | non-commercial  | 
| 8.60303830911493   | HUMAN_OBSERVATION  | United States                    | Arachnida         | 6056                  | 521                      | non-commercial  | 
| 8.58536585365854   | PRESERVED_SPECIMEN | Iran                             | Liliopsida        | 1025                  | 88                       | total           | 
| 8.55264967136925   | HUMAN_OBSERVATION  | United States                    | Magnoliopsida     | 36363                 | 3110                     | open commercial | 
| 8.53658536585366   | HUMAN_OBSERVATION  | Zambia                           | Mammalia          | 328                   | 28                       | non-commercial  | 
| 8.53080568720379   | PRESERVED_SPECIMEN | United States                    | Arthoniomycetes   | 422                   | 36                       | non-commercial  | 
| 8.49056603773585   | PRESERVED_SPECIMEN | Australia                        | Amphibia          | 318                   | 27                       | open commercial | 
| 8.48985725018783   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Magnoliopsida     | 1331                  | 113                      | total           | 
| 8.48985725018783   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Magnoliopsida     | 1331                  | 113                      | non-commercial  | 
| 8.48484848484849   | PRESERVED_SPECIMEN | Argentina                        | Polypodiopsida    | 660                   | 56                       | total           | 
| 8.45936939246347   | PRESERVED_SPECIMEN | Papua New Guinea                 | Insecta           | 3901                  | 330                      | non-commercial  | 
| 8.43926553672316   | HUMAN_OBSERVATION  | United States                    | Reptilia          | 2832                  | 239                      | open commercial | 
| 8.4375             | HUMAN_OBSERVATION  | New Zealand                      | Arachnida         | 640                   | 54                       | open commercial | 
| 8.4375             | PRESERVED_SPECIMEN | Samoa                            | Polypodiopsida    | 320                   | 27                       | total           | 
| 8.41836734693877   | PRESERVED_SPECIMEN | United States                    | Polypodiopsida    | 1568                  | 132                      | open commercial | 
| 8.41269841269841   | PRESERVED_SPECIMEN | Réunion                          | Liliopsida        | 630                   | 53                       | total           | 
| 8.40787119856887   | HUMAN_OBSERVATION  | United States                    | Elasmobranchii    | 559                   | 47                       | non-commercial  | 
| 8.38323353293413   | PRESERVED_SPECIMEN | Guadeloupe                       | Bryopsida         | 334                   | 28                       | open commercial | 
| 8.38323353293413   | PRESERVED_SPECIMEN | Guadeloupe                       | Bryopsida         | 334                   | 28                       | non-commercial  | 
| 8.38323353293413   | PRESERVED_SPECIMEN | Guadeloupe                       | Bryopsida         | 334                   | 28                       | total           | 
| 8.38011775982473   | HUMAN_OBSERVATION  | Italy                            | Magnoliopsida     | 7303                  | 612                      | total           | 
| 8.37209302325581   | PRESERVED_SPECIMEN | Ireland                          | Actinopterygii    | 430                   | 36                       | non-commercial  | 
| 8.37209302325581   | PRESERVED_SPECIMEN | Ireland                          | Actinopterygii    | 430                   | 36                       | total           | 
| 8.37209302325581   | PRESERVED_SPECIMEN | Ireland                          | Actinopterygii    | 430                   | 36                       | open commercial | 
| 8.3664247569492    | HUMAN_OBSERVATION  | Italy                            | Magnoliopsida     | 7303                  | 611                      | non-commercial  | 
| 8.36472065285625   | PRESERVED_SPECIMEN | Paraguay                         | Magnoliopsida     | 6372                  | 533                      | total           | 
| 8.36120401337793   | PRESERVED_SPECIMEN | Australia                        | Pinopsida         | 299                   | 25                       | non-commercial  | 
| 8.34553440702782   | PRESERVED_SPECIMEN | Réunion                          | Bryopsida         | 683                   | 57                       | total           | 
| 8.32227236527741   | PRESERVED_SPECIMEN | Bolivia                          | Magnoliopsida     | 15068                 | 1254                     | total           | 
| 8.30769230769231   | HUMAN_OBSERVATION  | Poland                           | Aves              | 650                   | 54                       | non-commercial  | 
| 8.22784810126582   | PRESERVED_SPECIMEN | United Kingdom                   | Liliopsida        | 2212                  | 182                      | non-commercial  | 
| 8.20690651639936   | PRESERVED_SPECIMEN | Madagascar                       | Insecta           | 6921                  | 568                      | total           | 
| 8.2063305978898    | PRESERVED_SPECIMEN | Japan                            | Liliopsida        | 2559                  | 210                      | non-commercial  | 
| 8.2063305978898    | PRESERVED_SPECIMEN | Japan                            | Liliopsida        | 2559                  | 210                      | open commercial | 
| 8.19775706839362   | PRESERVED_SPECIMEN | Chile                            | Magnoliopsida     | 6331                  | 519                      | non-commercial  | 
| 8.18330605564648   | HUMAN_OBSERVATION  | Trinidad & Tobago                | Aves              | 611                   | 50                       | total           | 
| 8.18330605564648   | HUMAN_OBSERVATION  | Trinidad & Tobago                | Aves              | 611                   | 50                       | non-commercial  | 
| 8.17776309268131   | HUMAN_OBSERVATION  | Australia                        | Liliopsida        | 6053                  | 495                      | total           | 
| 8.09298321136461   | PRESERVED_SPECIMEN | Canada                           | Agaricomycetes    | 4646                  | 376                      | total           | 
| 8.07566387777374   | HUMAN_OBSERVATION  | Taiwan                           | Magnoliopsida     | 5498                  | 444                      | non-commercial  | 
| 8.07566387777374   | HUMAN_OBSERVATION  | Taiwan                           | Magnoliopsida     | 5498                  | 444                      | total           | 
| 8.06067554458065   | PRESERVED_SPECIMEN | Argentina                        | Magnoliopsida     | 11339                 | 914                      | total           | 
| 8.04661487236404   | HUMAN_OBSERVATION  | Fiji                             | Actinopterygii    | 1802                  | 145                      | total           | 
| 8.02603036876356   | PRESERVED_SPECIMEN | Venezuela                        | Sordariomycetes   | 461                   | 37                       | open commercial | 
| 8.02603036876356   | PRESERVED_SPECIMEN | Venezuela                        | Sordariomycetes   | 461                   | 37                       | non-commercial  | 
| 8.02603036876356   | PRESERVED_SPECIMEN | Venezuela                        | Sordariomycetes   | 461                   | 37                       | total           | 
| 8.01152737752161   | HUMAN_OBSERVATION  | Italy                            | Liliopsida        | 1735                  | 139                      | total           | 
| 8                  | PRESERVED_SPECIMEN | Peru                             | Reptilia          | 525                   | 42                       | non-commercial  | 
| 7.91788856304985   | PRESERVED_SPECIMEN | Réunion                          | Polypodiopsida    | 341                   | 27                       | open commercial | 
| 7.91788856304985   | PRESERVED_SPECIMEN | Réunion                          | Polypodiopsida    | 341                   | 27                       | non-commercial  | 
| 7.91322568716874   | PRESERVED_SPECIMEN | Philippines                      | Magnoliopsida     | 8113                  | 642                      | total           | 
| 7.90645879732739   | PRESERVED_SPECIMEN | Nigeria                          | Actinopterygii    | 898                   | 71                       | open commercial | 
| 7.90645879732739   | PRESERVED_SPECIMEN | Nigeria                          | Actinopterygii    | 898                   | 71                       | total           | 
| 7.90645879732739   | PRESERVED_SPECIMEN | Nigeria                          | Actinopterygii    | 898                   | 71                       | non-commercial  | 
| 7.90629575402635   | PRESERVED_SPECIMEN | Réunion                          | Bryopsida         | 683                   | 54                       | non-commercial  | 
| 7.90629575402635   | PRESERVED_SPECIMEN | Réunion                          | Bryopsida         | 683                   | 54                       | open commercial | 
| 7.89625360230548   | HUMAN_OBSERVATION  | Italy                            | Liliopsida        | 1735                  | 137                      | non-commercial  | 
| 7.89473684210526   | PRESERVED_SPECIMEN | Madagascar                       | Mammalia          | 266                   | 21                       | total           | 
| 7.89049919484702   | PRESERVED_SPECIMEN | New Caledonia                    | Bryopsida         | 621                   | 49                       | open commercial | 
| 7.89049919484702   | PRESERVED_SPECIMEN | New Caledonia                    | Bryopsida         | 621                   | 49                       | non-commercial  | 
| 7.89049919484702   | PRESERVED_SPECIMEN | New Caledonia                    | Bryopsida         | 621                   | 49                       | total           | 
| 7.85907859078591   | HUMAN_OBSERVATION  | Panama                           | Reptilia          | 369                   | 29                       | non-commercial  | 
| 7.85907859078591   | HUMAN_OBSERVATION  | Panama                           | Reptilia          | 369                   | 29                       | total           | 
| 7.85854616895874   | HUMAN_OBSERVATION  | Sri Lanka                        | Aves              | 509                   | 40                       | total           | 
| 7.85123966942149   | PRESERVED_SPECIMEN | Norway                           | Arachnida         | 968                   | 76                       | total           | 
| 7.78364116094987   | PRESERVED_SPECIMEN | United States                    | Cyanophyceae      | 758                   | 59                       | total           | 
| 7.76859504132231   | PRESERVED_SPECIMEN | Nigeria                          | Liliopsida        | 1210                  | 94                       | total           | 
| 7.76315789473684   | PRESERVED_SPECIMEN | Australia                        | Mammalia          | 760                   | 59                       | total           | 
| 7.71929824561404   | PRESERVED_SPECIMEN | Tajikistan                       | Liliopsida        | 570                   | 44                       | total           | 
| 7.71573604060914   | PRESERVED_SPECIMEN | Belarus                          | Magnoliopsida     | 985                   | 76                       | non-commercial  | 
| 7.71573604060914   | PRESERVED_SPECIMEN | Belarus                          | Magnoliopsida     | 985                   | 76                       | total           | 
| 7.71573604060914   | PRESERVED_SPECIMEN | Belarus                          | Magnoliopsida     | 985                   | 76                       | open commercial | 
| 7.65815760266371   | HUMAN_OBSERVATION  | Fiji                             | Actinopterygii    | 1802                  | 138                      | non-commercial  | 
| 7.65606595995289   | HUMAN_OBSERVATION  | Norway                           | Leotiomycetes     | 849                   | 65                       | total           | 
| 7.65418502202643   | HUMAN_OBSERVATION  | Germany                          | Magnoliopsida     | 10896                 | 834                      | total           | 
| 7.60719225449516   | PRESERVED_SPECIMEN | Panama                           | Magnoliopsida     | 7953                  | 605                      | total           | 
| 7.60517799352751   | PRESERVED_SPECIMEN | Sri Lanka                        | Bryopsida         | 618                   | 47                       | open commercial | 
| 7.60517799352751   | PRESERVED_SPECIMEN | Sri Lanka                        | Bryopsida         | 618                   | 47                       | non-commercial  | 
| 7.60517799352751   | PRESERVED_SPECIMEN | Sri Lanka                        | Bryopsida         | 618                   | 47                       | total           | 
| 7.59259259259259   | PRESERVED_SPECIMEN | Northern Mariana Islands         | Magnoliopsida     | 540                   | 41                       | total           | 
| 7.55043227665706   | PRESERVED_SPECIMEN | Italy                            | Liliopsida        | 1735                  | 131                      | total           | 
| 7.54716981132075   | PRESERVED_SPECIMEN | New Caledonia                    | Hydrozoa          | 318                   | 24                       | open commercial | 
| 7.54716981132075   | PRESERVED_SPECIMEN | New Caledonia                    | Hydrozoa          | 318                   | 24                       | non-commercial  | 
| 7.54716981132075   | PRESERVED_SPECIMEN | New Caledonia                    | Hydrozoa          | 318                   | 24                       | total           | 
| 7.53424657534247   | HUMAN_OBSERVATION  | New Zealand                      | Pinopsida         | 292                   | 22                       | open commercial | 
| 7.51219512195122   | PRESERVED_SPECIMEN | Iran                             | Liliopsida        | 1025                  | 77                       | non-commercial  | 
| 7.51211997643967   | HUMAN_OBSERVATION  | Australia                        | Magnoliopsida     | 22071                 | 1658                     | total           | 
| 7.49124400051887   | PRESERVED_SPECIMEN | Norway                           | Insecta           | 15418                 | 1155                     | total           | 
| 7.49118074289272   | PRESERVED_SPECIMEN | Morocco                          | Magnoliopsida     | 4819                  | 361                      | total           | 
| 7.46887966804979   | PRESERVED_SPECIMEN | United Kingdom                   | Hexanauplia       | 964                   | 72                       | total           | 
| 7.46887966804979   | PRESERVED_SPECIMEN | United Kingdom                   | Hexanauplia       | 964                   | 72                       | non-commercial  | 
| 7.46887966804979   | PRESERVED_SPECIMEN | United Kingdom                   | Hexanauplia       | 964                   | 72                       | open commercial | 
| 7.42857142857143   | HUMAN_OBSERVATION  | Norway                           | Sordariomycetes   | 700                   | 52                       | total           | 
| 7.40740740740741   | PRESERVED_SPECIMEN | New Caledonia                    | Insecta           | 1026                  | 76                       | total           | 
| 7.40421868273784   | PRESERVED_SPECIMEN | Canada                           | Agaricomycetes    | 4646                  | 344                      | non-commercial  | 
| 7.3943661971831    | PRESERVED_SPECIMEN | New Caledonia                    | Demospongiae      | 284                   | 21                       | total           | 
| 7.37051792828685   | PRESERVED_SPECIMEN | United Arab Emirates             | Insecta           | 502                   | 37                       | total           | 
| 7.3512252042007    | PRESERVED_SPECIMEN | United Kingdom                   | Rhynchonellata    | 857                   | 63                       | open commercial | 
| 7.3512252042007    | PRESERVED_SPECIMEN | United Kingdom                   | Rhynchonellata    | 857                   | 63                       | non-commercial  | 
| 7.3512252042007    | PRESERVED_SPECIMEN | United Kingdom                   | Rhynchonellata    | 857                   | 63                       | total           | 
| 7.34612839179351   | PRESERVED_SPECIMEN | Portugal                         | Magnoliopsida     | 4533                  | 333                      | total           | 
| 7.33695652173913   | PRESERVED_SPECIMEN | Palau                            | Magnoliopsida     | 736                   | 54                       | total           | 
| 7.31382978723404   | PRESERVED_SPECIMEN | Colombia                         | Bryopsida         | 1504                  | 110                      | non-commercial  | 
| 7.31382978723404   | PRESERVED_SPECIMEN | Colombia                         | Bryopsida         | 1504                  | 110                      | open commercial | 
| 7.31382978723404   | PRESERVED_SPECIMEN | Colombia                         | Bryopsida         | 1504                  | 110                      | total           | 
| 7.30543318649045   | HUMAN_OBSERVATION  | Germany                          | Magnoliopsida     | 10896                 | 796                      | non-commercial  | 
| 7.2967032967033    | PRESERVED_SPECIMEN | Tajikistan                       | Magnoliopsida     | 2275                  | 166                      | open commercial | 
| 7.2967032967033    | PRESERVED_SPECIMEN | Tajikistan                       | Magnoliopsida     | 2275                  | 166                      | non-commercial  | 
| 7.2967032967033    | PRESERVED_SPECIMEN | Tajikistan                       | Magnoliopsida     | 2275                  | 166                      | total           | 
| 7.29492798998121   | PRESERVED_SPECIMEN | Ireland                          | Insecta           | 3194                  | 233                      | total           | 
| 7.28712416800551   | PRESERVED_SPECIMEN | Costa Rica                       | Magnoliopsida     | 8714                  | 635                      | total           | 
| 7.26915520628684   | HUMAN_OBSERVATION  | Serbia                           | Aves              | 509                   | 37                       | non-commercial  | 
| 7.26915520628684   | HUMAN_OBSERVATION  | Serbia                           | Aves              | 509                   | 37                       | total           | 
| 7.2632944228275    | PRESERVED_SPECIMEN | Greenland                        | Lecanoromycetes   | 771                   | 56                       | total           | 
| 7.25590955806783   | HUMAN_OBSERVATION  | United States                    | Lecanoromycetes   | 4865                  | 353                      | total           | 
| 7.24233983286908   | PRESERVED_SPECIMEN | Norway                           | Jungermanniopsida | 359                   | 26                       | total           | 
| 7.24233983286908   | PRESERVED_SPECIMEN | St. Vincent & Grenadines         | Insecta           | 359                   | 26                       | total           | 
| 7.23905723905724   | PRESERVED_SPECIMEN | Canada                           | Florideophyceae   | 594                   | 43                       | open commercial | 
| 7.23905723905724   | PRESERVED_SPECIMEN | Canada                           | Florideophyceae   | 594                   | 43                       | non-commercial  | 
| 7.23905723905724   | PRESERVED_SPECIMEN | Canada                           | Florideophyceae   | 594                   | 43                       | total           | 
| 7.22543352601156   | HUMAN_OBSERVATION  | Uzbekistan                       | Aves              | 346                   | 25                       | non-commercial  | 
| 7.22543352601156   | HUMAN_OBSERVATION  | Uzbekistan                       | Aves              | 346                   | 25                       | total           | 
| 7.22049689440994   | HUMAN_OBSERVATION  | Panama                           | Aves              | 1288                  | 93                       | total           | 
| 7.2108843537415    | PRESERVED_SPECIMEN | Thailand                         | Polypodiopsida    | 735                   | 53                       | total           | 
| 7.17683838521136   | PRESERVED_SPECIMEN | Australia                        | Magnoliopsida     | 22071                 | 1584                     | total           | 
| 7.17368961973279   | HUMAN_OBSERVATION  | United States                    | Lecanoromycetes   | 4865                  | 349                      | non-commercial  | 
| 7.15883668903803   | HUMAN_OBSERVATION  | Malaysia                         | Reptilia          | 447                   | 32                       | non-commercial  | 
| 7.15883668903803   | HUMAN_OBSERVATION  | Malaysia                         | Reptilia          | 447                   | 32                       | total           | 
| 7.14285714285714   | PRESERVED_SPECIMEN | Norway                           | Sordariomycetes   | 700                   | 50                       | total           | 
| 7.13838447088291   | PRESERVED_SPECIMEN | Ireland                          | Insecta           | 3194                  | 228                      | non-commercial  | 
| 7.13838447088291   | PRESERVED_SPECIMEN | Ireland                          | Insecta           | 3194                  | 228                      | open commercial | 
| 7.13678844519966   | PRESERVED_SPECIMEN | Fiji                             | Insecta           | 1177                  | 84                       | total           | 
| 7.1301247771836    | HUMAN_OBSERVATION  | United States                    | Asteroidea        | 561                   | 40                       | non-commercial  | 
| 7.10703894013496   | HUMAN_OBSERVATION  | Australia                        | Insecta           | 32306                 | 2296                     | total           | 
| 7.08812260536398   | HUMAN_OBSERVATION  | Romania                          | Aves              | 522                   | 37                       | total           | 
| 7.08812260536398   | HUMAN_OBSERVATION  | Romania                          | Aves              | 522                   | 37                       | non-commercial  | 
| 7.07692307692308   | PRESERVED_SPECIMEN | United States                    | Lycopodiopsida    | 325                   | 23                       | open commercial | 
| 7.04323570432357   | PRESERVED_SPECIMEN | Chile                            | Bryopsida         | 1434                  | 101                      | total           | 
| 7.02179176755448   | HUMAN_OBSERVATION  | Australia                        | Asteroidea        | 413                   | 29                       | total           | 
| 7.01107011070111   | HUMAN_OBSERVATION  | Canada                           | Actinopterygii    | 1626                  | 114                      | non-commercial  | 
| 7.01107011070111   | HUMAN_OBSERVATION  | Canada                           | Actinopterygii    | 1626                  | 114                      | total           | 
| 6.97674418604651   | HUMAN_OBSERVATION  | Indonesia                        | Amphibia          | 387                   | 27                       | non-commercial  | 
| 6.97674418604651   | HUMAN_OBSERVATION  | Indonesia                        | Amphibia          | 387                   | 27                       | total           | 
| 6.97368421052632   | PRESERVED_SPECIMEN | Australia                        | Mammalia          | 760                   | 53                       | non-commercial  | 
| 6.97350069735007   | PRESERVED_SPECIMEN | Chile                            | Bryopsida         | 1434                  | 100                      | open commercial | 
| 6.97350069735007   | PRESERVED_SPECIMEN | Chile                            | Bryopsida         | 1434                  | 100                      | non-commercial  | 
| 6.96378830083566   | PRESERVED_SPECIMEN | St. Vincent & Grenadines         | Insecta           | 359                   | 25                       | non-commercial  | 
| 6.95652173913043   | PRESERVED_SPECIMEN | Germany                          | Pucciniomycetes   | 690                   | 48                       | non-commercial  | 
| 6.95652173913043   | PRESERVED_SPECIMEN | Germany                          | Pucciniomycetes   | 690                   | 48                       | total           | 
| 6.92913385826772   | PRESERVED_SPECIMEN | Guam                             | Magnoliopsida     | 635                   | 44                       | total           | 
| 6.92640692640693   | PRESERVED_SPECIMEN | Vanuatu                          | Liliopsida        | 462                   | 32                       | open commercial | 
| 6.92640692640693   | PRESERVED_SPECIMEN | Vanuatu                          | Liliopsida        | 462                   | 32                       | total           | 
| 6.92640692640693   | PRESERVED_SPECIMEN | Vanuatu                          | Liliopsida        | 462                   | 32                       | non-commercial  | 
| 6.91927512355848   | PRESERVED_SPECIMEN | Ecuador                          | Amphibia          | 607                   | 42                       | non-commercial  | 
| 6.91927512355848   | PRESERVED_SPECIMEN | Ecuador                          | Amphibia          | 607                   | 42                       | total           | 
| 6.91344583560152   | PRESERVED_SPECIMEN | United States                    | Mammalia          | 5511                  | 381                      | total           | 
| 6.90196078431372   | PRESERVED_SPECIMEN | U.S. Virgin Islands              | Magnoliopsida     | 1275                  | 88                       | non-commercial  | 
| 6.89102564102564   | PRESERVED_SPECIMEN | Uzbekistan                       | Liliopsida        | 624                   | 43                       | total           | 
| 6.88524590163934   | HUMAN_OBSERVATION  | United States                    | Ascidiacea        | 305                   | 21                       | total           | 
| 6.87876182287188   | HUMAN_OBSERVATION  | New Zealand                      | Actinopterygii    | 1163                  | 80                       | non-commercial  | 
| 6.87876182287188   | HUMAN_OBSERVATION  | New Zealand                      | Actinopterygii    | 1163                  | 80                       | total           | 
| 6.87865022712524   | HUMAN_OBSERVATION  | Kenya                            | Aves              | 1541                  | 106                      | total           | 
| 6.87830687830688   | PRESERVED_SPECIMEN | United Kingdom                   | Polypodiopsida    | 378                   | 26                       | total           | 
| 6.875              | PRESERVED_SPECIMEN | Samoa                            | Polypodiopsida    | 320                   | 22                       | non-commercial  | 
| 6.875              | PRESERVED_SPECIMEN | Samoa                            | Polypodiopsida    | 320                   | 22                       | open commercial | 
| 6.8649885583524    | HUMAN_OBSERVATION  | Norway                           | Gastropoda        | 874                   | 60                       | total           | 
| 6.86274509803922   | HUMAN_OBSERVATION  | North Korea                      | Aves              | 306                   | 21                       | total           | 
| 6.86274509803922   | HUMAN_OBSERVATION  | North Korea                      | Aves              | 306                   | 21                       | non-commercial  | 
| 6.85840707964602   | PRESERVED_SPECIMEN | Congo - Kinshasa                 | Polypodiopsida    | 452                   | 31                       | total           | 
| 6.85714285714286   | HUMAN_OBSERVATION  | Honduras                         | Reptilia          | 350                   | 24                       | non-commercial  | 
| 6.85714285714286   | HUMAN_OBSERVATION  | Honduras                         | Reptilia          | 350                   | 24                       | total           | 
| 6.83229813664596   | HUMAN_OBSERVATION  | Panama                           | Aves              | 1288                  | 88                       | non-commercial  | 
| 6.82936429836646   | PRESERVED_SPECIMEN | Peru                             | Magnoliopsida     | 20324                 | 1388                     | non-commercial  | 
| 6.82730923694779   | PRESERVED_SPECIMEN | Colombia                         | Reptilia          | 747                   | 51                       | total           | 
| 6.82618907809747   | HUMAN_OBSERVATION  | New Zealand                      | Magnoliopsida     | 6812                  | 465                      | open commercial | 
| 6.82352941176471   | PRESERVED_SPECIMEN | U.S. Virgin Islands              | Magnoliopsida     | 1275                  | 87                       | open commercial | 
| 6.80997960144359   | HUMAN_OBSERVATION  | Mexico                           | Liliopsida        | 6373                  | 434                      | total           | 
| 6.78336980306346   | PRESERVED_SPECIMEN | Cuba                             | Insecta           | 2285                  | 155                      | total           | 
| 6.77966101694915   | PRESERVED_SPECIMEN | Australia                        | Asteroidea        | 413                   | 28                       | non-commercial  | 
| 6.77966101694915   | PRESERVED_SPECIMEN | Australia                        | Asteroidea        | 413                   | 28                       | total           | 
| 6.77312775330396   | PRESERVED_SPECIMEN | Germany                          | Magnoliopsida     | 10896                 | 738                      | total           | 
| 6.76862870377765   | HUMAN_OBSERVATION  | Canada                           | Insecta           | 25042                 | 1695                     | total           | 
| 6.76068950078352   | PRESERVED_SPECIMEN | India                            | Liliopsida        | 4467                  | 302                      | total           | 
| 6.74886437378326   | HUMAN_OBSERVATION  | Kenya                            | Aves              | 1541                  | 104                      | non-commercial  | 
| 6.74721481249019   | HUMAN_OBSERVATION  | Mexico                           | Liliopsida        | 6373                  | 430                      | non-commercial  | 
| 6.74250258531541   | PRESERVED_SPECIMEN | China                            | Magnoliopsida     | 24175                 | 1630                     | total           | 
| 6.73963133640553   | HUMAN_OBSERVATION  | China                            | Aves              | 1736                  | 117                      | total           | 
| 6.72047182989291   | PRESERVED_SPECIMEN | Iran                             | Magnoliopsida     | 6443                  | 433                      | total           | 
| 6.71256454388985   | PRESERVED_SPECIMEN | Sudan                            | Actinopterygii    | 581                   | 39                       | non-commercial  | 
| 6.71256454388985   | PRESERVED_SPECIMEN | Sudan                            | Actinopterygii    | 581                   | 39                       | total           | 
| 6.71052631578947   | PRESERVED_SPECIMEN | Australia                        | Mammalia          | 760                   | 51                       | open commercial | 
| 6.68016194331984   | PRESERVED_SPECIMEN | France                           | Polypodiopsida    | 494                   | 33                       | non-commercial  | 
| 6.68016194331984   | PRESERVED_SPECIMEN | France                           | Polypodiopsida    | 494                   | 33                       | open commercial | 
| 6.67447306791569   | PRESERVED_SPECIMEN | Algeria                          | Liliopsida        | 854                   | 57                       | open commercial | 
| 6.67447306791569   | PRESERVED_SPECIMEN | Algeria                          | Liliopsida        | 854                   | 57                       | non-commercial  | 
| 6.67447306791569   | PRESERVED_SPECIMEN | Algeria                          | Liliopsida        | 854                   | 57                       | total           | 
| 6.67038794306447   | PRESERVED_SPECIMEN | Armenia                          | Magnoliopsida     | 3583                  | 239                      | total           | 
| 6.66666666666667   | HUMAN_OBSERVATION  | Australia                        | Demospongiae      | 1140                  | 76                       | total           | 
| 6.64739884393064   | PRESERVED_SPECIMEN | Sweden                           | Polypodiopsida    | 346                   | 23                       | total           | 
| 6.64084338311636   | HUMAN_OBSERVATION  | Canada                           | Insecta           | 25042                 | 1663                     | non-commercial  | 
| 6.60899653979239   | PRESERVED_SPECIMEN | Guinea                           | Magnoliopsida     | 2890                  | 191                      | total           | 
| 6.57419448056639   | PRESERVED_SPECIMEN | Madagascar                       | Insecta           | 6921                  | 455                      | non-commercial  | 
| 6.57327586206897   | PRESERVED_SPECIMEN | Finland                          | Liliopsida        | 928                   | 61                       | total           | 
| 6.56167979002625   | PRESERVED_SPECIMEN | Guadeloupe                       | Polypodiopsida    | 381                   | 25                       | open commercial | 
| 6.56167979002625   | PRESERVED_SPECIMEN | Guadeloupe                       | Polypodiopsida    | 381                   | 25                       | non-commercial  | 
| 6.51870246779451   | PRESERVED_SPECIMEN | Iran                             | Magnoliopsida     | 6443                  | 420                      | non-commercial  | 
| 6.51465798045603   | PRESERVED_SPECIMEN | Jamaica                          | Liliopsida        | 1535                  | 100                      | total           | 
| 6.5                | PRESERVED_SPECIMEN | Brazil                           | Florideophyceae   | 600                   | 39                       | open commercial | 
| 6.5                | PRESERVED_SPECIMEN | Brazil                           | Florideophyceae   | 600                   | 39                       | non-commercial  | 
| 6.49819494584837   | HUMAN_OBSERVATION  | New Zealand                      | Bivalvia          | 1108                  | 72                       | non-commercial  | 
| 6.49819494584837   | HUMAN_OBSERVATION  | New Zealand                      | Bivalvia          | 1108                  | 72                       | total           | 
| 6.45161290322581   | PRESERVED_SPECIMEN | Cuba                             | Bryopsida         | 527                   | 34                       | total           | 
| 6.45161290322581   | PRESERVED_SPECIMEN | Cuba                             | Bryopsida         | 527                   | 34                       | open commercial | 
| 6.45161290322581   | PRESERVED_SPECIMEN | Cuba                             | Bryopsida         | 527                   | 34                       | non-commercial  | 
| 6.44567219152855   | HUMAN_OBSERVATION  | Czechia                          | Aves              | 543                   | 35                       | total           | 
| 6.44567219152855   | HUMAN_OBSERVATION  | Czechia                          | Aves              | 543                   | 35                       | non-commercial  | 
| 6.44171779141104   | PRESERVED_SPECIMEN | Belarus                          | Liliopsida        | 326                   | 21                       | open commercial | 
| 6.44171779141104   | PRESERVED_SPECIMEN | Belarus                          | Liliopsida        | 326                   | 21                       | non-commercial  | 
| 6.44171779141104   | PRESERVED_SPECIMEN | Belarus                          | Liliopsida        | 326                   | 21                       | total           | 
| 6.43356643356643   | HUMAN_OBSERVATION  | Norway                           | Aves              | 715                   | 46                       | non-commercial  | 
| 6.42939150401837   | HUMAN_OBSERVATION  | Indonesia                        | Reptilia          | 871                   | 56                       | non-commercial  | 
| 6.42939150401837   | HUMAN_OBSERVATION  | Indonesia                        | Reptilia          | 871                   | 56                       | total           | 
| 6.42711613261715   | PRESERVED_SPECIMEN | Jamaica                          | Magnoliopsida     | 5399                  | 347                      | total           | 
| 6.42570281124498   | PRESERVED_SPECIMEN | Kenya                            | Mammalia          | 747                   | 48                       | total           | 
| 6.42504118616145   | PRESERVED_SPECIMEN | Germany                          | Polypodiopsida    | 607                   | 39                       | total           | 
| 6.42115203021719   | PRESERVED_SPECIMEN | Angola                           | Aves              | 1059                  | 68                       | total           | 
| 6.41956438670233   | PRESERVED_SPECIMEN | China                            | Liliopsida        | 5234                  | 336                      | total           | 
| 6.41200545702592   | HUMAN_OBSERVATION  | Israel                           | Liliopsida        | 733                   | 47                       | total           | 
| 6.41200545702592   | HUMAN_OBSERVATION  | Israel                           | Liliopsida        | 733                   | 47                       | non-commercial  | 
| 6.40569395017794   | HUMAN_OBSERVATION  | United Arab Emirates             | Aves              | 562                   | 36                       | non-commercial  | 
| 6.40569395017794   | HUMAN_OBSERVATION  | United Arab Emirates             | Aves              | 562                   | 36                       | total           | 
| 6.40394088669951   | HUMAN_OBSERVATION  | Ireland                          | Aves              | 609                   | 39                       | total           | 
| 6.40394088669951   | HUMAN_OBSERVATION  | Ireland                          | Aves              | 609                   | 39                       | non-commercial  | 
| 6.4                | HUMAN_OBSERVATION  | Italy                            | Aves              | 625                   | 40                       | open commercial | 
| 6.3992359121299    | PRESERVED_SPECIMEN | United States                    | Eurotiomycetes    | 1047                  | 67                       | non-commercial  | 
| 6.39129221322914   | PRESERVED_SPECIMEN | Armenia                          | Magnoliopsida     | 3583                  | 229                      | non-commercial  | 
| 6.37755102040816   | HUMAN_OBSERVATION  | United States                    | Polypodiopsida    | 1568                  | 100                      | open commercial | 
| 6.37362637362637   | PRESERVED_SPECIMEN | Sweden                           | Liliopsida        | 4550                  | 290                      | total           | 
| 6.36942675159236   | PRESERVED_SPECIMEN | Myanmar (Burma)                  | Liliopsida        | 1727                  | 110                      | total           | 
| 6.32672332389046   | PRESERVED_SPECIMEN | Angola                           | Aves              | 1059                  | 67                       | open commercial | 
| 6.32672332389046   | PRESERVED_SPECIMEN | Angola                           | Aves              | 1059                  | 67                       | non-commercial  | 
| 6.29439947133653   | PRESERVED_SPECIMEN | Australia                        | Liliopsida        | 6053                  | 381                      | total           | 
| 6.29183400267738   | PRESERVED_SPECIMEN | Colombia                         | Reptilia          | 747                   | 47                       | non-commercial  | 
| 6.26398210290828   | PRESERVED_SPECIMEN | Malaysia                         | Reptilia          | 447                   | 28                       | total           | 
| 6.20689655172414   | HUMAN_OBSERVATION  | Denmark                          | Gastropoda        | 580                   | 36                       | total           | 
| 6.17960877296977   | PRESERVED_SPECIMEN | Guatemala                        | Magnoliopsida     | 6748                  | 417                      | total           | 
| 6.17027588252744   | HUMAN_OBSERVATION  | New Zealand                      | Gastropoda        | 3371                  | 208                      | total           | 
| 6.1624649859944    | HUMAN_OBSERVATION  | Caribbean Netherlands            | Actinopterygii    | 357                   | 22                       | total           | 
| 6.16016427104723   | PRESERVED_SPECIMEN | Madagascar                       | Reptilia          | 487                   | 30                       | total           | 
| 6.14754098360656   | PRESERVED_SPECIMEN | Ethiopia                         | Liliopsida        | 1464                  | 90                       | total           | 
| 6.14583333333333   | PRESERVED_SPECIMEN | Morocco                          | Agaricomycetes    | 960                   | 59                       | non-commercial  | 
| 6.14583333333333   | PRESERVED_SPECIMEN | Morocco                          | Agaricomycetes    | 960                   | 59                       | total           | 
| 6.14583333333333   | PRESERVED_SPECIMEN | Morocco                          | Agaricomycetes    | 960                   | 59                       | open commercial | 
| 6.14432989690722   | HUMAN_OBSERVATION  | Canada                           | Lecanoromycetes   | 2425                  | 149                      | total           | 
| 6.1437908496732    | PRESERVED_SPECIMEN | Indonesia                        | Mammalia          | 765                   | 47                       | total           | 
| 6.13496932515337   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Actinopterygii    | 489                   | 30                       | non-commercial  | 
| 6.13496932515337   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Actinopterygii    | 489                   | 30                       | total           | 
| 6.1284046692607    | PRESERVED_SPECIMEN | France                           | Aves              | 1028                  | 63                       | open commercial | 
| 6.1284046692607    | PRESERVED_SPECIMEN | France                           | Aves              | 1028                  | 63                       | non-commercial  | 
| 6.12377850162866   | PRESERVED_SPECIMEN | Jamaica                          | Liliopsida        | 1535                  | 94                       | non-commercial  | 
| 6.1121964833938    | PRESERVED_SPECIMEN | Armenia                          | Magnoliopsida     | 3583                  | 219                      | open commercial | 
| 6.11111111111111   | PRESERVED_SPECIMEN | Micronesia (Federated States of) | Liliopsida        | 360                   | 22                       | total           | 
| 6.11094630673391   | HUMAN_OBSERVATION  | New Zealand                      | Gastropoda        | 3371                  | 206                      | non-commercial  | 
| 6.10978520286396   | HUMAN_OBSERVATION  | Burkina Faso                     | Magnoliopsida     | 2095                  | 128                      | total           | 
| 6.09318996415771   | HUMAN_OBSERVATION  | United States                    | Myxomycetes       | 558                   | 34                       | total           | 
| 6.08262683353519   | PRESERVED_SPECIMEN | Malaysia                         | Insecta           | 7431                  | 452                      | total           | 
| 6.08108108108108   | PRESERVED_SPECIMEN | Norway                           | Lecanoromycetes   | 1924                  | 117                      | total           | 
| 6.07734806629834   | PRESERVED_SPECIMEN | Australia                        | Reptilia          | 1267                  | 77                       | total           | 
| 6.06741573033708   | PRESERVED_SPECIMEN | Bahamas                          | Insecta           | 445                   | 27                       | total           | 
| 6.06617647058824   | PRESERVED_SPECIMEN | Greenland                        | Bryopsida         | 544                   | 33                       | total           | 
| 6.02409638554217   | HUMAN_OBSERVATION  | Colombia                         | Reptilia          | 747                   | 45                       | non-commercial  | 
| 6.02409638554217   | HUMAN_OBSERVATION  | Colombia                         | Reptilia          | 747                   | 45                       | total           | 
| 6.02150537634409   | PRESERVED_SPECIMEN | French Polynesia                 | Liliopsida        | 465                   | 28                       | non-commercial  | 
| 6.02150537634409   | PRESERVED_SPECIMEN | French Polynesia                 | Liliopsida        | 465                   | 28                       | open commercial | 
| 6.02061855670103   | HUMAN_OBSERVATION  | Canada                           | Lecanoromycetes   | 2425                  | 146                      | non-commercial  | 
| 6.01719197707736   | PRESERVED_SPECIMEN | Madagascar                       | Aves              | 349                   | 21                       | non-commercial  | 
| 6.01092896174863   | PRESERVED_SPECIMEN | Ethiopia                         | Liliopsida        | 1464                  | 88                       | non-commercial  | 
| 6.00375234521576   | PRESERVED_SPECIMEN | Ecuador                          | Reptilia          | 533                   | 32                       | open commercial | 
| 6.00113765642776   | PRESERVED_SPECIMEN | Japan                            | Magnoliopsida     | 7032                  | 422                      | total           | 
| 5.98861396978323   | PRESERVED_SPECIMEN | Canada                           | Magnoliopsida     | 9134                  | 547                      | open commercial | 
| 5.98802395209581   | HUMAN_OBSERVATION  | New Zealand                      | Anthozoa          | 501                   | 30                       | total           | 
| 5.96491228070175   | PRESERVED_SPECIMEN | Venezuela                        | Agaricomycetes    | 570                   | 34                       | open commercial | 
| 5.96491228070175   | PRESERVED_SPECIMEN | Venezuela                        | Agaricomycetes    | 570                   | 34                       | total           | 
| 5.96491228070175   | PRESERVED_SPECIMEN | Venezuela                        | Agaricomycetes    | 570                   | 34                       | non-commercial  | 
| 5.96426694692591   | PRESERVED_SPECIMEN | Algeria                          | Magnoliopsida     | 3806                  | 227                      | total           | 
| 5.95804449277332   | PRESERVED_SPECIMEN | Australia                        | Magnoliopsida     | 22071                 | 1315                     | non-commercial  | 
| 5.95375722543353   | HUMAN_OBSERVATION  | South Africa                     | Arachnida         | 1730                  | 103                      | total           | 
| 5.95375722543353   | HUMAN_OBSERVATION  | South Africa                     | Arachnida         | 1730                  | 103                      | non-commercial  | 
| 5.94493116395494   | PRESERVED_SPECIMEN | Chile                            | Liliopsida        | 1598                  | 95                       | total           | 
| 5.94262295081967   | PRESERVED_SPECIMEN | Ethiopia                         | Liliopsida        | 1464                  | 87                       | open commercial | 
| 5.9331797235023    | HUMAN_OBSERVATION  | China                            | Aves              | 1736                  | 103                      | non-commercial  | 
| 5.91949486977111   | PRESERVED_SPECIMEN | Australia                        | Reptilia          | 1267                  | 75                       | non-commercial  | 
| 5.91397849462366   | HUMAN_OBSERVATION  | United States                    | Myxomycetes       | 558                   | 33                       | non-commercial  | 
| 5.90339892665474   | PRESERVED_SPECIMEN | Seychelles                       | Magnoliopsida     | 559                   | 33                       | total           | 
| 5.88055130168453   | PRESERVED_SPECIMEN | Haiti                            | Magnoliopsida     | 3265                  | 192                      | total           | 
| 5.87467362924282   | PRESERVED_SPECIMEN | Equatorial Guinea                | Liliopsida        | 766                   | 45                       | total           | 
| 5.87012987012987   | PRESERVED_SPECIMEN | Guadeloupe                       | Magnoliopsida     | 1925                  | 113                      | total           | 
| 5.83289542827115   | PRESERVED_SPECIMEN | Algeria                          | Magnoliopsida     | 3806                  | 222                      | non-commercial  | 
| 5.8287795992714    | HUMAN_OBSERVATION  | Israel                           | Magnoliopsida     | 2745                  | 160                      | total           | 
| 5.8287795992714    | HUMAN_OBSERVATION  | Israel                           | Magnoliopsida     | 2745                  | 160                      | non-commercial  | 
| 5.82726326742976   | PRESERVED_SPECIMEN | Morocco                          | Liliopsida        | 961                   | 56                       | total           | 
| 5.82010582010582   | HUMAN_OBSERVATION  | Malaysia                         | Mammalia          | 378                   | 22                       | total           | 
| 5.82010582010582   | HUMAN_OBSERVATION  | Malaysia                         | Mammalia          | 378                   | 22                       | non-commercial  | 
| 5.79807477053951   | PRESERVED_SPECIMEN | India                            | Liliopsida        | 4467                  | 259                      | non-commercial  | 
| 5.79804560260586   | PRESERVED_SPECIMEN | Jamaica                          | Liliopsida        | 1535                  | 89                       | open commercial | 
| 5.78842315369261   | HUMAN_OBSERVATION  | New Zealand                      | Anthozoa          | 501                   | 29                       | non-commercial  | 
| 5.78703703703704   | PRESERVED_SPECIMEN | Greenland                        | Magnoliopsida     | 432                   | 25                       | non-commercial  | 
| 5.78532742491384   | PRESERVED_SPECIMEN | Chile                            | Insecta           | 4062                  | 235                      | total           | 
| 5.78034682080925   | HUMAN_OBSERVATION  | St. Kitts & Nevis                | Magnoliopsida     | 519                   | 30                       | non-commercial  | 
| 5.78034682080925   | HUMAN_OBSERVATION  | St. Kitts & Nevis                | Magnoliopsida     | 519                   | 30                       | total           | 
| 5.77868852459016   | HUMAN_OBSERVATION  | Peru                             | Aves              | 2440                  | 141                      | total           | 
| 5.7540725170783    | PRESERVED_SPECIMEN | Algeria                          | Magnoliopsida     | 3806                  | 219                      | open commercial | 
| 5.70934256055363   | PRESERVED_SPECIMEN | Tanzania                         | Mammalia          | 578                   | 33                       | open commercial | 
| 5.69965306459607   | PRESERVED_SPECIMEN | Australia                        | Liliopsida        | 6053                  | 345                      | non-commercial  | 
| 5.67066521264995   | PRESERVED_SPECIMEN | Solomon Islands                  | Insecta           | 917                   | 52                       | total           | 
| 5.65371024734982   | PRESERVED_SPECIMEN | Norway                           | Leotiomycetes     | 849                   | 48                       | total           | 
| 5.6390977443609    | HUMAN_OBSERVATION  | United Kingdom                   | Mammalia          | 532                   | 30                       | total           | 
| 5.6390977443609    | PRESERVED_SPECIMEN | Sri Lanka                        | Polypodiopsida    | 532                   | 30                       | total           | 
| 5.62851782363977   | HUMAN_OBSERVATION  | Ecuador                          | Reptilia          | 533                   | 30                       | non-commercial  | 
| 5.62851782363977   | HUMAN_OBSERVATION  | Ecuador                          | Reptilia          | 533                   | 30                       | total           | 
| 5.625              | HUMAN_OBSERVATION  | Congo - Brazzaville              | Magnoliopsida     | 3360                  | 189                      | total           | 
| 5.625              | PRESERVED_SPECIMEN | Vanuatu                          | Magnoliopsida     | 1120                  | 63                       | total           | 
| 5.62248995983936   | PRESERVED_SPECIMEN | Kenya                            | Mammalia          | 747                   | 42                       | non-commercial  | 
| 5.60747663551402   | PRESERVED_SPECIMEN | Fiji                             | Insecta           | 1177                  | 66                       | non-commercial  | 
| 5.59857057772484   | PRESERVED_SPECIMEN | Italy                            | Lecanoromycetes   | 1679                  | 94                       | total           | 
| 5.59491371480472   | PRESERVED_SPECIMEN | Kenya                            | Magnoliopsida     | 5505                  | 308                      | total           | 
| 5.570375019614     | PRESERVED_SPECIMEN | Mexico                           | Liliopsida        | 6373                  | 355                      | non-commercial  | 
| 5.56213017751479   | PRESERVED_SPECIMEN | Germany                          | Leotiomycetes     | 1690                  | 94                       | non-commercial  | 
| 5.56213017751479   | PRESERVED_SPECIMEN | Germany                          | Leotiomycetes     | 1690                  | 94                       | total           | 
| 5.56107249255213   | PRESERVED_SPECIMEN | Switzerland                      | Liliopsida        | 1007                  | 56                       | total           | 
| 5.55253130103429   | PRESERVED_SPECIMEN | Fiji                             | Magnoliopsida     | 1837                  | 102                      | total           | 
| 5.54414784394251   | PRESERVED_SPECIMEN | Madagascar                       | Reptilia          | 487                   | 27                       | non-commercial  | 
| 5.52995391705069   | HUMAN_OBSERVATION  | Brazil                           | Mammalia          | 868                   | 48                       | total           | 
| 5.52995391705069   | HUMAN_OBSERVATION  | Brazil                           | Mammalia          | 868                   | 48                       | non-commercial  | 
| 5.52879100711172   | PRESERVED_SPECIMEN | Malaysia                         | Liliopsida        | 4359                  | 241                      | total           | 
| 5.52763819095477   | PRESERVED_SPECIMEN | Thailand                         | Mammalia          | 398                   | 22                       | total           | 
| 5.52593310712555   | PRESERVED_SPECIMEN | Guyana                           | Liliopsida        | 2063                  | 114                      | total           | 
| 5.51147330045035   | PRESERVED_SPECIMEN | Nicaragua                        | Magnoliopsida     | 4663                  | 257                      | total           | 
| 5.49428909019299   | PRESERVED_SPECIMEN | Ethiopia                         | Magnoliopsida     | 5078                  | 279                      | total           | 
| 5.47945205479452   | PRESERVED_SPECIMEN | Italy                            | Lecanoromycetes   | 1679                  | 92                       | non-commercial  | 
| 5.4519368723099    | HUMAN_OBSERVATION  | Mexico                           | Polypodiopsida    | 1394                  | 76                       | non-commercial  | 
| 5.4519368723099    | HUMAN_OBSERVATION  | Mexico                           | Polypodiopsida    | 1394                  | 76                       | total           | 
| 5.44871794871795   | PRESERVED_SPECIMEN | Uzbekistan                       | Liliopsida        | 624                   | 34                       | non-commercial  | 
| 5.44871794871795   | PRESERVED_SPECIMEN | Uzbekistan                       | Liliopsida        | 624                   | 34                       | open commercial | 
| 5.44692737430168   | PRESERVED_SPECIMEN | Dominica                         | Magnoliopsida     | 1432                  | 78                       | total           | 
| 5.4380664652568    | HUMAN_OBSERVATION  | Austria                          | Aves              | 662                   | 36                       | non-commercial  | 
| 5.4380664652568    | HUMAN_OBSERVATION  | Austria                          | Aves              | 662                   | 36                       | total           | 
| 5.4375             | PRESERVED_SPECIMEN | Kenya                            | Liliopsida        | 1600                  | 87                       | total           | 
| 5.41736053288926   | PRESERVED_SPECIMEN | South Africa                     | Magnoliopsida     | 19216                 | 1041                     | total           | 
| 5.41082164328657   | PRESERVED_SPECIMEN | Brazil                           | Amphibia          | 998                   | 54                       | non-commercial  | 
| 5.40865384615385   | PRESERVED_SPECIMEN | Colombia                         | Amphibia          | 832                   | 45                       | total           | 
| 5.37848605577689   | PRESERVED_SPECIMEN | Uganda                           | Mammalia          | 502                   | 27                       | total           | 
| 5.37613233556518   | PRESERVED_SPECIMEN | Ethiopia                         | Magnoliopsida     | 5078                  | 273                      | non-commercial  | 
| 5.374763804325     | PRESERVED_SPECIMEN | Kenya                            | Insecta           | 4763                  | 256                      | total           | 
| 5.37273337810611   | PRESERVED_SPECIMEN | India                            | Liliopsida        | 4467                  | 240                      | open commercial | 
| 5.37136506760511   | PRESERVED_SPECIMEN | Jamaica                          | Magnoliopsida     | 5399                  | 290                      | non-commercial  | 
| 5.36912751677852   | PRESERVED_SPECIMEN | Malaysia                         | Reptilia          | 447                   | 24                       | non-commercial  | 
| 5.35399788657978   | HUMAN_OBSERVATION  | Australia                        | Agaricomycetes    | 2839                  | 152                      | non-commercial  | 
| 5.35279805352798   | PRESERVED_SPECIMEN | Solomon Islands                  | Polypodiopsida    | 411                   | 22                       | non-commercial  | 
| 5.35279805352798   | PRESERVED_SPECIMEN | Solomon Islands                  | Polypodiopsida    | 411                   | 22                       | total           | 
| 5.35279805352798   | PRESERVED_SPECIMEN | Solomon Islands                  | Polypodiopsida    | 411                   | 22                       | open commercial | 
| 5.32243415077203   | PRESERVED_SPECIMEN | Kenya                            | Magnoliopsida     | 5505                  | 293                      | non-commercial  | 
| 5.32232163340216   | PRESERVED_SPECIMEN | Malaysia                         | Liliopsida        | 4359                  | 232                      | non-commercial  | 
| 5.31665363565285   | PRESERVED_SPECIMEN | United Kingdom                   | Aves              | 1279                  | 68                       | total           | 
| 5.31377228695774   | HUMAN_OBSERVATION  | Mexico                           | Insecta           | 28492                 | 1514                     | total           | 
| 5.3133514986376    | HUMAN_OBSERVATION  | Australia                        | Polypodiopsida    | 734                   | 39                       | non-commercial  | 
| 5.31238309016087   | PRESERVED_SPECIMEN | Tanzania                         | Liliopsida        | 2673                  | 142                      | total           | 
| 5.30426884650318   | PRESERVED_SPECIMEN | Kenya                            | Magnoliopsida     | 5505                  | 292                      | open commercial | 
| 5.29736116581331   | PRESERVED_SPECIMEN | Ethiopia                         | Magnoliopsida     | 5078                  | 269                      | open commercial | 
| 5.28935905413815   | HUMAN_OBSERVATION  | Switzerland                      | Magnoliopsida     | 4821                  | 255                      | total           | 
| 5.27027027027027   | PRESERVED_SPECIMEN | India                            | Reptilia          | 740                   | 39                       | total           | 
| 5.26861646961211   | HUMAN_OBSERVATION  | Switzerland                      | Magnoliopsida     | 4821                  | 254                      | non-commercial  | 
| 5.26315789473684   | HUMAN_OBSERVATION  | United Kingdom                   | Mammalia          | 532                   | 28                       | non-commercial  | 
| 5.25761617296083   | HUMAN_OBSERVATION  | Mexico                           | Insecta           | 28492                 | 1498                     | non-commercial  | 
| 5.22889542209156   | HUMAN_OBSERVATION  | United States                    | Liliopsida        | 9524                  | 498                      | open commercial | 
| 5.22322498203019   | PRESERVED_SPECIMEN | Canada                           | Insecta           | 25042                 | 1308                     | total           | 
| 5.21609538002981   | PRESERVED_SPECIMEN | Cape Verde                       | Magnoliopsida     | 671                   | 35                       | total           | 
| 5.2094522019334    | HUMAN_OBSERVATION  | New Zealand                      | Liliopsida        | 1862                  | 97                       | open commercial | 
| 5.20231213872832   | PRESERVED_SPECIMEN | NA                               | Phaeophyceae      | 519                   | 27                       | non-commercial  | 
| 5.20231213872832   | PRESERVED_SPECIMEN | NA                               | Phaeophyceae      | 519                   | 27                       | total           | 
| 5.20231213872832   | PRESERVED_SPECIMEN | NA                               | Phaeophyceae      | 519                   | 27                       | open commercial | 
| 5.2003410059676    | PRESERVED_SPECIMEN | New Zealand                      | Bryopsida         | 1173                  | 61                       | total           | 
| 5.2003410059676    | PRESERVED_SPECIMEN | New Zealand                      | Bryopsida         | 1173                  | 61                       | open commercial | 
| 5.2003410059676    | PRESERVED_SPECIMEN | New Zealand                      | Bryopsida         | 1173                  | 61                       | non-commercial  | 
| 5.19480519480519   | PRESERVED_SPECIMEN | Norway                           | Pezizomycetes     | 462                   | 24                       | total           | 
| 5.18783542039356   | PRESERVED_SPECIMEN | United States                    | Elasmobranchii    | 559                   | 29                       | total           | 
| 5.18763796909492   | PRESERVED_SPECIMEN | Paraguay                         | Insecta           | 2718                  | 141                      | total           | 
| 5.1875             | PRESERVED_SPECIMEN | Kenya                            | Liliopsida        | 1600                  | 83                       | open commercial | 
| 5.1875             | PRESERVED_SPECIMEN | Kenya                            | Liliopsida        | 1600                  | 83                       | non-commercial  | 
| 5.18099851971471   | PRESERVED_SPECIMEN | Malaysia                         | Insecta           | 7431                  | 385                      | non-commercial  | 
| 5.18084066471163   | PRESERVED_SPECIMEN | Vietnam                          | Aves              | 1023                  | 53                       | total           | 
| 5.18018018018018   | PRESERVED_SPECIMEN | Canada                           | Pucciniomycetes   | 444                   | 23                       | open commercial | 
| 5.18018018018018   | PRESERVED_SPECIMEN | Canada                           | Pucciniomycetes   | 444                   | 23                       | non-commercial  | 
| 5.18018018018018   | PRESERVED_SPECIMEN | Canada                           | Pucciniomycetes   | 444                   | 23                       | total           | 
| 5.16129032258065   | HUMAN_OBSERVATION  | Malawi                           | Aves              | 775                   | 40                       | total           | 
| 5.13182674199623   | PRESERVED_SPECIMEN | Paraguay                         | Magnoliopsida     | 6372                  | 327                      | non-commercial  | 
| 5.12295081967213   | HUMAN_OBSERVATION  | Peru                             | Aves              | 2440                  | 125                      | non-commercial  | 
| 5.11811023622047   | PRESERVED_SPECIMEN | Belize                           | Insecta           | 1270                  | 65                       | total           | 
| 5.11205778847935   | PRESERVED_SPECIMEN | Jamaica                          | Magnoliopsida     | 5399                  | 276                      | open commercial | 
| 5.10805500982318   | HUMAN_OBSERVATION  | Sri Lanka                        | Aves              | 509                   | 26                       | non-commercial  | 
| 5.10440835266821   | PRESERVED_SPECIMEN | South Africa                     | Polypodiopsida    | 431                   | 22                       | open commercial | 
| 5.10440835266821   | PRESERVED_SPECIMEN | South Africa                     | Polypodiopsida    | 431                   | 22                       | non-commercial  | 
| 5.10267579340386   | PRESERVED_SPECIMEN | South Africa                     | Lecanoromycetes   | 1607                  | 82                       | total           | 
| 5.08115737473536   | PRESERVED_SPECIMEN | Indonesia                        | Bryopsida         | 1417                  | 72                       | open commercial | 
| 5.08115737473536   | PRESERVED_SPECIMEN | Indonesia                        | Bryopsida         | 1417                  | 72                       | non-commercial  | 
| 5.08115737473536   | PRESERVED_SPECIMEN | Indonesia                        | Bryopsida         | 1417                  | 72                       | total           | 
| 5.07246376811594   | PRESERVED_SPECIMEN | China                            | Amphibia          | 414                   | 21                       | total           | 
| 5.0682261208577    | PRESERVED_SPECIMEN | New Caledonia                    | Insecta           | 1026                  | 52                       | non-commercial  | 
| 5.05050505050505   | PRESERVED_SPECIMEN | Tanzania                         | Liliopsida        | 2673                  | 135                      | non-commercial  | 
| 5.03731343283582   | PRESERVED_SPECIMEN | New Zealand                      | Aves              | 536                   | 27                       | non-commercial  | 
| 5.03731343283582   | PRESERVED_SPECIMEN | Haiti                            | Polypodiopsida    | 536                   | 27                       | non-commercial  | 
| 5.03731343283582   | PRESERVED_SPECIMEN | Haiti                            | Polypodiopsida    | 536                   | 27                       | open commercial | 
| 5.03225806451613   | HUMAN_OBSERVATION  | Malawi                           | Aves              | 775                   | 39                       | non-commercial  | 
| 5.02283105022831   | HUMAN_OBSERVATION  | Spain                            | Mammalia          | 657                   | 33                       | total           | 
| 5.01437240498243   | PRESERVED_SPECIMEN | Papua New Guinea                 | Gastropoda        | 3131                  | 157                      | total           | 
| 5.01216545012165   | PRESERVED_SPECIMEN | Senegal                          | Magnoliopsida     | 2055                  | 103                      | total           | 
| 5.01216545012165   | PRESERVED_SPECIMEN | Senegal                          | Magnoliopsida     | 2055                  | 103                      | open commercial | 
| 5.01216545012165   | PRESERVED_SPECIMEN | Senegal                          | Magnoliopsida     | 2055                  | 103                      | non-commercial  | 
| 5                  | PRESERVED_SPECIMEN | Vanuatu                          | Magnoliopsida     | 1120                  | 56                       | non-commercial  | 
| 5                  | PRESERVED_SPECIMEN | Vanuatu                          | Magnoliopsida     | 1120                  | 56                       | open commercial | 
| 5                  | HUMAN_OBSERVATION  | Denmark                          | Gastropoda        | 580                   | 29                       | non-commercial  | 
| 4.99139414802065   | PRESERVED_SPECIMEN | Sudan                            | Actinopterygii    | 581                   | 29                       | open commercial | 
| 4.98188405797101   | HUMAN_OBSERVATION  | United States                    | Diplopoda         | 1104                  | 55                       | total           | 
| 4.98177399756987   | HUMAN_OBSERVATION  | Denmark                          | Liliopsida        | 823                   | 41                       | total           | 
| 4.9800796812749    | PRESERVED_SPECIMEN | Uganda                           | Mammalia          | 502                   | 25                       | non-commercial  | 
| 4.96644295302013   | PRESERVED_SPECIMEN | Sudan                            | Insecta           | 745                   | 37                       | total           | 
| 4.94841421474971   | PRESERVED_SPECIMEN | China                            | Liliopsida        | 5234                  | 259                      | non-commercial  | 
| 4.93760173629951   | PRESERVED_SPECIMEN | Canada                           | Bryopsida         | 1843                  | 91                       | non-commercial  | 
| 4.93421052631579   | PRESERVED_SPECIMEN | Antarctica                       | Polychaeta        | 608                   | 30                       | total           | 
| 4.93147332354381   | PRESERVED_SPECIMEN | Panama                           | Insecta           | 8172                  | 403                      | total           | 
| 4.9302204251989    | HUMAN_OBSERVATION  | United Kingdom                   | Magnoliopsida     | 7667                  | 378                      | non-commercial  | 
| 4.9302204251989    | HUMAN_OBSERVATION  | United Kingdom                   | Magnoliopsida     | 7667                  | 378                      | total           | 
| 4.93012422360249   | HUMAN_OBSERVATION  | Mexico                           | Arachnida         | 2576                  | 127                      | total           | 
| 4.89208633093525   | PRESERVED_SPECIMEN | United States                    | Lecanoromycetes   | 4865                  | 238                      | open commercial | 
| 4.89130434782609   | HUMAN_OBSERVATION  | United States                    | Diplopoda         | 1104                  | 54                       | non-commercial  | 
| 4.87012987012987   | HUMAN_OBSERVATION  | Finland                          | Aves              | 616                   | 30                       | total           | 
| 4.87012987012987   | HUMAN_OBSERVATION  | Finland                          | Aves              | 616                   | 30                       | non-commercial  | 
| 4.86503452605147   | PRESERVED_SPECIMEN | Paraguay                         | Magnoliopsida     | 6372                  | 310                      | open commercial | 
| 4.85467901628873   | PRESERVED_SPECIMEN | Guyana                           | Magnoliopsida     | 6262                  | 304                      | non-commercial  | 
| 4.85248447204969   | HUMAN_OBSERVATION  | Mexico                           | Arachnida         | 2576                  | 125                      | non-commercial  | 
| 4.85074626865672   | PRESERVED_SPECIMEN | New Zealand                      | Aves              | 536                   | 26                       | open commercial | 
| 4.83870967741935   | PRESERVED_SPECIMEN | United States                    | Myxomycetes       | 558                   | 27                       | total           | 
| 4.8372513562387    | PRESERVED_SPECIMEN | United Kingdom                   | Liliopsida        | 2212                  | 107                      | open commercial | 
| 4.82410491257286   | PRESERVED_SPECIMEN | South Africa                     | Magnoliopsida     | 19216                 | 927                      | non-commercial  | 
| 4.81563570421116   | HUMAN_OBSERVATION  | Australia                        | Arachnida         | 4963                  | 239                      | total           | 
| 4.80824270177447   | HUMAN_OBSERVATION  | Botswana                         | Insecta           | 1747                  | 84                       | non-commercial  | 
| 4.80824270177447   | HUMAN_OBSERVATION  | Botswana                         | Insecta           | 1747                  | 84                       | total           | 
| 4.80693459416864   | PRESERVED_SPECIMEN | Uzbekistan                       | Magnoliopsida     | 2538                  | 122                      | total           | 
| 4.7970479704797    | PRESERVED_SPECIMEN | Tajikistan                       | Insecta           | 813                   | 39                       | total           | 
| 4.78581515769653   | PRESERVED_SPECIMEN | Mexico                           | Liliopsida        | 6373                  | 305                      | open commercial | 
| 4.78011472275335   | HUMAN_OBSERVATION  | Ecuador                          | Mammalia          | 523                   | 25                       | non-commercial  | 
| 4.78011472275335   | HUMAN_OBSERVATION  | Ecuador                          | Mammalia          | 523                   | 25                       | total           | 
| 4.77741585233442   | PRESERVED_SPECIMEN | United Kingdom                   | Polychaeta        | 921                   | 44                       | open commercial | 
| 4.77741585233442   | PRESERVED_SPECIMEN | United Kingdom                   | Polychaeta        | 921                   | 44                       | non-commercial  | 
| 4.77741585233442   | PRESERVED_SPECIMEN | United Kingdom                   | Polychaeta        | 921                   | 44                       | total           | 
| 4.77657935285054   | PRESERVED_SPECIMEN | Jamaica                          | Insecta           | 1298                  | 62                       | total           | 
| 4.77453580901857   | PRESERVED_SPECIMEN | United States                    | Hexanauplia       | 1885                  | 90                       | total           | 
| 4.75524475524475   | PRESERVED_SPECIMEN | Isle of Man                      | Insecta           | 715                   | 34                       | non-commercial  | 
| 4.75524475524475   | PRESERVED_SPECIMEN | Isle of Man                      | Insecta           | 715                   | 34                       | total           | 
| 4.75524475524475   | PRESERVED_SPECIMEN | Isle of Man                      | Insecta           | 715                   | 34                       | open commercial | 
| 4.7449055481184    | PRESERVED_SPECIMEN | United States                    | Actinopterygii    | 6723                  | 319                      | total           | 
| 4.73738414006179   | PRESERVED_SPECIMEN | Guinea                           | Liliopsida        | 971                   | 46                       | non-commercial  | 
| 4.73738414006179   | PRESERVED_SPECIMEN | Guinea                           | Liliopsida        | 971                   | 46                       | open commercial | 
| 4.73684210526316   | HUMAN_OBSERVATION  | Australia                        | Mammalia          | 760                   | 36                       | open commercial | 
| 4.72854640980736   | HUMAN_OBSERVATION  | Portugal                         | Liliopsida        | 1142                  | 54                       | total           | 
| 4.72103004291846   | PRESERVED_SPECIMEN | Singapore                        | Insecta           | 1631                  | 77                       | total           | 
| 4.70941883767535   | PRESERVED_SPECIMEN | Brazil                           | Amphibia          | 998                   | 47                       | open commercial | 
| 4.70907297830375   | PRESERVED_SPECIMEN | Argentina                        | Insecta           | 8112                  | 382                      | total           | 
| 4.68959186015377   | PRESERVED_SPECIMEN | Mexico                           | Magnoliopsida     | 26143                 | 1226                     | non-commercial  | 
| 4.67532467532468   | PRESERVED_SPECIMEN | Guadeloupe                       | Magnoliopsida     | 1925                  | 90                       | non-commercial  | 
| 4.67532467532468   | PRESERVED_SPECIMEN | Guadeloupe                       | Magnoliopsida     | 1925                  | 90                       | open commercial | 
| 4.6740467404674    | PRESERVED_SPECIMEN | Tajikistan                       | Insecta           | 813                   | 38                       | non-commercial  | 
| 4.67120181405896   | PRESERVED_SPECIMEN | Algeria                          | Insecta           | 2205                  | 103                      | total           | 
| 4.66439135381115   | HUMAN_OBSERVATION  | Italy                            | Actinopterygii    | 879                   | 41                       | non-commercial  | 
| 4.66439135381115   | HUMAN_OBSERVATION  | Italy                            | Actinopterygii    | 879                   | 41                       | total           | 
| 4.66167275428713   | PRESERVED_SPECIMEN | Australia                        | Insecta           | 32306                 | 1506                     | total           | 
| 4.64135021097046   | PRESERVED_SPECIMEN | Thailand                         | Reptilia          | 474                   | 22                       | total           | 
| 4.62415970666123   | PRESERVED_SPECIMEN | India                            | Insecta           | 9818                  | 454                      | total           | 
| 4.62295658287924   | PRESERVED_SPECIMEN | United States                    | Insecta           | 85335                 | 3945                     | non-commercial  | 
| 4.61811722912966   | HUMAN_OBSERVATION  | Estonia                          | Aves              | 563                   | 26                       | open commercial | 
| 4.57516339869281   | HUMAN_OBSERVATION  | Germany                          | Liliopsida        | 2448                  | 112                      | total           | 
| 4.57442819647544   | PRESERVED_SPECIMEN | Philippines                      | Liliopsida        | 2667                  | 122                      | total           | 
| 4.57052797478329   | PRESERVED_SPECIMEN | Uzbekistan                       | Magnoliopsida     | 2538                  | 116                      | open commercial | 
| 4.57052797478329   | PRESERVED_SPECIMEN | Uzbekistan                       | Magnoliopsida     | 2538                  | 116                      | non-commercial  | 
| 4.55089820359281   | PRESERVED_SPECIMEN | Ireland                          | Malacostraca      | 835                   | 38                       | non-commercial  | 
| 4.55089820359281   | PRESERVED_SPECIMEN | Ireland                          | Malacostraca      | 835                   | 38                       | total           | 
| 4.55089820359281   | PRESERVED_SPECIMEN | Ireland                          | Malacostraca      | 835                   | 38                       | open commercial | 
| 4.54545454545455   | PRESERVED_SPECIMEN | Tanzania                         | Reptilia          | 484                   | 22                       | total           | 
| 4.53125            | PRESERVED_SPECIMEN | Colombia                         | Aves              | 2560                  | 116                      | total           | 
| 4.5302636464909    | PRESERVED_SPECIMEN | United Kingdom                   | Gastropoda        | 2693                  | 122                      | total           | 
| 4.5302636464909    | PRESERVED_SPECIMEN | United Kingdom                   | Gastropoda        | 2693                  | 122                      | non-commercial  | 
| 4.52796200769672   | PRESERVED_SPECIMEN | Indonesia                        | Insecta           | 12213                 | 553                      | total           | 
| 4.52747710241465   | PRESERVED_SPECIMEN | South Africa                     | Magnoliopsida     | 19216                 | 870                      | open commercial | 
| 4.52296819787986   | PRESERVED_SPECIMEN | Egypt                            | Insecta           | 1415                  | 64                       | total           | 
| 4.51158940397351   | PRESERVED_SPECIMEN | Cambodia                         | Magnoliopsida     | 2416                  | 109                      | total           | 
| 4.50932964754665   | PRESERVED_SPECIMEN | Peru                             | Liliopsida        | 5788                  | 261                      | total           | 
| 4.50885668276973   | PRESERVED_SPECIMEN | Greece                           | Liliopsida        | 1242                  | 56                       | total           | 
| 4.50563204005006   | PRESERVED_SPECIMEN | Chile                            | Liliopsida        | 1598                  | 72                       | non-commercial  | 
| 4.49567723342939   | PRESERVED_SPECIMEN | Italy                            | Liliopsida        | 1735                  | 78                       | non-commercial  | 
| 4.49313033791311   | PRESERVED_SPECIMEN | United Kingdom                   | Gastropoda        | 2693                  | 121                      | open commercial | 
| 4.48987390141383   | PRESERVED_SPECIMEN | China                            | Liliopsida        | 5234                  | 235                      | open commercial | 
| 4.45621001544231   | HUMAN_OBSERVATION  | Portugal                         | Magnoliopsida     | 4533                  | 202                      | total           | 
| 4.4529262086514    | HUMAN_OBSERVATION  | Belgium                          | Aves              | 786                   | 35                       | total           | 
| 4.4519266741489    | PRESERVED_SPECIMEN | Tanzania                         | Liliopsida        | 2673                  | 119                      | open commercial | 
| 4.45029713668287   | PRESERVED_SPECIMEN | Ecuador                          | Magnoliopsida     | 14808                 | 659                      | non-commercial  | 
| 4.44697833523375   | PRESERVED_SPECIMEN | Mexico                           | Florideophyceae   | 877                   | 39                       | total           | 
| 4.44101048105348   | PRESERVED_SPECIMEN | India                            | Magnoliopsida     | 14884                 | 661                      | total           | 
| 4.43947620568508   | PRESERVED_SPECIMEN | Papua New Guinea                 | Gastropoda        | 3131                  | 139                      | non-commercial  | 
| 4.43947620568508   | PRESERVED_SPECIMEN | Papua New Guinea                 | Gastropoda        | 3131                  | 139                      | open commercial | 
| 4.43548387096774   | PRESERVED_SPECIMEN | Iran                             | Insecta           | 2976                  | 132                      | total           | 
| 4.43108439100423   | PRESERVED_SPECIMEN | Venezuela                        | Liliopsida        | 4491                  | 199                      | total           | 
| 4.42953020134228   | PRESERVED_SPECIMEN | Sudan                            | Insecta           | 745                   | 33                       | non-commercial  | 
| 4.42834138486312   | PRESERVED_SPECIMEN | Greece                           | Liliopsida        | 1242                  | 55                       | non-commercial  | 
| 4.41778697001034   | PRESERVED_SPECIMEN | China                            | Magnoliopsida     | 24175                 | 1068                     | non-commercial  | 
| 4.41558441558442   | HUMAN_OBSERVATION  | India                            | Mammalia          | 770                   | 34                       | total           | 
| 4.40944881889764   | PRESERVED_SPECIMEN | Belize                           | Insecta           | 1270                  | 56                       | non-commercial  | 
| 4.40467997247075   | PRESERVED_SPECIMEN | Malaysia                         | Liliopsida        | 4359                  | 192                      | open commercial | 
| 4.40097799511002   | PRESERVED_SPECIMEN | Congo - Kinshasa                 | Actinopterygii    | 1636                  | 72                       | total           | 
| 4.39844760672704   | HUMAN_OBSERVATION  | New Zealand                      | Agaricomycetes    | 2319                  | 102                      | open commercial | 
| 4.38862710646115   | PRESERVED_SPECIMEN | Canada                           | Insecta           | 25042                 | 1099                     | non-commercial  | 
| 4.38741721854305   | PRESERVED_SPECIMEN | Cambodia                         | Magnoliopsida     | 2416                  | 106                      | open commercial | 
| 4.38741721854305   | PRESERVED_SPECIMEN | Cambodia                         | Magnoliopsida     | 2416                  | 106                      | non-commercial  | 
| 4.3755988502076    | PRESERVED_SPECIMEN | Guyana                           | Magnoliopsida     | 6262                  | 274                      | open commercial | 
| 4.36864153201676   | HUMAN_OBSERVATION  | United States                    | Malacostraca      | 6684                  | 292                      | total           | 
| 4.36619718309859   | HUMAN_OBSERVATION  | United States                    | Echinoidea        | 710                   | 31                       | total           | 
| 4.36005625879044   | PRESERVED_SPECIMEN | Armenia                          | Liliopsida        | 711                   | 31                       | total           | 
| 4.34782608695652   | HUMAN_OBSERVATION  | Belarus                          | Aves              | 506                   | 22                       | total           | 
| 4.34782608695652   | HUMAN_OBSERVATION  | Belarus                          | Aves              | 506                   | 22                       | non-commercial  | 
| 4.33369447453954   | PRESERVED_SPECIMEN | Panama                           | Liliopsida        | 3692                  | 160                      | total           | 
| 4.33212996389892   | HUMAN_OBSERVATION  | Canada                           | Arachnida         | 1662                  | 72                       | total           | 
| 4.32989690721649   | HUMAN_OBSERVATION  | Australia                        | Cephalopoda       | 485                   | 21                       | total           | 
| 4.2719614921781    | HUMAN_OBSERVATION  | Canada                           | Arachnida         | 1662                  | 71                       | non-commercial  | 
| 4.2620363062352    | PRESERVED_SPECIMEN | Australia                        | Reptilia          | 1267                  | 54                       | open commercial | 
| 4.25531914893617   | PRESERVED_SPECIMEN | Moldova                          | Magnoliopsida     | 940                   | 40                       | total           | 
| 4.25531914893617   | PRESERVED_SPECIMEN | Moldova                          | Magnoliopsida     | 940                   | 40                       | non-commercial  | 
| 4.21052631578947   | PRESERVED_SPECIMEN | Tajikistan                       | Liliopsida        | 570                   | 24                       | open commercial | 
| 4.21052631578947   | PRESERVED_SPECIMEN | Tajikistan                       | Liliopsida        | 570                   | 24                       | non-commercial  | 
| 4.20609884332282   | PRESERVED_SPECIMEN | Mexico                           | Mammalia          | 951                   | 40                       | total           | 
| 4.18897409926205   | PRESERVED_SPECIMEN | Venezuela                        | Magnoliopsida     | 13822                 | 579                      | non-commercial  | 
| 4.17665183156453   | HUMAN_OBSERVATION  | Madagascar                       | Liliopsida        | 2921                  | 122                      | non-commercial  | 
| 4.17665183156453   | HUMAN_OBSERVATION  | Madagascar                       | Liliopsida        | 2921                  | 122                      | total           | 
| 4.17636587703683   | PRESERVED_SPECIMEN | Italy                            | Magnoliopsida     | 7303                  | 305                      | total           | 
| 4.16922133660331   | PRESERVED_SPECIMEN | Singapore                        | Insecta           | 1631                  | 68                       | non-commercial  | 
| 4.16666666666667   | HUMAN_OBSERVATION  | Germany                          | Liliopsida        | 2448                  | 102                      | non-commercial  | 
| 4.16184971098266   | HUMAN_OBSERVATION  | Iceland                          | Magnoliopsida     | 865                   | 36                       | total           | 
| 4.15929203539823   | HUMAN_OBSERVATION  | Canada                           | Bivalvia          | 1130                  | 47                       | non-commercial  | 
| 4.15929203539823   | HUMAN_OBSERVATION  | Canada                           | Bivalvia          | 1130                  | 47                       | total           | 
| 4.15584415584416   | HUMAN_OBSERVATION  | India                            | Mammalia          | 770                   | 32                       | non-commercial  | 
| 4.14893617021277   | PRESERVED_SPECIMEN | Moldova                          | Magnoliopsida     | 940                   | 39                       | open commercial | 
| 4.14861712762413   | HUMAN_OBSERVATION  | South Korea                      | Insecta           | 6002                  | 249                      | total           | 
| 4.13318025258324   | PRESERVED_SPECIMEN | South Africa                     | Actinopterygii    | 2613                  | 108                      | total           | 
| 4.13318025258324   | HUMAN_OBSERVATION  | South Africa                     | Actinopterygii    | 2613                  | 108                      | total           | 
| 4.13318025258324   | PRESERVED_SPECIMEN | South Africa                     | Actinopterygii    | 2613                  | 108                      | non-commercial  | 
| 4.13195601466178   | HUMAN_OBSERVATION  | South Korea                      | Insecta           | 6002                  | 248                      | non-commercial  | 
| 4.1025641025641    | HUMAN_OBSERVATION  | Serbia                           | Insecta           | 1755                  | 72                       | non-commercial  | 
| 4.1025641025641    | HUMAN_OBSERVATION  | Serbia                           | Insecta           | 1755                  | 72                       | total           | 
| 4.09535452322738   | PRESERVED_SPECIMEN | Congo - Kinshasa                 | Actinopterygii    | 1636                  | 67                       | non-commercial  | 
| 4.09491006505932   | HUMAN_OBSERVATION  | South Africa                     | Actinopterygii    | 2613                  | 107                      | non-commercial  | 
| 4.09457900807382   | PRESERVED_SPECIMEN | Germany                          | Bacillariophyceae | 1734                  | 71                       | non-commercial  | 
| 4.09457900807382   | PRESERVED_SPECIMEN | Germany                          | Bacillariophyceae | 1734                  | 71                       | total           | 
| 4.07673860911271   | PRESERVED_SPECIMEN | Martinique                       | Magnoliopsida     | 1668                  | 68                       | total           | 
| 4.05445840813884   | HUMAN_OBSERVATION  | United States                    | Malacostraca      | 6684                  | 271                      | non-commercial  | 
| 4.05338606030648   | PRESERVED_SPECIMEN | Malaysia                         | Magnoliopsida     | 12138                 | 492                      | total           | 
| 4.04858299595142   | HUMAN_OBSERVATION  | Colombia                         | Mammalia          | 741                   | 30                       | non-commercial  | 
| 4.04858299595142   | HUMAN_OBSERVATION  | Colombia                         | Mammalia          | 741                   | 30                       | total           | 
| 4.04673696209746   | PRESERVED_SPECIMEN | Congo - Kinshasa                 | Insecta           | 3509                  | 142                      | total           | 
| 4.04624277456647   | HUMAN_OBSERVATION  | Iceland                          | Magnoliopsida     | 865                   | 35                       | non-commercial  | 
| 4.04413651526816   | PRESERVED_SPECIMEN | United Kingdom                   | Insecta           | 19485                 | 788                      | total           | 
| 4.04354587869362   | PRESERVED_SPECIMEN | Greece                           | Magnoliopsida     | 5787                  | 234                      | total           | 
| 4.04284727021424   | PRESERVED_SPECIMEN | Peru                             | Liliopsida        | 5788                  | 234                      | non-commercial  | 
| 4.04040404040404   | PRESERVED_SPECIMEN | United States                    | Pezizomycetes     | 693                   | 28                       | non-commercial  | 
| 4.0394973070018    | HUMAN_OBSERVATION  | Australia                        | Insecta           | 32306                 | 1305                     | non-commercial  | 
| 4.03422982885086   | PRESERVED_SPECIMEN | Congo - Kinshasa                 | Actinopterygii    | 1636                  | 66                       | open commercial | 
| 4.02922040862915   | PRESERVED_SPECIMEN | Tanzania                         | Magnoliopsida     | 8761                  | 353                      | total           | 
| 4.02802101576182   | HUMAN_OBSERVATION  | Portugal                         | Liliopsida        | 1142                  | 46                       | non-commercial  | 
| 4.02802101576182   | HUMAN_OBSERVATION  | France                           | Reptilia          | 571                   | 23                       | non-commercial  | 
| 4.02802101576182   | HUMAN_OBSERVATION  | France                           | Reptilia          | 571                   | 23                       | total           | 
| 4.01727861771058   | PRESERVED_SPECIMEN | United States                    | Dothideomycetes   | 4630                  | 186                      | total           | 
| 4.01007768213311   | PRESERVED_SPECIMEN | Kenya                            | Insecta           | 4763                  | 191                      | non-commercial  | 
| 4.00763358778626   | PRESERVED_SPECIMEN | Zambia                           | Actinopterygii    | 524                   | 21                       | non-commercial  | 
| 4.00763358778626   | PRESERVED_SPECIMEN | Zambia                           | Actinopterygii    | 524                   | 21                       | total           | 
| 4.00763358778626   | PRESERVED_SPECIMEN | Zambia                           | Actinopterygii    | 524                   | 21                       | open commercial | 
| 3.99059385090552   | PRESERVED_SPECIMEN | Mexico                           | Insecta           | 28492                 | 1137                     | total           | 
| 3.98959236773634   | PRESERVED_SPECIMEN | Taiwan                           | Polypodiopsida    | 1153                  | 46                       | total           | 
| 3.98698128559805   | PRESERVED_SPECIMEN | Sri Lanka                        | Liliopsida        | 1229                  | 49                       | total           | 
| 3.98249452954048   | PRESERVED_SPECIMEN | Cuba                             | Insecta           | 2285                  | 91                       | non-commercial  | 
| 3.97805212620027   | PRESERVED_SPECIMEN | Burkina Faso                     | Liliopsida        | 729                   | 29                       | total           | 
| 3.97694524495677   | PRESERVED_SPECIMEN | Italy                            | Liliopsida        | 1735                  | 69                       | open commercial | 
| 3.9727582292849    | PRESERVED_SPECIMEN | Norway                           | Liliopsida        | 881                   | 35                       | open commercial | 
| 3.96825396825397   | PRESERVED_SPECIMEN | Réunion                          | Liliopsida        | 630                   | 25                       | non-commercial  | 
| 3.96825396825397   | PRESERVED_SPECIMEN | Réunion                          | Liliopsida        | 630                   | 25                       | open commercial | 
| 3.93811533052039   | PRESERVED_SPECIMEN | Armenia                          | Liliopsida        | 711                   | 28                       | non-commercial  | 
| 3.92927308447937   | PRESERVED_SPECIMEN | Seychelles                       | Gastropoda        | 1018                  | 40                       | open commercial | 
| 3.92927308447937   | PRESERVED_SPECIMEN | Seychelles                       | Gastropoda        | 1018                  | 40                       | non-commercial  | 
| 3.92927308447937   | PRESERVED_SPECIMEN | Seychelles                       | Gastropoda        | 1018                  | 40                       | total           | 
| 3.92749244712991   | PRESERVED_SPECIMEN | Cameroon                         | Actinopterygii    | 993                   | 39                       | total           | 
| 3.92584514721919   | PRESERVED_SPECIMEN | Solomon Islands                  | Insecta           | 917                   | 36                       | non-commercial  | 
| 3.91964723174914   | PRESERVED_SPECIMEN | India                            | Aves              | 2041                  | 80                       | total           | 
| 3.91891891891892   | PRESERVED_SPECIMEN | India                            | Reptilia          | 740                   | 29                       | non-commercial  | 
| 3.91705069124424   | PRESERVED_SPECIMEN | Brazil                           | Mammalia          | 868                   | 34                       | total           | 
| 3.91644908616188   | PRESERVED_SPECIMEN | South Africa                     | Reptilia          | 766                   | 30                       | total           | 
| 3.91600454029512   | HUMAN_OBSERVATION  | New Zealand                      | Lecanoromycetes   | 1762                  | 69                       | total           | 
| 3.90366396530076   | PRESERVED_SPECIMEN | Tanzania                         | Magnoliopsida     | 8761                  | 342                      | non-commercial  | 
| 3.88362209872507   | HUMAN_OBSERVATION  | Italy                            | Insecta           | 15295                 | 594                      | total           | 
| 3.87990762124711   | PRESERVED_SPECIMEN | Yemen                            | Magnoliopsida     | 2165                  | 84                       | non-commercial  | 
| 3.87990762124711   | PRESERVED_SPECIMEN | Yemen                            | Magnoliopsida     | 2165                  | 84                       | total           | 
| 3.87840670859539   | PRESERVED_SPECIMEN | Trinidad & Tobago                | Liliopsida        | 954                   | 37                       | total           | 
| 3.85925085130533   | HUMAN_OBSERVATION  | New Zealand                      | Lecanoromycetes   | 1762                  | 68                       | non-commercial  | 
| 3.8389707408176    | PRESERVED_SPECIMEN | Morocco                          | Magnoliopsida     | 4819                  | 185                      | open commercial | 
| 3.8389707408176    | PRESERVED_SPECIMEN | Morocco                          | Magnoliopsida     | 4819                  | 185                      | non-commercial  | 
| 3.82701875239189   | PRESERVED_SPECIMEN | South Africa                     | Actinopterygii    | 2613                  | 100                      | open commercial | 
| 3.81341881286614   | HUMAN_OBSERVATION  | United States                    | Gastropoda        | 18094                 | 690                      | total           | 
| 3.81231671554252   | PRESERVED_SPECIMEN | Brazil                           | Reptilia          | 1023                  | 39                       | total           | 
| 3.80948234577039   | HUMAN_OBSERVATION  | South Africa                     | Insecta           | 22969                 | 875                      | total           | 
| 3.79746835443038   | PRESERVED_SPECIMEN | Armenia                          | Liliopsida        | 711                   | 27                       | open commercial | 
| 3.79206756933258   | HUMAN_OBSERVATION  | South Africa                     | Insecta           | 22969                 | 871                      | non-commercial  | 
| 3.78640776699029   | PRESERVED_SPECIMEN | Latvia                           | Magnoliopsida     | 1030                  | 39                       | total           | 
| 3.78590078328982   | PRESERVED_SPECIMEN | South Africa                     | Reptilia          | 766                   | 29                       | non-commercial  | 
| 3.78548895899054   | HUMAN_OBSERVATION  | Egypt                            | Actinopterygii    | 1268                  | 48                       | total           | 
| 3.78548895899054   | HUMAN_OBSERVATION  | Egypt                            | Actinopterygii    | 1268                  | 48                       | non-commercial  | 
| 3.74513618677043   | PRESERVED_SPECIMEN | Saudi Arabia                     | Magnoliopsida     | 2056                  | 77                       | non-commercial  | 
| 3.74513618677043   | PRESERVED_SPECIMEN | Saudi Arabia                     | Magnoliopsida     | 2056                  | 77                       | total           | 
| 3.73793665896425   | PRESERVED_SPECIMEN | Australia                        | Magnoliopsida     | 22071                 | 825                      | open commercial | 
| 3.73395565927655   | HUMAN_OBSERVATION  | Israel                           | Insecta           | 1714                  | 64                       | total           | 
| 3.72975842845766   | PRESERVED_SPECIMEN | Bolivia                          | Magnoliopsida     | 15068                 | 562                      | non-commercial  | 
| 3.72883633431873   | PRESERVED_SPECIMEN | India                            | Magnoliopsida     | 14884                 | 555                      | non-commercial  | 
| 3.72881355932203   | HUMAN_OBSERVATION  | Mexico                           | Sordariomycetes   | 590                   | 22                       | total           | 
| 3.72881355932203   | HUMAN_OBSERVATION  | Mexico                           | Sordariomycetes   | 590                   | 22                       | non-commercial  | 
| 3.72670807453416   | HUMAN_OBSERVATION  | Zambia                           | Aves              | 805                   | 30                       | total           | 
| 3.71456500488759   | PRESERVED_SPECIMEN | Brazil                           | Reptilia          | 1023                  | 38                       | non-commercial  | 
| 3.71352785145889   | PRESERVED_SPECIMEN | Solomon Islands                  | Liliopsida        | 754                   | 28                       | total           | 
| 3.71352785145889   | PRESERVED_SPECIMEN | Solomon Islands                  | Liliopsida        | 754                   | 28                       | non-commercial  | 
| 3.70308867485885   | PRESERVED_SPECIMEN | South Africa                     | Liliopsida        | 6022                  | 223                      | total           | 
| 3.7007874015748    | PRESERVED_SPECIMEN | Belize                           | Insecta           | 1270                  | 47                       | open commercial | 
| 3.69794366683947   | PRESERVED_SPECIMEN | Greece                           | Magnoliopsida     | 5787                  | 214                      | non-commercial  | 
| 3.69747899159664   | HUMAN_OBSERVATION  | Indonesia                        | Aves              | 2380                  | 88                       | total           | 
| 3.69389865563599   | PRESERVED_SPECIMEN | China                            | Magnoliopsida     | 24175                 | 893                      | open commercial | 
| 3.69187078452254   | PRESERVED_SPECIMEN | Colombia                         | Liliopsida        | 8451                  | 312                      | total           | 
| 3.68679374500628   | PRESERVED_SPECIMEN | Tanzania                         | Magnoliopsida     | 8761                  | 323                      | open commercial | 
| 3.6826495304004    | PRESERVED_SPECIMEN | Malaysia                         | Magnoliopsida     | 12138                 | 447                      | non-commercial  | 
| 3.67561260210035   | HUMAN_OBSERVATION  | Israel                           | Insecta           | 1714                  | 63                       | non-commercial  | 
| 3.66218236173393   | PRESERVED_SPECIMEN | Gabon                            | Insecta           | 1338                  | 49                       | total           | 
| 3.65296803652968   | HUMAN_OBSERVATION  | Spain                            | Mammalia          | 657                   | 24                       | non-commercial  | 
| 3.64238410596026   | PRESERVED_SPECIMEN | Mexico                           | Jungermanniopsida | 604                   | 22                       | non-commercial  | 
| 3.64238410596026   | PRESERVED_SPECIMEN | Mexico                           | Jungermanniopsida | 604                   | 22                       | open commercial | 
| 3.64238410596026   | PRESERVED_SPECIMEN | Mexico                           | Jungermanniopsida | 604                   | 22                       | total           | 
| 3.63501483679525   | PRESERVED_SPECIMEN | Austria                          | Liliopsida        | 1348                  | 49                       | total           | 
| 3.62776025236593   | PRESERVED_SPECIMEN | Egypt                            | Actinopterygii    | 1268                  | 46                       | total           | 
| 3.62768496420048   | PRESERVED_SPECIMEN | Burkina Faso                     | Magnoliopsida     | 2095                  | 76                       | total           | 
| 3.62095531587057   | PRESERVED_SPECIMEN | Jamaica                          | Insecta           | 1298                  | 47                       | non-commercial  | 
| 3.61881785283474   | PRESERVED_SPECIMEN | Canada                           | Leotiomycetes     | 829                   | 30                       | total           | 
| 3.61881785283474   | PRESERVED_SPECIMEN | Canada                           | Leotiomycetes     | 829                   | 30                       | non-commercial  | 
| 3.61613351877608   | HUMAN_OBSERVATION  | New Zealand                      | Malacostraca      | 1438                  | 52                       | total           | 
| 3.61613351877608   | HUMAN_OBSERVATION  | New Zealand                      | Malacostraca      | 1438                  | 52                       | non-commercial  | 
| 3.61596009975062   | PRESERVED_SPECIMEN | France                           | Bryopsida         | 1604                  | 58                       | non-commercial  | 
| 3.61596009975062   | PRESERVED_SPECIMEN | France                           | Bryopsida         | 1604                  | 58                       | total           | 
| 3.60915492957746   | HUMAN_OBSERVATION  | Mexico                           | Reptilia          | 1136                  | 41                       | open commercial | 
| 3.60750360750361   | PRESERVED_SPECIMEN | United States                    | Pezizomycetes     | 693                   | 25                       | open commercial | 
| 3.60340444346192   | PRESERVED_SPECIMEN | Brazil                           | Insecta           | 27141                 | 978                      | total           | 
| 3.5978835978836    | PRESERVED_SPECIMEN | United Kingdom                   | Cephalopoda       | 945                   | 34                       | open commercial | 
| 3.5978835978836    | PRESERVED_SPECIMEN | United Kingdom                   | Cephalopoda       | 945                   | 34                       | total           | 
| 3.5978835978836    | PRESERVED_SPECIMEN | United Kingdom                   | Cephalopoda       | 945                   | 34                       | non-commercial  | 
| 3.59375            | PRESERVED_SPECIMEN | Colombia                         | Aves              | 2560                  | 92                       | non-commercial  | 
| 3.59223300970874   | PRESERVED_SPECIMEN | Latvia                           | Magnoliopsida     | 1030                  | 37                       | non-commercial  | 
| 3.57379219060225   | HUMAN_OBSERVATION  | Portugal                         | Magnoliopsida     | 4533                  | 162                      | non-commercial  | 
| 3.56652949245542   | PRESERVED_SPECIMEN | Burkina Faso                     | Liliopsida        | 729                   | 26                       | non-commercial  | 
| 3.56652949245542   | PRESERVED_SPECIMEN | Burkina Faso                     | Liliopsida        | 729                   | 26                       | open commercial | 
| 3.56652949245542   | HUMAN_OBSERVATION  | Burkina Faso                     | Liliopsida        | 729                   | 26                       | total           | 
| 3.56138706654171   | PRESERVED_SPECIMEN | Angola                           | Actinopterygii    | 1067                  | 38                       | total           | 
| 3.55902777777778   | PRESERVED_SPECIMEN | Gabon                            | Magnoliopsida     | 4608                  | 164                      | non-commercial  | 
| 3.55476560764275   | PRESERVED_SPECIMEN | Germany                          | Agaricomycetes    | 4501                  | 160                      | total           | 
| 3.55476560764275   | PRESERVED_SPECIMEN | Germany                          | Agaricomycetes    | 4501                  | 160                      | non-commercial  | 
| 3.55195770692219   | PRESERVED_SPECIMEN | Australia                        | Liliopsida        | 6053                  | 215                      | open commercial | 
| 3.55169692186267   | HUMAN_OBSERVATION  | Australia                        | Reptilia          | 1267                  | 45                       | open commercial | 
| 3.53717026378897   | PRESERVED_SPECIMEN | Martinique                       | Magnoliopsida     | 1668                  | 59                       | open commercial | 
| 3.53717026378897   | PRESERVED_SPECIMEN | Martinique                       | Magnoliopsida     | 1668                  | 59                       | non-commercial  | 
| 3.52941176470588   | PRESERVED_SPECIMEN | Antarctica                       | Gastropoda        | 595                   | 21                       | total           | 
| 3.52112676056338   | HUMAN_OBSERVATION  | United States                    | Echinoidea        | 710                   | 25                       | non-commercial  | 
| 3.51906158357771   | PRESERVED_SPECIMEN | Cambodia                         | Liliopsida        | 682                   | 24                       | total           | 
| 3.51906158357771   | PRESERVED_SPECIMEN | Vietnam                          | Aves              | 1023                  | 36                       | non-commercial  | 
| 3.515625           | PRESERVED_SPECIMEN | Gabon                            | Magnoliopsida     | 4608                  | 162                      | open commercial | 
| 3.51351351351351   | PRESERVED_SPECIMEN | Tanzania                         | Actinopterygii    | 1850                  | 65                       | open commercial | 
| 3.51351351351351   | PRESERVED_SPECIMEN | Tanzania                         | Actinopterygii    | 1850                  | 65                       | total           | 
| 3.51351351351351   | PRESERVED_SPECIMEN | Tanzania                         | Actinopterygii    | 1850                  | 65                       | non-commercial  | 
| 3.51157222665603   | PRESERVED_SPECIMEN | United Kingdom                   | Bryopsida         | 1253                  | 44                       | total           | 
| 3.50259451445515   | PRESERVED_SPECIMEN | Bolivia                          | Insecta           | 5396                  | 189                      | total           | 
| 3.49521707137601   | PRESERVED_SPECIMEN | Paraguay                         | Insecta           | 2718                  | 95                       | non-commercial  | 
| 3.49243306169965   | HUMAN_OBSERVATION  | United States                    | Florideophyceae   | 1718                  | 60                       | total           | 
| 3.49127182044888   | PRESERVED_SPECIMEN | France                           | Bryopsida         | 1604                  | 56                       | open commercial | 
| 3.48986399794714   | PRESERVED_SPECIMEN | United Kingdom                   | Insecta           | 19485                 | 680                      | non-commercial  | 
| 3.47826086956522   | PRESERVED_SPECIMEN | Costa Rica                       | Bryopsida         | 920                   | 32                       | open commercial | 
| 3.47826086956522   | PRESERVED_SPECIMEN | Costa Rica                       | Bryopsida         | 920                   | 32                       | non-commercial  | 
| 3.47826086956522   | PRESERVED_SPECIMEN | Costa Rica                       | Bryopsida         | 920                   | 32                       | total           | 
| 3.46766635426429   | PRESERVED_SPECIMEN | Angola                           | Actinopterygii    | 1067                  | 37                       | non-commercial  | 
| 3.46766635426429   | PRESERVED_SPECIMEN | Angola                           | Actinopterygii    | 1067                  | 37                       | open commercial | 
| 3.46420323325635   | PRESERVED_SPECIMEN | United Kingdom                   | Insecta           | 19485                 | 675                      | open commercial | 
| 3.45991561181435   | HUMAN_OBSERVATION  | Thailand                         | Aves              | 1185                  | 41                       | total           | 
| 3.45911949685535   | HUMAN_OBSERVATION  | Denmark                          | Aves              | 636                   | 22                       | open commercial | 
| 3.45563139931741   | PRESERVED_SPECIMEN | Japan                            | Magnoliopsida     | 7032                  | 243                      | non-commercial  | 
| 3.45508390918065   | PRESERVED_SPECIMEN | Syria                            | Magnoliopsida     | 3039                  | 105                      | total           | 
| 3.45400199269346   | PRESERVED_SPECIMEN | South Africa                     | Liliopsida        | 6022                  | 208                      | non-commercial  | 
| 3.4349539073557    | PRESERVED_SPECIMEN | Mexico                           | Magnoliopsida     | 26143                 | 898                      | open commercial | 
| 3.4257748776509    | PRESERVED_SPECIMEN | Morocco                          | Aves              | 613                   | 21                       | total           | 
| 3.42217834814084   | PRESERVED_SPECIMEN | Syria                            | Magnoliopsida     | 3039                  | 104                      | open commercial | 
| 3.42217834814084   | PRESERVED_SPECIMEN | Syria                            | Magnoliopsida     | 3039                  | 104                      | non-commercial  | 
| 3.41977771444856   | PRESERVED_SPECIMEN | Congo - Kinshasa                 | Insecta           | 3509                  | 120                      | non-commercial  | 
| 3.41901466468941   | PRESERVED_SPECIMEN | Malaysia                         | Magnoliopsida     | 12138                 | 415                      | open commercial | 
| 3.41779611078374   | PRESERVED_SPECIMEN | Angola                           | Insecta           | 1697                  | 58                       | total           | 
| 3.41530054644809   | PRESERVED_SPECIMEN | Dominican Republic               | Insecta           | 2196                  | 75                       | total           | 
| 3.41252699784017   | PRESERVED_SPECIMEN | United States                    | Dothideomycetes   | 4630                  | 158                      | non-commercial  | 
| 3.39285714285714   | PRESERVED_SPECIMEN | Australia                        | Gymnolaemata      | 1120                  | 38                       | non-commercial  | 
| 3.39285714285714   | PRESERVED_SPECIMEN | Australia                        | Gymnolaemata      | 1120                  | 38                       | open commercial | 
| 3.39285714285714   | PRESERVED_SPECIMEN | Australia                        | Gymnolaemata      | 1120                  | 38                       | total           | 
| 3.37552742616034   | HUMAN_OBSERVATION  | Thailand                         | Aves              | 1185                  | 40                       | non-commercial  | 
| 3.36711343576332   | HUMAN_OBSERVATION  | Italy                            | Insecta           | 15295                 | 515                      | non-commercial  | 
| 3.36022991046756   | HUMAN_OBSERVATION  | United States                    | Gastropoda        | 18094                 | 608                      | non-commercial  | 
| 3.359375           | PRESERVED_SPECIMEN | Colombia                         | Aves              | 2560                  | 86                       | open commercial | 
| 3.35664335664336   | HUMAN_OBSERVATION  | Norway                           | Aves              | 715                   | 24                       | open commercial | 
| 3.35570469798658   | PRESERVED_SPECIMEN | Sudan                            | Insecta           | 745                   | 25                       | open commercial | 
| 3.34890965732087   | HUMAN_OBSERVATION  | Congo - Kinshasa                 | Aves              | 1284                  | 43                       | non-commercial  | 
| 3.34890965732087   | HUMAN_OBSERVATION  | Congo - Kinshasa                 | Aves              | 1284                  | 43                       | total           | 
| 3.34394904458599   | PRESERVED_SPECIMEN | Guyana                           | Actinopterygii    | 1256                  | 42                       | non-commercial  | 
| 3.34394904458599   | PRESERVED_SPECIMEN | Guyana                           | Actinopterygii    | 1256                  | 42                       | total           | 
| 3.33776154101627   | PRESERVED_SPECIMEN | South Africa                     | Liliopsida        | 6022                  | 201                      | open commercial | 
| 3.33333333333333   | PRESERVED_SPECIMEN | Réunion                          | Insecta           | 720                   | 24                       | total           | 
| 3.33082140165787   | PRESERVED_SPECIMEN | Indonesia                        | Liliopsida        | 6635                  | 221                      | total           | 
| 3.31034482758621   | PRESERVED_SPECIMEN | Nigeria                          | Insecta           | 2175                  | 72                       | total           | 
| 3.30691601573636   | PRESERVED_SPECIMEN | Indonesia                        | Magnoliopsida     | 17539                 | 580                      | total           | 
| 3.30226904376013   | PRESERVED_SPECIMEN | Ecuador                          | Magnoliopsida     | 14808                 | 489                      | open commercial | 
| 3.29234430781436   | PRESERVED_SPECIMEN | Honduras                         | Magnoliopsida     | 5042                  | 166                      | total           | 
| 3.28738069989396   | HUMAN_OBSERVATION  | Taiwan                           | Liliopsida        | 1886                  | 62                       | total           | 
| 3.28738069989396   | HUMAN_OBSERVATION  | Taiwan                           | Liliopsida        | 1886                  | 62                       | non-commercial  | 
| 3.28381548084441   | PRESERVED_SPECIMEN | United Kingdom                   | Aves              | 1279                  | 42                       | open commercial | 
| 3.28381548084441   | PRESERVED_SPECIMEN | United Kingdom                   | Aves              | 1279                  | 42                       | non-commercial  | 
| 3.27706057596822   | HUMAN_OBSERVATION  | Switzerland                      | Liliopsida        | 1007                  | 33                       | total           | 
| 3.27706057596822   | HUMAN_OBSERVATION  | Switzerland                      | Liliopsida        | 1007                  | 33                       | non-commercial  | 
| 3.2707622298066    | PRESERVED_SPECIMEN | Japan                            | Magnoliopsida     | 7032                  | 230                      | open commercial | 
| 3.25708602685231   | PRESERVED_SPECIMEN | Guatemala                        | Insecta           | 4022                  | 131                      | total           | 
| 3.25621251071123   | HUMAN_OBSERVATION  | Germany                          | Mammalia          | 1167                  | 38                       | total           | 
| 3.25621251071123   | HUMAN_OBSERVATION  | Germany                          | Mammalia          | 1167                  | 38                       | non-commercial  | 
| 3.2501076194576    | HUMAN_OBSERVATION  | Canada                           | Agaricomycetes    | 4646                  | 151                      | total           | 
| 3.24769752787203   | PRESERVED_SPECIMEN | Guyana                           | Liliopsida        | 2063                  | 67                       | open commercial | 
| 3.24769752787203   | PRESERVED_SPECIMEN | Guyana                           | Liliopsida        | 2063                  | 67                       | non-commercial  | 
| 3.24754901960784   | PRESERVED_SPECIMEN | Australia                        | Bryopsida         | 1632                  | 53                       | total           | 
| 3.24754901960784   | PRESERVED_SPECIMEN | Australia                        | Bryopsida         | 1632                  | 53                       | non-commercial  | 
| 3.24754901960784   | PRESERVED_SPECIMEN | Australia                        | Bryopsida         | 1632                  | 53                       | open commercial | 
| 3.24350107321727   | PRESERVED_SPECIMEN | Suriname                         | Magnoliopsida     | 4193                  | 136                      | total           | 
| 3.23517212774782   | HUMAN_OBSERVATION  | United States                    | Bivalvia          | 7233                  | 234                      | total           | 
| 3.23370896619304   | PRESERVED_SPECIMEN | India                            | Aves              | 2041                  | 66                       | open commercial | 
| 3.23370896619304   | PRESERVED_SPECIMEN | India                            | Aves              | 2041                  | 66                       | non-commercial  | 
| 3.23315118397086   | PRESERVED_SPECIMEN | Dominican Republic               | Insecta           | 2196                  | 71                       | non-commercial  | 
| 3.2258064516129    | PRESERVED_SPECIMEN | Cambodia                         | Liliopsida        | 682                   | 22                       | non-commercial  | 
| 3.22115384615385   | HUMAN_OBSERVATION  | Botswana                         | Magnoliopsida     | 2080                  | 67                       | non-commercial  | 
| 3.22115384615385   | HUMAN_OBSERVATION  | Botswana                         | Magnoliopsida     | 2080                  | 67                       | total           | 
| 3.22061191626409   | PRESERVED_SPECIMEN | Greece                           | Liliopsida        | 1242                  | 40                       | open commercial | 
| 3.20197044334975   | PRESERVED_SPECIMEN | Zimbabwe                         | Aves              | 812                   | 26                       | total           | 
| 3.20167564332735   | PRESERVED_SPECIMEN | United States                    | Malacostraca      | 6684                  | 214                      | total           | 
| 3.20121951219512   | PRESERVED_SPECIMEN | Jamaica                          | Bryopsida         | 656                   | 21                       | non-commercial  | 
| 3.20121951219512   | PRESERVED_SPECIMEN | Jamaica                          | Bryopsida         | 656                   | 21                       | total           | 
| 3.20121951219512   | PRESERVED_SPECIMEN | Jamaica                          | Bryopsida         | 656                   | 21                       | open commercial | 
| 3.19439033891702   | HUMAN_OBSERVATION  | Spain                            | Liliopsida        | 2567                  | 82                       | total           | 
| 3.19004524886878   | PRESERVED_SPECIMEN | Turkey                           | Magnoliopsida     | 8840                  | 282                      | open commercial | 
| 3.17899101589496   | PRESERVED_SPECIMEN | Pakistan                         | Insecta           | 1447                  | 46                       | total           | 
| 3.17820658342792   | PRESERVED_SPECIMEN | Zambia                           | Liliopsida        | 1762                  | 56                       | total           | 
| 3.17540322580645   | PRESERVED_SPECIMEN | Guyana                           | Insecta           | 1984                  | 63                       | total           | 
| 3.1733746130031    | PRESERVED_SPECIMEN | Norway                           | Magnoliopsida     | 3876                  | 123                      | open commercial | 
| 3.17258883248731   | PRESERVED_SPECIMEN | Mozambique                       | Aves              | 788                   | 25                       | non-commercial  | 
| 3.17258883248731   | PRESERVED_SPECIMEN | Mozambique                       | Aves              | 788                   | 25                       | open commercial | 
| 3.17258883248731   | PRESERVED_SPECIMEN | Mozambique                       | Aves              | 788                   | 25                       | total           | 
| 3.16133246244285   | PRESERVED_SPECIMEN | Ecuador                          | Insecta           | 7655                  | 242                      | total           | 
| 3.15221899626711   | HUMAN_OBSERVATION  | United States                    | Bivalvia          | 7233                  | 228                      | non-commercial  | 
| 3.14026517794836   | PRESERVED_SPECIMEN | Costa Rica                       | Polypodiopsida    | 1433                  | 45                       | non-commercial  | 
| 3.13725490196078   | HUMAN_OBSERVATION  | Lithuania                        | Magnoliopsida     | 765                   | 24                       | non-commercial  | 
| 3.13725490196078   | HUMAN_OBSERVATION  | Lithuania                        | Magnoliopsida     | 765                   | 24                       | total           | 
| 3.12965722801788   | PRESERVED_SPECIMEN | Cape Verde                       | Magnoliopsida     | 671                   | 21                       | non-commercial  | 
| 3.12965722801788   | PRESERVED_SPECIMEN | Cape Verde                       | Magnoliopsida     | 671                   | 21                       | open commercial | 
| 3.12389066382677   | PRESERVED_SPECIMEN | United States                    | Polychaeta        | 2817                  | 88                       | total           | 
| 3.12145289443814   | PRESERVED_SPECIMEN | Zambia                           | Liliopsida        | 1762                  | 55                       | open commercial | 
| 3.12145289443814   | PRESERVED_SPECIMEN | Zambia                           | Liliopsida        | 1762                  | 55                       | non-commercial  | 
| 3.11986863711002   | PRESERVED_SPECIMEN | United Kingdom                   | Bivalvia          | 1218                  | 38                       | non-commercial  | 
| 3.11986863711002   | PRESERVED_SPECIMEN | United Kingdom                   | Bivalvia          | 1218                  | 38                       | open commercial | 
| 3.11986863711002   | PRESERVED_SPECIMEN | United Kingdom                   | Bivalvia          | 1218                  | 38                       | total           | 
| 3.1172557714882    | PRESERVED_SPECIMEN | United Kingdom                   | Magnoliopsida     | 7667                  | 239                      | total           | 
| 3.11493018259936   | PRESERVED_SPECIMEN | New Zealand                      | Liliopsida        | 1862                  | 58                       | total           | 
| 3.11438278595697   | HUMAN_OBSERVATION  | Venezuela                        | Aves              | 1766                  | 55                       | total           | 
| 3.11252992817239   | PRESERVED_SPECIMEN | United Kingdom                   | Bryopsida         | 1253                  | 39                       | non-commercial  | 
| 3.11015118790497   | PRESERVED_SPECIMEN | United States                    | Dothideomycetes   | 4630                  | 144                      | open commercial | 
| 3.1055900621118    | HUMAN_OBSERVATION  | Zambia                           | Aves              | 805                   | 25                       | non-commercial  | 
| 3.10509554140127   | PRESERVED_SPECIMEN | Guyana                           | Actinopterygii    | 1256                  | 39                       | open commercial | 
| 3.09506263817244   | PRESERVED_SPECIMEN | Indonesia                        | Insecta           | 12213                 | 378                      | non-commercial  | 
| 3.09056705186778   | PRESERVED_SPECIMEN | India                            | Magnoliopsida     | 14884                 | 460                      | open commercial | 
| 3.08898109727985   | PRESERVED_SPECIMEN | Lebanon                          | Magnoliopsida     | 2169                  | 67                       | total           | 
| 3.08898109727985   | PRESERVED_SPECIMEN | Lebanon                          | Magnoliopsida     | 2169                  | 67                       | non-commercial  | 
| 3.06990250985273   | PRESERVED_SPECIMEN | Switzerland                      | Magnoliopsida     | 4821                  | 148                      | total           | 
| 3.06771417882529   | HUMAN_OBSERVATION  | Tanzania                         | Liliopsida        | 2673                  | 82                       | total           | 
| 3.0672268907563    | HUMAN_OBSERVATION  | Indonesia                        | Aves              | 2380                  | 73                       | non-commercial  | 
| 3.06410828499182   | PRESERVED_SPECIMEN | United States                    | Actinopterygii    | 6723                  | 206                      | non-commercial  | 
| 3.05633570130514   | HUMAN_OBSERVATION  | Australia                        | Liliopsida        | 6053                  | 185                      | non-commercial  | 
| 3.05039787798408   | PRESERVED_SPECIMEN | Solomon Islands                  | Liliopsida        | 754                   | 23                       | open commercial | 
| 3.04332259219477   | PRESERVED_SPECIMEN | Nepal                            | Magnoliopsida     | 5586                  | 170                      | total           | 
| 3.04287690179806   | PRESERVED_SPECIMEN | Lebanon                          | Magnoliopsida     | 2169                  | 66                       | open commercial | 
| 3.03555941023417   | PRESERVED_SPECIMEN | Taiwan                           | Polypodiopsida    | 1153                  | 35                       | non-commercial  | 
| 3.03272146847566   | PRESERVED_SPECIMEN | United Kingdom                   | Bryopsida         | 1253                  | 38                       | open commercial | 
| 3.02542069459363   | PRESERVED_SPECIMEN | Nepal                            | Magnoliopsida     | 5586                  | 169                      | non-commercial  | 
| 3.0132583366814    | PRESERVED_SPECIMEN | Egypt                            | Magnoliopsida     | 2489                  | 75                       | total           | 
| 3.0005837711617    | PRESERVED_SPECIMEN | Papua New Guinea                 | Magnoliopsida     | 8565                  | 257                      | total           | 
| 2.99539170506912   | PRESERVED_SPECIMEN | Brazil                           | Mammalia          | 868                   | 26                       | non-commercial  | 
| 2.9935851746258    | PRESERVED_SPECIMEN | New Caledonia                    | Malacostraca      | 1403                  | 42                       | total           | 
| 2.97941495124594   | PRESERVED_SPECIMEN | Panama                           | Liliopsida        | 3692                  | 110                      | non-commercial  | 
| 2.97482837528604   | PRESERVED_SPECIMEN | Norway                           | Gastropoda        | 874                   | 26                       | total           | 
| 2.97090352220521   | PRESERVED_SPECIMEN | Haiti                            | Magnoliopsida     | 3265                  | 97                       | non-commercial  | 
| 2.96589223924864   | PRESERVED_SPECIMEN | Cameroon                         | Insecta           | 4046                  | 120                      | total           | 
| 2.96442687747036   | PRESERVED_SPECIMEN | Slovakia                         | Insecta           | 5060                  | 150                      | total           | 
| 2.96176628971459   | PRESERVED_SPECIMEN | Japan                            | Bryopsida         | 1857                  | 55                       | total           | 
| 2.95890919209721   | PRESERVED_SPECIMEN | Colombia                         | Insecta           | 10781                 | 319                      | total           | 
| 2.95628352927748   | HUMAN_OBSERVATION  | Tanzania                         | Magnoliopsida     | 8761                  | 259                      | total           | 
| 2.94882914137034   | PRESERVED_SPECIMEN | Taiwan                           | Polypodiopsida    | 1153                  | 34                       | open commercial | 
| 2.94695481335953   | PRESERVED_SPECIMEN | Canada                           | Aves              | 1018                  | 30                       | total           | 
| 2.94511378848728   | PRESERVED_SPECIMEN | Kenya                            | Mammalia          | 747                   | 22                       | open commercial | 
| 2.94458110259007   | PRESERVED_SPECIMEN | Venezuela                        | Magnoliopsida     | 13822                 | 407                      | open commercial | 
| 2.94117647058824   | PRESERVED_SPECIMEN | Colombia                         | Agaricomycetes    | 748                   | 22                       | non-commercial  | 
| 2.94117647058824   | PRESERVED_SPECIMEN | Colombia                         | Agaricomycetes    | 748                   | 22                       | open commercial | 
| 2.94117647058824   | PRESERVED_SPECIMEN | Colombia                         | Agaricomycetes    | 748                   | 22                       | total           | 
| 2.94117647058824   | PRESERVED_SPECIMEN | Chile                            | Liliopsida        | 1598                  | 47                       | open commercial | 
| 2.93290478103656   | PRESERVED_SPECIMEN | Egypt                            | Magnoliopsida     | 2489                  | 73                       | non-commercial  | 
| 2.92044310171198   | PRESERVED_SPECIMEN | Cameroon                         | Actinopterygii    | 993                   | 29                       | non-commercial  | 
| 2.91798107255521   | PRESERVED_SPECIMEN | Egypt                            | Actinopterygii    | 1268                  | 37                       | non-commercial  | 
| 2.91666666666667   | PRESERVED_SPECIMEN | Réunion                          | Insecta           | 720                   | 21                       | non-commercial  | 
| 2.91616038882138   | PRESERVED_SPECIMEN | Denmark                          | Liliopsida        | 823                   | 24                       | total           | 
| 2.91036088474971   | HUMAN_OBSERVATION  | United States                    | Florideophyceae   | 1718                  | 50                       | non-commercial  | 
| 2.89915966386555   | PRESERVED_SPECIMEN | Indonesia                        | Aves              | 2380                  | 69                       | total           | 
| 2.89855072463768   | PRESERVED_SPECIMEN | Madagascar                       | Gastropoda        | 2898                  | 84                       | total           | 
| 2.8892455858748    | PRESERVED_SPECIMEN | Australia                        | Bivalvia          | 2492                  | 72                       | non-commercial  | 
| 2.8892455858748    | PRESERVED_SPECIMEN | Australia                        | Bivalvia          | 2492                  | 72                       | total           | 
| 2.87935187212612   | HUMAN_OBSERVATION  | Canada                           | Magnoliopsida     | 9134                  | 263                      | open commercial | 
| 2.87206266318538   | PRESERVED_SPECIMEN | South Africa                     | Reptilia          | 766                   | 22                       | open commercial | 
| 2.86699328615496   | HUMAN_OBSERVATION  | United States                    | Mammalia          | 5511                  | 158                      | open commercial | 
| 2.86532951289398   | PRESERVED_SPECIMEN | United States                    | Eurotiomycetes    | 1047                  | 30                       | open commercial | 
| 2.85986653956149   | PRESERVED_SPECIMEN | Tunisia                          | Magnoliopsida     | 2098                  | 60                       | total           | 
| 2.85406569736134   | PRESERVED_SPECIMEN | Japan                            | Bryopsida         | 1857                  | 53                       | open commercial | 
| 2.85406569736134   | PRESERVED_SPECIMEN | Japan                            | Bryopsida         | 1857                  | 53                       | non-commercial  | 
| 2.85326086956522   | HUMAN_OBSERVATION  | Peru                             | Mammalia          | 736                   | 21                       | total           | 
| 2.85326086956522   | HUMAN_OBSERVATION  | Peru                             | Mammalia          | 736                   | 21                       | non-commercial  | 
| 2.85103349964362   | PRESERVED_SPECIMEN | New Caledonia                    | Malacostraca      | 1403                  | 40                       | non-commercial  | 
| 2.85103349964362   | PRESERVED_SPECIMEN | New Caledonia                    | Malacostraca      | 1403                  | 40                       | open commercial | 
| 2.84911717495987   | PRESERVED_SPECIMEN | Australia                        | Bivalvia          | 2492                  | 71                       | open commercial | 
| 2.84728213977567   | HUMAN_OBSERVATION  | Spain                            | Actinopterygii    | 1159                  | 33                       | total           | 
| 2.84414106939704   | PRESERVED_SPECIMEN | Italy                            | Actinopterygii    | 879                   | 25                       | total           | 
| 2.84011220196353   | PRESERVED_SPECIMEN | Tanzania                         | Insecta           | 5704                  | 162                      | total           | 
| 2.83945633158391   | PRESERVED_SPECIMEN | Malaysia                         | Insecta           | 7431                  | 211                      | open commercial | 
| 2.83932464635197   | PRESERVED_SPECIMEN | Costa Rica                       | Insecta           | 19723                 | 560                      | total           | 
| 2.83400809716599   | PRESERVED_SPECIMEN | Guinea                           | Insecta           | 741                   | 21                       | total           | 
| 2.83251231527094   | PRESERVED_SPECIMEN | Zimbabwe                         | Aves              | 812                   | 23                       | non-commercial  | 
| 2.83251231527094   | PRESERVED_SPECIMEN | Zimbabwe                         | Aves              | 812                   | 23                       | open commercial | 
| 2.82658517952636   | PRESERVED_SPECIMEN | Canada                           | Sordariomycetes   | 1309                  | 37                       | total           | 
| 2.82148670645686   | HUMAN_OBSERVATION  | Canada                           | Bryopsida         | 1843                  | 52                       | total           | 
| 2.81962978906586   | HUMAN_OBSERVATION  | Canada                           | Agaricomycetes    | 4646                  | 131                      | non-commercial  | 
| 2.81318681318681   | PRESERVED_SPECIMEN | Sweden                           | Liliopsida        | 4550                  | 128                      | non-commercial  | 
| 2.81173594132029   | PRESERVED_SPECIMEN | Colombia                         | Magnoliopsida     | 22086                 | 621                      | non-commercial  | 
| 2.81156759238008   | PRESERVED_SPECIMEN | Costa Rica                       | Magnoliopsida     | 8714                  | 245                      | non-commercial  | 
| 2.79898218829517   | HUMAN_OBSERVATION  | Italy                            | Arachnida         | 1179                  | 33                       | total           | 
| 2.79809220985692   | PRESERVED_SPECIMEN | Philippines                      | Insecta           | 6290                  | 176                      | total           | 
| 2.77938621887666   | PRESERVED_SPECIMEN | Myanmar (Burma)                  | Liliopsida        | 1727                  | 48                       | non-commercial  | 
| 2.77033065236819   | PRESERVED_SPECIMEN | Iraq                             | Magnoliopsida     | 2238                  | 62                       | total           | 
| 2.76792544683219   | HUMAN_OBSERVATION  | Spain                            | Magnoliopsida     | 14379                 | 398                      | total           | 
| 2.76532137518685   | PRESERVED_SPECIMEN | Gabon                            | Insecta           | 1338                  | 37                       | non-commercial  | 
| 2.76453765490944   | PRESERVED_SPECIMEN | Gabon                            | Liliopsida        | 1049                  | 29                       | non-commercial  | 
| 2.76166804750069   | HUMAN_OBSERVATION  | Mexico                           | Actinopterygii    | 3621                  | 100                      | total           | 
| 2.76166804750069   | HUMAN_OBSERVATION  | Mexico                           | Actinopterygii    | 3621                  | 100                      | non-commercial  | 
| 2.75545350172216   | PRESERVED_SPECIMEN | Indonesia                        | Reptilia          | 871                   | 24                       | total           | 
| 2.7501909854851    | PRESERVED_SPECIMEN | Canada                           | Sordariomycetes   | 1309                  | 36                       | non-commercial  | 
| 2.73704789833822   | PRESERVED_SPECIMEN | Vietnam                          | Aves              | 1023                  | 28                       | open commercial | 
| 2.73003033367037   | HUMAN_OBSERVATION  | Norway                           | Malacostraca      | 989                   | 27                       | total           | 
| 2.72464814146517   | PRESERVED_SPECIMEN | Venezuela                        | Insecta           | 5542                  | 151                      | total           | 
| 2.72397094430993   | PRESERVED_SPECIMEN | Jamaica                          | Gastropoda        | 1652                  | 45                       | total           | 
| 2.72397094430993   | PRESERVED_SPECIMEN | Jamaica                          | Gastropoda        | 1652                  | 45                       | non-commercial  | 
| 2.72397094430993   | PRESERVED_SPECIMEN | Jamaica                          | Gastropoda        | 1652                  | 45                       | open commercial | 
| 2.7190332326284    | PRESERVED_SPECIMEN | Cameroon                         | Actinopterygii    | 993                   | 27                       | open commercial | 
| 2.71156138259833   | HUMAN_OBSERVATION  | Denmark                          | Magnoliopsida     | 3356                  | 91                       | total           | 
| 2.69360269360269   | PRESERVED_SPECIMEN | Jamaica                          | Actinopterygii    | 891                   | 24                       | open commercial | 
| 2.69360269360269   | PRESERVED_SPECIMEN | Jamaica                          | Actinopterygii    | 891                   | 24                       | total           | 
| 2.69360269360269   | PRESERVED_SPECIMEN | Jamaica                          | Actinopterygii    | 891                   | 24                       | non-commercial  | 
| 2.69073569482289   | PRESERVED_SPECIMEN | Equatorial Guinea                | Magnoliopsida     | 2936                  | 79                       | total           | 
| 2.68231349538977   | HUMAN_OBSERVATION  | Russia                           | Agaricomycetes    | 2386                  | 64                       | non-commercial  | 
| 2.68231349538977   | HUMAN_OBSERVATION  | Russia                           | Agaricomycetes    | 2386                  | 64                       | total           | 
| 2.67579340385812   | PRESERVED_SPECIMEN | South Africa                     | Lecanoromycetes   | 1607                  | 43                       | non-commercial  | 
| 2.66920877025739   | PRESERVED_SPECIMEN | Gabon                            | Liliopsida        | 1049                  | 28                       | open commercial | 
| 2.6635784597568    | PRESERVED_SPECIMEN | Myanmar (Burma)                  | Liliopsida        | 1727                  | 46                       | open commercial | 
| 2.6620059155687    | PRESERVED_SPECIMEN | Malawi                           | Magnoliopsida     | 3719                  | 99                       | total           | 
| 2.6587086272382    | HUMAN_OBSERVATION  | Canada                           | Bryopsida         | 1843                  | 49                       | non-commercial  | 
| 2.65644255785294   | PRESERVED_SPECIMEN | Italy                            | Magnoliopsida     | 7303                  | 194                      | non-commercial  | 
| 2.65355902136152   | PRESERVED_SPECIMEN | Sweden                           | Magnoliopsida     | 13529                 | 359                      | total           | 
| 2.6431718061674    | PRESERVED_SPECIMEN | Germany                          | Magnoliopsida     | 10896                 | 288                      | non-commercial  | 
| 2.63511696692659   | PRESERVED_SPECIMEN | Malawi                           | Magnoliopsida     | 3719                  | 98                       | non-commercial  | 
| 2.63157894736842   | PRESERVED_SPECIMEN | Australia                        | Demospongiae      | 1140                  | 30                       | non-commercial  | 
| 2.63157894736842   | PRESERVED_SPECIMEN | Australia                        | Demospongiae      | 1140                  | 30                       | open commercial | 
| 2.63026676639242   | PRESERVED_SPECIMEN | Thailand                         | Magnoliopsida     | 8022                  | 211                      | total           | 
| 2.6271186440678    | PRESERVED_SPECIMEN | Chad                             | Magnoliopsida     | 1180                  | 31                       | total           | 
| 2.6271186440678    | PRESERVED_SPECIMEN | Chad                             | Magnoliopsida     | 1180                  | 31                       | open commercial | 
| 2.6271186440678    | PRESERVED_SPECIMEN | Chad                             | Magnoliopsida     | 1180                  | 31                       | non-commercial  | 
| 2.62529832935561   | PRESERVED_SPECIMEN | Burkina Faso                     | Magnoliopsida     | 2095                  | 55                       | open commercial | 
| 2.62529832935561   | PRESERVED_SPECIMEN | Burkina Faso                     | Magnoliopsida     | 2095                  | 55                       | non-commercial  | 
| 2.62096774193548   | PRESERVED_SPECIMEN | Guyana                           | Insecta           | 1984                  | 52                       | non-commercial  | 
| 2.61904761904762   | PRESERVED_SPECIMEN | United Kingdom                   | Globothalamea     | 840                   | 22                       | total           | 
| 2.61904761904762   | PRESERVED_SPECIMEN | United Kingdom                   | Globothalamea     | 840                   | 22                       | non-commercial  | 
| 2.61904761904762   | PRESERVED_SPECIMEN | United Kingdom                   | Globothalamea     | 840                   | 22                       | open commercial | 
| 2.61744966442953   | PRESERVED_SPECIMEN | Bolivia                          | Liliopsida        | 4470                  | 117                      | total           | 
| 2.61660978384528   | PRESERVED_SPECIMEN | Italy                            | Actinopterygii    | 879                   | 23                       | non-commercial  | 
| 2.61558784676354   | PRESERVED_SPECIMEN | Papua New Guinea                 | Liliopsida        | 3785                  | 99                       | total           | 
| 2.61309010230494   | PRESERVED_SPECIMEN | Philippines                      | Magnoliopsida     | 8113                  | 212                      | non-commercial  | 
| 2.61020881670534   | PRESERVED_SPECIMEN | Mexico                           | Aves              | 1724                  | 45                       | total           | 
| 2.61016949152542   | HUMAN_OBSERVATION  | United States                    | Bryopsida         | 2950                  | 77                       | non-commercial  | 
| 2.61016949152542   | HUMAN_OBSERVATION  | United States                    | Bryopsida         | 2950                  | 77                       | total           | 
| 2.60296540362438   | HUMAN_OBSERVATION  | New Zealand                      | Insecta           | 6070                  | 158                      | open commercial | 
| 2.60047281323877   | PRESERVED_SPECIMEN | Central African Republic         | Liliopsida        | 846                   | 22                       | non-commercial  | 
| 2.60047281323877   | PRESERVED_SPECIMEN | Central African Republic         | Liliopsida        | 846                   | 22                       | total           | 
| 2.60013619761035   | PRESERVED_SPECIMEN | Australia                        | Insecta           | 32306                 | 840                      | non-commercial  | 
| 2.58162490508732   | PRESERVED_SPECIMEN | Germany                          | Bryopsida         | 1317                  | 34                       | total           | 
| 2.57820556892403   | PRESERVED_SPECIMEN | Central African Republic         | Magnoliopsida     | 2909                  | 75                       | non-commercial  | 
| 2.57820556892403   | PRESERVED_SPECIMEN | Central African Republic         | Magnoliopsida     | 2909                  | 75                       | total           | 
| 2.56685448528754   | PRESERVED_SPECIMEN | Peru                             | Insecta           | 11181                 | 287                      | total           | 
| 2.56273358248799   | PRESERVED_SPECIMEN | United Kingdom                   | Lecanoromycetes   | 1873                  | 48                       | total           | 
| 2.557856272838     | PRESERVED_SPECIMEN | Nepal                            | Liliopsida        | 1642                  | 42                       | total           | 
| 2.55506607929515   | PRESERVED_SPECIMEN | Guinea-Bissau                    | Magnoliopsida     | 1135                  | 29                       | total           | 
| 2.55220417633411   | PRESERVED_SPECIMEN | Mauritania                       | Magnoliopsida     | 862                   | 22                       | non-commercial  | 
| 2.55220417633411   | PRESERVED_SPECIMEN | Mauritania                       | Magnoliopsida     | 862                   | 22                       | total           | 
| 2.55220417633411   | PRESERVED_SPECIMEN | Mauritania                       | Magnoliopsida     | 862                   | 22                       | open commercial | 
| 2.55133789670193   | PRESERVED_SPECIMEN | French Polynesia                 | Magnoliopsida     | 1607                  | 41                       | non-commercial  | 
| 2.55047821466525   | PRESERVED_SPECIMEN | Laos                             | Liliopsida        | 941                   | 24                       | non-commercial  | 
| 2.55047821466525   | PRESERVED_SPECIMEN | Laos                             | Liliopsida        | 941                   | 24                       | total           | 
| 2.54968128983877   | PRESERVED_SPECIMEN | Philippines                      | Liliopsida        | 2667                  | 68                       | non-commercial  | 
| 2.54237288135593   | PRESERVED_SPECIMEN | Cameroon                         | Aves              | 1062                  | 27                       | total           | 
| 2.53841015364061   | PRESERVED_SPECIMEN | Venezuela                        | Liliopsida        | 4491                  | 114                      | non-commercial  | 
| 2.53635734072022   | HUMAN_OBSERVATION  | Germany                          | Insecta           | 23104                 | 586                      | total           | 
| 2.53480899678686   | PRESERVED_SPECIMEN | Honduras                         | Insecta           | 2801                  | 71                       | total           | 
| 2.53388332351208   | PRESERVED_SPECIMEN | Angola                           | Insecta           | 1697                  | 43                       | non-commercial  | 
| 2.53317249698432   | PRESERVED_SPECIMEN | Canada                           | Leotiomycetes     | 829                   | 21                       | open commercial | 
| 2.52873563218391   | PRESERVED_SPECIMEN | French Polynesia                 | Actinopterygii    | 1740                  | 44                       | total           | 
| 2.52756117235816   | PRESERVED_SPECIMEN | Malawi                           | Magnoliopsida     | 3719                  | 94                       | open commercial | 
| 2.52680882534204   | PRESERVED_SPECIMEN | Philippines                      | Magnoliopsida     | 8113                  | 205                      | open commercial | 
| 2.51716247139588   | HUMAN_OBSERVATION  | Norway                           | Gastropoda        | 874                   | 22                       | non-commercial  | 
| 2.5028441410694    | HUMAN_OBSERVATION  | Honduras                         | Aves              | 879                   | 22                       | total           | 
| 2.5028441410694    | HUMAN_OBSERVATION  | Honduras                         | Aves              | 879                   | 22                       | non-commercial  | 
| 2.49593054801953   | PRESERVED_SPECIMEN | Canada                           | Bryopsida         | 1843                  | 46                       | open commercial | 
| 2.49581091807038   | PRESERVED_SPECIMEN | Argentina                        | Magnoliopsida     | 11339                 | 283                      | non-commercial  | 
| 2.48681235870384   | PRESERVED_SPECIMEN | Indonesia                        | Liliopsida        | 6635                  | 165                      | non-commercial  | 
| 2.4831867563373    | PRESERVED_SPECIMEN | Mexico                           | Lecanoromycetes   | 1933                  | 48                       | total           | 
| 2.4806781351284    | PRESERVED_SPECIMEN | Thailand                         | Magnoliopsida     | 8022                  | 199                      | non-commercial  | 
| 2.47815312377723   | PRESERVED_SPECIMEN | United Kingdom                   | Magnoliopsida     | 7667                  | 190                      | non-commercial  | 
| 2.47507734616707   | PRESERVED_SPECIMEN | Central African Republic         | Magnoliopsida     | 2909                  | 72                       | open commercial | 
| 2.46781115879828   | PRESERVED_SPECIMEN | Papua New Guinea                 | Malacostraca      | 1864                  | 46                       | total           | 
| 2.46137925936876   | PRESERVED_SPECIMEN | Sweden                           | Magnoliopsida     | 13529                 | 333                      | non-commercial  | 
| 2.45982289275172   | PRESERVED_SPECIMEN | India                            | Actinopterygii    | 3049                  | 75                       | total           | 
| 2.45971162001696   | HUMAN_OBSERVATION  | Italy                            | Arachnida         | 1179                  | 29                       | non-commercial  | 
| 2.45755138516533   | PRESERVED_SPECIMEN | Iraq                             | Magnoliopsida     | 2238                  | 55                       | non-commercial  | 
| 2.45718540580789   | PRESERVED_SPECIMEN | Suriname                         | Liliopsida        | 1343                  | 33                       | total           | 
| 2.45227378550365   | PRESERVED_SPECIMEN | Iran                             | Magnoliopsida     | 6443                  | 158                      | open commercial | 
| 2.45098039215686   | PRESERVED_SPECIMEN | Philippines                      | Aves              | 1020                  | 25                       | total           | 
| 2.45003223726628   | PRESERVED_SPECIMEN | NA                               | Florideophyceae   | 1551                  | 38                       | non-commercial  | 
| 2.45003223726628   | PRESERVED_SPECIMEN | NA                               | Florideophyceae   | 1551                  | 38                       | open commercial | 
| 2.45003223726628   | PRESERVED_SPECIMEN | NA                               | Florideophyceae   | 1551                  | 38                       | total           | 
| 2.44173140954495   | HUMAN_OBSERVATION  | Canada                           | Mammalia          | 901                   | 22                       | open commercial | 
| 2.44122965641953   | HUMAN_OBSERVATION  | United Kingdom                   | Liliopsida        | 2212                  | 54                       | total           | 
| 2.43719535058118   | PRESERVED_SPECIMEN | Philippines                      | Liliopsida        | 2667                  | 65                       | open commercial | 
| 2.43605359317905   | PRESERVED_SPECIMEN | Nepal                            | Liliopsida        | 1642                  | 40                       | non-commercial  | 
| 2.42976461655277   | PRESERVED_SPECIMEN | Germany                          | Bryopsida         | 1317                  | 32                       | open commercial | 
| 2.42976461655277   | PRESERVED_SPECIMEN | Germany                          | Bryopsida         | 1317                  | 32                       | non-commercial  | 
| 2.42868157286045   | HUMAN_OBSERVATION  | Denmark                          | Insecta           | 7782                  | 189                      | total           | 
| 2.42342231516792   | HUMAN_OBSERVATION  | Taiwan                           | Insecta           | 8129                  | 197                      | total           | 
| 2.41935483870968   | PRESERVED_SPECIMEN | Czechia                          | Insecta           | 5208                  | 126                      | total           | 
| 2.41817293600391   | PRESERVED_SPECIMEN | Costa Rica                       | Liliopsida        | 4094                  | 99                       | total           | 
| 2.41587575496117   | HUMAN_OBSERVATION  | Spain                            | Actinopterygii    | 1159                  | 28                       | non-commercial  | 
| 2.40256273358249   | PRESERVED_SPECIMEN | United Kingdom                   | Lecanoromycetes   | 1873                  | 45                       | non-commercial  | 
| 2.39669421487603   | PRESERVED_SPECIMEN | Nigeria                          | Liliopsida        | 1210                  | 29                       | open commercial | 
| 2.39669421487603   | PRESERVED_SPECIMEN | Nigeria                          | Liliopsida        | 1210                  | 29                       | non-commercial  | 
| 2.39602169981917   | HUMAN_OBSERVATION  | United Kingdom                   | Liliopsida        | 2212                  | 53                       | non-commercial  | 
| 2.39126156268451   | PRESERVED_SPECIMEN | Peru                             | Magnoliopsida     | 20324                 | 486                      | open commercial | 
| 2.3801190059503    | PRESERVED_SPECIMEN | Morocco                          | Insecta           | 2857                  | 68                       | total           | 
| 2.34864300626305   | PRESERVED_SPECIMEN | Nicaragua                        | Liliopsida        | 1916                  | 45                       | total           | 
| 2.3462783171521    | HUMAN_OBSERVATION  | Costa Rica                       | Aves              | 1236                  | 29                       | open commercial | 
| 2.3447820343461    | HUMAN_OBSERVATION  | United States                    | Arachnida         | 6056                  | 142                      | open commercial | 
| 2.34313571316245   | PRESERVED_SPECIMEN | French Guiana                    | Insecta           | 6359                  | 149                      | total           | 
| 2.33463035019455   | PRESERVED_SPECIMEN | Afghanistan                      | Insecta           | 1542                  | 36                       | total           | 
| 2.32860110803324   | HUMAN_OBSERVATION  | Germany                          | Insecta           | 23104                 | 538                      | non-commercial  | 
| 2.32771822358346   | PRESERVED_SPECIMEN | Haiti                            | Magnoliopsida     | 3265                  | 76                       | open commercial | 
| 2.32496697490092   | PRESERVED_SPECIMEN | Papua New Guinea                 | Liliopsida        | 3785                  | 88                       | non-commercial  | 
| 2.31942518593218   | HUMAN_OBSERVATION  | Greece                           | Insecta           | 7933                  | 184                      | total           | 
| 2.31729055258467   | PRESERVED_SPECIMEN | Central African Republic         | Insecta           | 1122                  | 26                       | total           | 
| 2.3130300693909    | HUMAN_OBSERVATION  | Denmark                          | Insecta           | 7782                  | 180                      | non-commercial  | 
| 2.30242688238955   | PRESERVED_SPECIMEN | French Polynesia                 | Magnoliopsida     | 1607                  | 37                       | open commercial | 
| 2.29681978798587   | HUMAN_OBSERVATION  | France                           | Actinopterygii    | 1698                  | 39                       | total           | 
| 2.29681978798587   | HUMAN_OBSERVATION  | France                           | Actinopterygii    | 1698                  | 39                       | non-commercial  | 
| 2.28706624605678   | PRESERVED_SPECIMEN | Egypt                            | Actinopterygii    | 1268                  | 29                       | open commercial | 
| 2.28673148021361   | PRESERVED_SPECIMEN | Italy                            | Magnoliopsida     | 7303                  | 167                      | open commercial | 
| 2.28215767634855   | PRESERVED_SPECIMEN | Venezuela                        | Bryopsida         | 964                   | 22                       | total           | 
| 2.28215767634855   | PRESERVED_SPECIMEN | Venezuela                        | Bryopsida         | 964                   | 22                       | open commercial | 
| 2.28215767634855   | PRESERVED_SPECIMEN | Venezuela                        | Bryopsida         | 964                   | 22                       | non-commercial  | 
| 2.28097459823743   | PRESERVED_SPECIMEN | Greece                           | Magnoliopsida     | 5787                  | 132                      | open commercial | 
| 2.27606461086637   | PRESERVED_SPECIMEN | Panama                           | Insecta           | 8172                  | 186                      | non-commercial  | 
| 2.27447782157582   | HUMAN_OBSERVATION  | Australia                        | Magnoliopsida     | 22071                 | 502                      | non-commercial  | 
| 2.26747847994961   | PRESERVED_SPECIMEN | Kenya                            | Insecta           | 4763                  | 108                      | open commercial | 
| 2.26525392765802   | PRESERVED_SPECIMEN | Uruguay                          | Magnoliopsida     | 2737                  | 62                       | total           | 
| 2.25950782997763   | PRESERVED_SPECIMEN | Bolivia                          | Liliopsida        | 4470                  | 101                      | non-commercial  | 
| 2.25375626043406   | PRESERVED_SPECIMEN | Belize                           | Liliopsida        | 1198                  | 27                       | total           | 
| 2.25318075200796   | HUMAN_OBSERVATION  | France                           | Magnoliopsida     | 14069                 | 317                      | total           | 
| 2.25119940952147   | HUMAN_OBSERVATION  | Taiwan                           | Insecta           | 8129                  | 183                      | non-commercial  | 
| 2.24828934506354   | PRESERVED_SPECIMEN | Brazil                           | Reptilia          | 1023                  | 23                       | open commercial | 
| 2.24607292629185   | HUMAN_OBSERVATION  | France                           | Magnoliopsida     | 14069                 | 316                      | non-commercial  | 
| 2.24331320103538   | MATERIAL_SAMPLE    | Spain                            | Actinopterygii    | 1159                  | 26                       | total           | 
| 2.24111282843895   | PRESERVED_SPECIMEN | France                           | Mammalia          | 1294                  | 29                       | total           | 
| 2.24111282843895   | PRESERVED_SPECIMEN | France                           | Mammalia          | 1294                  | 29                       | open commercial | 
| 2.24111282843895   | PRESERVED_SPECIMEN | France                           | Mammalia          | 1294                  | 29                       | non-commercial  | 
| 2.24022878932316   | PRESERVED_SPECIMEN | Tunisia                          | Magnoliopsida     | 2098                  | 47                       | open commercial | 
| 2.24022878932316   | PRESERVED_SPECIMEN | Tunisia                          | Magnoliopsida     | 2098                  | 47                       | non-commercial  | 
| 2.23380491437081   | PRESERVED_SPECIMEN | Suriname                         | Liliopsida        | 1343                  | 30                       | open commercial | 
| 2.23380491437081   | PRESERVED_SPECIMEN | Suriname                         | Liliopsida        | 1343                  | 30                       | non-commercial  | 
| 2.22667557336896   | PRESERVED_SPECIMEN | Venezuela                        | Liliopsida        | 4491                  | 100                      | open commercial | 
| 2.22584147665581   | PRESERVED_SPECIMEN | Côte d’Ivoire                    | Magnoliopsida     | 3684                  | 82                       | total           | 
| 2.22208467442436   | HUMAN_OBSERVATION  | Spain                            | Insecta           | 16156                 | 359                      | total           | 
| 2.21752903907075   | PRESERVED_SPECIMEN | Guam                             | Gastropoda        | 947                   | 21                       | total           | 
| 2.21752903907075   | PRESERVED_SPECIMEN | Guam                             | Gastropoda        | 947                   | 21                       | non-commercial  | 
| 2.21696082651743   | PRESERVED_SPECIMEN | Canada                           | Agaricomycetes    | 4646                  | 103                      | open commercial | 
| 2.21621621621622   | HUMAN_OBSERVATION  | Luxembourg                       | Magnoliopsida     | 1850                  | 41                       | total           | 
| 2.20689655172414   | PRESERVED_SPECIMEN | Nigeria                          | Insecta           | 2175                  | 48                       | non-commercial  | 
| 2.20597504096811   | HUMAN_OBSERVATION  | Greece                           | Insecta           | 7933                  | 175                      | non-commercial  | 
| 2.20125786163522   | PRESERVED_SPECIMEN | Trinidad & Tobago                | Liliopsida        | 954                   | 21                       | non-commercial  | 
| 2.20125786163522   | PRESERVED_SPECIMEN | Trinidad & Tobago                | Liliopsida        | 954                   | 21                       | open commercial | 
| 2.19941348973607   | PRESERVED_SPECIMEN | Malawi                           | Liliopsida        | 1364                  | 30                       | total           | 
| 2.19941348973607   | PRESERVED_SPECIMEN | Malawi                           | Liliopsida        | 1364                  | 30                       | open commercial | 
| 2.19941348973607   | PRESERVED_SPECIMEN | Malawi                           | Liliopsida        | 1364                  | 30                       | non-commercial  | 
| 2.19744178419154   | PRESERVED_SPECIMEN | India                            | Actinopterygii    | 3049                  | 67                       | non-commercial  | 
| 2.19744178419154   | PRESERVED_SPECIMEN | India                            | Actinopterygii    | 3049                  | 67                       | open commercial | 
| 2.19229564672722   | PRESERVED_SPECIMEN | Belize                           | Magnoliopsida     | 3193                  | 70                       | total           | 
| 2.18732473359506   | PRESERVED_SPECIMEN | Sri Lanka                        | Insecta           | 3566                  | 78                       | total           | 
| 2.18522372528616   | PRESERVED_SPECIMEN | Morocco                          | Liliopsida        | 961                   | 21                       | non-commercial  | 
| 2.18522372528616   | PRESERVED_SPECIMEN | Morocco                          | Liliopsida        | 961                   | 21                       | open commercial | 
| 2.18387705581019   | PRESERVED_SPECIMEN | Mozambique                       | Insecta           | 3709                  | 81                       | total           | 
| 2.17889908256881   | PRESERVED_SPECIMEN | Paraguay                         | Liliopsida        | 1744                  | 38                       | total           | 
| 2.17571487774555   | PRESERVED_SPECIMEN | Thailand                         | Insecta           | 4826                  | 105                      | total           | 
| 2.17391304347826   | PRESERVED_SPECIMEN | Tanzania                         | Insecta           | 5704                  | 124                      | non-commercial  | 
| 2.16572504708098   | PRESERVED_SPECIMEN | Cameroon                         | Aves              | 1062                  | 23                       | non-commercial  | 
| 2.16270589714573   | PRESERVED_SPECIMEN | Panama                           | Magnoliopsida     | 7953                  | 172                      | non-commercial  | 
| 2.16216216216216   | HUMAN_OBSERVATION  | Luxembourg                       | Magnoliopsida     | 1850                  | 40                       | non-commercial  | 
| 2.16198237152836   | PRESERVED_SPECIMEN | Austria                          | Magnoliopsida     | 6013                  | 130                      | total           | 
| 2.14723926380368   | PRESERVED_SPECIMEN | Norway                           | Dothideomycetes   | 978                   | 21                       | total           | 
| 2.14602285980872   | HUMAN_OBSERVATION  | Bulgaria                         | Insecta           | 4287                  | 92                       | total           | 
| 2.14529497805948   | HUMAN_OBSERVATION  | Canada                           | Gastropoda        | 2051                  | 44                       | total           | 
| 2.14521452145215   | PRESERVED_SPECIMEN | Madagascar                       | Malacostraca      | 1212                  | 26                       | total           | 
| 2.13986322523715   | PRESERVED_SPECIMEN | Portugal                         | Magnoliopsida     | 4533                  | 97                       | non-commercial  | 
| 2.13898567557104   | HUMAN_OBSERVATION  | Madagascar                       | Magnoliopsida     | 10332                 | 221                      | total           | 
| 2.13898567557104   | HUMAN_OBSERVATION  | Madagascar                       | Magnoliopsida     | 10332                 | 221                      | non-commercial  | 
| 2.13592233009709   | PRESERVED_SPECIMEN | Latvia                           | Magnoliopsida     | 1030                  | 22                       | open commercial | 
| 2.13151927437642   | PRESERVED_SPECIMEN | Algeria                          | Insecta           | 2205                  | 47                       | non-commercial  | 
| 2.13143872113677   | PRESERVED_SPECIMEN | Bolivia                          | Bryopsida         | 1689                  | 36                       | non-commercial  | 
| 2.13143872113677   | PRESERVED_SPECIMEN | Bolivia                          | Bryopsida         | 1689                  | 36                       | total           | 
| 2.13110956682882   | PRESERVED_SPECIMEN | Zambia                           | Magnoliopsida     | 4317                  | 92                       | total           | 
| 2.13034244757101   | PRESERVED_SPECIMEN | Bolivia                          | Magnoliopsida     | 15068                 | 321                      | open commercial | 
| 2.12895641952196   | PRESERVED_SPECIMEN | South Africa                     | Insecta           | 22969                 | 489                      | total           | 
| 2.12652844231792   | PRESERVED_SPECIMEN | Ghana                            | Insecta           | 1881                  | 40                       | total           | 
| 2.12269652437602   | HUMAN_OBSERVATION  | Bulgaria                         | Insecta           | 4287                  | 91                       | non-commercial  | 
| 2.12258526114954   | PRESERVED_SPECIMEN | Suriname                         | Magnoliopsida     | 4193                  | 89                       | non-commercial  | 
| 2.11786372007366   | PRESERVED_SPECIMEN | Trinidad & Tobago                | Insecta           | 3258                  | 69                       | total           | 
| 2.11726384364821   | PRESERVED_SPECIMEN | Côte d’Ivoire                    | Magnoliopsida     | 3684                  | 78                       | open commercial | 
| 2.11726384364821   | PRESERVED_SPECIMEN | Côte d’Ivoire                    | Magnoliopsida     | 3684                  | 78                       | non-commercial  | 
| 2.10884353741497   | PRESERVED_SPECIMEN | Kenya                            | Actinopterygii    | 1470                  | 31                       | total           | 
| 2.10794533240676   | PRESERVED_SPECIMEN | Zambia                           | Magnoliopsida     | 4317                  | 91                       | open commercial | 
| 2.10794533240676   | PRESERVED_SPECIMEN | Zambia                           | Magnoliopsida     | 4317                  | 91                       | non-commercial  | 
| 2.09876543209877   | HUMAN_OBSERVATION  | Canada                           | Malacostraca      | 1620                  | 34                       | total           | 
| 2.09876543209877   | HUMAN_OBSERVATION  | Canada                           | Malacostraca      | 1620                  | 34                       | non-commercial  | 
| 2.09723546234509   | PRESERVED_SPECIMEN | Ethiopia                         | Aves              | 1049                  | 22                       | total           | 
| 2.09574233399515   | PRESERVED_SPECIMEN | Portugal                         | Magnoliopsida     | 4533                  | 95                       | open commercial | 
| 2.09471766848816   | PRESERVED_SPECIMEN | Guatemala                        | Liliopsida        | 2196                  | 46                       | total           | 
| 2.0945372204925    | PRESERVED_SPECIMEN | El Salvador                      | Magnoliopsida     | 3533                  | 74                       | total           | 
| 2.08851317752362   | PRESERVED_SPECIMEN | Guatemala                        | Insecta           | 4022                  | 84                       | non-commercial  | 
| 2.08700491605602   | PRESERVED_SPECIMEN | Colombia                         | Insecta           | 10781                 | 225                      | non-commercial  | 
| 2.07336523125997   | PRESERVED_SPECIMEN | Ghana                            | Insecta           | 1881                  | 39                       | non-commercial  | 
| 2.07197382769902   | HUMAN_OBSERVATION  | United States                    | Leotiomycetes     | 1834                  | 38                       | total           | 
| 2.07197382769902   | HUMAN_OBSERVATION  | United States                    | Leotiomycetes     | 1834                  | 38                       | non-commercial  | 
| 2.06631427198462   | PRESERVED_SPECIMEN | Sierra Leone                     | Magnoliopsida     | 2081                  | 43                       | total           | 
| 2.06631427198462   | PRESERVED_SPECIMEN | Sierra Leone                     | Magnoliopsida     | 2081                  | 43                       | open commercial | 
| 2.06631427198462   | PRESERVED_SPECIMEN | Sierra Leone                     | Magnoliopsida     | 2081                  | 43                       | non-commercial  | 
| 2.05859065716548   | PRESERVED_SPECIMEN | Mexico                           | Agaricomycetes    | 2526                  | 52                       | non-commercial  | 
| 2.05859065716548   | PRESERVED_SPECIMEN | Mexico                           | Agaricomycetes    | 2526                  | 52                       | open commercial | 
| 2.05859065716548   | PRESERVED_SPECIMEN | Mexico                           | Agaricomycetes    | 2526                  | 52                       | total           | 
| 2.04878048780488   | PRESERVED_SPECIMEN | Iran                             | Liliopsida        | 1025                  | 21                       | open commercial | 
| 2.04152249134948   | PRESERVED_SPECIMEN | Guinea                           | Magnoliopsida     | 2890                  | 59                       | non-commercial  | 
| 2.04152249134948   | PRESERVED_SPECIMEN | Guinea                           | Magnoliopsida     | 2890                  | 59                       | open commercial | 
| 2.04081632653061   | PRESERVED_SPECIMEN | Kenya                            | Actinopterygii    | 1470                  | 30                       | non-commercial  | 
| 2.04081632653061   | PRESERVED_SPECIMEN | Kenya                            | Actinopterygii    | 1470                  | 30                       | open commercial | 
| 2.03862660944206   | PRESERVED_SPECIMEN | Papua New Guinea                 | Malacostraca      | 1864                  | 38                       | non-commercial  | 
| 2.03759279734639   | PRESERVED_SPECIMEN | Chile                            | Magnoliopsida     | 6331                  | 129                      | open commercial | 
| 2.03497615262321   | PRESERVED_SPECIMEN | Philippines                      | Insecta           | 6290                  | 128                      | non-commercial  | 
| 2.03297944431895   | PRESERVED_SPECIMEN | Mozambique                       | Magnoliopsida     | 4427                  | 90                       | total           | 
| 2.02898550724638   | PRESERVED_SPECIMEN | United States                    | Aves              | 3450                  | 70                       | open commercial | 
| 2.0268893868405    | PRESERVED_SPECIMEN | India                            | Insecta           | 9818                  | 199                      | non-commercial  | 
| 2.02298850574713   | PRESERVED_SPECIMEN | Nigeria                          | Insecta           | 2175                  | 44                       | open commercial | 
| 2.02168180486376   | PRESERVED_SPECIMEN | Uganda                           | Insecta           | 3413                  | 69                       | total           | 
| 2.02122283981809   | PRESERVED_SPECIMEN | New Caledonia                    | Gastropoda        | 3958                  | 80                       | total           | 
| 2.01342281879195   | PRESERVED_SPECIMEN | Bolivia                          | Liliopsida        | 4470                  | 90                       | open commercial | 
| 2.00333889816361   | PRESERVED_SPECIMEN | Suriname                         | Magnoliopsida     | 4193                  | 84                       | open commercial | 
| 2.00292092635093   | PRESERVED_SPECIMEN | Spain                            | Magnoliopsida     | 14379                 | 288                      | non-commercial  | 
| 2                  | HUMAN_OBSERVATION  | Luxembourg                       | Magnoliopsida     | 1850                  | 37                       | open commercial | 
| 1.99704142011834   | PRESERVED_SPECIMEN | Argentina                        | Insecta           | 8112                  | 162                      | non-commercial  | 
| 1.98944988696307   | PRESERVED_SPECIMEN | Indonesia                        | Liliopsida        | 6635                  | 132                      | open commercial | 
| 1.98889916743756   | HUMAN_OBSERVATION  | Singapore                        | Magnoliopsida     | 2162                  | 43                       | total           | 
| 1.98889916743756   | HUMAN_OBSERVATION  | Singapore                        | Magnoliopsida     | 2162                  | 43                       | non-commercial  | 
| 1.985559566787     | HUMAN_OBSERVATION  | New Zealand                      | Bivalvia          | 1108                  | 22                       | open commercial | 
| 1.9774011299435    | PRESERVED_SPECIMEN | Cameroon                         | Aves              | 1062                  | 21                       | open commercial | 
| 1.97726149283243   | PRESERVED_SPECIMEN | Cameroon                         | Insecta           | 4046                  | 80                       | non-commercial  | 
| 1.97288658657555   | PRESERVED_SPECIMEN | Congo - Kinshasa                 | Magnoliopsida     | 9073                  | 179                      | total           | 
| 1.96947316592811   | PRESERVED_SPECIMEN | Chile                            | Insecta           | 4062                  | 80                       | non-commercial  | 
| 1.96887900920927   | PRESERVED_SPECIMEN | Laos                             | Magnoliopsida     | 3149                  | 62                       | non-commercial  | 
| 1.96887900920927   | PRESERVED_SPECIMEN | Laos                             | Magnoliopsida     | 3149                  | 62                       | total           | 
| 1.96887900920927   | PRESERVED_SPECIMEN | Laos                             | Magnoliopsida     | 3149                  | 62                       | open commercial | 
| 1.96078431372549   | PRESERVED_SPECIMEN | Central African Republic         | Insecta           | 1122                  | 22                       | non-commercial  | 
| 1.95413436692506   | PRESERVED_SPECIMEN | Afghanistan                      | Magnoliopsida     | 6192                  | 121                      | total           | 
| 1.95369030390738   | PRESERVED_SPECIMEN | Mauritius                        | Magnoliopsida     | 1382                  | 27                       | total           | 
| 1.952436876101     | PRESERVED_SPECIMEN | New Zealand                      | Magnoliopsida     | 6812                  | 133                      | total           | 
| 1.95177956371986   | PRESERVED_SPECIMEN | Turkey                           | Liliopsida        | 1742                  | 34                       | open commercial | 
| 1.9501625135428    | PRESERVED_SPECIMEN | Panama                           | Liliopsida        | 3692                  | 72                       | open commercial | 
| 1.94954128440367   | PRESERVED_SPECIMEN | Paraguay                         | Liliopsida        | 1744                  | 34                       | non-commercial  | 
| 1.94954128440367   | PRESERVED_SPECIMEN | Paraguay                         | Liliopsida        | 1744                  | 34                       | open commercial | 
| 1.9492025989368    | PRESERVED_SPECIMEN | China                            | Actinopterygii    | 3386                  | 66                       | total           | 
| 1.94840834248079   | PRESERVED_SPECIMEN | Sri Lanka                        | Magnoliopsida     | 3644                  | 71                       | non-commercial  | 
| 1.94475411866716   | HUMAN_OBSERVATION  | Russia                           | Insecta           | 16146                 | 314                      | total           | 
| 1.94032964740246   | PRESERVED_SPECIMEN | Spain                            | Magnoliopsida     | 14379                 | 279                      | open commercial | 
| 1.9388194743645    | PRESERVED_SPECIMEN | Trinidad & Tobago                | Magnoliopsida     | 2321                  | 45                       | total           | 
| 1.93503800967519   | PRESERVED_SPECIMEN | Pakistan                         | Insecta           | 1447                  | 28                       | non-commercial  | 
| 1.93317116886442   | PRESERVED_SPECIMEN | Ecuador                          | Liliopsida        | 7811                  | 151                      | total           | 
| 1.93290379915574   | OBSERVATION        | Germany                          | Agaricomycetes    | 4501                  | 87                       | total           | 
| 1.93290379915574   | OBSERVATION        | Germany                          | Agaricomycetes    | 4501                  | 87                       | non-commercial  | 
| 1.92826841496336   | HUMAN_OBSERVATION  | Indonesia                        | Actinopterygii    | 5186                  | 100                      | total           | 
| 1.92826841496336   | HUMAN_OBSERVATION  | Indonesia                        | Actinopterygii    | 5186                  | 100                      | non-commercial  | 
| 1.92644483362522   | PRESERVED_SPECIMEN | Niger                            | Magnoliopsida     | 1142                  | 22                       | non-commercial  | 
| 1.92644483362522   | PRESERVED_SPECIMEN | Niger                            | Magnoliopsida     | 1142                  | 22                       | total           | 
| 1.92644483362522   | PRESERVED_SPECIMEN | Niger                            | Magnoliopsida     | 1142                  | 22                       | open commercial | 
| 1.9177608845888    | PRESERVED_SPECIMEN | Peru                             | Liliopsida        | 5788                  | 111                      | open commercial | 
| 1.91761363636364   | HUMAN_OBSERVATION  | Ireland                          | Magnoliopsida     | 1408                  | 27                       | non-commercial  | 
| 1.91761363636364   | HUMAN_OBSERVATION  | Ireland                          | Magnoliopsida     | 1408                  | 27                       | total           | 
| 1.91693290734824   | PRESERVED_SPECIMEN | Colombia                         | Liliopsida        | 8451                  | 162                      | non-commercial  | 
| 1.91480635143845   | HUMAN_OBSERVATION  | United States                    | Insecta           | 85335                 | 1634                     | open commercial | 
| 1.91412312467667   | HUMAN_OBSERVATION  | Mexico                           | Lecanoromycetes   | 1933                  | 37                       | non-commercial  | 
| 1.91412312467667   | HUMAN_OBSERVATION  | Mexico                           | Lecanoromycetes   | 1933                  | 37                       | total           | 
| 1.90985485103132   | PRESERVED_SPECIMEN | Canada                           | Sordariomycetes   | 1309                  | 25                       | open commercial | 
| 1.9047619047619    | PRESERVED_SPECIMEN | Congo - Brazzaville              | Magnoliopsida     | 3360                  | 64                       | open commercial | 
| 1.9047619047619    | PRESERVED_SPECIMEN | Congo - Brazzaville              | Magnoliopsida     | 3360                  | 64                       | total           | 
| 1.9047619047619    | PRESERVED_SPECIMEN | Congo - Brazzaville              | Magnoliopsida     | 3360                  | 64                       | non-commercial  | 
| 1.90151145782545   | HUMAN_OBSERVATION  | Canada                           | Gastropoda        | 2051                  | 39                       | non-commercial  | 
| 1.89530685920578   | PRESERVED_SPECIMEN | New Zealand                      | Bivalvia          | 1108                  | 21                       | total           | 
| 1.89530685920578   | PRESERVED_SPECIMEN | New Zealand                      | Bivalvia          | 1108                  | 21                       | non-commercial  | 
| 1.89520624303233   | HUMAN_OBSERVATION  | Russia                           | Insecta           | 16146                 | 306                      | non-commercial  | 
| 1.89461219656602   | PRESERVED_SPECIMEN | Bolivia                          | Bryopsida         | 1689                  | 32                       | open commercial | 
| 1.89352360043908   | PRESERVED_SPECIMEN | Sri Lanka                        | Magnoliopsida     | 3644                  | 69                       | open commercial | 
| 1.87713310580205   | PRESERVED_SPECIMEN | China                            | Reptilia          | 1172                  | 22                       | total           | 
| 1.87612438961707   | HUMAN_OBSERVATION  | Denmark                          | Insecta           | 7782                  | 146                      | open commercial | 
| 1.87553282182438   | HUMAN_OBSERVATION  | New Zealand                      | Bryopsida         | 1173                  | 22                       | non-commercial  | 
| 1.87553282182438   | HUMAN_OBSERVATION  | New Zealand                      | Bryopsida         | 1173                  | 22                       | total           | 
| 1.8733850129199    | PRESERVED_SPECIMEN | Afghanistan                      | Magnoliopsida     | 6192                  | 116                      | non-commercial  | 
| 1.85897435897436   | PRESERVED_SPECIMEN | Puerto Rico                      | Insecta           | 1560                  | 29                       | total           | 
| 1.85783936361304   | HUMAN_OBSERVATION  | United Kingdom                   | Insecta           | 19485                 | 362                      | total           | 
| 1.85703098780624   | HUMAN_OBSERVATION  | United States                    | Agaricomycetes    | 8939                  | 166                      | open commercial | 
| 1.84609002281684   | PRESERVED_SPECIMEN | Switzerland                      | Magnoliopsida     | 4821                  | 89                       | non-commercial  | 
| 1.84085510688836   | PRESERVED_SPECIMEN | Suriname                         | Insecta           | 1684                  | 31                       | total           | 
| 1.83905047606626   | PRESERVED_SPECIMEN | United Kingdom                   | Magnoliopsida     | 7667                  | 141                      | open commercial | 
| 1.83612577461556   | PRESERVED_SPECIMEN | Costa Rica                       | Magnoliopsida     | 8714                  | 160                      | open commercial | 
| 1.83611948479035   | HUMAN_OBSERVATION  | Finland                          | Magnoliopsida     | 3649                  | 67                       | total           | 
| 1.83611948479035   | HUMAN_OBSERVATION  | Finland                          | Magnoliopsida     | 3649                  | 67                       | non-commercial  | 
| 1.83066361556064   | PRESERVED_SPECIMEN | Réunion                          | Magnoliopsida     | 1311                  | 24                       | total           | 
| 1.82191429304593   | HUMAN_OBSERVATION  | United Kingdom                   | Insecta           | 19485                 | 355                      | non-commercial  | 
| 1.82015756587884   | PRESERVED_SPECIMEN | Colombia                         | Magnoliopsida     | 22086                 | 402                      | open commercial | 
| 1.81437543614794   | PRESERVED_SPECIMEN | Costa Rica                       | Polypodiopsida    | 1433                  | 26                       | open commercial | 
| 1.80849746067137   | PRESERVED_SPECIMEN | Russia                           | Insecta           | 16146                 | 292                      | total           | 
| 1.80837563451777   | HUMAN_OBSERVATION  | France                           | Liliopsida        | 3152                  | 57                       | non-commercial  | 
| 1.80837563451777   | HUMAN_OBSERVATION  | France                           | Liliopsida        | 3152                  | 57                       | total           | 
| 1.79948586118252   | PRESERVED_SPECIMEN | Papua New Guinea                 | Bryopsida         | 1167                  | 21                       | total           | 
| 1.79763739085773   | PRESERVED_SPECIMEN | NA                               | Reptilia          | 1947                  | 35                       | total           | 
| 1.79372197309417   | PRESERVED_SPECIMEN | Honduras                         | Liliopsida        | 1784                  | 32                       | total           | 
| 1.79340028694405   | PRESERVED_SPECIMEN | Mexico                           | Polypodiopsida    | 1394                  | 25                       | non-commercial  | 
| 1.79175118323191   | HUMAN_OBSERVATION  | United States                    | Anthozoa          | 2958                  | 53                       | total           | 
| 1.7897885717183    | PRESERVED_SPECIMEN | Costa Rica                       | Insecta           | 19723                 | 353                      | non-commercial  | 
| 1.78803641092328   | HUMAN_OBSERVATION  | Nicaragua                        | Insecta           | 3076                  | 55                       | non-commercial  | 
| 1.78803641092328   | HUMAN_OBSERVATION  | Nicaragua                        | Insecta           | 3076                  | 55                       | total           | 
| 1.78571428571429   | PRESERVED_SPECIMEN | China                            | Aves              | 1736                  | 31                       | total           | 
| 1.78033415502602   | HUMAN_OBSERVATION  | United States                    | Sordariomycetes   | 3651                  | 65                       | total           | 
| 1.77865612648221   | PRESERVED_SPECIMEN | Tunisia                          | Insecta           | 2024                  | 36                       | total           | 
| 1.77222652076195   | PRESERVED_SPECIMEN | Brazil                           | Insecta           | 27141                 | 481                      | non-commercial  | 
| 1.77175612298072   | PRESERVED_SPECIMEN | China                            | Polypodiopsida    | 1919                  | 34                       | non-commercial  | 
| 1.76678445229682   | PRESERVED_SPECIMEN | Egypt                            | Insecta           | 1415                  | 25                       | non-commercial  | 
| 1.76638176638177   | PRESERVED_SPECIMEN | Bolivia                          | Aves              | 1755                  | 31                       | total           | 
| 1.7651430694909    | PRESERVED_SPECIMEN | Russia                           | Insecta           | 16146                 | 285                      | non-commercial  | 
| 1.75867122618466   | PRESERVED_SPECIMEN | Costa Rica                       | Liliopsida        | 4094                  | 72                       | non-commercial  | 
| 1.75517551755176   | HUMAN_OBSERVATION  | Australia                        | Gastropoda        | 8888                  | 156                      | total           | 
| 1.75513698630137   | PRESERVED_SPECIMEN | Solomon Islands                  | Gastropoda        | 2336                  | 41                       | total           | 
| 1.75294439879485   | HUMAN_OBSERVATION  | United States                    | Sordariomycetes   | 3651                  | 64                       | non-commercial  | 
| 1.75131348511384   | PRESERVED_SPECIMEN | Côte d’Ivoire                    | Insecta           | 1713                  | 30                       | total           | 
| 1.74322080796901   | HUMAN_OBSERVATION  | South Africa                     | Gastropoda        | 3614                  | 63                       | total           | 
| 1.74322080796901   | HUMAN_OBSERVATION  | South Africa                     | Gastropoda        | 3614                  | 63                       | non-commercial  | 
| 1.73151354654716   | HUMAN_OBSERVATION  | India                            | Insecta           | 9818                  | 170                      | total           | 
| 1.72268907563025   | PRESERVED_SPECIMEN | Indonesia                        | Aves              | 2380                  | 41                       | non-commercial  | 
| 1.72268907563025   | PRESERVED_SPECIMEN | Indonesia                        | Aves              | 2380                  | 41                       | open commercial | 
| 1.71972837110856   | PRESERVED_SPECIMEN | Argentina                        | Magnoliopsida     | 11339                 | 195                      | open commercial | 
| 1.71496156120639   | PRESERVED_SPECIMEN | Argentina                        | Liliopsida        | 3382                  | 58                       | total           | 
| 1.70889805539187   | PRESERVED_SPECIMEN | Angola                           | Insecta           | 1697                  | 29                       | open commercial | 
| 1.70848905499199   | PRESERVED_SPECIMEN | United Kingdom                   | Lecanoromycetes   | 1873                  | 32                       | open commercial | 
| 1.70575692963753   | HUMAN_OBSERVATION  | United States                    | Pucciniomycetes   | 1407                  | 24                       | total           | 
| 1.70015455950541   | HUMAN_OBSERVATION  | France                           | Mammalia          | 1294                  | 22                       | total           | 
| 1.70015455950541   | HUMAN_OBSERVATION  | France                           | Mammalia          | 1294                  | 22                       | non-commercial  | 
| 1.6827783745077    | HUMAN_OBSERVATION  | Canada                           | Liliopsida        | 2793                  | 47                       | open commercial | 
| 1.6798418972332    | PRESERVED_SPECIMEN | Tunisia                          | Insecta           | 2024                  | 34                       | non-commercial  | 
| 1.66425470332851   | PRESERVED_SPECIMEN | Mauritius                        | Magnoliopsida     | 1382                  | 23                       | non-commercial  | 
| 1.66425470332851   | PRESERVED_SPECIMEN | Mauritius                        | Magnoliopsida     | 1382                  | 23                       | open commercial | 
| 1.66122812221893   | PRESERVED_SPECIMEN | New Zealand                      | Gastropoda        | 3371                  | 56                       | non-commercial  | 
| 1.66122812221893   | PRESERVED_SPECIMEN | New Zealand                      | Gastropoda        | 3371                  | 56                       | total           | 
| 1.66011358671909   | PRESERVED_SPECIMEN | China                            | Bryopsida         | 2289                  | 38                       | total           | 
| 1.65895061728395   | HUMAN_OBSERVATION  | Czechia                          | Magnoliopsida     | 2592                  | 43                       | non-commercial  | 
| 1.65895061728395   | HUMAN_OBSERVATION  | Czechia                          | Magnoliopsida     | 2592                  | 43                       | total           | 
| 1.65652467883705   | PRESERVED_SPECIMEN | United States                    | Anthozoa          | 2958                  | 49                       | total           | 
| 1.65505226480836   | PRESERVED_SPECIMEN | Vietnam                          | Insecta           | 2296                  | 38                       | total           | 
| 1.65451486259114   | PRESERVED_SPECIMEN | Sri Lanka                        | Insecta           | 3566                  | 59                       | non-commercial  | 
| 1.6532618409294    | PRESERVED_SPECIMEN | Iraq                             | Magnoliopsida     | 2238                  | 37                       | open commercial | 
| 1.64874551971326   | HUMAN_OBSERVATION  | Cyprus                           | Magnoliopsida     | 1395                  | 23                       | non-commercial  | 
| 1.64874551971326   | HUMAN_OBSERVATION  | Cyprus                           | Magnoliopsida     | 1395                  | 23                       | total           | 
| 1.64663263625885   | PRESERVED_SPECIMEN | Angola                           | Magnoliopsida     | 6073                  | 100                      | open commercial | 
| 1.64663263625885   | PRESERVED_SPECIMEN | Angola                           | Magnoliopsida     | 6073                  | 100                      | non-commercial  | 
| 1.64556962025316   | PRESERVED_SPECIMEN | Afghanistan                      | Liliopsida        | 1580                  | 26                       | total           | 
| 1.64437012263099   | PRESERVED_SPECIMEN | NA                               | Polypodiopsida    | 3588                  | 59                       | total           | 
| 1.64413591523566   | PRESERVED_SPECIMEN | Uruguay                          | Magnoliopsida     | 2737                  | 45                       | non-commercial  | 
| 1.64413591523566   | PRESERVED_SPECIMEN | Uruguay                          | Magnoliopsida     | 2737                  | 45                       | open commercial | 
| 1.64281928987811   | PRESERVED_SPECIMEN | Myanmar (Burma)                  | Insecta           | 1887                  | 31                       | total           | 
| 1.63468372423596   | HUMAN_OBSERVATION  | United States                    | Pucciniomycetes   | 1407                  | 23                       | non-commercial  | 
| 1.63294284700036   | PRESERVED_SPECIMEN | Colombia                         | Liliopsida        | 8451                  | 138                      | open commercial | 
| 1.63156333432216   | PRESERVED_SPECIMEN | New Zealand                      | Gastropoda        | 3371                  | 55                       | open commercial | 
| 1.62752848174843   | PRESERVED_SPECIMEN | Brazil                           | Agaricomycetes    | 4301                  | 70                       | total           | 
| 1.624335499114     | PRESERVED_SPECIMEN | China                            | Actinopterygii    | 3386                  | 55                       | non-commercial  | 
| 1.624335499114     | PRESERVED_SPECIMEN | China                            | Actinopterygii    | 3386                  | 55                       | open commercial | 
| 1.62162162162162   | PRESERVED_SPECIMEN | Luxembourg                       | Magnoliopsida     | 1850                  | 30                       | total           | 
| 1.61443905817174   | PRESERVED_SPECIMEN | Germany                          | Insecta           | 23104                 | 373                      | total           | 
| 1.60707111289675   | PRESERVED_SPECIMEN | Egypt                            | Magnoliopsida     | 2489                  | 40                       | open commercial | 
| 1.60614525139665   | PRESERVED_SPECIMEN | Dominica                         | Magnoliopsida     | 1432                  | 23                       | open commercial | 
| 1.60614525139665   | PRESERVED_SPECIMEN | Dominica                         | Magnoliopsida     | 1432                  | 23                       | non-commercial  | 
| 1.60183066361556   | PRESERVED_SPECIMEN | Réunion                          | Magnoliopsida     | 1311                  | 21                       | open commercial | 
| 1.60183066361556   | PRESERVED_SPECIMEN | Réunion                          | Magnoliopsida     | 1311                  | 21                       | non-commercial  | 
| 1.58785755983654   | PRESERVED_SPECIMEN | Papua New Guinea                 | Magnoliopsida     | 8565                  | 136                      | non-commercial  | 
| 1.58750480092178   | PRESERVED_SPECIMEN | Ecuador                          | Liliopsida        | 7811                  | 124                      | non-commercial  | 
| 1.58653846153846   | PRESERVED_SPECIMEN | Botswana                         | Magnoliopsida     | 2080                  | 33                       | total           | 
| 1.58653846153846   | PRESERVED_SPECIMEN | Botswana                         | Magnoliopsida     | 2080                  | 33                       | open commercial | 
| 1.58653846153846   | PRESERVED_SPECIMEN | Botswana                         | Magnoliopsida     | 2080                  | 33                       | non-commercial  | 
| 1.58520475561427   | PRESERVED_SPECIMEN | Papua New Guinea                 | Liliopsida        | 3785                  | 60                       | open commercial | 
| 1.57273918741809   | PRESERVED_SPECIMEN | China                            | Bryopsida         | 2289                  | 36                       | open commercial | 
| 1.57273918741809   | PRESERVED_SPECIMEN | China                            | Bryopsida         | 2289                  | 36                       | non-commercial  | 
| 1.57223375852863   | HUMAN_OBSERVATION  | New Zealand                      | Gastropoda        | 3371                  | 53                       | open commercial | 
| 1.56854756569566   | HUMAN_OBSERVATION  | India                            | Insecta           | 9818                  | 154                      | non-commercial  | 
| 1.56648451730419   | PRESERVED_SPECIMEN | Israel                           | Magnoliopsida     | 2745                  | 43                       | total           | 
| 1.56331422615946   | PRESERVED_SPECIMEN | China                            | Polypodiopsida    | 1919                  | 30                       | open commercial | 
| 1.55913978494624   | PRESERVED_SPECIMEN | Austria                          | Lecanoromycetes   | 1860                  | 29                       | total           | 
| 1.55823918971562   | PRESERVED_SPECIMEN | Spain                            | Liliopsida        | 2567                  | 40                       | non-commercial  | 
| 1.55408205553253   | PRESERVED_SPECIMEN | Thailand                         | Insecta           | 4826                  | 75                       | non-commercial  | 
| 1.53894472361809   | HUMAN_OBSERVATION  | Poland                           | Magnoliopsida     | 3184                  | 49                       | non-commercial  | 
| 1.53894472361809   | HUMAN_OBSERVATION  | Poland                           | Magnoliopsida     | 3184                  | 49                       | total           | 
| 1.53769841269841   | PRESERVED_SPECIMEN | Kyrgyzstan                       | Insecta           | 2016                  | 31                       | total           | 
| 1.53280196198651   | PRESERVED_SPECIMEN | Singapore                        | Insecta           | 1631                  | 25                       | open commercial | 
| 1.5206567083838    | HUMAN_OBSERVATION  | Malaysia                         | Insecta           | 7431                  | 113                      | total           | 
| 1.52004560136804   | PRESERVED_SPECIMEN | Brazil                           | Actinopterygii    | 5263                  | 80                       | total           | 
| 1.51898734177215   | PRESERVED_SPECIMEN | Afghanistan                      | Liliopsida        | 1580                  | 24                       | non-commercial  | 
| 1.51467339854844   | PRESERVED_SPECIMEN | India                            | Gastropoda        | 3169                  | 48                       | non-commercial  | 
| 1.51467339854844   | PRESERVED_SPECIMEN | India                            | Gastropoda        | 3169                  | 48                       | total           | 
| 1.51127644733783   | PRESERVED_SPECIMEN | Brazil                           | Agaricomycetes    | 4301                  | 65                       | open commercial | 
| 1.51127644733783   | PRESERVED_SPECIMEN | Brazil                           | Agaricomycetes    | 4301                  | 65                       | non-commercial  | 
| 1.50919556366699   | PRESERVED_SPECIMEN | Mexico                           | Insecta           | 28492                 | 430                      | non-commercial  | 
| 1.50719956937155   | HUMAN_OBSERVATION  | Malaysia                         | Insecta           | 7431                  | 112                      | non-commercial  | 
| 1.50679897096656   | PRESERVED_SPECIMEN | Australia                        | Actinopterygii    | 5442                  | 82                       | total           | 
| 1.50537634408602   | PRESERVED_SPECIMEN | Austria                          | Lecanoromycetes   | 1860                  | 28                       | non-commercial  | 
| 1.50412421154779   | PRESERVED_SPECIMEN | Liberia                          | Magnoliopsida     | 2061                  | 31                       | total           | 
| 1.50115473441109   | HUMAN_OBSERVATION  | South Korea                      | Magnoliopsida     | 2598                  | 39                       | non-commercial  | 
| 1.50115473441109   | HUMAN_OBSERVATION  | South Korea                      | Magnoliopsida     | 2598                  | 39                       | total           | 
| 1.49253731343284   | PRESERVED_SPECIMEN | Kenya                            | Aves              | 1541                  | 23                       | total           | 
| 1.48383677795443   | PRESERVED_SPECIMEN | Myanmar (Burma)                  | Insecta           | 1887                  | 28                       | non-commercial  | 
| 1.48311770274535   | PRESERVED_SPECIMEN | India                            | Gastropoda        | 3169                  | 47                       | open commercial | 
| 1.48032723022984   | PRESERVED_SPECIMEN | Spain                            | Liliopsida        | 2567                  | 38                       | open commercial | 
| 1.45942790426153   | PRESERVED_SPECIMEN | Côte d’Ivoire                    | Insecta           | 1713                  | 25                       | non-commercial  | 
| 1.45719489981785   | PRESERVED_SPECIMEN | Israel                           | Magnoliopsida     | 2745                  | 40                       | non-commercial  | 
| 1.45368492224476   | HUMAN_OBSERVATION  | United States                    | Anthozoa          | 2958                  | 43                       | non-commercial  | 
| 1.4510575504181    | PRESERVED_SPECIMEN | Zimbabwe                         | Magnoliopsida     | 4066                  | 59                       | total           | 
| 1.4510575504181    | PRESERVED_SPECIMEN | Zimbabwe                         | Magnoliopsida     | 4066                  | 59                       | non-commercial  | 
| 1.4505893019039    | HUMAN_OBSERVATION  | Portugal                         | Insecta           | 5515                  | 80                       | total           | 
| 1.4505893019039    | HUMAN_OBSERVATION  | Portugal                         | Insecta           | 5515                  | 80                       | non-commercial  | 
| 1.45003265839321   | PRESERVED_SPECIMEN | Ecuador                          | Insecta           | 7655                  | 111                      | non-commercial  | 
| 1.44542644433802   | PRESERVED_SPECIMEN | South Africa                     | Insecta           | 22969                 | 332                      | non-commercial  | 
| 1.44260282381829   | PRESERVED_SPECIMEN | Trinidad & Tobago                | Insecta           | 3258                  | 47                       | non-commercial  | 
| 1.41884222474461   | HUMAN_OBSERVATION  | New Zealand                      | Lecanoromycetes   | 1762                  | 25                       | open commercial | 
| 1.41738157403954   | PRESERVED_SPECIMEN | Brazil                           | Aves              | 2681                  | 38                       | total           | 
| 1.41206675224647   | HUMAN_OBSERVATION  | Swaziland                        | Magnoliopsida     | 2337                  | 33                       | non-commercial  | 
| 1.41206675224647   | HUMAN_OBSERVATION  | Swaziland                        | Magnoliopsida     | 2337                  | 33                       | total           | 
| 1.40199514693988   | PRESERVED_SPECIMEN | Mozambique                       | Insecta           | 3709                  | 52                       | non-commercial  | 
| 1.39118535834426   | PRESERVED_SPECIMEN | Indonesia                        | Magnoliopsida     | 17539                 | 244                      | non-commercial  | 
| 1.38975316324414   | PRESERVED_SPECIMEN | Switzerland                      | Magnoliopsida     | 4821                  | 67                       | open commercial | 
| 1.38888888888889   | PRESERVED_SPECIMEN | Kyrgyzstan                       | Insecta           | 2016                  | 28                       | non-commercial  | 
| 1.38321995464853   | PRESERVED_SPECIMEN | Philippines                      | Actinopterygii    | 4410                  | 61                       | total           | 
| 1.3787160706592    | PRESERVED_SPECIMEN | Vanuatu                          | Gastropoda        | 2321                  | 32                       | total           | 
| 1.37668424135911   | PRESERVED_SPECIMEN | Croatia                          | Insecta           | 3414                  | 47                       | total           | 
| 1.37134608444605   | PRESERVED_SPECIMEN | Venezuela                        | Insecta           | 5542                  | 76                       | non-commercial  | 
| 1.36752136752137   | PRESERVED_SPECIMEN | Bolivia                          | Aves              | 1755                  | 24                       | non-commercial  | 
| 1.3545347467609    | PRESERVED_SPECIMEN | France                           | Actinopterygii    | 1698                  | 23                       | total           | 
| 1.35268076733891   | PRESERVED_SPECIMEN | Zimbabwe                         | Magnoliopsida     | 4066                  | 55                       | open commercial | 
| 1.35013501350135   | PRESERVED_SPECIMEN | Australia                        | Gastropoda        | 8888                  | 120                      | total           | 
| 1.34778786990917   | PRESERVED_SPECIMEN | Uganda                           | Insecta           | 3413                  | 46                       | non-commercial  | 
| 1.34715025906736   | HUMAN_OBSERVATION  | Argentina                        | Mammalia          | 1930                  | 26                       | total           | 
| 1.34715025906736   | HUMAN_OBSERVATION  | Argentina                        | Mammalia          | 1930                  | 26                       | non-commercial  | 
| 1.34264232008593   | PRESERVED_SPECIMEN | New Zealand                      | Liliopsida        | 1862                  | 25                       | non-commercial  | 
| 1.34264232008593   | PRESERVED_SPECIMEN | New Zealand                      | Liliopsida        | 1862                  | 25                       | open commercial | 
| 1.33565621370499   | PRESERVED_SPECIMEN | Ecuador                          | Polypodiopsida    | 1722                  | 23                       | non-commercial  | 
| 1.33343979559246   | HUMAN_OBSERVATION  | France                           | Insecta           | 25048                 | 334                      | total           | 
| 1.33333333333333   | PRESERVED_SPECIMEN | Ethiopia                         | Insecta           | 2025                  | 27                       | total           | 
| 1.33088572739789   | PRESERVED_SPECIMEN | Panama                           | Actinopterygii    | 2179                  | 29                       | total           | 
| 1.32450331125828   | HUMAN_OBSERVATION  | Spain                            | Liliopsida        | 2567                  | 34                       | non-commercial  | 
| 1.31322957198444   | PRESERVED_SPECIMEN | Saudi Arabia                     | Magnoliopsida     | 2056                  | 27                       | open commercial | 
| 1.31054131054131   | PRESERVED_SPECIMEN | Bolivia                          | Aves              | 1755                  | 23                       | open commercial | 
| 1.30948578728841   | HUMAN_OBSERVATION  | France                           | Insecta           | 25048                 | 328                      | non-commercial  | 
| 1.30346232179226   | HUMAN_OBSERVATION  | Italy                            | Agaricomycetes    | 2455                  | 32                       | total           | 
| 1.30346232179226   | HUMAN_OBSERVATION  | Italy                            | Agaricomycetes    | 2455                  | 32                       | non-commercial  | 
| 1.30282550280922   | PRESERVED_SPECIMEN | China                            | Insecta           | 12281                 | 160                      | total           | 
| 1.29718942291701   | PRESERVED_SPECIMEN | Austria                          | Magnoliopsida     | 6013                  | 78                       | non-commercial  | 
| 1.29597197898424   | PRESERVED_SPECIMEN | Papua New Guinea                 | Magnoliopsida     | 8565                  | 111                      | open commercial | 
| 1.29510876398843   | PRESERVED_SPECIMEN | Panama                           | Magnoliopsida     | 7953                  | 103                      | open commercial | 
| 1.28855693026968   | PRESERVED_SPECIMEN | Indonesia                        | Magnoliopsida     | 17539                 | 226                      | open commercial | 
| 1.28262826282628   | PRESERVED_SPECIMEN | Australia                        | Gastropoda        | 8888                  | 114                      | non-commercial  | 
| 1.27758420441347   | PRESERVED_SPECIMEN | Ecuador                          | Polypodiopsida    | 1722                  | 22                       | open commercial | 
| 1.27157129881926   | PRESERVED_SPECIMEN | Ecuador                          | Aves              | 2202                  | 28                       | total           | 
| 1.26887843525625   | HUMAN_OBSERVATION  | Spain                            | Insecta           | 16156                 | 205                      | non-commercial  | 
| 1.26744334912303   | PRESERVED_SPECIMEN | Ecuador                          | Liliopsida        | 7811                  | 99                       | open commercial | 
| 1.26728110599078   | PRESERVED_SPECIMEN | China                            | Aves              | 1736                  | 22                       | non-commercial  | 
| 1.26429861529199   | HUMAN_OBSERVATION  | Australia                        | Anthozoa          | 1661                  | 21                       | total           | 
| 1.26398673849979   | HUMAN_OBSERVATION  | Thailand                         | Insecta           | 4826                  | 61                       | non-commercial  | 
| 1.26398673849979   | HUMAN_OBSERVATION  | Thailand                         | Insecta           | 4826                  | 61                       | total           | 
| 1.26008064516129   | PRESERVED_SPECIMEN | Guyana                           | Insecta           | 1984                  | 25                       | open commercial | 
| 1.2494614390349    | PRESERVED_SPECIMEN | Trinidad & Tobago                | Magnoliopsida     | 2321                  | 29                       | non-commercial  | 
| 1.2494614390349    | PRESERVED_SPECIMEN | Trinidad & Tobago                | Magnoliopsida     | 2321                  | 29                       | open commercial | 
| 1.24858115777526   | PRESERVED_SPECIMEN | New Zealand                      | Lecanoromycetes   | 1762                  | 22                       | total           | 
| 1.24843945068664   | PRESERVED_SPECIMEN | Hungary                          | Magnoliopsida     | 3204                  | 40                       | total           | 
| 1.23282846072561   | HUMAN_OBSERVATION  | Australia                        | Agaricomycetes    | 2839                  | 35                       | open commercial | 
| 1.23253903040263   | PRESERVED_SPECIMEN | Malawi                           | Insecta           | 3651                  | 45                       | total           | 
| 1.23096181931984   | HUMAN_OBSERVATION  | Spain                            | Magnoliopsida     | 14379                 | 177                      | non-commercial  | 
| 1.22520420070012   | PRESERVED_SPECIMEN | Israel                           | Insecta           | 1714                  | 21                       | total           | 
| 1.22506125306265   | PRESERVED_SPECIMEN | Morocco                          | Insecta           | 2857                  | 35                       | non-commercial  | 
| 1.22309197651663   | PRESERVED_SPECIMEN | Hong Kong SAR China              | Insecta           | 2044                  | 25                       | total           | 
| 1.20967741935484   | PRESERVED_SPECIMEN | China                            | Aves              | 1736                  | 21                       | open commercial | 
| 1.20695775647852   | HUMAN_OBSERVATION  | United States                    | Polychaeta        | 2817                  | 34                       | total           | 
| 1.20692832135618   | HUMAN_OBSERVATION  | Russia                           | Magnoliopsida     | 10854                 | 131                      | total           | 
| 1.20559395595563   | PRESERVED_SPECIMEN | Myanmar (Burma)                  | Magnoliopsida     | 6221                  | 75                       | total           | 
| 1.20481927710843   | HUMAN_OBSERVATION  | Sweden                           | Magnoliopsida     | 13529                 | 163                      | total           | 
| 1.20092378752887   | PRESERVED_SPECIMEN | Yemen                            | Magnoliopsida     | 2165                  | 26                       | open commercial | 
| 1.19771512806339   | HUMAN_OBSERVATION  | Russia                           | Magnoliopsida     | 10854                 | 130                      | non-commercial  | 
| 1.19742774780102   | HUMAN_OBSERVATION  | Sweden                           | Magnoliopsida     | 13529                 | 162                      | non-commercial  | 
| 1.18951936987623   | PRESERVED_SPECIMEN | Myanmar (Burma)                  | Magnoliopsida     | 6221                  | 74                       | non-commercial  | 
| 1.18492373629144   | PRESERVED_SPECIMEN | Greece                           | Insecta           | 7933                  | 94                       | total           | 
| 1.18464052287582   | PRESERVED_SPECIMEN | Germany                          | Liliopsida        | 2448                  | 29                       | non-commercial  | 
| 1.17803534106023   | PRESERVED_SPECIMEN | Brazil                           | Actinopterygii    | 5263                  | 62                       | non-commercial  | 
| 1.17624373312765   | PRESERVED_SPECIMEN | Indonesia                        | Actinopterygii    | 5186                  | 61                       | total           | 
| 1.17416829745597   | PRESERVED_SPECIMEN | Hong Kong SAR China              | Insecta           | 2044                  | 24                       | open commercial | 
| 1.17416829745597   | HUMAN_OBSERVATION  | Hong Kong SAR China              | Insecta           | 2044                  | 24                       | open commercial | 
| 1.17416829745597   | PRESERVED_SPECIMEN | Hong Kong SAR China              | Insecta           | 2044                  | 24                       | non-commercial  | 
| 1.16340560549974   | HUMAN_OBSERVATION  | France                           | Arachnida         | 1891                  | 22                       | total           | 
| 1.16340560549974   | HUMAN_OBSERVATION  | France                           | Arachnida         | 1891                  | 22                       | non-commercial  | 
| 1.1609907120743    | HUMAN_OBSERVATION  | Norway                           | Magnoliopsida     | 3876                  | 45                       | non-commercial  | 
| 1.1572498298162    | PRESERVED_SPECIMEN | Papua New Guinea                 | Actinopterygii    | 2938                  | 34                       | total           | 
| 1.14879649890591   | PRESERVED_SPECIMEN | Ecuador                          | Actinopterygii    | 1828                  | 21                       | total           | 
| 1.14503816793893   | PRESERVED_SPECIMEN | Germany                          | Arachnida         | 3406                  | 39                       | total           | 
| 1.14244912531239   | PRESERVED_SPECIMEN | Honduras                         | Insecta           | 2801                  | 32                       | non-commercial  | 
| 1.14226375908619   | PRESERVED_SPECIMEN | Romania                          | Magnoliopsida     | 2889                  | 33                       | total           | 
| 1.13052415210689   | PRESERVED_SPECIMEN | Colombia                         | Polypodiopsida    | 1946                  | 22                       | non-commercial  | 
| 1.12600536193029   | PRESERVED_SPECIMEN | Nepal                            | Insecta           | 1865                  | 21                       | total           | 
| 1.12026359143328   | PRESERVED_SPECIMEN | New Zealand                      | Insecta           | 6070                  | 68                       | total           | 
| 1.11884634510194   | PRESERVED_SPECIMEN | Guatemala                        | Insecta           | 4022                  | 45                       | open commercial | 
| 1.10902423754584   | PRESERVED_SPECIMEN | Peru                             | Insecta           | 11181                 | 124                      | non-commercial  | 
| 1.10717449069973   | PRESERVED_SPECIMEN | Rwanda                           | Magnoliopsida     | 2258                  | 25                       | total           | 
| 1.10046148384807   | HUMAN_OBSERVATION  | United States                    | Polychaeta        | 2817                  | 31                       | non-commercial  | 
| 1.09598140152773   | PRESERVED_SPECIMEN | Australia                        | Lecanoromycetes   | 3011                  | 33                       | total           | 
| 1.08451757666417   | PRESERVED_SPECIMEN | Thailand                         | Magnoliopsida     | 8022                  | 87                       | open commercial | 
| 1.08232207281076   | HUMAN_OBSERVATION  | Spain                            | Gastropoda        | 3049                  | 33                       | total           | 
| 1.08010801080108   | PRESERVED_SPECIMEN | Australia                        | Gastropoda        | 8888                  | 96                       | open commercial | 
| 1.07828750079755   | PRESERVED_SPECIMEN | Austria                          | Insecta           | 15673                 | 169                      | total           | 
| 1.07100848139664   | HUMAN_OBSERVATION  | Australia                        | Insecta           | 32306                 | 346                      | open commercial | 
| 1.0677808727948    | PRESERVED_SPECIMEN | Philippines                      | Malacostraca      | 2154                  | 23                       | total           | 
| 1.06341079165026   | PRESERVED_SPECIMEN | Malaysia                         | Actinopterygii    | 2539                  | 27                       | total           | 
| 1.0611419909045    | PRESERVED_SPECIMEN | New Caledonia                    | Gastropoda        | 3958                  | 42                       | non-commercial  | 
| 1.0611419909045    | PRESERVED_SPECIMEN | New Caledonia                    | Gastropoda        | 3958                  | 42                       | open commercial | 
| 1.050825648724     | PRESERVED_SPECIMEN | Nicaragua                        | Magnoliopsida     | 4663                  | 49                       | non-commercial  | 
| 1.0412018444147    | PRESERVED_SPECIMEN | United States                    | Actinopterygii    | 6723                  | 70                       | open commercial | 
| 1.03973264017824   | HUMAN_OBSERVATION  | United Kingdom                   | Gastropoda        | 2693                  | 28                       | non-commercial  | 
| 1.03973264017824   | HUMAN_OBSERVATION  | United Kingdom                   | Gastropoda        | 2693                  | 28                       | total           | 
| 1.02774922918808   | HUMAN_OBSERVATION  | United States                    | Lecanoromycetes   | 4865                  | 50                       | open commercial | 
| 1.02402520677432   | PRESERVED_SPECIMEN | Malaysia                         | Actinopterygii    | 2539                  | 26                       | non-commercial  | 
| 1.02138090698625   | PRESERVED_SPECIMEN | Philippines                      | Gastropoda        | 7343                  | 75                       | total           | 
| 1.02129239910869   | PRESERVED_SPECIMEN | Spain                            | Insecta           | 16156                 | 165                      | total           | 
| 1.01672679567071   | HUMAN_OBSERVATION  | Spain                            | Gastropoda        | 3049                  | 31                       | non-commercial  | 
| 1.01335789958544   | HUMAN_OBSERVATION  | Slovenia                         | Insecta           | 2171                  | 22                       | total           | 
| 1.01335789958544   | HUMAN_OBSERVATION  | Slovenia                         | Insecta           | 2171                  | 22                       | non-commercial  | 
| 1.0129525074726    | HUMAN_OBSERVATION  | South Africa                     | Liliopsida        | 6022                  | 61                       | open commercial | 
| 1.00827689992476   | PRESERVED_SPECIMEN | Zimbabwe                         | Insecta           | 6645                  | 67                       | total           | 
| 1.00219229564673   | PRESERVED_SPECIMEN | Belize                           | Magnoliopsida     | 3193                  | 32                       | non-commercial  | 
| 1.00182149362477   | PRESERVED_SPECIMEN | Guatemala                        | Liliopsida        | 2196                  | 22                       | non-commercial  | 
| 1.00074128984433   | PRESERVED_SPECIMEN | Bolivia                          | Insecta           | 5396                  | 54                       | non-commercial  | 
| 0.999743655472956  | PRESERVED_SPECIMEN | Papua New Guinea                 | Insecta           | 3901                  | 39                       | open commercial | 
| 0.992131371878207  | PRESERVED_SPECIMEN | Estonia                          | Agaricomycetes    | 2923                  | 29                       | non-commercial  | 
| 0.992131371878207  | PRESERVED_SPECIMEN | Estonia                          | Agaricomycetes    | 2923                  | 29                       | total           | 
| 0.99009900990099   | HUMAN_OBSERVATION  | Australia                        | Gastropoda        | 8888                  | 88                       | non-commercial  | 
| 0.986842105263158  | PRESERVED_SPECIMEN | France                           | Lecanoromycetes   | 2128                  | 21                       | total           | 
| 0.984639621898385  | PRESERVED_SPECIMEN | Malaysia                         | Actinopterygii    | 2539                  | 25                       | open commercial | 
| 0.983416891631315  | PRESERVED_SPECIMEN | Indonesia                        | Actinopterygii    | 5186                  | 51                       | non-commercial  | 
| 0.98120738400133   | PRESERVED_SPECIMEN | Austria                          | Magnoliopsida     | 6013                  | 59                       | open commercial | 
| 0.973906651966189  | PRESERVED_SPECIMEN | Australia                        | Actinopterygii    | 5442                  | 53                       | non-commercial  | 
| 0.973674720519293  | HUMAN_OBSERVATION  | Benin                            | Magnoliopsida     | 2773                  | 27                       | total           | 
| 0.968914008881712  | HUMAN_OBSERVATION  | Russia                           | Liliopsida        | 2477                  | 24                       | non-commercial  | 
| 0.968914008881712  | HUMAN_OBSERVATION  | Russia                           | Liliopsida        | 2477                  | 24                       | total           | 
| 0.967032967032967  | PRESERVED_SPECIMEN | Sudan                            | Magnoliopsida     | 2275                  | 22                       | total           | 
| 0.967032967032967  | PRESERVED_SPECIMEN | Sudan                            | Magnoliopsida     | 2275                  | 22                       | non-commercial  | 
| 0.967032967032967  | PRESERVED_SPECIMEN | Sudan                            | Magnoliopsida     | 2275                  | 22                       | open commercial | 
| 0.966891297978318  | PRESERVED_SPECIMEN | Uganda                           | Insecta           | 3413                  | 33                       | open commercial | 
| 0.963775340644732  | PRESERVED_SPECIMEN | Germany                          | Dothideomycetes   | 3009                  | 29                       | non-commercial  | 
| 0.963775340644732  | PRESERVED_SPECIMEN | Germany                          | Dothideomycetes   | 3009                  | 29                       | total           | 
| 0.963130173062453  | PRESERVED_SPECIMEN | Zimbabwe                         | Insecta           | 6645                  | 64                       | non-commercial  | 
| 0.960799385088393  | PRESERVED_SPECIMEN | Somalia                          | Magnoliopsida     | 2602                  | 25                       | total           | 
| 0.960799385088393  | PRESERVED_SPECIMEN | Somalia                          | Magnoliopsida     | 2602                  | 25                       | open commercial | 
| 0.960799385088393  | PRESERVED_SPECIMEN | Somalia                          | Magnoliopsida     | 2602                  | 25                       | non-commercial  | 
| 0.958188153310104  | PRESERVED_SPECIMEN | Vietnam                          | Insecta           | 2296                  | 22                       | non-commercial  | 
| 0.955734406438632  | HUMAN_OBSERVATION  | Nigeria                          | Magnoliopsida     | 3976                  | 38                       | total           | 
| 0.95553105475928   | PRESERVED_SPECIMEN | Australia                        | Actinopterygii    | 5442                  | 52                       | open commercial | 
| 0.953029271613342  | PRESERVED_SPECIMEN | Papua New Guinea                 | Actinopterygii    | 2938                  | 28                       | non-commercial  | 
| 0.952613580850024  | PRESERVED_SPECIMEN | Costa Rica                       | Liliopsida        | 4094                  | 39                       | open commercial | 
| 0.942782834850455  | PRESERVED_SPECIMEN | Nicaragua                        | Insecta           | 3076                  | 29                       | total           | 
| 0.941681810672394  | HUMAN_OBSERVATION  | Australia                        | Liliopsida        | 6053                  | 57                       | open commercial | 
| 0.936329588014981  | PRESERVED_SPECIMEN | Hungary                          | Magnoliopsida     | 3204                  | 30                       | non-commercial  | 
| 0.935499753815854  | PRESERVED_SPECIMEN | Chile                            | Insecta           | 4062                  | 38                       | open commercial | 
| 0.93232599260569   | PRESERVED_SPECIMEN | Myanmar (Burma)                  | Magnoliopsida     | 6221                  | 58                       | open commercial | 
| 0.930583501006036  | PRESERVED_SPECIMEN | Nigeria                          | Magnoliopsida     | 3976                  | 37                       | non-commercial  | 
| 0.930583501006036  | PRESERVED_SPECIMEN | Nigeria                          | Magnoliopsida     | 3976                  | 37                       | open commercial | 
| 0.927197802197802  | HUMAN_OBSERVATION  | Mexico                           | Malacostraca      | 2912                  | 27                       | total           | 
| 0.927197802197802  | HUMAN_OBSERVATION  | Mexico                           | Malacostraca      | 2912                  | 27                       | non-commercial  | 
| 0.925925925925926  | PRESERVED_SPECIMEN | Czechia                          | Magnoliopsida     | 2592                  | 24                       | total           | 
| 0.919556366699424  | HUMAN_OBSERVATION  | Mexico                           | Insecta           | 28492                 | 262                      | open commercial | 
| 0.910908686958454  | HUMAN_OBSERVATION  | Germany                          | Agaricomycetes    | 4501                  | 41                       | non-commercial  | 
| 0.910908686958454  | HUMAN_OBSERVATION  | Germany                          | Agaricomycetes    | 4501                  | 41                       | total           | 
| 0.909727081875437  | PRESERVED_SPECIMEN | Bulgaria                         | Insecta           | 4287                  | 39                       | total           | 
| 0.895188362551287  | PRESERVED_SPECIMEN | Brazil                           | Aves              | 2681                  | 24                       | non-commercial  | 
| 0.894425810573391  | HUMAN_OBSERVATION  | Australia                        | Malacostraca      | 6261                  | 56                       | total           | 
| 0.892758734707374  | PRESERVED_SPECIMEN | Congo - Kinshasa                 | Magnoliopsida     | 9073                  | 81                       | non-commercial  | 
| 0.876918258690886  | PRESERVED_SPECIMEN | Belize                           | Magnoliopsida     | 3193                  | 28                       | open commercial | 
| 0.873146622734761  | PRESERVED_SPECIMEN | New Zealand                      | Insecta           | 6070                  | 53                       | non-commercial  | 
| 0.870353581142339  | PRESERVED_SPECIMEN | Portugal                         | Insecta           | 5515                  | 48                       | total           | 
| 0.859693596384878  | PRESERVED_SPECIMEN | Congo - Kinshasa                 | Magnoliopsida     | 9073                  | 78                       | open commercial | 
| 0.856007337205748  | PRESERVED_SPECIMEN | Uganda                           | Magnoliopsida     | 3271                  | 28                       | total           | 
| 0.85278276481149   | HUMAN_OBSERVATION  | United States                    | Malacostraca      | 6684                  | 57                       | open commercial | 
| 0.85111086548027   | PRESERVED_SPECIMEN | United States                    | Gastropoda        | 18094                 | 154                      | total           | 
| 0.844694724362774  | PRESERVED_SPECIMEN | Guatemala                        | Magnoliopsida     | 6748                  | 57                       | non-commercial  | 
| 0.83210964268233   | PRESERVED_SPECIMEN | Panama                           | Insecta           | 8172                  | 68                       | open commercial | 
| 0.83073727933541   | PRESERVED_SPECIMEN | Romania                          | Magnoliopsida     | 2889                  | 24                       | non-commercial  | 
| 0.824083417423478  | HUMAN_OBSERVATION  | Mexico                           | Gastropoda        | 5946                  | 49                       | total           | 
| 0.816882232811436  | PRESERVED_SPECIMEN | Papua New Guinea                 | Actinopterygii    | 2938                  | 24                       | open commercial | 
| 0.807265388496468  | HUMAN_OBSERVATION  | Mexico                           | Gastropoda        | 5946                  | 48                       | non-commercial  | 
| 0.806057645334636  | HUMAN_OBSERVATION  | Costa Rica                       | Liliopsida        | 4094                  | 33                       | total           | 
| 0.806057645334636  | HUMAN_OBSERVATION  | Costa Rica                       | Liliopsida        | 4094                  | 33                       | non-commercial  | 
| 0.804644530454268  | PRESERVED_SPECIMEN | India                            | Insecta           | 9818                  | 79                       | open commercial | 
| 0.798458149779736  | PRESERVED_SPECIMEN | Germany                          | Magnoliopsida     | 10896                 | 87                       | open commercial | 
| 0.790590050134979  | PRESERVED_SPECIMEN | Indonesia                        | Actinopterygii    | 5186                  | 41                       | open commercial | 
| 0.78581503123111   | HUMAN_OBSERVATION  | Australia                        | Arachnida         | 4963                  | 39                       | non-commercial  | 
| 0.785175879396985  | PRESERVED_SPECIMEN | Poland                           | Magnoliopsida     | 3184                  | 25                       | total           | 
| 0.783353733170135  | HUMAN_OBSERVATION  | United Kingdom                   | Agaricomycetes    | 4085                  | 32                       | total           | 
| 0.783289817232376  | PRESERVED_SPECIMEN | Brazil                           | Aves              | 2681                  | 21                       | open commercial | 
| 0.771493952271984  | PRESERVED_SPECIMEN | Italy                            | Insecta           | 15295                 | 118                      | total           | 
| 0.764292265362275  | PRESERVED_SPECIMEN | Uganda                           | Magnoliopsida     | 3271                  | 25                       | non-commercial  | 
| 0.764292265362275  | PRESERVED_SPECIMEN | Uganda                           | Magnoliopsida     | 3271                  | 25                       | open commercial | 
| 0.760324866079143  | HUMAN_OBSERVATION  | Greece                           | Magnoliopsida     | 5787                  | 44                       | non-commercial  | 
| 0.760324866079143  | HUMAN_OBSERVATION  | Greece                           | Magnoliopsida     | 5787                  | 44                       | total           | 
| 0.758873929008568  | HUMAN_OBSERVATION  | United Kingdom                   | Agaricomycetes    | 4085                  | 31                       | non-commercial  | 
| 0.754345687110528  | PRESERVED_SPECIMEN | Spain                            | Gastropoda        | 3049                  | 23                       | non-commercial  | 
| 0.754345687110528  | PRESERVED_SPECIMEN | Spain                            | Gastropoda        | 3049                  | 23                       | total           | 
| 0.74102223066692   | PRESERVED_SPECIMEN | Brazil                           | Actinopterygii    | 5263                  | 39                       | open commercial | 
| 0.739247311827957  | PRESERVED_SPECIMEN | Iran                             | Insecta           | 2976                  | 22                       | non-commercial  | 
| 0.736648250460405  | PRESERVED_SPECIMEN | Trinidad & Tobago                | Insecta           | 3258                  | 24                       | open commercial | 
| 0.733998825601879  | HUMAN_OBSERVATION  | Germany                          | Arachnida         | 3406                  | 25                       | total           | 
| 0.733998825601879  | HUMAN_OBSERVATION  | Germany                          | Arachnida         | 3406                  | 25                       | non-commercial  | 
| 0.732839345330185  | HUMAN_OBSERVATION  | China                            | Insecta           | 12281                 | 90                       | total           | 
| 0.726312314295147  | PRESERVED_SPECIMEN | Brazil                           | Lecanoromycetes   | 3029                  | 22                       | total           | 
| 0.719913067101331  | HUMAN_OBSERVATION  | Colombia                         | Magnoliopsida     | 22086                 | 159                      | total           | 
| 0.719913067101331  | HUMAN_OBSERVATION  | Colombia                         | Magnoliopsida     | 22086                 | 159                      | non-commercial  | 
| 0.718620249121686  | PRESERVED_SPECIMEN | France                           | Insecta           | 25048                 | 180                      | total           | 
| 0.715214564369311  | PRESERVED_SPECIMEN | Nicaragua                        | Insecta           | 3076                  | 22                       | non-commercial  | 
| 0.707675557974959  | PRESERVED_SPECIMEN | United States                    | Mammalia          | 5511                  | 39                       | non-commercial  | 
| 0.705912013109795  | PRESERVED_SPECIMEN | Greece                           | Insecta           | 7933                  | 56                       | non-commercial  | 
| 0.70382129059404   | HUMAN_OBSERVATION  | Mexico                           | Magnoliopsida     | 26143                 | 184                      | open commercial | 
| 0.696849030470914  | PRESERVED_SPECIMEN | Germany                          | Insecta           | 23104                 | 161                      | non-commercial  | 
| 0.694444444444444  | HUMAN_OBSERVATION  | Gabon                            | Magnoliopsida     | 4608                  | 32                       | total           | 
| 0.694168980563269  | PRESERVED_SPECIMEN | Honduras                         | Magnoliopsida     | 5042                  | 35                       | non-commercial  | 
| 0.688750409970482  | PRESERVED_SPECIMEN | Spain                            | Gastropoda        | 3049                  | 21                       | open commercial | 
| 0.687791697371653  | PRESERVED_SPECIMEN | Indonesia                        | Insecta           | 12213                 | 84                       | open commercial | 
| 0.687222526302986  | HUMAN_OBSERVATION  | Netherlands                      | Insecta           | 16443                 | 113                      | total           | 
| 0.684218354901086  | HUMAN_OBSERVATION  | United States                    | Actinopterygii    | 6723                  | 46                       | open commercial | 
| 0.681723563696919  | HUMAN_OBSERVATION  | South Africa                     | Magnoliopsida     | 19216                 | 131                      | open commercial | 
| 0.681140911025969  | HUMAN_OBSERVATION  | Netherlands                      | Insecta           | 16443                 | 112                      | non-commercial  | 
| 0.678925035360679  | PRESERVED_SPECIMEN | Ghana                            | Magnoliopsida     | 3535                  | 24                       | total           | 
| 0.67369654364382   | HUMAN_OBSERVATION  | Croatia                          | Insecta           | 3414                  | 23                       | total           | 
| 0.671560206153366  | HUMAN_OBSERVATION  | Switzerland                      | Insecta           | 6403                  | 43                       | total           | 
| 0.665124349334876  | HUMAN_OBSERVATION  | Italy                            | Gastropoda        | 3458                  | 23                       | total           | 
| 0.662800331400166  | PRESERVED_SPECIMEN | Mexico                           | Actinopterygii    | 3621                  | 24                       | total           | 
| 0.655430711610487  | PRESERVED_SPECIMEN | Hungary                          | Magnoliopsida     | 3204                  | 21                       | open commercial | 
| 0.652439853201033  | HUMAN_OBSERVATION  | Australia                        | Magnoliopsida     | 22071                 | 144                      | open commercial | 
| 0.651986714232993  | PRESERVED_SPECIMEN | Taiwan                           | Insecta           | 8129                  | 53                       | non-commercial  | 
| 0.651412751404609  | PRESERVED_SPECIMEN | China                            | Insecta           | 12281                 | 80                       | non-commercial  | 
| 0.651412751404609  | HUMAN_OBSERVATION  | China                            | Insecta           | 12281                 | 80                       | non-commercial  | 
| 0.644405389572349  | PRESERVED_SPECIMEN | Croatia                          | Insecta           | 3414                  | 22                       | non-commercial  | 
| 0.643362642075917  | PRESERVED_SPECIMEN | Nicaragua                        | Magnoliopsida     | 4663                  | 30                       | open commercial | 
| 0.640324847727628  | HUMAN_OBSERVATION  | Switzerland                      | Insecta           | 6403                  | 41                       | non-commercial  | 
| 0.631136044880785  | PRESERVED_SPECIMEN | Tanzania                         | Insecta           | 5704                  | 36                       | open commercial | 
| 0.630475722590682  | HUMAN_OBSERVATION  | Indonesia                        | Insecta           | 12213                 | 77                       | total           | 
| 0.622347949080622  | PRESERVED_SPECIMEN | Ghana                            | Magnoliopsida     | 3535                  | 22                       | non-commercial  | 
| 0.622347949080622  | PRESERVED_SPECIMEN | Ghana                            | Magnoliopsida     | 3535                  | 22                       | open commercial | 
| 0.616937745372967  | PRESERVED_SPECIMEN | Sri Lanka                        | Insecta           | 3566                  | 22                       | open commercial | 
| 0.615114235500879  | HUMAN_OBSERVATION  | Croatia                          | Insecta           | 3414                  | 21                       | non-commercial  | 
| 0.614612188365651  | PRESERVED_SPECIMEN | Germany                          | Insecta           | 23104                 | 142                      | open commercial | 
| 0.612518343648312  | HUMAN_OBSERVATION  | Austria                          | Insecta           | 15673                 | 96                       | total           | 
| 0.609893833295686  | PRESERVED_SPECIMEN | Mozambique                       | Magnoliopsida     | 4427                  | 27                       | open commercial | 
| 0.609893833295686  | PRESERVED_SPECIMEN | Mozambique                       | Magnoliopsida     | 4427                  | 27                       | non-commercial  | 
| 0.597768331562168  | HUMAN_OBSERVATION  | Belgium                          | Insecta           | 7528                  | 45                       | total           | 
| 0.597723737001556  | HUMAN_OBSERVATION  | Indonesia                        | Insecta           | 12213                 | 73                       | non-commercial  | 
| 0.597065847833504  | PRESERVED_SPECIMEN | Turkey                           | Insecta           | 5862                  | 35                       | total           | 
| 0.579950289975145  | PRESERVED_SPECIMEN | Mexico                           | Actinopterygii    | 3621                  | 21                       | non-commercial  | 
| 0.576036866359447  | HUMAN_OBSERVATION  | Czechia                          | Insecta           | 5208                  | 30                       | total           | 
| 0.574235947170293  | HUMAN_OBSERVATION  | Austria                          | Insecta           | 15673                 | 90                       | non-commercial  | 
| 0.572337042925278  | PRESERVED_SPECIMEN | Philippines                      | Insecta           | 6290                  | 36                       | open commercial | 
| 0.571200850159405  | HUMAN_OBSERVATION  | Belgium                          | Insecta           | 7528                  | 43                       | non-commercial  | 
| 0.56980056980057   | PRESERVED_SPECIMEN | Japan                            | Insecta           | 17550                 | 100                      | total           | 
| 0.568828213879408  | HUMAN_OBSERVATION  | Japan                            | Magnoliopsida     | 7032                  | 40                       | non-commercial  | 
| 0.568828213879408  | HUMAN_OBSERVATION  | Japan                            | Magnoliopsida     | 7032                  | 40                       | total           | 
| 0.56852184320766   | PRESERVED_SPECIMEN | United States                    | Malacostraca      | 6684                  | 38                       | non-commercial  | 
| 0.562236451663283  | PRESERVED_SPECIMEN | Switzerland                      | Insecta           | 6403                  | 36                       | total           | 
| 0.557620817843866  | PRESERVED_SPECIMEN | Bhutan                           | Magnoliopsida     | 4842                  | 27                       | total           | 
| 0.557620817843866  | PRESERVED_SPECIMEN | Bhutan                           | Magnoliopsida     | 4842                  | 27                       | non-commercial  | 
| 0.552669393169006  | HUMAN_OBSERVATION  | United States                    | Gastropoda        | 18094                 | 100                      | open commercial | 
| 0.551405193881181  | PRESERVED_SPECIMEN | NA                               | Aves              | 5622                  | 31                       | total           | 
| 0.550505697093842  | HUMAN_OBSERVATION  | Ecuador                          | Liliopsida        | 7811                  | 43                       | non-commercial  | 
| 0.550505697093842  | HUMAN_OBSERVATION  | Ecuador                          | Liliopsida        | 7811                  | 43                       | total           | 
| 0.537634408602151  | HUMAN_OBSERVATION  | Czechia                          | Insecta           | 5208                  | 28                       | non-commercial  | 
| 0.533491404860699  | PRESERVED_SPECIMEN | Guatemala                        | Magnoliopsida     | 6748                  | 36                       | open commercial | 
| 0.532309977717257  | PRESERVED_SPECIMEN | Spain                            | Insecta           | 16156                 | 86                       | non-commercial  | 
| 0.528707912067526  | HUMAN_OBSERVATION  | Colombia                         | Insecta           | 10781                 | 57                       | total           | 
| 0.525369832711185  | HUMAN_OBSERVATION  | United States                    | Bivalvia          | 7233                  | 38                       | open commercial | 
| 0.523638539796529  | PRESERVED_SPECIMEN | United States                    | Malacostraca      | 6684                  | 35                       | open commercial | 
| 0.510156757258139  | HUMAN_OBSERVATION  | Colombia                         | Insecta           | 10781                 | 55                       | non-commercial  | 
| 0.507263085081854  | PRESERVED_SPECIMEN | Brazil                           | Arachnida         | 4337                  | 22                       | total           | 
| 0.507263085081854  | PRESERVED_SPECIMEN | Brazil                           | Arachnida         | 4337                  | 22                       | non-commercial  | 
| 0.499119201409278  | PRESERVED_SPECIMEN | New Zealand                      | Magnoliopsida     | 6812                  | 34                       | non-commercial  | 
| 0.498919008814236  | HUMAN_OBSERVATION  | Austria                          | Magnoliopsida     | 6013                  | 30                       | total           | 
| 0.496331463098835  | PRESERVED_SPECIMEN | Japan                            | Actinopterygii    | 4634                  | 23                       | total           | 
| 0.49583498611662   | PRESERVED_SPECIMEN | Honduras                         | Magnoliopsida     | 5042                  | 25                       | open commercial | 
| 0.48443922489724   | PRESERVED_SPECIMEN | New Zealand                      | Magnoliopsida     | 6812                  | 33                       | open commercial | 
| 0.483172275908031  | HUMAN_OBSERVATION  | South Korea                      | Insecta           | 6002                  | 29                       | open commercial | 
| 0.482288375187095  | HUMAN_OBSERVATION  | Austria                          | Magnoliopsida     | 6013                  | 29                       | non-commercial  | 
| 0.47886393659181   | PRESERVED_SPECIMEN | United States                    | Arachnida         | 6056                  | 29                       | total           | 
| 0.473352033660589  | HUMAN_OBSERVATION  | Tanzania                         | Insecta           | 5704                  | 27                       | total           | 
| 0.470904809956273  | PRESERVED_SPECIMEN | Mexico                           | Gastropoda        | 5946                  | 28                       | total           | 
| 0.470742072572736  | PRESERVED_SPECIMEN | Italy                            | Insecta           | 15295                 | 72                       | non-commercial  | 
| 0.461285008237232  | PRESERVED_SPECIMEN | New Zealand                      | Insecta           | 6070                  | 28                       | open commercial | 
| 0.460122699386503  | PRESERVED_SPECIMEN | United States                    | Cephalopoda       | 4564                  | 21                       | total           | 
| 0.450883287752236  | PRESERVED_SPECIMEN | Sweden                           | Magnoliopsida     | 13529                 | 61                       | open commercial | 
| 0.439262039773181  | HUMAN_OBSERVATION  | Canada                           | Insecta           | 25042                 | 110                      | open commercial | 
| 0.437818009702994  | HUMAN_OBSERVATION  | Colombia                         | Liliopsida        | 8451                  | 37                       | total           | 
| 0.437818009702994  | HUMAN_OBSERVATION  | Colombia                         | Liliopsida        | 8451                  | 37                       | non-commercial  | 
| 0.437268752102254  | PRESERVED_SPECIMEN | Mexico                           | Gastropoda        | 5946                  | 26                       | non-commercial  | 
| 0.437268752102254  | PRESERVED_SPECIMEN | Mexico                           | Gastropoda        | 5946                  | 26                       | open commercial | 
| 0.43517679057117   | PRESERVED_SPECIMEN | Portugal                         | Insecta           | 5515                  | 24                       | non-commercial  | 
| 0.429645542427497  | PRESERVED_SPECIMEN | Nepal                            | Magnoliopsida     | 5586                  | 24                       | open commercial | 
| 0.42647560559536   | PRESERVED_SPECIMEN | Turkey                           | Insecta           | 5862                  | 25                       | non-commercial  | 
| 0.424197713021025  | HUMAN_OBSERVATION  | Belgium                          | Magnoliopsida     | 10844                 | 46                       | non-commercial  | 
| 0.424197713021025  | HUMAN_OBSERVATION  | Belgium                          | Magnoliopsida     | 10844                 | 46                       | total           | 
| 0.423187480038326  | PRESERVED_SPECIMEN | France                           | Insecta           | 25048                 | 106                      | non-commercial  | 
| 0.420757363253857  | HUMAN_OBSERVATION  | Tanzania                         | Insecta           | 5704                  | 24                       | non-commercial  | 
| 0.417661097852029  | PRESERVED_SPECIMEN | Mexico                           | Insecta           | 28492                 | 119                      | open commercial | 
| 0.415012630819199  | PRESERVED_SPECIMEN | Venezuela                        | Insecta           | 5542                  | 23                       | open commercial | 
| 0.406804733727811  | HUMAN_OBSERVATION  | Argentina                        | Insecta           | 8112                  | 33                       | total           | 
| 0.405617806621711  | PRESERVED_SPECIMEN | Costa Rica                       | Insecta           | 19723                 | 80                       | open commercial | 
| 0.402402030582554  | PRESERVED_SPECIMEN | Australia                        | Insecta           | 32306                 | 130                      | open commercial | 
| 0.39488232506713   | HUMAN_OBSERVATION  | Chile                            | Magnoliopsida     | 6331                  | 25                       | total           | 
| 0.39488232506713   | HUMAN_OBSERVATION  | Chile                            | Magnoliopsida     | 6331                  | 25                       | non-commercial  | 
| 0.394477317554241  | HUMAN_OBSERVATION  | Argentina                        | Insecta           | 8112                  | 32                       | non-commercial  | 
| 0.383325347388596  | HUMAN_OBSERVATION  | Australia                        | Malacostraca      | 6261                  | 24                       | non-commercial  | 
| 0.379788639365918  | PRESERVED_SPECIMEN | United States                    | Arachnida         | 6056                  | 23                       | non-commercial  | 
| 0.372130724733798  | PRESERVED_SPECIMEN | Brazil                           | Insecta           | 27141                 | 101                      | open commercial | 
| 0.361077336870417  | HUMAN_OBSERVATION  | Brazil                           | Insecta           | 27141                 | 98                       | total           | 
| 0.353708411628164  | PRESERVED_SPECIMEN | United States                    | Gastropoda        | 18094                 | 64                       | non-commercial  | 
| 0.35183112106189   | PRESERVED_SPECIMEN | Japan                            | Gastropoda        | 6253                  | 22                       | non-commercial  | 
| 0.35183112106189   | PRESERVED_SPECIMEN | Japan                            | Gastropoda        | 6253                  | 22                       | total           | 
| 0.351699882766706  | HUMAN_OBSERVATION  | France                           | Gastropoda        | 7677                  | 27                       | total           | 
| 0.351699882766706  | HUMAN_OBSERVATION  | France                           | Gastropoda        | 7677                  | 27                       | non-commercial  | 
| 0.345821325648415  | HUMAN_OBSERVATION  | Netherlands                      | Magnoliopsida     | 6940                  | 24                       | total           | 
| 0.345821325648415  | HUMAN_OBSERVATION  | Netherlands                      | Magnoliopsida     | 6940                  | 24                       | non-commercial  | 
| 0.342655023764784  | HUMAN_OBSERVATION  | Brazil                           | Insecta           | 27141                 | 93                       | non-commercial  | 
| 0.336182336182336  | PRESERVED_SPECIMEN | Japan                            | Insecta           | 17550                 | 59                       | non-commercial  | 
| 0.334448160535117  | PRESERVED_SPECIMEN | Indonesia                        | Gastropoda        | 6578                  | 22                       | non-commercial  | 
| 0.334448160535117  | PRESERVED_SPECIMEN | Indonesia                        | Gastropoda        | 6578                  | 22                       | total           | 
| 0.332741792369122  | PRESERVED_SPECIMEN | NA                               | Liliopsida        | 13524                 | 45                       | total           | 
| 0.325648039598802  | PRESERVED_SPECIMEN | France                           | Gastropoda        | 7677                  | 25                       | total           | 
| 0.319245971419884  | PRESERVED_SPECIMEN | Indonesia                        | Gastropoda        | 6578                  | 21                       | open commercial | 
| 0.304827813478333  | HUMAN_OBSERVATION  | Malaysia                         | Magnoliopsida     | 12138                 | 37                       | total           | 
| 0.304827813478333  | HUMAN_OBSERVATION  | Malaysia                         | Magnoliopsida     | 12138                 | 37                       | non-commercial  | 
| 0.304758587661631  | PRESERVED_SPECIMEN | South Africa                     | Insecta           | 22969                 | 70                       | open commercial | 
| 0.304321363359708  | PRESERVED_SPECIMEN | Poland                           | Insecta           | 9858                  | 30                       | total           | 
| 0.304161482095949  | PRESERVED_SPECIMEN | United States                    | Bivalvia          | 7233                  | 22                       | total           | 
| 0.300457217504899  | PRESERVED_SPECIMEN | Ecuador                          | Insecta           | 7655                  | 23                       | open commercial | 
| 0.299605066049299  | PRESERVED_SPECIMEN | Philippines                      | Gastropoda        | 7343                  | 22                       | non-commercial  | 
| 0.29407290980074   | HUMAN_OBSERVATION  | Costa Rica                       | Insecta           | 19723                 | 58                       | total           | 
| 0.29407290980074   | HUMAN_OBSERVATION  | Costa Rica                       | Insecta           | 19723                 | 58                       | non-commercial  | 
| 0.283455764931332  | PRESERVED_SPECIMEN | France                           | Insecta           | 25048                 | 71                       | open commercial | 
| 0.278267322140803  | PRESERVED_SPECIMEN | Colombia                         | Insecta           | 10781                 | 30                       | open commercial | 
| 0.272344639762317  | PRESERVED_SPECIMEN | Spain                            | Insecta           | 16156                 | 44                       | open commercial | 
| 0.27063599458728   | HUMAN_OBSERVATION  | Taiwan                           | Insecta           | 8129                  | 22                       | open commercial | 
| 0.259965337954939  | HUMAN_OBSERVATION  | Spain                            | Insecta           | 16156                 | 42                       | open commercial | 
| 0.233618233618234  | HUMAN_OBSERVATION  | Japan                            | Insecta           | 17550                 | 41                       | non-commercial  | 
| 0.233618233618234  | HUMAN_OBSERVATION  | Japan                            | Insecta           | 17550                 | 41                       | total           | 
| 0.232537340130579  | PRESERVED_SPECIMEN | Peru                             | Insecta           | 11181                 | 26                       | open commercial | 
| 0.232121145130983  | PRESERVED_SPECIMEN | United States                    | Gastropoda        | 18094                 | 42                       | open commercial | 
| 0.229297116147808  | HUMAN_OBSERVATION  | Argentina                        | Magnoliopsida     | 11339                 | 26                       | total           | 
| 0.229297116147808  | HUMAN_OBSERVATION  | Argentina                        | Magnoliopsida     | 11339                 | 26                       | non-commercial  | 
| 0.219851803599055  | PRESERVED_SPECIMEN | China                            | Insecta           | 12281                 | 27                       | open commercial | 
| 0.217964492880998  | PRESERVED_SPECIMEN | United States                    | Insecta           | 85335                 | 186                      | open commercial | 
| 0.217837543462779  | HUMAN_OBSERVATION  | Sweden                           | Insecta           | 23871                 | 52                       | total           | 
| 0.21389284986759   | HUMAN_OBSERVATION  | India                            | Insecta           | 9818                  | 21                       | open commercial | 
| 0.213648359934649  | HUMAN_OBSERVATION  | Sweden                           | Insecta           | 23871                 | 51                       | non-commercial  | 
| 0.203458799593082  | PRESERVED_SPECIMEN | NA                               | Magnoliopsida     | 57997                 | 118                      | total           | 
| 0.201731942530998  | HUMAN_OBSERVATION  | Peru                             | Magnoliopsida     | 20324                 | 41                       | non-commercial  | 
| 0.201731942530998  | HUMAN_OBSERVATION  | Peru                             | Magnoliopsida     | 20324                 | 41                       | total           | 
| 0.195840086439762  | HUMAN_OBSERVATION  | Ecuador                          | Magnoliopsida     | 14808                 | 29                       | non-commercial  | 
| 0.195840086439762  | HUMAN_OBSERVATION  | Ecuador                          | Magnoliopsida     | 14808                 | 29                       | total           | 
| 0.194566048224585  | PRESERVED_SPECIMEN | Finland                          | Insecta           | 14391                 | 28                       | total           | 
| 0.182448458310527  | PRESERVED_SPECIMEN | Netherlands                      | Insecta           | 16443                 | 30                       | total           | 
| 0.182448458310527  | PRESERVED_SPECIMEN | Netherlands                      | Insecta           | 16443                 | 30                       | non-commercial  | 
| 0.169990192873488  | PRESERVED_SPECIMEN | Italy                            | Insecta           | 15295                 | 26                       | open commercial | 
| 0.159509985325081  | PRESERVED_SPECIMEN | Austria                          | Insecta           | 15673                 | 25                       | non-commercial  | 
| 0.155738359555946  | PRESERVED_SPECIMEN | Canada                           | Insecta           | 25042                 | 39                       | open commercial | 
| 0.152873323605031  | PRESERVED_SPECIMEN | Finland                          | Insecta           | 14391                 | 22                       | non-commercial  | 
| 0.11729713878765   | PRESERVED_SPECIMEN | Sweden                           | Insecta           | 23871                 | 28                       | total           | 
| 0.0586237219166509 | PRESERVED_SPECIMEN | NA                               | Magnoliopsida     | 57997                 | 34                       | non-commercial  | 
| 0.0568994948014552 | PRESERVED_SPECIMEN | NA                               | Magnoliopsida     | 57997                 | 33                       | open commercial | 








