---
title: How to efficiently offer support/resources to train students who might start studying SDM approaches but need a lot of guidance to get going?
description: 
background: 
    img: https://inaturalist-open-data.s3.amazonaws.com/photos/72261586/large.jpeg
    by: J. Richard Abbott
    href: https://www.inaturalist.org/people/jrichardabbott
  
permalink: /faqs/new-to-SDMs/
toc: true
comments: true
navigation: faqs-navigation
---

By: 
[Courtney Burk]({{ 'best-practices-wg-team/#Courtney+Burk' | relative_url }}), [Alana Westwood]({{ 'best-practices-wg-team/#Dr.+Alana+Westwood' | relative_url }}), and [Robert Buchkowski]({{ 'best-practices-wg-team/#Dr.+Robert+Buchkowski' | relative_url }})

So, you want to learn how to create and utilize SDMs.? First, what is an SDM? An SDM, or a species
distribution model is a now common method in the fields of biogeography, ecology, and conservation
to predict species distribution, movement, and/or abundance across a landscape. You’ve probably heard
several terms that all fall under the umbrella of species distribution modelling, including habitat models,
climate envelopes, ecological niche models (ENMs), resource selection functions (RSFs), bioclimatic
models, connectivity models, and range maps. SDMs use algorithms to fit mathematical functions that
describe species presence/absence across environmental space and the relationship to each
environmental variable and then generate predictive maps of species distribution in geographical
space, aka predictive forecasting (Figure 1). In some cases, SDMs are used to explain or understand how
environmental conditions influence the occurrence or abundance of a species.


![Figure provided by Zurell, 2020.](../assets/images/Zurell2020.png)
<br>Figure 1: The main modelling cycle in species distribution modelling (Zurell, 2020).


There are two main data components to an SDM: (1) species data and (2) environmental data. Species
data can comprise presence-only data (just where that species has been observed), presence-absence
data (known presence and absence locations based on surveys), abundance-absence data (which
includes counts), or occupancy data (repeated site surveys). Regardless of the data type you need to have
coordinates of the locations where the species of interest occurred (or <i>didn’t</i> occur). These can be
archived species location data, such as from museum records or citizen science initiatives
(e.g., ebird, iNaturalist, FrogWatch, etc.), or a new dataset you collect in the field. 
Environmental data is both the biotic and abiotic conditions that describe where a
species is present or absent. Now, there are dozens of variables to choose from to incorporate into your
SDM. The variables you choose largely depend on the scale of your model and the completeness of data
available.

But how much data do you need? Where do you get this data? What do I do? Unfortunately, this is not
the place to learn all the ins and outs for SDMs.

As you explore SDMs, there are <b>hundreds</b> of resources out there and available to help you meet
your needs with learning how to utilize this powerful data tool to your advantage. However, we have
put together a shortlist of platforms and base programs to choose from (Table 1). Each
of them has their benefits, caveats, and data requirements. Table 1, a non-exhaustive list, describes
some commonly used platforms, required data, and links to further tutorials or readings to help you on
your way! 

Table 1: Modelling methods, type of species data required, and suggested further reading.

