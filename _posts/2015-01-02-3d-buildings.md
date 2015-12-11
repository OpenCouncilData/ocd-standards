---
category: Misc
path: '/3d-buildings'
title: '3D buildings'
---
## 3D buildings 0.2

A 3D model (not just outline plus height) of buildings and other physical features, used for planning, architecture and communicating proposed construction. Model files should be textured if possible.

A collection of 3D model files should be bundled with a point origin file, to correctly locate each 3D model file in real-world coordinates.

File|Contents
----|----
`origins.csv` (1 file)| one row per model, with latitude and longitude of the origin of that file
`(modelname).3ds` (1+ files)| one file per model. Each model must be oriented with north (increasing latitude) along the positive `Y` axis, and east (increasing longitude) along the positive `X` axis. 

In the fields below, "council ID" means the text string identifying the council, given by the part of the council's website before ".vic.gov.au". Hence, "melbourne", "geelong", "corangamite" etc.

####General recommendations:

&nbsp; | Recommendation
------|------------
Format| Autodesk 3DS. (It has many limitations but is widely used and understood.) CityGML is another emerging possibility.
Dataset name| [Council name] 3D Buildings
data.gov.au tag| `opencouncildata-3d-buildings-0.2`

#### Required fields for origins.csv

Field | Description
------|------------
`filename`| filename of the model referred to. *For example: buildings.3ds*
`lat`| latitude of the origin (Y value 0), in decimal degrees. *For example: -37.5*
`lon`| longitude of the origin (X value 0), in decimal degrees. *For example: 144.5*
`elevation`| elevation of the origin (Z value 0) relative to sea level, in metres.

#### Recommended fields
Field | Description
------|------------
`status`| status of the physical building. One of: `proposed` (in the planning process, work not yet begun), `construction`, `built` (finished), `demolished` (demolition has commenced). If not provided, `built` is assumed.
`desc`| text description of the building. 
`updated`| date of most recent update to this model file, in ISO 8601 format.
`date_built`| date of expected or actual finishing of construction, in ISO 8601 format. *For example: 2012-12-11*
`ref`| council-specific identifier for the model.

#### Optional fields
Field | Description
------|------------
`src`| source of the model as a whole. One of: `AAM` (AAM Group), council ID, `architect` (provided by any architecture firm), or other value as appropriate.
`textur_src`| source of texture imagery. One of: `Pictometry`, `Earthmine`, `Graphical`, `None`, or other value if appropriate.
`geom_src`| source of geometry. One of: `Pictometry` (provided by Pictometry), `architect` (provided by any architecture firm), council ID (created by the council, such as the GIS team), or other value as appropriate.
`date_demol`| date of expected or actual demolition, in ISO 8601 format, or blank if none.
`file_url`| URL where model file can be downloaded. This should be a direct download link, not a landing page.
`height`| height of building in metres. *For example: 44.5*
`material`| primary external building material, one of: `brick`, `wood`, `glass`, `concrete` or other value as appropriate.
`footprint`| council-specific ID of building footprint separately maintained by the council.
`bldg_id`| council-specific ID for the building itself.
`prop_id`| council-specific ID for the property housing the building.
`plan_id`| planning application ID.
`plan_auth`| planning body in which the `plan_id` applies.
`version`| version of the model, in council-specific format.
`suburb`| name of suburb building is within.

#### Fields under discussion
* `isPrimary`
* `renderType`: `textured`, `color_layers`
* `IsWFinding`: `Yes`, `No`
* `ModelNorth`: `WGS84`, `Normal`
* `Position`: `XYZ`, `Minimum Z`, `Normal`
* `IsLOD`: `Yes`, `No`
* `PlansDMRef`
* `Easting`
* `Northing`
 