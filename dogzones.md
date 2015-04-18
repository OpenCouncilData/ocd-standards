## Dog zones 0.1

Dog zones are regions which share restrictions or permissions on dog walking, including off-leash, on-leash, or prohibition. Councils are encouraged to provide comprehensive information on where dog walking is allowed or restricted, including other sources of regulations such as state or national parks.

####General recommendations:

* Format: GeoJSON (preferred) in EPSG:4326; zipped shapefile
* Dataset name: [Council name] Garbage Collection Zones
* data.gov.au tags: `dog-walking`, `opencouncildata`, `ocd-dogzones-0.1`
* Polygon areas should not overlap, with the single exception of the `Default` polygon described under `name`.

####Required fields:
* `status`: one of `offleash`, `onleash`, `no`

####Recommended fields:

* `name`: a short name used by your council to identify a zone, such as "Fido Beach". If the special name `Default` is used, this is taken to describe general default regulations for public areas throughout the council area, and should be on a polygon covering the whole LGA boundary.
* `regulation`: free text field describing the source of the regulation in force. For example, `Council` or `State park regulations`
* `comment`: free text field that could include more specific restrictions, information on dog waste management, etc.
* `off_rules`: free text field with specific rules about off-leash dog walking.
####Optional fields:

* `url`: URL pointing to more information about dog walking in this area.
* `ref`: internal council reference number, if any.
* `on_rules`: free text field with specific rules about on-leash dog walking.
* `no_rules`: free text field with specific rules about dog-prohibited areas.
* `status_1`: a different status restriction (as above) that applies during a limited set of dates and/or hours. Outside those dates/hours, `status` applies. Either `dates_1`, or `hours_1`, or both, must be provided.
* `dates_1`: comma-separated, slashed pairs of dates definining ranges during which this status applies (eg, `2015-12-01/2016-01-28,2016-04-03/2016-04-13`)
* `hours_1`: hyphenated range of 0-padded 24-hour times defining time range during which this status applies (eg, `18:00-08:30`). (Comma-separated ranges allowed if necessary.)
* `status_2`,`dates_2`,`hours_2`: an additional status that overrides `status_1` in complex situations.

For example, these restrictions: *"Off-leash permitted from 1 December until 28 February and during the Victorian Easter school holidays each year between the hours of 6.00pm and 9.00am. At all other times during this period dogs are permitted on-leash in this area. Outside of these dates dogs are permitted off-leash at all time"*

Would be implemented as:

* `status`:`offleash`
* `status_1`: `onleash`
* `dates_1`: `2015-12-01/2016-02-28,2016-03-25/2016-04-11`
* `hours_1`: `18:00-09:00`*