---
title: How much species data is enough to build a robust model?
description: 
background: 
    img: https://inaturalist-open-data.s3.amazonaws.com/photos/87200498/original.jpg
    by: Ian Bryson
    href: https://inaturalist.ca/people/icbryson
  
permalink: /faqs/how-much-data/
toc: true
comments: true
navigation: faqs-navigation
---

## How much species data is enough to build a robust model

By: [Robert Buchkowski]({{ 'best-practices-wg-team/#Dr.+Robert+Buchkowski' | relative_url }}), [Alana Westwood]({{ 'best-practices-wg-team/#Dr.+Alana+Westwood' | relative_url }}), [Courtney Burk]({{ 'best-practices-wg-team/#Courtney+Burk' | relative_url }}), and SDM workshop 2023 contributors

Species distribution models (SDMs) are data-hungry. Although the goal is often to predict the presence of a species across variable environmental conditions. To reflect a species’ niche, it would be ideal to have systematic surveys of their abundance and/or occupancy across the entirety of their range and at multiple time stamps, to capture each portion of their life cycle. The more location data about where species are, the better. With that, there are two streams of data to consider with creating SDMs. (1) pre-collected species location data, or (2) self-collected samples. Both pose their own challenges and deliberation. Robust location data for species are rarely available. Often, species’ locations are available only as a hodge-podge of occurrences cobbled together from different locations (e.g. eBird, iNaturalist, Conservation Data Centres/NatureServe, GBIF). Presence-absence data are usually only available from systematic surveys, and abundance data are rare (although some places, like the Boreal Avian Modelling Project, collate these data for birds). Occupancy data—where individuals are tracked, or measured repeated times in the same location—are generally only available from academic studies undertaken in relatively small regions.

Yet, planning to collect samples yourself gets even more difficult, especially when estimating the appropriate power for your model. If this is your chosen route, a power analysis is a helpful tool to focus your efforts and help you determine the smallest sample size needed to predict a particular effect at the desired level of significance. For example, less than 20 sites even in a small area is probably not enough, but the value of spending the effort to sample 200 sites as opposed to 100 sites can only be judged in context. For many large-scale SDMs, you might even have most of the independent variables from remote sensing before you start. In this case, you can simulate many examples of presence-absence data and see whether your model can recreate the relationships that you input. The R package `virtualspecies` is a great tool for this type of test.

So, what can you do with the location data you have, and how much is enough? Some basic rules of thumb are (1) at least 10 occurrences (or locations) per dependent variable in your model, and (2) more occurrences than independent variables in your model. However, authors offering advice on SDMs rarely give specific numbers and always add caveats. Our goal here is to explain why and describe how you can evaluate your sampling design to see if you have “enough” location data.

### Scale

The first thing that affects the amount of data needed to build an SDM is scale. Building an SDM at a larger scale for a more variable environment requires more data. This is because you need enough information about presence in all the environment types where your SDM will be applied to build a reliable model. The scale also matters because larger spatial scales also have more variables that can control species distribution. For example, variables like climate and ecological zone only matter at large enough scales (e.g. provincial, continental). One hundred occurrence locations might be excellent for a small-scale model in an individual protected area, but certainly would be nowhere near enough (by several orders of magnitude) for a continental-scale model.

### Habitat selection consistency

A related influence is context-dependent habitat selection. Some species use one habitat type in Eastern North America but another in Western. More data is required for an SDM at this scale to capture this interaction between habitat preferences across ecological zones.

Furthermore, species might use different habitats during ontogeny or annual migration. If a species is a habitat generalist or uses different habitats at different life stages that are hard to tell apart (e.g., breeding versus foraging) then you will need more data to get a consistent signal. You need more data on generalists or species that switch habitat types during their lives because the occurrence records are likely to have more data in transient habitat: which makes the actual habitat harder to discern.

### Home range size

The third aspect that affects the amount of data that you need is a species home range size. Species with larger home ranges will occur in more habitat patches and be harder to match to useful variables beyond generic climate or ecological zones. This is akin to the issue described above where broad habitat use will require more data simply because your data will contain less information about unsuitable habitat. In fact, you risk building a data-poor model that returns relationships that are obvious even without an SDM (I.e., no woodpeckers living above the tree line).

### Complex mathematical relationships

The fourth is the presence of independent variables that require more coefficients. Two examples are non-linear relationships for a continuous variable or a categorical variable with many levels. Notably, all presence-absence SDMs are based on a non-Gaussian relationship usually using a logistic regression. However, in a logistic regression we can use polynomials to capture non-monotonic relationships between the species presence and continuous variables. A good example are species that prefer intermediate temperatures or middle-aged stands. Just like categorical variables with many levels, polynomials add more coefficients to our model and so they require more data to estimate.

## Final notes

A final note is that not all data points are equal and this highlights the benefits of running example SDMs during the study design. New data will have more or less of an impact on your ability to fit the model depending on the sites values for each independent variable. 

The value of new data will always be to improve your information (assuming it is collected correctly). But, don’t be alarmed if this makes your model ‘worse’ in terms of its statistical validation (e.g. AUC). For example, imagine a study where you have data from many forest stands for a generalist bird species that lives in both hardwood and softwood stands. Your current data is mostly hardwood stands, so that is the only place you have observed it. Going out and surveying a few softwood standards, finding the bird there, and adding those data might make your model fit look worse, but will give you a better understanding of the bird’s true habitat requirements.

In summary, there is no universal rule for the amount of data required for an SDM. However, projects meant to span multiple ecological zones at scales of hundreds of thousands of kilometers likely require at least thousands, but preferably hundreds of thousands of records. Data sets on the order of one hundred sites are likely only valuable for small areas of hundreds of square kilometers or in the case of larger geographic areas wherein the possible habitat is partially defined (i.e., fish don’t live on land 😊).
