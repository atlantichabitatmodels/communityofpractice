---
title: "Model Spotlight: Species Distribution Model for Fraxinus nigra (Wisqoq; Black Ash)"
description: Fraxinus nigra is an ecologically and culturally important species facing imminent threats
background: /assets/images/iNat97730535.jpeg
author: [Jocelyn Pender]
categories: [Model Spotlight, SDM, Nova Scotia, Species at Risk, Fraxinus nigra, Wisqoq, Black Ash]
comments: false
---

In partnership with Parks Canada, the Atlantic Canada Conservation Data Centre (AC CDC) has developed a *Fraxinus nigra* (Wisqoq; Black Ash) species distribution model extending across mainland Nova Scotia.

*Fraxinus nigra* is an ecologically and culturally important species facing imminent threats (e.g., the arrival of Emerald Ash Borer in Nova Scotia; COSEWIC, 2018). The cultural significance and value of *Fraxinus nigra* (Black Ash; Wisqoq) cannot be understated. It has been a part of l’nuk culture since time immemorial. Its highly flexible wood, that can be peeled into thin strips, is an important component of its cultural significance (see [wisqoq.ca](http://wisqoq.ca/) for more information).

We used an inductive modelling approach (i.e., where potential habitat is inferred from the data), leveraging a machine learning algorithm. Our modelling goals were to:
1. Understand where potential *Fraxinus nigra* (Black Ash, Wisqoq) habitat is distributed in mainland Nova Scotia
2. Determine where to prioritize field work to find additional occurrences of *Fraxinus nigra*
3. Supply information to decision makers about high potential areas of *Fraxinus nigra* habitat (e.g., for management or planning applications)

We produced a 50m resolution predictive surface output showing areas of high and low probability of suitable habitat. The final model has an AUC score of 0.8403 when evaluated against training data and an AUC score of 0.8408 when evaluated against testing data. The variable with the highest importance is canopy closure (derived from LiDAR data). 

We consulted species experts on its quality and biological feasibility. The model quality was rated by our experts as between 3-star and 4-star on a five-star scale. The experts emphasized that the selected model overestimates probable suitable habitat. *Fraxinus nigra* is a rare species; it is infrequent to absent in almost every area identified anecdotally (and by the model) as probably suitable.


Model details:

| Field                     | Description                                                                                         |
| ------------------------- | --------------------------------------------------------------------------------------------------- |
| Project name              | Mapping Existing and Potential *Fraxinus nigra* (Black Ash, Wisqoq) Habitat in Mainland Nova Scotia |
| Project date              | 2022                                                                                                |
| Project partners          | AC CDC, Parks Canada                                                                                |
| Primary contact           | jocelyn.pender@accdc.ca, james.churchill@accdc.ca                                                   |
| Short project description | SDM for Wisqoq (Black Ash, *Fraxinus nigra*) using lidar-derived and other metrics                  |
| Project documentation     | AC CDC                                                                                              |
| Province                  | NS                                                                                                  |
| Study site                | NS                                                                                                  |
| Geographic extent         | Mainland NS                                                                                         |
| Modelling approach        | Species Distribution Model                                                                          |
| Modelling software        | Maxent                                                                                              |
| Model grain size          | 50m                                                                                                 |
| Product description       | 50m-resolution predictive raster showing continuous probability of suitable conditions              |
| Data sensitivity          | sensitive                                                                                           |
| Data use restrictions     | permission required from NS/AC CDC                                                                  |
| Data location inputs      | AC CDC                                                                                              |
| Data location outputs     | AC CDC                                                                                              |

Photo by [Pierre Cartier](https://www.inaturalist.org/people/pcartier).
  