## Childcare Centres 0.1

Facilities that look after young children during the day.

####General recommendations:

      | Recommendation
------|------------
Format| Point data. CSV (preferred), GeoJSON
Dataset name| [Council name] childcare centres
data.gov.au tag| `childcare-centres`, `opencouncildata`, `ocd-childcare-centres-0.1`

#### Required fields

Field | Description
------|------------
`lat`, `lon`| Latitude, longitude, decimal degrees. (EPSG:4326) 
`name`| Name of the centre

#### Recommended fields
Field | Description
------|------------
`operator`| The council (or company) that operates the centre. 
`contact_ph`| The centre's telephone number.
`url`| A URL with more information about the centre.

#### Optional fields
Field | Description
------|------------
`ref`| The internal council ID for the centre, if any.
