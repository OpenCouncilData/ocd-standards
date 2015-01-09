# Open Council Data

This repository contains lightweight standards for the publishing of council data. It's developed for councils in Victoria, Australia, but would probably apply to other states - and maybe elsewhere, too.

The primary goal: to allow datasets from different councils to be easily joined up into something bigger, to support research, app development, knowledge exchange between councils, and use by the public.

### Background
This project arose during the course of Steve Bennett's stint as [data guru in residence](http://melbdataguru.tumblr.com). A [basic presentation on these standards](http://tinyurl.com/opendatamav) was given at the MAV (Municipal Association of Victoria) technical forum, December 2014.


### Principles
We try to make conforming to the standard as easy as possible.

1. As few required fields as possible.
2. Standards are for **transforming** already-collected data. Standards for **collecting** data is as harder problem.
3. The simplest transformation is simply renaming a field, so let's do that.


### General guidelines

* All date fields should be provided as ISO8601 ("2014-11-03")
* Additional fields can (and should) be provided, but should be included after recommended fields.
* Numeric values should be provided as a single numeric value ("1.3"). Don't include a range ("1.2 - 1.4"), nor units ("1.3m").