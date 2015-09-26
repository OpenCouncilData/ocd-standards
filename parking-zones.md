## Parking zones 0.1
**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

Areas in which parking is regulated, including on-street metered and unmetered parking, no-parking zones and car parks.

Councils are encouraged to include parking zones provided by private operators, for maximum utility.

####General recommendations:

&nbsp;| Recommendation
------|------------
Format| GeoJSON in EPSG:4326
Dataset name| [Council name] Parking Zones
data.gov.au tags| `parking-restrictions`, `opencouncildata`, `ocd-parking-restrictions-0.1`
Spatial type|Polygon. Each polygon represents one area within which restrictions are identical. For parking on both sides of a street, two separate polygons should be used.


####Required fields
(none)
####Recommended fields
Field | Description
------|------------
`updated`| The most recent date and time at which this information was known to be current, in combined ISO8601 format (eg, `2015-06-04T08:15+10`)
`ref`| The council's identifier for the parking zone.

####Time-dependent restrictions
Field | Description
------|------------
`start`, `end`|Time at which this parking restriction commences/ends, in 24 hour time. Times outside this range are assumed to be free, unless additional restrictions given.<br/>*For example: 17:30*
`days`|Semicolon-delimited list of days on which this restriction applies.  If times are different on different days, create a separate set of restrictions for the other days as explained below.<br/>*For example: `Friday;Saturday;Sunday`.*
`mode`|Semicolon-delimited list of one or more of: `free`,`fee`,`loading zone`,`no standing`,`no parking`,`clearway`, `disabled`
`hourlyfee`|Cost in dollars per hour for the first hour of parking. If paying for one hour is not possible (eg, maximum stay is 30 minutes at $2.20), still convert it to an hourly rate (eg, `4.40`).
`onlyfor`|If parking is restricted to a certain type of vehicle, provide a semicolon-delimited list of: `motorcycle`,`bus`,etc.
`notfor`|If parking is prohibited for certain types of vehicle, provide a semicolon-delimited list of: `caravan`, etc.
`start2`, `end2`, `mode2`, `hourlyfee2`, etc.|When different times of day have different restrictions, specify them with additional columns ending in `2`,`3` etc.

####Optional fields
Field | Description
------|------------
`operator`|The organisation that manages this parking zone. eg `Melbourne`, `VicRoads`, `Interpark`.
`sensor`|Whether an electronic sensor detects overstays. `yes`/`no`
`type`|One of `street` (on-street parking), `carpark`
`feemode`|`ticket`,`meter`,`android`,`ios`,`web`
`payment`|Options for physical payments. One or more of: `card`,`coin`,`note`. Do *not* include payment types for smartphone/web payments, which are assumed to support credit card.
`info_url`|The URL of a webpage with more information about parking in this area.
`capacity`:The number of vehicles that can be accommodated simultaneously.
