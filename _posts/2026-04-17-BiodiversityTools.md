---
title: "Creating Public Biodiversity Tools Using Species Distribution Modelling"
background: 
    img: https://inaturalist-open-data.s3.amazonaws.com/photos/348268187/large.jpg
    by: Alex Stach
    href: https://www.inaturalist.org/people/alexstach
author: [Miranda Frison]
tags: [MaxEnt, SDM, Species at Risk, Biodiversity, Ducks Unlimited Canada, Alberta, Saskatchewan, Manitoba, Conservation, Restoration]
comments: false 
---

On November 7th, 2025, the Community of Practice was joined by <a href="https://protect.checkpoint.com/v2/r03/___https://www.ducks.ca/researcher/james-paterson/___.YzFjOmR1Y2tzdW5saW1pdGVkY2FuYWRhOmM6bzp
                                                                 iNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OjJiZmI6NGZkMzhjOWM0MmU4M2EzOTI0NDRkYmY1ZWFiYjJhMDUwYjQyZGM4NGJiMWQzMTYyZGIxNTZjZWNhYTQwMWQ1NzpwOlQ6Rg">James Paterson</a> (Table 1). 
He is a Research Scientist in Biodiversity at the Institute for Wetland and Waterfowl Research, the science arm of <a href="https://protect.checkpoint.com/v2/r03/___https://www.ducks.ca/___.YzFjOmR1Y
                                                                                                                     2tzdW5saW1pdGVkY2FuYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1Yjdj
                                                                                                                     ODY4NjNmMmY2NTdhODo3OjEwZWY6ZGE4OT
                                                                                                                     Q5YzFlZjEzY2U2YTIxZGRlOWUzMjQ5NDQwMWYxZmJmYjQ1N2E2
                                                                                                                     OWM3YzY5NmQ0NDVlOTQ3YmFmNzE1MDpwOlQ6Rg">Ducks Unlimited Canada</a>.

James highlighted how Canada is losing a large amount of biodiversity, largely due to land and sea use changes. His team developed a tool to predict the amount 
of biodiversity loss based on land cover. They focused on Alberta, Saskatchewan, and Manitoba for the tool. However, they are working on expanding it to include Eastern Canada!

The biodiversity mapping and assessment tool uses over 1.2 million observations 
of 329 species (<a href="https://protect.checkpoint.com/v2/r03/___https://www.gbif.org/___.YzFjOmR1Y2tzdW5saW
                  1pdGVkY2FuYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OjJiMDg6ZWNmNjMwN2YwN2Y4YT
                  I2Zjg4NmY5NWU5NGFkZDg5MjhmZDFhNWZmMDFmOTY1NjQ0ODk2OGVkZTIzNDAzZGU2ODpwOlQ6Rg">Global Biodiversity Information Facility</a>, 
                  <a href="https://protect.checkpoint.com/v2/r03/___https://www.alberta.ca/alberta-conservation-information-management-system___.YzFjOmR1Y2tzdW5saW1pdGVkY2F
                    uYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OjJiNTY6ZDJlNjAwZTUzMzZkMjYxNDI2ZTc3MTg5NDE5Nzk1YmVhMGQ3ZjRjNGExYjljOWZlYThmZGIzOGIzMmU4ZjFlYzpwOlQ6Rg">Alberta Conservation Information Management System</a>, 
                    <a href="https://protect.checkpoint.com/v2/r03/___https://www.inaturalist.org/___.YzFjOmR1Y2tzdW5saW1pdGVkY2FuYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OmUwYzA6YTEyMTY3NjgyMzE0OGNkYmExMTE1MWIyZDlkZjQ5OWJiYWRiMmM2MWMwODY0OTc1MzhiYWU5N2JjY2EwNGY0NDpwOlQ6Rg">iNaturalist</a>, 
                    <a href="https://protect.checkpoint.com/v2/r03/___https://www.biodiversity.sk.ca/___.YzFjOmR1Y2tzdW5saW1pdGVkY2FuYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OjU4Yzk6YWNkNDNmN2FkYzE3NWY2ZjNmMmFmM2ExYTk0MDFhMTkyN2Q2ZWRmOGYzM2NlMTRmOGJiM2Q1ZmNlZTg5OWYxMjpwOlQ6Rg">Saskatchewan Conservation Data Centre</a>, 
<a href="https://protect.checkpoint.com/v2/r03/___https://www.usgs.gov/centers/eesc/science/north-american-breeding-bird-survey___.YzFjOmR1Y2tzdW5saW1pdGVkY2FuYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OmZmMDU6ZGIyMmViYTRjOGMxNmJhMjRjZGYzYzA0Y2U0YzcyMDQ5ZWU5MGY2NDY2YzkwOWVhOTNkNGVmNTE1ZjcyMGJmMDpwOlQ6Rg">The North American Breeding Bird Survey</a>, 
<a href="https://protect.checkpoint.com/v2/r03/___https://www.gov.mb.ca/nrnd/fish-wildlife/cdc/index.html___.YzFjOmR1Y2tzdW5saW1pdGVkY2FuYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OjlmYjI6ZTMwZTk3OGQyODFlMmI3YzZkZDRhMTBhMDE5ZWViMjg1ZDBlZDg3Yzc4MTAyMzc1OWUxNTUzOGVlMDIyNjczZjpwOlQ6Rg">Manitoba Conservation Data Centre</a>), 
a land use time series at 30m resolution (<a href="https://protect.checkpoint.com/v2/r03/___https://agriculture.canada.ca/en/agricultural-production___.YzFjOmR1Y2tzdW5saW1pdGVkY2FuYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OjA4MzI6Zjg5MjY5Yjk5ZDE5MjQyMzE0ZjViZjcwN2VhM2VkY2UyYTgwZDg5ZmU4ZTQ0OWZiYTZmMjZhMWIxNGE1Njc3NDpwOlQ6Rg">Agriculture and Agri-Food Canada</a>), 
and a 30 second resolution dataset for climate variables (<a href="https://protect.checkpoint.com/v2/r03/___https://www.worldclim.org/___.YzFjOmR1Y2tzdW5saW1pdGVkY2FuYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OjMxZDk6NDc4YmVlOGQ2ZDg2N2Y4Njc1MDBhZTI0ZTA3MDMzMTE3YjlkZWQ0MWVkMjNjZDUxNGNiMTQ0MTEzMjVmNzIxZTpwOlQ6Rg">WorldClim</a>).

