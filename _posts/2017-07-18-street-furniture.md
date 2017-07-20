---
category: Infrastructure
path: '/street-furniture'
title: 'Street furniture'
---
## Street furniture 0.1 (draft for comment)
**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

[Street furniture](https://en.wikipedia.org/wiki/Street_furniture) is the collective term for equipment that serves the public, installed in outdoor space. It includes street lights, signs, bollards, seats, bins, water fountains, barbecues and picnic tables. It does not include buildings or things usually found within buildings, such as toilets, nor road infrastructure such as speed humps, median strips.

&rarr; <i>**[Find datasets matching "furniture" on data.gov.au](https://data.gov.au/dataset?q=furniture&sort=extras_harvest_portal+asc%2C+score+desc)**</i>

#### General recommendations:

&nbsp;| Recommendation
------|------------
Format| Point data. CSV (preferred), GeoJSON
Dataset name| [Council name] street furniture
data.gov.au tag| `street-furniture`, `opencouncildata`

#### Required fields

Field | Description
------|------------
`lat`, `lon`| Latitude, longitude, decimal degrees. (EPSG:4326) 
`type`| Primary classification, from the table below.

Type | Description/synonyms | Possible subtypes
---- |-------------|---------
`bbq`|Barbecue | `electric`,`gas`
`light`|Street light, street lamp
`drinking water`|Drinking fountain, water tap, water bubbler | `fountain` (water goes up for drinking), `tap` (water goes down for filling a bottle), `fountain,tap` (both)
`bicycle parking`|Bicycle hoop, bicycle rack, bicycle rails| `hoop` (loop for two bikes), `rack` (more complex structure for more than two bikes), `pole-mounted` (hoops attached to street signs)
`seat`|Bench
`bollard`|Obstruction primarily intended to block vehicles| `fixed` (permanently in place), `removable` (sometimes not present), `automatic` (raised/lowered by machinery)
`postbox`|Mail box, letter box, for posting letters.|
`flagpole`||
`table`|Picnic table
`sign`|Street signs
`info`|Information boards, maps, plaques|`map`, `history`
`planter`|Raised box for flowers and small plants.
`tree guard`|Protective structure around a tree.
`bin`|Rubbish/litter/garbage/recycling bin for the public.|`landfill`,`recycling`,`commingled` (for waste that will be separated into landfill and recycling later),`organic`,`cardboard`
`advertising`|Signs, poster poles, banner spaces used for promotions.|`bollard` (advertising column), `banner`, `billboard`

#### Recommended fields

Field | Description
------|------------
`owned_by`| The council name, or other organisation, that owns the item.
`managed_by`| The council name, or other organisation, that manages the item.
`subtype` | A subclassification according to the table above (if possible)
`ref`| The internal council ID for the item, if any.

#### Optional fields

Field | Description
------|------------
`address` | Street address. E.g. "274 Gower Street, Preston, VIC 3072"
`access`| Free text description of accessibility. For example: "Fully accessible to wheelchair users; disabled parking at front."
`desc`| Free text description of the item.
`model`|A code identifying the specific manufacturing model of the item.
`info`|URL of a page with relevant information. For instance, bookable banner spaces could link to a page with information about booking them.