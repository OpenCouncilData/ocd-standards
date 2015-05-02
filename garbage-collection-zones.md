## Garbage collection zones 2.2

Zones are physical regions within which residential garbage collection of a given type (waste for landfill, recycling, green waste) are collected on the same day.

Zones that share the same boundaries should be provided as a single polygon with multiple sets of tags (`rub_day`, `grn_day` etc).

[OpenBinMap.org](http://openbinmap.org) shows garbage collection zones already published:

<iframe src="http://openbinmap.org?embed=true" style="height: 600px; width: 800px;"></iframe>

####General recommendations:

&nbsp;| Recommendation
------|------------
 Format| GeoJSON (preferred) in EPSG:4326, Zipped shapefile
 Dataset name| [Council name] Garbage Collection Zones
 data.gov.au tags| `waste-collection`, `ocd-garbage`, `ocd-garbage-2.1`

####Required fields:

At least one of the following fields should have a value. If multiple collection types share a zone, publish a single polygon with values in several columns. For example, in one area, rubbish is collected on Tuesdays, and recycling is every second Thursday. If the zones are different (even if overlapping), publish multiple polygons.*

Field | Description
------|------------
`rub_day`| Day of the week when rubbish is collected. (E.g., `monday`)
`rub_weeks`| Number of weeks between rubbish collections. Leave blank for one-off or irregular collections. (E.g. `2` for fortnightly)
 `rub_start`| Date of one rubbish collection, to calculate future collection dates from, in ISO 8601. E.g. `2015-04-01`.
 `rub_dates`| (optional) Comma-separated list of dates of future collections. Use this for irregular collections, or in addition to other fields to facilitate data use. E.g. `2015-04-01,2015-04-08,2015-04-15,2015-04-22`
 `rec_day`, `rec_weeks`, `rec_start`, `rec_dates`| Schedule for recycling collection, as above.
 `grn_day`, `grn_weeks`, `grn_start`, `grn_dates`| Schedule for green waste collection, as above.
 `hw_day`, `hw_weeks`, `hw_start`, `hw_dates`| Schedule for hard waste collection, as above.

####Recommended fields:

Field | Description
------|------------
`name`| a short name used by your council to identify a zone, such as "Monday waste collection 2" or "Tuesday Area 1".

####Optional fields:

Field | Description
------|------------
`desc`| A free text field.
`rub_name`| A short name describing the physical bin used for rubbish (for example, `Landfill bin (red lid`)
`rec_name`, `grn_name`, `hw_name`| As above for other collections types (for example `Black recycling tub`, `Garden waste bin`)
`rub_desc`| free text field with specific comments about rules for acceptable rubbish collection.
`rec_desc`, `grn_desc`, `hw_desc`| as above, for recycling, green waste, or hard waste comments.
`rub_url`| URL pointing to a page with more information specifically about rubbish collection
`rec_url`, `grn_url`, `hw_url`| as above, for pages specifically about each collection type. If there is no page specifically about a type, leave it blank and use the `info_url` field.
`rub_scope`| one of `all` (all residents receive this service), `optional` (residents need to sign up to the service), `booked` (residents sign up for individual collection dates)
`rec_scope`, `grn_scope`, `hw_scope`| as above for other collection types.
`rub_ok`, `rec_ok`,`grn_ok`, `hw_ok`| semi-colon separated list of things that can be included in this collection type. For example: `Plastic bottles; tin cans`
`rub_notok`, `rec_notok`, `grn_notok`, `hw_notok`| semi-colon separated list of things that must not be included in this collection type. For example: `Nappies; car batteries`.
`info_url`| The page on your council website with information about garbage collection in general, eg http://www.geelongaustralia.com.au/residents/waste/ This can be an alternative to, or in addition to, a description field.
`missed_ph`| The phone number to call for a missed rubbish collection.
