---
category: Services
path: '/facilities'
title: 'Facilities'
---
## Facilities 0.1 (draft for comment)
**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

"Facilities" are a broad range of services and amenities provided by the council which generally meet three criteria:
- they are in a specific building
- they are accessible by certain members of the public, at least sometimes
- they generally involve interaction with staff.

The range of services provided varies greatly across the country. It would be very difficult to define a precise vocabulary which every council agrees on, so if none the proposed types fits your need, please use another, and please open an issue or start a discussion to suggest it.

&rarr; <i>**[Find datasets tagged \[facilities\] on data.gov.au](http://data.gov.au/dataset?sort=extras_harvest_portal+asc%2C+score+desc&q=&tags=facilities)**</i>

#### General recommendations:

&nbsp;| Recommendation
------|------------
Format| Point data. CSV (preferred), GeoJSON
Dataset name| [Council name] services and facilities
data.gov.au tag| `facilities`, `opencouncildata`

#### Required fields

Field | Description
------|------------
`lat`, `lon`| Latitude, longitude, decimal degrees. (EPSG:4326) 
`name`| Name of the facility. Each should be unique if at all possible.
`type`| Primary classification, from the list above.

Types: `library`, `aged care`, `neighbourhood house`, `health clinic`, `medical service`, `food service`, `place of worship`, `childcare`, `kindergarten`, `swimming pool`, `gym`, `transfer station`


#### Recommended fields

Field | Description
------|------------
`owned_by`|The council name, or other organisation, that owns the facility.
`managed_by`|The council name, or other organisation, that manages the facility.
`contact_ph`| The facility's telephone number.
`url`| A URL with more information about the facility.
`subtype` | A subclassification according to the council's needs. (No defined list of these at present.)
`address` | Street address. E.g. "274 Gower Street, Preston, VIC 3072"
`access`| Free text description of accessibility. For example: "Fully accessible to wheelchair users; disabled parking at front."
`monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`, `sunday`| Normal opening hours on each day, in 24 hour `HH:MM-HH:MM` format. For example: `08:00-17:30`.
`holiday`| Normal opening hours on public holidays.
`desc`| Free text description of the facility

#### Optional fields

Field | Description
------|------------
`type2`| If a facility fits equally into several categories (for example, a childcare centre is also a kindergarten), add the extra type here. If there are two distinct services housed together (for example, a childcare centre and a maternal health clinic), it's better to have two distinct entries with slightly different locations.
`ref`| The internal council ID for the facility, if any.
