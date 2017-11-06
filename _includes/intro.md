These are lightweight standards for Australian councils publishing open data. This is an open collaboration between councils, Open Knowledge Australia, MAV Technology, the Local Government Spatial Reference Group and other interested participants. 

[Steve Bennett](http://stevebennett.me) is the de facto maintainer of the standards. [Send email](mailto:stevage@gmail.com) if you're interested in helping out.

### Goals

The Open Council Data Standards focus on making it easy to join datasets across council boundaries, to support research, app development, knowledge exchange between councils, and use by the public. They focus on datasets which are:

- commonly held by many different councils
- of use to data consumers in aggregated forms
- not already available in aggregated forms

See the number of datasets already published by councils on the [Open Council Data Map](http://map.opencouncildata.org).

The long term vision is an Open Council Data Platform, which automatically aggregates conformant datasets from all councils. You can see [a prototype here](https://opencouncildata.github.io/Datasite).

<figure>
<img src="images/garbage-zones-aggregated.png" style="width:357px;height:285px;">
<figcaption>Garbage collection zones published by Victorian councils (July 2017).</figcaption>
</figure>

<!-- <iframe width='100%' height='480' frameborder='0'
src='https://stevage.cartodb.com/viz/43494ef2-61f3-11e5-a667-0e4fddd5de28/embed_map'
allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen>
</iframe>
 -->

### Principles for standards
We try to make conforming to the standard as easy as possible.

1. Minimise required fields.
2. No requirements about data collection or managment, only **transformation** of existing data.
3. Follow common field names as much as possible.
4. Field names must be 10 characters or fewer, due to legacy Shapefile attribute limitations.

### General guidelines for all datasets

OpenCouncilData standards cover two types of datasets only:

* **Tabular datasets** (spreadsheets), **point datasets** (spatial): [CSV format](http://frictionlessdata.io/guides/csv/).
    - No headers.
    - Indicate unknown or null values as empty values (two consecutive commas)
    - Add any additional, non-standard, fields after standard fields.
    - For **point datasets**, `lat` and `lon` columns are *required*, containing decimal degrees (eg -37.5). See the [CSV-geo-au format](https://github.com/NICTA/nationalmap/wiki/csv-geo-au) for more info.
* **Spatial data** (lines and polygons): [GeoJSON format](http://geojson.org/geojson-spec.html).
    - Locations must be given in [EPSG:4326](http://spatialreference.org/ref/epsg/wgs-84/) (latitude/longitude in decimal degrees, not projected coordinates such as eastings and northings).

Requirements that apply to both types:

* Express dates as `2017-01-20`. 
* Express times as either `2017-01-20T04:30Z` (UTC time) or `2017-01-20T14:30T10` (local time with timezone). [More information](https://en.wikipedia.org/wiki/ISO_8601).
* Express numeric values as a single numeric value: `1.3`. Don't include a range (`1.2 - 1.4`), nor units (`1.3m`).

For more advice, including licensing, please see the [Open Council Data Toolkit](http://opencouncildata.org).

### Participate

These standards are maintained in a [Github repository](http://github.com/OpenCouncilData/open-council-data) that anyone can contribute to.

You can help create and refine these standards by:

* participating on the [Open Council Data Google Group](https://groups.google.com/forum/#!forum/opencouncildata)
* raising and commenting on issues on the [Github issue tracker](https://github.com/OpenCouncilData/open-council-data/issues)
* uploading your data to data.gov.au ([get started here](http://opencouncildata.org))
