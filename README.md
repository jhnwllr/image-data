
# GBIF image data

**Basis of record** tells us roughly whether an image was collected in situ (**human observation** like with a phone) or was collected or digitized by a museum (**preserved specimen**). Plants are often collected by museums as **preserved specimens** aka "herbarium sheets". For simplicity I have ignored other types of basis of record, since there are very few images with other types of basis of record :

https://www.gbif.org/occurrence/search?basis_of_record=FOSSIL_SPECIMEN&basis_of_record=LIVING_SPECIMEN&basis_of_record=UNKNOWN&basis_of_record=LITERATURE&basis_of_record=MATERIAL_SAMPLE&basis_of_record=MACHINE_OBSERVATION&basis_of_record=OBSERVATION&media_type=StillImage

# Licensces 

There are many types of licenses. I have mostly broken things down into **non-commercial** and **commercial**. **Non-commerical** meaning anyone normal private citizen can use the photo not for profit. And **commercial** meaning a business could use the image to make a profit. 

# Image counts 

Below I look at raw image counts on GBIF. 

## Images counts by kingdom, basisofrecord, and license

Two things to notice here: 

* There are a lot of "herbarium sheets" (preserved specimens) for plants.
* There are very few human observations available for commercial use. 

**iNaturalist** images are **licensed as non-commercial** on GBIF, but might still be available? Still there are millions of images available through the GBIF network. 

<img src="https://raw.githubusercontent.com/jhnwllr/image-data/master/plots/kingdomBORBarplot.png" alt="imagedata" width = "700"/>

## Here I have images broken down by class, basisofrecord, and license

At a lower taxonomic level we see that **flowering plants (magnoliopsida, liliopsida)** have many many images. Many are probably "herbarium sheets" (preserved specimens), but there are still millions of human observations. Again howevers **commercial use** might be difficult for many groups...

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

**Percent coverage (num. sp. >10 img/total num. sp. in class)**. Here we see that global image coverage is quite poor for most groups with the exception of maybe **Aves** (birds) and a few plant classes (**Pinopsida**, **Lycopodiopsida**, **Polypodiopsida**), although many of these plant classes are "preserved specimens" aka probably herbarium sheets. Other groups have very poor global image coverage even considering preserved museum specimens. 

The global look for images for commercial use is even worse, although there is reasonable non-commercial (open access) image coverage. 

**Species counts** were taken from **GBIF backbone** and probably should be interpreted with caution. Duplicates might explain why we see >100% in some cases. A better measure might be the total number of species for which we have **at least 1 occurrence**. Still this graphs shows that **regional breakdowns** are probably necessary for an image dataset with good coverage. 

![](https://raw.githubusercontent.com/jhnwllr/image-data/master/plots/percentageCoverageBarplot.png)

# Possible good regional image datasets

<iframe src="https://jhnwllr.github.io/charts/franceGrid.html" style="border: none; height: 600px; width: 100%;"></iframe>













