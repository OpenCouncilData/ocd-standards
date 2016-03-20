These are lightweight standards for Australian councils publishing open data. This is an open collaboration between councils, Open Knowledge Australia, MAV Technology, the Local Government Spatial Reference Group and other interested participants. 

[Steve Bennett](http://stevebennett.me) (Open Knowledge) and Will McIntosh (City of Melbourne) chair the group.

### Why

 To allow datasets from different councils to be easily joined up into something bigger, to support research, app development, knowledge exchange between councils, and use by the public.

See the number of datasets already published by councils on the [Open Council Data Map](http://map.opencouncildata.org).

<!-- <iframe width='100%' height='480' frameborder='0'
src='https://stevage.cartodb.com/viz/43494ef2-61f3-11e5-a667-0e4fddd5de28/embed_map'
allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen>
</iframe>
 -->

### Principles
We try to make conforming to the standard as easy as possible.

1. As few required fields as possible.
2. These are interoperability standards are for **transforming** already-collected data only.
3. Match common field names as much as possible.
4. Field names must be 10 characters or fewer, due to Shapefile attribute limitations.

### General guidelines

* All date fields should be provided as YYYY-MM-DD
* Additional fields can (and should) be provided, but should be included after recommended fields.
* Numeric values should be provided as a single numeric value ("1.3"). Don't include a range ("1.2 - 1.4"), nor units ("1.3m").
* Spatial data should presented as raw latitude/longitude ([EPSG:4326](http://spatialreference.org/ref/epsg/wgs-84/)), not eastings and northings (projected coordinates).
* Spatial data should be provided in [CSV-geo-au format](https://github.com/NICTA/nationalmap/wiki/csv-geo-au) if point data, and also [GeoJSON](http://geojson.org/geojson-spec.html).
* Unknown information should be indicated as:
    - CSV: empty value (two consecutive commas)
    - GeoJSON: no attribute (preferred), or ""
    - Shapefile: no attribute (preferred), or ""

For more advice, including licensing, please see the [Open Council Data Toolkit](http://opencouncildata.org).

### Participate

These standards are maintained in a [Github repository](http://github.com/OpenCouncilData/open-council-data) that anyone can contribute to.

You can help create and refine these standards by:

* participating on the [Open Council Data Google Group](https://groups.google.com/forum/#!forum/opencouncildata)
* raising and commenting on issues on the [Github issue tracker](https://github.com/OpenCouncilData/open-council-data/issues)
* joining the fortnightly [Open Council Data video Meetup](http://www.meetup.com/Open-Knowledge-Melbourne/events/) ([email Will McIntosh](mailto:will.mcintosh@melbourne.vic.gov.au))
* coming to a weekly [Open Knowledge Melbourne meetup](https://www.meetup.com/Open-Knowledge-Melbourne/)
* uploading your data to data.gov.au ([get started here](http://opencouncildata.org))
