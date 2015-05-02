## Toilets 1.2

Public toilets known about or operated by the council.

####General recommendations:

      | Recommendation
------|------------
Format| CSV (preferred), GeoJSON, Shapefile, 
Dataset name| [Council name] Public Toilets
data.gov.au tag| `toilets`, `opencouncildata`, `ocd-toilets-1.2`

#### Required fields

Field | Description
------|------------
`lat`, `lon`| Latitude, longitude, decimal degrees of building centroid or entrance. (EPSG:4326)

#### Recommended fields

Field | Description
------|------------
`name`| A description that may help identify the facility (eg, "Smith Reserve Playground")
`female`| Whether toilets for women are available (`yes`,`no`). (Tag unisex toilets as `yes`)
`male`| Whether toilets for men are available (`yes`, `no`). (Tag unisex toilets as `yes`)
`wheelchair`| Whether toilets accessible by wheelchair users are available. (`yes`, `no`)
`week_open`| What time the toilets open on weekdays, in 0-padded 24 hour time. `00:00` for always open/closed.
`week_close`| What time the toilets close on weekdays, in 0-padded 24 hour time. `24:00` for always open, `00:00` for always closed.
`sat_open`| As above for Saturdays.
`sat_close`| As above for Saturdays.
`sun_open`| As above for Sundays.
`sun_close`| As above for Sundays.

#### Optional fields
Field | Description
------|------------
`comment`| Any additional comments, such as for opening hours that can't be represented in the above scheme.
`access_cmt`| Additional comments about accessibility, such as if the toilets are inside a building that is difficult to access.
`needle_bin`| Whether a syringe disposal bin is present (`yes`/`no`).
`operator`| The name of the organisation managing the toilet (eg, your council name, or a business name.)
`drink_tap`| Whether water for drinking is available (`yes`/`no`)