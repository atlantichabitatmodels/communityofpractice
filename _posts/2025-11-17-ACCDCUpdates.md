---
title: "An overview of habitat modelling projects for Species at Risk Models in the Maritimes"
background: 
    img: /assets/images/BankSwallow_GuillaumeDaigle.jpg
    by: Guillaume Daigle
author: [Miranda Frison]
tags: [Model Spotlight, SDM, HSI, NS, NB, PEI, Birds, Lichen, Species at Risk, Canada Warbler, Olive-sided Flycatcher, Eastern Wood-Pewee, Bank Swallow, Black Ash, Eastern Waterfan, Wrinkled Shingle Lichen]
comments: false 
---
The [Atlantic Canada Conservation Data Centre](http://accdc.com//) (AC CDC) houses Atlantic Canada’s most extensive biodiversity database, maintaining over 3.1 million records, essential to accurate and effective monitoring of Species at Risk (SAR). AC CDC is uniquely positioned to leverage both biodiversity and geospatial data to create derived products used to improve conservation outcomes for many SAR. AC CDC creates species distribution models (SDMs) and habitat suitability index (HSI) models which are used in conservation status rank updates, recovery plans, targeted field surveys and other conservation efforts. AC CDC primarily uses MaxEnt for creating SDMs and ArcGIS Pro to create HSIs.

On October 3<sup>rd</sup>, 2025, [Charity Robicheau](https://www.linkedin.com/in/charity-robicheau-96682a86/) shared with the Community of Practice an overview of the AC CDC’s ongoing habitat modelling work over the past five years. Her role as the Senior Conservation Data Analyst has enabled her to be involved in multiple modelling projects for SAR which are actively used by partner organizations today. 

Since 2018, AC CDC has created habitat models for numerous SAR. Eight species were highlighted within the presentation (**Table 1**). Due to some species being classified as “location sensitive” by the New Brunswick and Nova Scotia provincial governments, this post will be limited to what information we can share publicly. If you wish to learn more about the AC CDC, please contact Charity Robicheau (**Table 2**).

<br></br>
**Table 1**. Eight species at risk highlighted in the Community of Practice presentation, including their COSEWIC Committee on the Status of Endangered Wildlife in Canada) and SARA (Species At Risk Act) designations, along with their provincial status within New Brunswick (NB) and Nova Scotia (NS).

| Scientific Name           | Common Name             | COSEWIC         | SARA            | Provincial Status                     |
| ------------------------- | ----------------------- | --------------- | --------------- | ------------------------------------- |
| *Riparia riparia*         | Bank Swallow            | Threatened      | Threatened      | Endangered (NB & NS)                  |           
| *Cardellina canadensis*   | Canada Warbler          | Special Concern | Threatened      | Threatened (NB); Endangered (NS)      |
| *Contopus cooperi*        | Olive-sided Flycatcher  | Special Concern | Special Concern | Endangered (NB); Threatened (NS)      |
| *Contopus virens*         | Eastern Wood=Peewee     | Special Concern | Special Concern | Special Concern (NB); Vulnerable (NS) |
| *Fraxinus nigra*          | Black Ash               | Threatened      |                 | Threatened (NS)                       |
| *Peltigera hydrothyria*   | Eastern Waterfan        | Threatened      | Threatened      | Threatened (NB & NS)                  |
| *Pannaria lurida*         | Wrinkled Shingle Lichen | Threatened      | Threatened      | Endangered (NB); Threatened (NS)      |

<br></br>
**Bank Swallows** (*Riparia riparia*)
+ Banks modelling algorithm developed to locate bank suitable structure for nesting
+ Hundreds of Fisheries and Oceans Canada (DFO) analysed using known presences from the AC CDC database, iNaturalist, and the North American Breeding Bird Survey (BBS)
+ Ground truthing conducted to determine if bank substrate provided suitable habitat

**Canada Warblers** (*Cardellina canadensis*), **Olive-sided Flycatchers** (*Contopus cooperi*), and **Eastern Wood-Pewees** (*Contopus virens*) for Prince Edward Island
+ Initial models completed in 2020, with improvements made in 2023 including LiDAR from 2020, new presence data, adding a shrub density metric, and depth to water table data
+ Modified model resulting in lowering subdivision lot sizes due to overlapping Canada Warbler habitat
+ Model aids Parks Canada with ARU placement for monitoring 

**Black Ash** (*Fraxinus nigra*)
+ Models were created both with and without climate variables, with experts selecting the models which included climate variables, as it provided robust understanding of the habitat
+ Resolution and occurrence records varied with models for each province due to data availability: Nova Scotia (50 m, 1000+ records), New Brunswick (50 m, 2300+ records), Prince Edward Island (30 m, 900+ records)
+ Targeted surveys based on models were conducted and consistently found Black Ash at areas deemed to have high habitat suitability
+ 324 new records of Black Ash were found in 2024 resulting from this work

**Eastern Waterfan Lichen** (*Peltigera hydrothyria*)
+ Summarized where the species has been found within Fundy National Park, NB and determined hotspots
+ Regression analysis was used to determine probability of occurrence and predicted density
+ More likely to find the lichen within the park than within 10 km of the park boundary and waterfan is highly sensitive to disturbance caused by humans (logging, suspended sediment in water, stream pH, etc.)

**Wrinkled Shingle Lichen** (*Pannaria lurida*)
+ HSI model was created due to lack of presence records
+ 22 new records were found on PEI, in addition to multiple other SAR lichens


<br></br>
**Table 2**. Key information from presentation, including method of contact.

| Field                     | Description                                                                                   |                                                                                                            
| ------------------------- | --------------------------------------------------------------------------------------------- |
| Project name              | An overview of habitat modelling projects for Species at Risk in the Maritimes                |
| Project date              | 2020-2025                                                                                     |                                                                                                                    
| Primary contact           | charity.robicheau@accdc.ca                                                                    |                                                                                                    
| Province(s)               | NB, NS, PEI                                                                                   |
| Modelling approach        | Maxent Species Distribution Model (SDM), Habitat Suitability Index Model (HSI)                |
| Modelling software        | Maxent                                                                                        |
| Model spatial resolution  | 30m (PEI), 50m (NB, NS)                                                                       |
| Data sensitivity          | Sensitive                                                                                     |
| Data use restrictions     | Upon request                                                                                  |
