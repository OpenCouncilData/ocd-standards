## Customer service centres 0.1
**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

Customer service centres are places where citizens go to pay fees (rates, fines, pet registration), deposit planning applications, or otherwise interact with council services.


####General recommendations:

* Format: Point data. CSV (preferred), GeoJSON, Shapefile
* Dataset name: [Council name] customer service centres
* data.gov.au tag: `customer-service-centres`, `opencouncildata`, `ocd-customer-service-centres-0.1`

#### Required fields

field | description
------|------------
`lat`, `lon` | Latitude, longitude, decimal degrees. (EPSG:4326)

#### Recommended fields

field | description
------|------------
| `name`| A name identifying the centre. E.g. "Preston Customer Service Centre"
| `services`| Comma-separated list of services provided by the centre. For example: "pet registration,parking fines,rates". Possible values include:<br/> `pet registration`, `parking fines`, `rates`, `planning`, `building permits`, `building permit`, `planning permit`, `engineering permit`, `general permit`, `infringements`, `licensing`, `pet registration`, `general tourism information`, `lodgements`, `keys`, `engineering permits`, `temporary car parking permits`, `collection/drop off`, `disabled parking application`, `fencing requests`, `local laws permit`, `pension rebate`, `stat dec`, `property information request` *(or other, please provide feedback)*
| `address` | Street address. E.g. "274 Gower Street, Preston, VIC 3072"
| `languages`| Comma separated list of non-English languages spoken at the centre (or provided by phone interpreter), in ISO 639-1 (two-letter) codes. For example: `it,vi,zh`
| `access`| Free text description of accessibility. For example: "Fully accessible to wheelchair users; disabled parking at front."
| `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`, `sunday`| Normal opening hours on each day, in 24 hour `HH:MM-HH:MM` format. For example: `08:00-17:30`.
| `holiday`| Normal opening hours on public holidays.

#### Optional fields
Field | Description
------|------------
<<<<<<< HEAD
`desc`| Free text description of services or other information.
`phone`| Telephone number of this center, if any.
