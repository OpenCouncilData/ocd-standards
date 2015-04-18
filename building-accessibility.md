## Building accessibility ratings 1.1

Some councils provide ratings on accessibility of buildings for wheelchair users. These ratings are in high demand by certain community groups wanting to choose venues suitable for all their members. These ratings may be available for only council buildings, or more broadly.

There are no known standards for this kind of data, and some councils combine them in different ways (eg, a rating of 0, 1 or 2 for the building as a whole).

####General recommendations:

* Format: CSV (preferred), Shapefile, GeoJSON
* Dataset name: [Council name] Building Accessibility Ratings
* data.gov.au tag: `opencouncildata-building-accessibility-1.1`

#### Required fields

* `lat`, `lon`: Latitude, longitude, decimal degrees of centroid or entrance to building. (EPSG:4326)
* 
#### Recommended fields
* `entrance`: Access into the building and its main services. Use one of these values, or blank if unknown.
 * `yes`: an unpowered, wheelchair user can enter the building and access public services without assistance
 * `assisted`: a wheelchair user can enter the building if assiste. _For example, a steep ramp, or a lift requiring an authorised operator._
 * `no`: there is limited or no access for wheelchair users. _For example, a cinema with a ramp entrance, but steps to individual theatres._

* `parking`: One of these values, or blank if unknown.
 * `yes`: disabled parking spaces are available
 * `no`: there is no designated disabled parking

* `toilets`: One of these values, or blank if unknown.
 * `yes`: toilets suitable for wheelchair users are available
 * `no`: there are no toilets suitable for use by wheelchair users

* `name`: A name identifying the building, organisation or business name.
* `address`: The building's street address.

#### Optional fields
* `id`: A council-specific identifier that can used to link to other council-published data for that building, such as a building footprint.
* `assessed`: Date of most recent accessibility assessment, in ISO 8601 (YYYY-MM-DD).
* `comment`: Text description supplementing the `entrance`,`parking` and `toilets` fields.

