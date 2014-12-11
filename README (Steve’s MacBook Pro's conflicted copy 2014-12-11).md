## Open Council Data

This repository contains lightweight standards for the publishing of council data. It's developed for councils in Victoria, Australia, but would probably apply to other states - and maybe elsewhere, too.

The primary goal: to allow datasets from different councils to be easily joined up into something bigger, to support research, app development, knowledge exchange between councils, and use by the public.

### Principles
We try to make conforming to the standard as easy as possible.

1. As few required fields as possible.
2. Standards are for **transforming** already-collected data. Standards for **collecting** data is as harder problem.

### Background
This project arose during the course of Steve Bennett's stint as [data guru in residence](http://melbdataguru.tumblr.com). A [basic presentation on these standards](http://tinyurl.com/opendatamav) was given at the MAV (Municipal Association of Victoria) technical forum, December 2014.

### Standards

#### Trees

Trees registers contain locations and information about individual trees within the council boundaries. They usually include "street trees", sometimes "park trees", but rarely trees on private property or in bushland. Reasons for collecting the data including planning future growth or maintenance of canopy cover, and managing risk of falling branches.

Format: CSV, one row per tree

Required fields:
* **`Lat`**: Latitude
* **`Lon`**: Longitude

Recommended fields:

* `genus`: Botanical genus
* `species`: Botanical genus
* `dbh`: Diameter at breast height (130cm above ground), in centimetres.
* `useful_life_min`: Lower bound on useful life expectancy, when surveyed, in years.
* `useful_life_max`: Upper bound on useful life expectancy, when surveyed, in years. Blank means an unbounded range, like "20+ 
years".
