---
category: Services
path: '/childcare'
title: 'Childcare centres'
---
## Childcare Centres 0.1
**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

Facilities that look after young children during the day.

&rarr; <i>**[Find datasets tagged \[childcare-centres\] on data.gov.au](http://data.gov.au/dataset?sort=extras_harvest_portal+asc%2C+score+desc&q=&tags=childcare-centres)**</i>


####General recommendations:

&nbsp;| Recommendation
------|------------
Format| Point data. CSV (preferred), GeoJSON
Dataset name| [Council name] childcare centres
data.gov.au tag| `childcare-centres`, `opencouncildata`, `ocd-childcare-centres-0.1`

#### Required fields

Field | Description
------|------------
`lat`, `lon`| Latitude, longitude, decimal degrees. (EPSG:4326) 
`name`| Name of the centre

#### Recommended fields
Field | Description
------|------------
`operator`| The council (or company) that operates the centre. 
`contact_ph`| The centre's telephone number.
`url`| A URL with more information about the centre.

#### Optional fields
Field | Description
------|------------
`ref`| The internal council ID for the centre, if any.
