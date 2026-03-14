---
title: How many seasons of field data should you collect for model building or validation?
description: 
background: 
    img: https://inaturalist-open-data.s3.amazonaws.com/photos/215189371/large.jpg
    by: Mark Connolly
    href: https://www.inaturalist.org/people/w_mark_c
  
permalink: /faqs/field-data/
toc: true
comments: true
navigation: faqs-navigation
---

By: [Alana Westwood]({{ 'best-practices-wg-team/#Dr.+Alana+Westwood' | relative_url }}), [Courtney Burk]({{ 'best-practices-wg-team/#Courtney+Burk' | relative_url }}), and [Robert Buchkowski]({{ 'best-practices-wg-team/#Dr.+Robert+Buchkowski' | relative_url }})

## Introduction

As all ecologists know, flora and fauna are a tricky thing to measure (some species worse than others!).
Their abundance often varies year-to-year due to either natural, cyclical fluctuations in population or
due to stochastic factors like major weather events or human disturbance. The researcher studying
black spruce trees will have a much easier time of it than the one studying the elusive common
nighthawk (not-so-common anymore!).

In the answer to this question, we consider the appropriate temporal spread and effort for 
field-collected data to build or validate your model. Note that we do <i>not</i> consider how much species data is
enough to build a robust model—that question is covered in <a href="https://atlantichabitatmodels.github.io/communityofpractice/faqs/how-much-data/">this post</a>.

There are four main considerations here: 1. The ecology of your species, 2. Major changes in your
study area or your species’ abundance, 3. Spatial bias in your dataset, and 4. Budget and resources.


### The ecology of your species

As previously mentioned, some species experience natural interannual variations in population size.
Other species use different habitats at different portions of their life cycle. If you are attempting to
model a species’ habitat during its breeding season, it would only be necessary to collect data during the
breeding season or validate a model constructed using breeding season data. However, if you wish
to model a species across its lifecycle, data will need to be collected at all relevant timepoints.

You will first need to look at the existing data you have representing the species’ occurrence,
abundance, or occupancy. Does it sufficiently cover all the temporal periods you wish to represent
within a one-year cycle? If this species is known to have interannual variation in abundance, examine
the spread of your existing dataset by year. Does the sample sufficiently represent the cycle over which
you expect to see population decreases and increases?

If the answer to either of the above is <b>no</b>, identify specifically which conditions are not represented in
the dataset. Whether or not you can supplement with a single season of collected data or a multi-year
effort depends on the ecology of your species, and where it currently is in its temporal cycle. For
example, if trying to model spruce budworm outbreaks but you do not have data on abundance from
outbreak years, additional data collection will be necessary, albeit challenging if you need to wait a few
decades for the next cycle. Similarly, if trying to validate a model on outbreaks, the model validation
field data must be collected during an outbreak year.

### Major changes in your study area or your species' abundance

If you plan to model present or future conditions for a species, it is important to ask whether the data
you have in hand are representative of real-world conditions now. Have the
environmental conditions of your study area changed in a substantive way over the time period the
data was collected, or since it was collected (e.g. forest fire, new subdivision, hurricane damage)? Has
the species experienced a sharp change in abundance that are not part of natural population cycles (e.g.
population rebounding after a captive breeding and release program)?

If the answer to either of these questions is <b>yes</b>, additional data collected is needed. These should be
targeted in areas of major habitat changes or expected population changes. Whether or not one year of
data collection is sufficient or not again depends on the species’ ecology, and whether there are
expected year-to-year changes in distribution and abundance.

### Spatial bias in your dataset

Ideally, your input dataset should represent presence/abundance/occurrence as well as absence of your
species, and be distributed across your study area using a random sample stratified across habitat types
or ecological conditions. However, we rarely have such an ideal dataset to work with. Look at your data.
Is your dataset heavily spatially-biased towards one portion of your study area? Is your
dataset biased towards species’ known habitat compared to available habitat within ths study area?

If you answered yes to either of the above, it is advisable to collect data in other regions before
modelling and expand your sampling criteria. For example, for species particularly sensitive to
anthropogenic disturbance including roads, it will be important to make efforts to sample in core
(interior) habitats, away from roads to construct an accurate model.

### Budget and resources

And, of course, there is the ecologist’s bane: the budget. There will only be so many financial
and human resources available to conduct sampling, and some have non-negotiable time constraints
(for example, a Master’s student is rarely able to complete more than one field season).

The size of the field crew will also determine whether you need multiple years to collect the amount of
data necessary to represent variation in habitat across the study area. If you don’t have large
interannual variation in the species ecology, you might easily get all the data that you need in a single
season with a large enough crew (or a big enough stockpile of Camera Traps or Acoustic Recording
Units). If you have a smaller crew, you might need multiple field seasons just to build up enough data.

We recommend that you engage with your current dataset to examine points 1-3, above, and make a
‘wishlist’ for sampling. Prioritize whichever way your dataset is least representative, and allocate
resources to collect more data there first. Share this ‘wishlist’ with allied organizations and
researchers who possibly could supplement your dataset with incidental observations during their
fieldwork, or refer to <a href="https://atlantichabitatmodels.github.io/communityofpractice/faqs/data-sources/">this post</a> 
to see if supplementary data already exists.

Finally, never forget the ecology and biology of your species. If there is insufficient information about
your species to even know if and how their populations are subject to inter or intra-annual variation (or
not!), you may want to target your first few seasons of data collection to answering these basic ecology
questions rather than building an incomplete or misleading species distribution model.















