---
title: What process should we use to obtain the most parsimonious set of predictor variables?
description: 
background: 
    img: https://inaturalist-open-data.s3.amazonaws.com/photos/216563241/large.jpg
    by: Braden J. Judson
    href: https://www.inaturalist.org/people/bradenjudson
  
permalink: /faqs/predictor-variables/
toc: true
comments: true
navigation: faqs-navigation
---

By: [Robert Buchkowski]({{ 'best-practices-wg-team/#Dr.+Robert+Buchkowski' | relative_url }}), [Alana Westwood]({{ 'best-practices-wg-team/#Dr.+Alana+Westwood' | relative_url }}), and [Courtney Burk]({{ 'best-practices-wg-team/#Courtney+Burk' | relative_url }})

## Introduction

Species distribution models (SDMs) can use both data collected in the field and data derived from
remote sensing. This means there is often a long list of potential variables (sometimes called covariates)
to include in your model. Remote sensing provides a huge amount of information that is made even
more overwhelming by the large number of metrics that have become available from remote sensing technologies like LiDAR. 
Field work is constrained by time or resources, so decisions are often made beforehand which variables might 
be important for the taxa being studied. However, fielddata can still produce long lists of possible variables, 
such as data on all co-occurring species, or data on trees across size classes.

A major challenge in species distribution modelling is deciding which variables to include in the final
model or even in preliminary models. This problem is made worse by three factors. First, correlations
among the hundreds of available variables are common due to ecological relationships or spatial
autocorrelation. If many correlated variables are included, they add redundancy while reducing
explanatory power, and may artificially inflate statistical validation using measures like ‘area under the
curve’. Second, many of these variables represent the same ecological process, so even if we could include them, 
interpreting differences in their coefficients would be challenging or arbitrary. Finally, models with too many
variables will run out of degrees of freedom or fail to converge. All this means that modelling your
species’ distribution or abundance the hundreds of available independent variables is not an option.

Considering this overload of information, there are two steps to selecting predictor variables for you
SDM. First, you need to simply select variables that you think could represent your species habitat
preferences. Second, you need to whittle down your list and select core variables for your final model. 

### How to build the initial variable list?

Two recommendations exist for building our initial variable list. The <b>first and most often cited</b> is to use
our ecological understanding of the species being modelled to choose reasonable variables. Some authors (e.g.
Westwood et al. 2019) develop a table of the known niche requirements of a given species, beginning
with the proximate factors to fulfill a species’ needs for shelter, food, and reproduction. For example, if
we are building a SDM for bees with long tongues, then it makes sense to select variables that indicate 

how many long-tubed flowers are available at each site. Variables describing the amount of grass at
each site are probably less important, while variables describing the number of short-tubed flowers
could be marginally important. In this example you can imagine how a list of hundreds of potential
variables describing a grassland plant community might be summarized into fewer than ten describing
the plants most likely to be important to the long-tongued bees.

If no data are available to represent these proximate factors, then, ‘ultimate factors’ are surmised.
These are proxy variables. For example, if there is no data layer on long-tubed flowers, soil type or
ecosystem classification including categories that are known to support long-tubed flower species would
serve as an ultimate proxy. Of course, using this approach requires detailed biological knowledge of the
species being modeled.

The <b>second option</b> is to take a quantitative approach and select one variable from each group of
correlated ones. To do this, you calculate the correlation matrix of all the possible variables and look for
blocks of variables that are highly correlated. If your sites are a good cross-section of the region you
hope to model, you can more confidently assume that all these correlated variables are describing the
same type of habitat. Once the variable groups are defined, you can either choose a variable from each
to include or produce some composite variable that describes the group.

The second approach is most justifiable for generic habitat features because the link between the
species habitat preference and these variables are probably indirect. For example, songbird distribution
might be predicted by the basal area of a forest stand or forest age. These two variables are probably
correlated, and both a proxy measure of some unknown or unmeasured variable(s) that the birds need.
Including only one of them in the initial model would be justified in this case but would not be justified if
forest age and basal area were uncorrelated.


### How to select the variables in our final model?

We can use model selection methods to determine which variables we keep in our final model. These
methods begin with assessing the fit of our global model using residual plots to determine whether the
model is a good fit. You shouldn’t see any patterns in the residuals. Sometimes you might have too
many variables and still cannot build a global model. The global model is the base model 
that was created and trained using field-sampled data of which predictions can be transferred 
to an area with little to no reference data.

In this case, you should explore the fit of several
sub-global models. Make sure to examine the residuals across space and check for overdispersion. If the
model fit is poor, you will need to go back to your variable list to look for excluded variables or consider
a different modelling approach. If the model fit statistics look okay, then you can proceed with model
selection.

Information criteria is often used as a model selection tool for SDMs, although removing variables with
insignificant is also okay. If you are using information criteria, make sure to correct them for
overdispersion and keep an eye out for uninformative variables. The latter are variables with small
coefficient estimates and large standard errors that sometimes end up in models with lower information
criteria scores. You can use backwards selection from a global model or run all possible model subsets to
find the final model with the lowest information criteria score. Your final model could be the model with
the lowest information criteria score or a model average combination of the best models.

Using more than one approach is key.

Species distribution models are challenging because we often have an overwhelming number of
variables from remote sensing or field surveys to include in our models. Selecting the most parsimonious
list of variables is not so complex once we have a well-specified global model. TThe challenge is how to
get from the list of hundreds of possible variables to a list of tens of variables to include in aour global
model, we suggest combining your understanding of the species
ecology to focus on the most likely variable set to make an initial variable list. Then, examine the
correlation between the initial variable list to identify which ones are providing new information about
the habitat at your study sites.
