---
category: Infrastructure
path: '/drainpipes'
title: 'Drainpipes'
---
## Drainpipes 0.2
**([Comments welcome!](https|//github.com/okfnau/open-council-data/issues))**

Drain pipes known about or maintained by the council.

&rarr; **Find [datasets tagged [drainpipes] on data.gov.au](http://data.gov.au/dataset?sort=extras_harvest_portal+asc%2C+score+desc&q=&tags=drainpipes)**

#### General recommendations:

&nbsp; | Recommendation
-------|------------
Format | GeoJSON (preferred), Shapefile
Dataset name| [Council name] council drain pipes
data.gov.au tag| `drainpipes`, `opencouncildata`, `ocd-drainpipes-0.2`



#### Required fields

(none)

#### Recommended fields

Field | Description
------|------------
`carrying`|The contents of the pipe: `Drinking water`, `Stormwater`, `Sewage`
`material`| One of: `Plastic`,`Concrete`,`Brick` (including stonework), `Metal`,`Earthenware`, `Earth`

#### Optional fields

Field | Description
------|------------
`mat_desc`| Free text description of the building material (eg `Fibre-reinforced concrete`)
`form`| The general shape. One of: `Pipe` (closed, buried pipe), `Exposed` (closed pipe at least partially visible), `Open`, `Culvert`
`height_mm`| The height in millimetres of the drain pipe if it's not symmetrical.
`width_mm`| The width in millimetres of the drain pipe.
`built`| The date the drain pipe was constructed.
`ref`| Council specific reference id for the drain pipe segment.
`comment`|Free text, other information as relevant.
`operator`|Name of council or organisation responsible for maintainance.