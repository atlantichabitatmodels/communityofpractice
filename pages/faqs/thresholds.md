---
title: How do we calibrate the predicted probability of occurrence/abundance to suitable and/or critical habitat?
description: 
background: 
    img: https://inaturalist-open-data.s3.amazonaws.com/photos/87199240/original.jpg
    by: Ian Bryson
    href: https://inaturalist.ca/people/icbryson
  
permalink: /faqs/thresholds/
toc: false
comments: true
navigation: faqs-navigation
---

By: [Courtney Burk]({{ 'best-practices-wg-team/#Courtney+Burk' | relative_url }}), [Alana Westwood]({{ 'best-practices-wg-team/#Dr.+Alana+Westwood' | relative_url }}), [Robert Buchkowski]({{ 'best-practices-wg-team/#Dr.+Robert+Buchkowski' | relative_url }}), Katherine Dearborn, Jordan Thomson, Chris Edge. 

Often, we build models of species distribution with goals of learning about a species’ habitat. We may wish to designate areas as critical habitat or location particular habitat types of high value for conservation, or assessing ecological impacts of various factors on that habitat (e.g. pollution, climate change), or risk of biological invasions.

Yet, many authors of species distribution models (SDMs) make a common and understandable mistake. SDMs predict the occurrence, abundance, or occupancy of species across a landscape (or seascape/waterscape). Many authors assume that areas of high occurrence/abundance/occupancy = suitable habitat. While there likely is a correlation between areas of high occupancy and suitable habitat, SDMs themselves **do not** predict habitat. To do so requires a step that most SDM-builders miss: **calibration**.

To truly calibrate probability of occurrence (or occupancy, or abundance) to habitat, it is necessary to develop a field-based assessment of habitat suitability (see [Westwood et al. 2019](https://conbio.onlinelibrary.wiley.com/doi/full/10.1111/csp2.163) for an example). Experts develop a quantitative or qualitative rating system for unsuitable to suitable habitat. At each location evaluated or habitat suitability, the probability of occurrence is sampled from the prediction raster. This can then be used to set ‘bins’. For example, if all sites rated in the field as ‘excellent habitat’ correspond to a probability of occurrence >0.9, than one can reasonably assume all areas predicted as 0.9 or above in the model likely represent excellent habitat. If all sites rated in the field as ‘unsuitable habitat’ have a probability of occurrence <0.3, then all areas predicted below this threshold can be ejected from candidacy for habitat protection or management.

However, the resources to conduct calibration are often not available, and are impossible on large scales (e.g. continental). In that case, the next best thing to do is set a **threshold** of probability of occurrence, below which are areas that are *unlikely* to represent suitable habitat.

> “This subsection is important in presence-only and presence–absence models, and in particular for mapping or transfer. In the case of a binary response variable, most SDM approaches produce continuous outputs such as habitat suitability indices or probabilities of occurrence. Whilst there are good arguments for retaining predictions on a continuous scale (Lawson et al. 2014, Guillera-Arroita et al. 2015), some users prefer to threshold them for certain applications. To do so, they need to define an adequate threshold to transform the data. Several different thresholds have been proposed depending on whether the presence–absence or presence only data are being used for modelling (Liu et al. 2005, 2013) or when modelling communities (Scherrer et al. 2018). Here, authors need to specify which threshold is used and explain why thresholding is deemed necessary.” 

There are several approaches found in the literature to go about defining the specific thresholds:
1. People often pick a number indicating relatively higher or lower probability of occurrence. The threshold chosen may depend on the downstream management purpose.
2. Sometimes, people will look at occurrence data and find the lowest probability of occurrence corresponding to a known presence of that species. However, this approach is problematic: it sets a low bar for occurrence because species may be temporarily present in an unsuitable area for various reasons (vagrant individuals, species interactions, etc.). Sometimes people will get around this using a quantile (i.e. discarding the most extreme cases).
3. There are Maxent/R SDM packages (e.g. maxSSS and maxFpb; Liu et al., 2013) that can pick a threshold for you by maximizing specificity and sensitivity.
As with most analyses, there is no one answer, and the approach to determining your thresholds depends on several considerations for your study, such as the purpose of the study, data availability, potential for model validation, and uncertainty. 
A good rule of thumb is to use independent ground-truthing data to maximize the value of true skill statistic (minimizes false positives/negatives in the prediction layer). Few SDM models use GPS species data or other validation techniques to validate their models, so it is can be hard to decide how much data is needed to build the model and how much is reserved for testing/statistical validation. Indeed, that is a question to be answered all on its own.
As a final note: remember to consider purpose and uncertainty with your models! 
“In any research, we reiterate that it is critical to state the purpose and method for selecting a threshold and to explore the sensitivity of the model to the threshold selected.” 
For example, if we don’t have great faith in model predictions, we might want to be more rigorous by setting a higher threshold. The degree of uncertainty in the model could influence how conservative we want to be.
---
## Literature to refer to:
Beazley, K., Reining, C., Doran, P., and Bettigole, C.. Integrating site-selection tools and expert judgement for conservation system design in the greater Northern Appalachians of Canada and the United States. <https://www.academia.edu/19649805/INTEGRATING_SITE_SELECTION_TOOLS_AND_EXPERT_JUDGMENT_FOR_CONSERVATION_SYSTEM_DESIGN_IN_THE_GREATER_NORTHERN_APPALACHIANS_OF_CANADA_AND_THE_UNITED_STATES?email_work_card=title>

Bean, W.T., Stafford, R. and Brashares, J.S. (2012), The effects of small sample size and sample bias on threshold selection and accuracy assessment of species distribution models. Ecography, 35: 250-258. <https://doi-org.proxy.hil.unb.ca/10.1111/j.1600-0587.2011.06545.x>

Liu, Canran & White, Matt & Newell, Graeme. (2013). Selecting thresholds for the prediction of species occurrence with presence-only data. Journal of Biogeography. 40. 778-789. <https://doi.org/10.2307/23463638>.

Majka, D., J. Jenness, and P. Beier. 2007. CorridorDesigner: ArcGIS tools for designing and evaluating corridors. Available at <http://corridordesign.org>.

Morrow C. 2019. Thresholding species distribution models. <https://babichmorrowc.github.io/post/2019-04-12-sdm-threshold/>

Muhammed, K.; Anandhi, A.; Chen, G. Comparing Methods for Estimating Habitat Suitability. Land. 2022, 11, 1754. <https://doi.org/10.3390/land11101754>

Westwood, R., Westwood, A., Hooshmandi, M., Pearson, K., LaFrance, K., Murray, C. A field-validated species distribution model to support management of the critically endangered Poweshiek skipperling (Oarisma poweshiek) butterfly in Canada. 2019. Conservation Science & Practice: e163.

Zurell et al. (2020) A standard protocol for reporting species distribution models. Ecography 43: 1261-1277. <https://doi.org/10.1111/ecog.04960>