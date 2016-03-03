---
category: Boundaries
path: '/garbage'
title: 'Garbage collection zones'
---
## Garbage collection zones 2.2

Zones are physical regions within which residential garbage collection of a given type (waste for landfill, recycling, green waste) are collected on the same day.

Zones that share the same boundaries should be provided as a single polygon with multiple sets of tags (`rub_day`, `grn_day` etc).

[OpenBinMap.org](http://openbinmap.org) shows garbage collection zones already published.

&rarr; <i>**[Find datasets tagged \[waste-collection\] on data.gov.au](http://data.gov.au/dataset?sort=extras_harvest_portal+asc%2C+score+desc&q=&tags=waste-collection)**</i>


#### General recommendations:

&nbsp;| Recommendation
------|------------
 Format| GeoJSON (preferred) in EPSG:4326, Zipped shapefile
 Dataset name| [Council name] Garbage Collection Zones
 data.gov.au tags| `waste-collection`, `ocd-garbage`, `ocd-garbage-2.1`

#### Required fields:

At least one of the following fields should have a value. If multiple collection types share a zone, publish a single polygon with values in several columns. For example, in one area, rubbish is collected on Tuesdays, and recycling is every second Thursday. If the zones are different (even if overlapping), publish multiple polygons.*

Field | Description|Example
------|------------|--------
`rub_day`| Day of the week when rubbish is collected.|`monday`
`rub_weeks`| Number of weeks between rubbish collections. Leave blank for one-off or irregular collections. |`2`
 `rub_start`| Date of one rubbish collection, to calculate future collection dates from, in ISO 8601.|`2015-04-01`
 `rub_dates`| (optional) Comma-separated list of dates of future collections. Use this for irregular collections, or in addition to other fields to facilitate data use.|`2015-04-01,2015-04-08,2015-04-15,2015-04-22`
 `rec_day`, `rec_weeks`, `rec_start`, `rec_dates`| Schedule for recycling collection, as above.
 `grn_day`, `grn_weeks`, `grn_start`, `grn_dates`| Schedule for green waste collection, as above.
 `hw_day`, `hw_weeks`, `hw_start`, `hw_dates`| Schedule for hard waste collection, as above.

#### Recommended fields:

Field | Description|Example
------|------------|-------
`name`| a short name used by your council to identify a zone|"Monday Area 2"

#### Optional fields:

Field | Description|Example
------|------------|-------
`desc`| A free text field.
`rub_name`, `rec_name`, `grn_name`, `hw_name`| A short name describing the physical bin used for that collection|`Landfill bin (red lid)`
`rub_desc`, `rec_desc`, `grn_desc`, `hw_desc`| free text field with specific comments about rules for acceptable rubbish collection.|
`rub_url`, `rec_url`, `grn_url`, `hw_url`| URL pointing to a page with more information specifically about each collection. If there is no page specifically about a type, leave it blank and use the `info_url` field.
`rub_scope`, `rec_scope`, `grn_scope`, `hw_scope`| one of:<br/> `all` (all residents receive this service)<br/> `optional` (residents need to sign up to the service),<br/> `booked` (residents sign up for individual collection dates)
`rub_ok`, `rec_ok`, `grn_ok`, `hw_ok`| semi-colon separated list of things that can be included in this collection type.|`Plastic bottles; tin cans`
`rub_notok`, `rec_notok`, `grn_notok`, `hw_notok`| semi-colon separated list of things that must not be included in this collection type.|`Nappies; car batteries`.
`info_url`| The page on your council website with information about garbage collection in general. This can be an alternative to, or in addition to, a description field. e.g. `http://www.geelongaustralia.com.au/residents/waste/`|
`missed_ph`| The phone number to call for a missed rubbish collection.
