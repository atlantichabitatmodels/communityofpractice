---
title: How do we determine appropriate spatial extents and cell size (model resolution)?
description: 
background: 
    img: https://inaturalist-open-data.s3.amazonaws.com/photos/256712966/original.jpg
    by: Nick Cairns
    href: https://inaturalist.ca/people/nacairns
permalink: /faqs/spatial-extent-cell-size/
toc: true
comments: true
navigation: faqs-navigation
---

## How to determine appropriate spatial extents and cell size (model resolution)

By: [Courtney Burk]({{ 'best-practices-wg-team/#Courtney+Burk' | relative_url }}), [Alana Westwood]({{ 'best-practices-wg-team/#Dr.+Alana+Westwood' | relative_url }}), Richard Westwood, Katherine Dearborn, Stephen, Chris Edge, Miranda Frison

When building models, we visualize the perfect system. We hope to encapsulate the boundary range and all the ecological and climate variables that influence the distribution of our selected species. Often, these perfect models do not work out as such, and are accompanied by caveats and constraints. In reality, the biology of our species chooses the spatial extent/resolution, and our data limits it. 

There are several critical considerations to keep in mind when collecting and scaling your data.

### The biology & ecology of the species

When considering the biology of your selected species, **first**, you must choose your boundaries that make sense in the context of your study. This can be species range, covariate layer extents, watersheds, ecoregions (both marine and terrestrial), historical range of species, climate envelopes, legislation or political, etc.). A few examples of boundaries are terrestrial ecozone/ecoprovince/ecoregion/ecodistrict boundaries in Canada, including coastal near-shore marine ecodistricts ([A National Ecological Framework for Canada](https://sis.agr.gc.ca/cansis/nsdb/ecostrat/gis_data.html)), watersheds ([National Hydrological Network](https://www.nrcan.gc.ca/science-and-data/science-and-research/earth-sciences/geography/topographic-information/geobase-surface-water-program-geeau/national-hydrographic-network/21361) or the [Geobase Watersheds layer](https://www.nrcan.gc.ca/science-and-data/science-and-research/earth-sciences/geography/topographic-information/geobase-surface-water-program-geeau/watershed-boundaries/20973), or [both major and sub drainage watershed polygons](https://www.arcgis.com/home/item.html?id=12b6e33d5a754c92b97ae5d0fed6940a)) or political boundaries from ESRI ([available here](https://hub.arcgis.com/datasets/geoplatform::political-boundaries-area/explore?location=14.726080%2C-0.000004%2C2.17)).

Keep in mind how relevant the temporal and spatial scale is if you are interested in projecting the model to another area – but be mindful of spatial autocorrelations. Practically, think about who is using the results, managing it, what boundaries they are using and where they have jurisdiction for management. You need to justify why you chose your boundaries/extent in your methods/study area section.

**Second**, think about your species' niche (fundamental and/or realized niche), how they select habitat, for what purpose, and across what scale. This includes their range but also the selection of individual sites.

**Third**, consider how your species disperse, where, how far, and when. Be aware that species might use different habitats during mating or annual migration.

**Finally**, consider the intent of your study and how the species’ niche is represented within that. Are you using pre-determined/collected location data or are you sampling for your study? Your input data may itself cause a limitation to your spatial extent. For example, if your occurrence, abundance, or occupancy data comes from highly biased sampling or is clustered in small areas, consider limiting your extent and refer to the power needed for a robust model.

If your species has an extensive range and adapts to various conditions, limit your spatial extent to areas of similar ecological conditions where habitats could occur. For example, Canada Warblers use upland dry shrubby habitat on the western side of their range and wet lowland shrubby habitat on the eastern side. Thus, the ecological relationships generated for the whole species' range using occurrence data across the whole range are a mean, and don't accurately reflect on-the-ground habitat conditions in any one place, and thus may not be useful for management. 

It is important to identify population subunits or subregions to derive ecological variable relationships that can be translated into management prescriptions. You should be reasonably sure that relationships between occurrences and predictor variables will be relatively consistent, and your population could reasonably disperse on the time frames you are modelling.

### Limitations in data availability and resolution

Once you have a framework of the biological factors/requirements, explore the data-limiting aspects of our models. This is a challenging task, and some compromises may need to be made. To start, explore the data thoroughly to be aware of spatial and temporal trends and their relationship to the biology and the ecology of the species in your study. Generally, the smallest available spatial resolution may be the best choice. data that is too coarse may not fit (e.g. climate data at 10km2 resolution when looking at crossing structures and roadway barriers for wood turtles). 

 

What should you do if you have a data layer that is much more coarse resolution than your other variables, but you think it is biologically important? Is it ***ever*** appropriate to break down/interpolate a coarse layer into a finer resolution to enable finer-resolution modelling?

Studies have found that coarsening data can artificially inflate prediction statistics. A workaround would be running multiple models at different resolutions to check for the effect strength of the variables at different scales. Imagine a situation where you want to include a coarse layer (e.g. climate or degree day data at 2km^2 resolution) but the rest of your data is fine (e.g. landcover data at 50m^2 resolution). There may be cases when this doesn’t inflate your model: for example, if you are sure that the coarse layer represents real values and are not an average of a wide range of values over each cell (for example, degree days over flat topography with similar landcover and not much microclimate variation). However, developing your own layers from measured data (e.g. using nearby weather stations) may still be better rather than large-scale climate projections that include errors. Alternatively, it may be better to run a model without the coarse data and overlay or extrapolate portions of the data to explore correlations. 

Other scenarios that could limit your data include the resolution of data availability and computing power. For example, you could be limited by the computing power of your computer, such as how long it takes to run, the RAM available, etc. A potential solution to a computation issue is to transfer data to a cloud and rent time on a "super-computer" through an organization or university, as universities often have computing clusters available. Also, ensure you have enough data storage capability for your model outputs!

Remember, the species' biology picks the spatial extent, and our data limits it. So, moving forward with your models, take the time to explore your options for data availability, boundary size/scale, and resolution potential. So long as you can justify why you have selected the inputs and variables that you did at a scale that make sense for your study and species. 
