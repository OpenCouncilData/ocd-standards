## Road closures 0.2
**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

Locations of planned and unplanned road closures due to events, maintenance, natural events or other reasons. For maximum usefulness, this dataset should be updated whenever new information is available (perhaps hourly). Past closures should be removed from the dataset within a short period (eg, 1 day) in order to keep the whole dataset size manageable.

####General recommendations:

&nbsp;| Recommendation
------|------------
Format| GeoJSON in EPSG:4326
Dataset name| [Council name] Road Closures
data.gov.au tags| `road-closures`, `opencouncildata`, `ocd-roadclosures-0.2`
Spatial type|Line data is preferred (representing each segment of road that is affected), but points (general location of closure) and polygon (region in which all roads are closed) are acceptable.

If possible, sort the data with most imminent closures first.



####Required fields
Field | Description
------|------------
`status`| The level of impact: `closed` (no movement), `restricted` (speed restrictions and possible lane closures), `open` (open, included if necessary to avoid doubt), `detour` (this line feature is a recommended detour around another closure)
`start_date`| Date of start of closure, in ISO8601 format: `2015-06-04`
`start_time`| Time of start of closure, in ISO8601 local timezone format: `08:30+10` (preferred) or no timezone format: `08:30`. For an unplanned closure without an exact known start date, use any time in the past. *Do not use UTC format*

####Recommended fields
Field | Description
------|------------
`end_date`, `end_time` | As for `start_date`, `start_time` for the anticipated end of the closure, if known.
`reason`| One of: `Works` (including road works, building construction, water mains), `Event`, `Unplanned` (e.g. emergency maintenance), `Crash`, `Natural` (fire, flood, weather)
`reason_desc`|Free text description of the reason for the closure or restriction.
`status_desc`|Free text description of the extent of the closure or restriction.
`direction`: Direction in which traffic is affected. One of `Both`, `Inbound`,`Outbound`,`North`,`South`,`West`,`East`, etc.
`updated`: The most recent date and time at which this information was known to be current, in combined ISO8601 format (eg, `2015-06-04T08:15+10`)

####Optional fields
Field | Description
------|------------
`source`|The source of the closure, eg `Victoria Police`, `Western Energy`
`delay_mins`|The number of minutes delay anticipated for motorists proceeding through an affected area. Can be either a single number `15` or a range `5-10`.
`impact`|The level of impact this is expected to have on traffic flows in the area, from `1` (minimal) to `5` (severe). This is intended to aid in filtering data for mapping.
`ref`| A council-specific identifier.
`event_id`| A council-specific identifier for an associated event, if any.
`url`|A website link for more information.
`phone`|A phone number to call for more information.
`daily_start`, `daily_end`|For works across multiple days, the time at which closure begins and ends each day, in ISO8601 local timezone (preferred) or no timezone format.