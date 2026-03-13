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

![Figure provided by Zurell, 2020.](/assets/images/Zurell2020.png/)
Figure 1: The main modelling cycle in species distribution modelling (Zurell, 2020).

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

| Method | Model Name/Software | Type | Species Data Type | Links for Further Learning |
| :--- | :--- | :--- | :--- | :--- |

| Climatic envelope | BIOCLIM | :--- | :--- | :--- |
| Gower metric | DOMAIN | :--- | :--- | :--- |
| Ecological niche factor analysis (ENFA) | BIOMAPPER | Suitability | Presence/background | :--- |
| Maximum entropy | MAXENT | Suitability | Presence/background | :--- |
| Genetic algorithm | GARP | Suitability | :--- | :--- |
| Regression: generalized linear model (GLM) and generalized additive model (GAM) | :--- | :--- | :--- | :--- |
| Artificial neural network (ANN) | SPECIES, MATLAB | :--- | :--- | :--- |
| Classification and regression trees (CART) | BIOMOD | :--- | :--- | :--- |
| Multivariate adaptive regression splines (MARS) | MARS (with R) | :--- | :--- | :--- |
| Favourability function (FF) | FF (with R) | :--- | :--- | :--- |
| Random forest (RF) | RF (with R) | :--- | :--- | :--- |
| Boosted regression trees (BRT) | BRT (with R) | :--- | :--- | :--- |
| Bayesian species distribution models | spOccupancy (with R) | :--- | :--- | :--- |

###Other Helpful Links
<a href="https://zoonproject.github.io/zoontutorials/articles/Choosing_A_Modelling_Method.html">Choosing a model method.</a>
<a href="http://www.r-gators.com/2018/01/24/introduction-to-species-distribution-models/">Video: Introduction to SDM.</a>

