---
category: Infrastructure
path: '/footpaths'
title: 'Footpaths'
---
## Footpaths 0.2
**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

Footpaths known about or maintained by the council.

#### General recommendations

* Format: Polyline geospatial data. GeoJSON (preferred), Shapefile
* Dataset name: [Council name] council footpaths
* data.gov.au tag: `footpaths`, `opencouncildata`, `ocd-footpaths-0.2`

#### Required fields

(None)

#### Recommended fields

Field | Description
------|------------
`paved`| Is the surface a hard material such as asphalt, concrete or slate? `yes` or `no`. 
 `surf`| The main construction material used to create the footpath. Use one of the following values where possible: <br/>`Asphalt`, `Concrete`, `Brick` (including slate, cobbles, setts), `Gravel` (including all graded, unsealed surfaces such as crushed limestone and chert), `Sand`, `Natural` (earth, grass, rocks), `Boardwalk` (including wooden and synthetic bridge decks) , `Sprayseal`. 
`width`| The width in meters of the footpath. E.g. `1.8`
`wheelchair`| Accessibility for wheelchair users. `yes` (no steps, suitable for unassisted use), `assisted` (occasional small steps navigable with assistance), `no` (significant obstacles such as steps, bollards or a steep gradient)

#### Optional fields

Field | Description
------|------------
`surf_desc`| A free-text description of the surface and condition. E.g. "Gravel path with steps and erosion control channels."
`operator`| The name of the council or other organisation (eg VicRoads) maintaining this footpath.
`ref`| Council specific reference id for the footpath segment. 
`bicycle`| Are bicycles allowed on this footpath? (Designated bike paths should be provided in a separate "bike paths" dataset.) One of: `allowed` (bicycles are allowed, as in most parks), `no` (bicycles are forbidden)