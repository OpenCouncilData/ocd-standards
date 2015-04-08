## Garbage collection zones 2.0

Zones are physical regions within which residential garbage collection of a given type (waste for landfill, recycling, green waste) are collected on the same day.

* To resolve: Is it better to have one polygon per waste type (and hence, several overlapping), or one polygon per zone, with repeated fields (eg, recycle_schedule, green_schedule, etc).

####General recommendations:

* Format: GeoJSON (preferred), Zipped shapefile
* Dataset name: [Council name] Garbage Collection Zones
* data.gov.au tag: `opencouncildata-garbage-1.2`

####Required fields:

*At least one of the following fields should have a value. If multiple collection types share a zone, publish a single polygon with values in several columns. For example, in one area, rubbish is collected on Tuesdays, and recycling is every second Thursday. If the zones are different (even if overlapping), publish multiple polygons.*

* `rub_day`: Day of the week when rubbish is collected. (E.g., `monday`)
* `rub_weeks`: Number of weeks between rubbish collections. (E.g. `2` for fortnightly)
* `rub_start`: Date of one rubbish collection, to calculate future collection dates from, in ISO 8601. E.g. `2015-04-01`.
* `rub_dates`: (optional) Comma-separated list of dates of future collections. Use this for irregular collections, or in addition to other fields to facilitate data use. E.g. `2015-04-01,2015-04-08,2015-04-15,2015-04-22`
* `rec_day`,`rec_weeks`, `rec_start`,`rec_dates`: Schedule for recycling collection, as above.
* `grn_day`,`grn_weeks`, `grn_start`,`grn_dates`: Schedule for green waste collection, as above.
* `hw_day`,`hw_weeks`,`hw_start`,`hw_dates`: Schedule for hard waste collection, as above.

####Recommended fields:

* `name`: a short name used by your council to identify a zone, such as "Monday waste collection 2" or "Tuesday Area 1".

####Optional fields:

* `desc`: A free text field.
* `rub_desc`: free text field with specific comments about rules for acceptable rubbish collection.
* `rec_desc`, `grn_desc`, `hw_desc`: as above, for recycling, green waste, or hard waste comments.
* `info_url`: The page on your council website with information about garbage collection, eg http://www.geelongaustralia.com.au/residents/waste/ This can be an alternative to, or in addition to, a description field.
* `missed_ph`: The phone number to call for a missed rubbish collection.
