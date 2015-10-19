# Open Council Data

This repository contains lightweight standards for the publishing of council data. The standards have initially been developed by councils in Victoria, Australia, but are open to other councils to use and participate in developing.

**See it online at http://opencouncildata.org (http://okfnau.github.io/open-council-data/)**

### Why

 To allow datasets from different councils to be easily joined up into something bigger, to support research, app development, knowledge exchange between councils, and use by the public.

[The Open Council Data Map](https://stevage.cartodb.com/viz/43494ef2-61f3-11e5-a667-0e4fddd5de28/map) shows the number of datasets (whether conforming to these standards or not) published by each council around Australia on data.gov.au, data.sa.gov.au, or several Socrata sites. It is updated hourly,
but does not automatically detect councils publishing their first dataset.

<iframe width='100%' height='480' frameborder='0'
src='https://stevage.cartodb.com/viz/43494ef2-61f3-11e5-a667-0e4fddd5de28/embed_map'
allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen>
</iframe>

### Who
This is an open collaboration between councils, Open Knowledge Australia, and other interested participants. [Steve Bennett](http://stevebennett.me) (Open Knowledge) and Will McIntosh (Melbourne City council) are currently leading the effort.

### Background
This is an open collaboration between councils, Open Knowledge Australia, and other interested participants. [Steve Bennett](http://stevebennett.me) (Open Knowledge) and Will McIntosh (City of Melbourne) are currently leading the effort.

### How councils can get started
* Adopt an Open Data policy
  - Download and adapt a template policy (links to come)
* [Create a data.gov.au account](https://toolkit.data.gov.au/index.php?title=Starting_on_datagovau#Getting_an_Account)
* Use tools to automatically extract and upload data
  - [FME workspaces](https://github.com/datagovau/ckan-api-examples/tree/master/FME)
  - OGR scripts

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
* Spatial data should presented as raw latitude/longitude ([EPSG:4326](http://spatialreference.org/ref/epsg/wgs-84/)), not eastings and northings (projected coordinates).
* Unknown information should be indicated as:
    - CSV: empty value (two consecutive commas)
    - GeoJSON: no attribute (preferred), or ""
    - Shapefile: no attribute (preferred), or ""

### Participate

You can help create and refine these standards by:

* participating on the [Open Council Data Google Group](https://groups.google.com/forum/#!forum/opencouncildata)
* raising and commenting on issues on the [Github issue tracker](https://github.com/OKFNau/open-council-data/issues)
* joining the fortnightly Skype chat (email Will McIntosh - will.mcintosh@melbourne.vic.gov.au )
* coming to a weekly [Open Knowledge Melbourne meetup](www.meetup.com/Open-Knowledge-Melbourne/)
* uploading your data to data.gov.au ([get started here]( https://toolkit.data.gov.au/index.php?title=How_to_use_data.gov.au#Getting_an_account_on_data.gov.au))