| <b>Method</b> | <b>Model Name/Software</b> | <b>Type</b> | <b>Species Data Type</b> | <b>Links for Further Learning</b> |
| Climatic envelope | BIOCLIM | Probability | Presence-only  | <a href="https://cran.r-project.org/web/packages/dismo/dismo.pdf">R tutorial</a>; <a href="https://onlinelibrary-wiley-com.proxy.hil.unb.ca/doi/full/10.1111/aec.12628">Booth, 2019</a> |
| Gower metric | DOMAIN | Probability | Presence-only  | <a href="https://www.whoi.edu/cms/files/Carpenter_etal_2003_53463.pdf">Carpenter et al., 1993</a>; <a href="https://cran.r-project.org/web/packages/dismo/dismo.pdf">R tutorial</a> |
| Ecological niche factor analysis (ENFA) | BIOMAPPER | Suitability | Presence/background | <a href="https://www2.unil.ch/biomapper/">BioMapper tutorial</a> |
| Maximum entropy | MAXENT | Suitability | Presence/background | <a href="https://www.youtube.com/watch?v=f9vwrZf6ncU">YouTube tutorial</a>; <a href="https://naturalis.github.io/mebioda/doc/week2/w2d5/Mebioda_PracticalManual_2019.pdf">Maxent step by step</a> |
| Genetic algorithm | GARP | Suitability | Presence/pseudoabsence | <a href="https://onlinelibrary-wiley-com.proxy.hil.unb.ca/doi/full/10.1111/ecog.05642">Haase et al., 2021</a>; <a href="http://www.bio-nica.info/Biblioteca/lee2004guidegarp.pdf">Tutorial</a> |
| Regression: generalized linear model (GLM) and generalized additive model (GAM) | GRASP | Probability | Presence/absence | <a href="https://www.researchgate.net/profile/Daniele_Ventura/post/What_is_the_best_way_of_analyzing_spatial_and_temporal_variation_in_species_composition_and_abundance_dataset/attachment/59d62fcf79197b807798df01/AS:359897272209408@1462817604512/download/Script_ModRegress.pdf">Tutorial</a>; <a href="https://www-sciencedirect-com.proxy.hil.unb.ca/science/article/pii/S0304380002002041">Guisan et al., 2002</a> |
| Artificial neural network (ANN) | SPECIES, MATLAB | Probability | Presence/absence | <a href="https://support.bccvl.org.au/support/solutions/articles/6000083200-artificial-neural-network">Introduction</a>; <a href="https://www.youtube.com/watch?v=ySwD2tYhtmQ">YouTube tutorial</a> |
| Classification and regression trees (CART) | BIOMOD | Probability | Presence/absence | <a href="https://www.researchgate.net/profile/Daniele_Ventura/post/What_is_the_best_way_of_analyzing_spatial_and_temporal_variation_in_species_composition_and_abundance_dataset/attachment/59d62fcf79197b807798df01/AS:359897272209408@1462817604512/download/Script_ModRegress.pdf">Tutorial</a> |
| Multivariate adaptive regression splines (MARS) | MARS (with R) | Probability | Presence/absence | <a href="https://support.biosecuritycommons.org.au/support/solutions/articles/6000262276-multivariate-adaptive-regression-splines-mars-sdm-explained">Introduction</a>; <a href="https://onlinelibrary.wiley.com/doi/full/10.1111/j.1472-4642.2007.00340.x">Elith and Leathwick, 2007</a>; <a href="http://www.r-gators.com/2018/01/24/introduction-to-species-distribution-models/">R tutorial</a> |
| Favourability function (FF) | FF (with R) | Probability | Presence/absence | <a href="https://biogeografia-uma.com/wp-content/uploads/2018/09/The_favourability_function.pdf">Introduction</a>; <a href="https://fuzzysim.r-forge.r-project.org/fuzzySim-modelling-tutorial.html">R tutorial</a> |
| Random forest (RF) | RF (with R) | Probability | Presence/background | <a href="https://onlinelibrary-wiley-com.proxy.hil.unb.ca/doi/10.1111/ecog.05615">Valavi et al., 2021</a> |
| Boosted regression trees (BRT) | BRT (with R) | Probability | Presence/absence | <a href="https://uc-r.github.io/regression_trees">R tutorial</a>; <a href="https://besjournals.onlinelibrary.wiley.com/doi/10.1111/j.1365-2656.2008.01390.x">Elith et al., 2008</a> |
| Bayesian species distribution models | spOccupancy (with R) | Probability | Presence/absence | <a href="https://www.jeffdoser.com/files/spoccupancy-web/">Single-Species, Multi-Species, and Integrated Spatial Occupancy Models</a> |

### Other Helpful Links
<a href="https://zoonproject.github.io/zoontutorials/articles/Choosing_A_Modelling_Method.html">Choosing a model method.</a>
<a href="http://www.r-gators.com/2018/01/24/introduction-to-species-distribution-models/">Video: Introduction to SDM.</a>

