---
category: Non-spatial
path: '/animalregistrations'
title: 'Animal registrations'
---
## Animal registrations 0.2

**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

Registrations of animals (usually cats and dogs). 

This may be a spatial dataset if it includes the location of the property where the animal is registered, or it may be non-spatial.

It is up to the council to decide whether to include data with privacy considerations such as location. This standard makes no recommendation on that issue.

#### General recommendations:

&nbsp;| Recommendation
------|------------
Format| CSV, also optionally GeoJSON if location data included.
Dataset name| [Council name] animal registrations
data.gov.au tag| `animal-registrations`, `opencouncildata`, `ocd-animal-registrations-0.2`

#### Required fields

Field | Description
------|------------
`name`| The registered name of the animal. If not known, it should be left blank. For example: `Rex`
`type` | The kind of animal: `dog`, `cat`, etc. 

#### Recommended fields

Field | Description
------|------------
`breed` | The breed of animal. Cross breeds can be indicated by as `Poodle X`. For example: `Kelpie`
`colour` | A simple description of the animal's colouring. `Tri` indicates three colours, usually black, tan and white. For example: `Grey`, `Black and white`
`sex` | Male or female: `M` or `F`
`desexed` | Whether the animal has been desexed (neutered). `Y` or `N`
`ref` | The animal's registration identifier.
`microchip`|Whether the animal has been fitted with a microchip. `Y` or `N`

#### Optional fields

Field | Description
------|------------
`lat`, `lon`| Latitude, longitude, decimal degrees of the property where the animal is registered. See the note in intro. (EPSG:4326) 
`suburb` | The suburb in which the animal is registered. For example: `Inverleigh`
`postcode` | The postcode in which the animal is registered. For example: `4563`
`expiration` | The date on which the registration expires. A date in the past or a blank value, indicates that the animal is currently unregistered.
`birth_year` | Year the animal was born.
`tattoo`|Whether the animal has been tattooed, usually in the ear to indicate desexing. `Y` or `N`
`deceased`|Whether the animal is deceased. `Y` or `N`
`class`|A council-specific registration classification. This can include terms like `Working dog`, `Pet`, `Pensioner`.