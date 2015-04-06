## Wards 0.1

Some councils are divided into areas called "wards", particularly for elections.

####General recommendations:

* Format: Polygon geospatial data. GeoJSON (preferred), Shapefile
* Dataset name: [Council name] council wards
* data.gov.au tag: `opencouncildata-wards-0.1`

#### Required fields

* `name`: Name of the ward, eg "Buckley".

#### Optional fields

* `councillor`: The name of the councillor that currently represents the region.
* `portfolio`: The portfolio held by the councillor, if any.
* `lga`: The name of the council which this ward belongs to.