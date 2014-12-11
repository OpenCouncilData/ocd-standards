## Open Council Data

This repository contains lightweight standards for the publishing of council data. It's developed for councils in Victoria, Australia, but would probably apply to other states - and maybe elsewhere, too.

The primary goal: to allow datasets from different councils to be easily joined up into something bigger, to support research, app development, knowledge exchange between councils, and use by the public.

### Principles
We try to make conforming to the standard as easy as possible.

1. As few required fields as possible.
2. Standards are for **transforming** already-collected data. Standards for **collecting** data is as harder problem.
3. The simplest transformation is simply renaming a field, so let's do that.

### Background
This project arose during the course of Steve Bennett's stint as [data guru in residence](http://melbdataguru.tumblr.com). A [basic presentation on these standards](http://tinyurl.com/opendatamav) was given at the MAV (Municipal Association of Victoria) technical forum, December 2014.

### Standards

#### Trees

Trees registers contain locations and information about individual trees within the council boundaries. They usually include "street trees", sometimes "park trees", but rarely trees on private property or in bushland. Reasons for collecting the data including planning future growth or maintenance of canopy cover, and managing risk of falling branches.

Format: CSV (preferred), Shapefile, GeoJSON

Required fields:
* `Lat`: Latitude
* `Lon`: Longitude

Recommended fields:

* `genus`: Botanical genus
* `species`: Botanical genus
* `dbh`: Diameter at breast height (130cm above ground), in centimetres.
* `useful_life_min`: Lower bound on useful life expectancy, when surveyed, in years.
* `useful_life_max`: Upper bound on useful life expectancy, when surveyed, in years. Blank means an unbounded range, like "20+ 
years".

#### Garbage collection zones

Zones are areas within which residential garbage collection of a given type (waste for landfill, recycling, green waste) are collected on the same day.

* To resolve: Is it better to have one polygon per waste type (and hence, several overlapping), or one polygon per zone, with repeated fields (eg, recycle_schedule, green_schedule, etc).

Format: GeoJSON (preferred), Zipped shapefile

Required fields:

At least one of the following fields should have a value. If multiple collection types share a zone, publish a single polygon with values in several columns. For example, in one area, rubbish is collected on Tuesdays, and recycling is every second Thursday. If the zones are different (even if overlapping), publish multiple polygons.

* `rubbish_schedule`: Schedule for general household rubbish, as above.. A repeated interval expressed in ISO8601. For example, `R/2014-09-08/P2W` (every 2 weeks, starting from Monday 8 Sep 2014). It's as simple as `R/` *`YYYY-MM-DD`*` /PxW` where `x` is 1 for weekly, 2 for fortnightly, 4 for monthly. etc.
* `recycling_schedule`: Recycling schedule as above.
* `green_schedule`: Schedule for green waste collection, as above.
* `*_schedule`: Schedule for some other kind of collection, as applicable. (Eg, hardwaste_schedule).

Recommended fields:
* `name`: a short name used by your council to identify a zone, such as "Monday waste collection 2" or "Tuesday Area 1".

Optional fields:
* `description`: A free text field. This could include information like rules for acceptable waste
* `rubbish_comment`, `green_comment`, `recycling_comment`: free text fields with specific comments about each kind of waste in this collection.
* `info_url`: The page on your council website with information about garbage collection, eg http://www.geelongaustralia.com.au/residents/waste/ This can be an alternative to, or in addition to, a description field.
* `missed_collection_phone`: The phone number to call for a missed rubbish collection.