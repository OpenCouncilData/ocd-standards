## Footpaths 0.2

Footpaths known about or maintained by the council.

####General recommendations

* Format: Polyline geospatial data. GeoJSON (preferred), Shapefile
* Dataset name: [Council name] council footpaths
* data.gov.au tag: `opencouncildata-footpaths-0.1`

#### Required fields

#### Recommended fields
* `paved`: Is the surface a hard material such as asphalt, concrete or slate? `yes` or `no`. 
* `surf`: The main construction material used to create the footpath. Use one of the following values where possible: `Asphalt`, `Concrete`, `Brick` (including slate, cobbles, setts), `Gravel` (including all graded, unsealed surfaces such as crushed limestone and chert), `Sand`, `Natural` (earth, grass, rocks), `Boardwalk` (including wooden and synthetic bridge decks) , `Sprayseal`. 
* `width`: The width in meters of the footpath. E.g. `1.8`
* `wheelchair`: Accessibility for wheelchair users. `yes` (no steps, suitable for unassisted use), `assisted` (occasional small steps navigable with assistance), `no` (significant obstacles such as steps, bollards or a steep gradient)

#### Optional fields
* `surf_desc`: A free-text description of the surface and condition. E.g. "U"
* `operator`: The name of the council or other organisation (eg VicRoads) maintaining this footpath.
* `ref`: Council specific reference id for the footpath segment. 
* `bicycle`: Are bicycles allowed on this footpath? (Designated bike paths should be provided in a separate "bike paths" dataset.) One of: `allowed` (bicycles are allowed, as in most parks), `no` (bicycles are forbidden)