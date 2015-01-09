### Garbage collection zones

Zones are physical regions within which residential garbage collection of a given type (waste for landfill, recycling, green waste) are collected on the same day.

* To resolve: Is it better to have one polygon per waste type (and hence, several overlapping), or one polygon per zone, with repeated fields (eg, recycle_schedule, green_schedule, etc).

Format: GeoJSON (preferred), Zipped shapefile

Required fields:

*At least one of the following fields should have a value. If multiple collection types share a zone, publish a single polygon with values in several columns. For example, in one area, rubbish is collected on Tuesdays, and recycling is every second Thursday. If the zones are different (even if overlapping), publish multiple polygons.*

* `rub_sched`: Schedule for general household rubbish.
* `rec_sched`: Recycling schedule.
* `grn_sched`: Schedule for green waste collection.
* `*_sched`: Schedule for some other kind of collection, as applicable. (Eg,  `hw_sched` for hard waste). Document these fields.

Schedules are repeated intervals expressed in ISO8601: `R/` *`YYYY-MM-DD`*` /PxW` where `x` is 1 for weekly, 2 for fortnightly, 4 for quasi-monthly. For example, `R/2014-09-08/P2W` (every 2 weeks, starting from Monday 8 Sep 2014). 

Recommended fields:

* `name`: a short name used by your council to identify a zone, such as "Monday waste collection 2" or "Tuesday Area 1".

Optional fields:

* `desc`: A free text field.
* `rub_cmt`: free text field with specific comments about rules for acceptable rubbish collection.
* `rec_cmt`: free text field with specific comments about rules for acceptable waste for recycling.
* `grn_cmt`: free text field with specific comments about rules for acceptable green waste.
* `info_url`: The page on your council website with information about garbage collection, eg http://www.geelongaustralia.com.au/residents/waste/ This can be an alternative to, or in addition to, a description field.
* `missed_col`: The phone number to call for a missed rubbish collection.
