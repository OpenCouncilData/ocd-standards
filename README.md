# Open Council Data

This repository contains lightweight standards for the publishing of council data. It's developed for councils in Victoria, Australia, but would probably apply to other states - and maybe elsewhere, too.

**See it online at http://opencouncil.data.org (http://okfnau.github.io/open-council-data/)**

The primary goal: to allow datasets from different councils to be easily joined up into something bigger, to support research, app development, knowledge exchange between councils, and use by the public.

This map shows the number of datasets (whether conforming to these standards or not) published by each council in Victoria. It is updated hourly,
but does not automatically detect councils publishing their first dataset.

<iframe width='100%' height='480' frameborder='0'
src='http://stevage1.cartodb.com/viz/ac41a874-7b34-11e4-ac15-0e4fddd5de28/embed_map'
allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen>
</iframe>

### Background
This project arose during the course of Steve Bennett's stint as [data guru in residence](http://melbdataguru.tumblr.com). A [basic presentation on these standards](http://tinyurl.com/opendatamav) was given at the MAV (Municipal Association of Victoria) technical forum, December 2014. Will McIntosh from City of Greater Geelong is now chairing the fortnightly Skype calls.

### Principles
We try to make conforming to the standard as easy as possible.

1. As few required fields as possible.
2. Standards are for **transforming** already-collected data. Standards for **collecting** data is a harder problem.
3. The simplest transformation is simply renaming a field, so let's do that.
4. Field names must be 10 characters or fewer, due to Shapefile attribute limitations.

### General guidelines

* All date fields should be provided as ISO8601 ("2014-11-03")
* Additional fields can (and should) be provided, but should be included after recommended fields.
* Numeric values should be provided as a single numeric value ("1.3"). Don't include a range ("1.2 - 1.4"), nor units ("1.3m").

### Participate

You can help create and refine these standards by:

* participating on the Google Group: [Open Data Working Group - Victoria](https://groups.google.com/forum/#!forum/opendatagroup)
* raising and commenting on issues on the [Github issue tracker](https://github.com/OKFNau/open-council-data/issues)
* joining the fortnightly Skype chat (email Will McIntosh - wmcintosh@geelongcity.vic.gov.au )
* coming to a weekly [Open Knowledge Melbourne meetup](www.meetup.com/Open-Knowledge-Melbourne/)