A key finding from this research indicated that sites with conservation easements supported more species diversity (39%) compared to sites with no protection. 
They also noted that conserving 20% of natural habitat in annual prairie cropland conserved 27% of the maximum species diversity. Conserving the same amount of natural habitat in tame grass fields 
conserved 74% of maximum species diversity. These are just some of the reasons why creating tools such as the one by Ducks Unlimited Canada is valuable; it provides researchers with ways to quantify the impact of 
land use changes to species over time. With this information, land can be prioritized for habitat conservation and restoration.

Want to try out the tool for yourself? Check it out on the <a href="https://protect.checkpoint.com/v2/r03/___https://www.ducks.ca/
                                                             our-work/science/prairie-biodiversity-mapping-tool/___.YzFjOmR1Y2tzdW5saW1pdGVkY2FuYWRhOmM
                                                             6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OjU0NmM6NWVhMGEwYWRkN2Q2Zjc1OTRmMm
                                                             UzZTAxNGFiNjIzZjNiZjU0OGYwMjM4MmYwNjRmNzNjZTZkYTI2M2VlMDQxNDpwOlQ6Rg">Ducks Unlimited Canada website</a>!

More details can be found in the <a href="https://protect.checkpoint.com/v2/r03/___https://www.sciencedirect.com/science/article/pii/S0006320724003161___.YzFjOmR1Y2tzdW5saW1pdGVkY2FuYWRhOmM6bzpiNGRiZjRkZDRkYjViNWI1YjdjODY4NjNmMmY2NTdhODo3OjNiODE6MzgzZDE0ZjU1M2FmYTI4ODA1NzE1YzE0MTI4NWEzOTkzNmZiOWUwM2NkOTNhMWNmNWRlMjJkNmE0MDEwNTc5NjpwOlQ6Rg">research article</a> published in October 2024.


Table 1. Key information from presentation, including method of contact.

| Field | Description |
| ----- | ----- |
| Project name | Predicting the effects of land cover change on biodiversity in Prairie Canada using species distribution models |
| Project date | 2024 |
| Primary contact | j_paterson@ducks.ca |
| Province(s) | AB, SK, MB |
| Modelling software | MaxEnt |
| Model spatial resolution | 805m |
