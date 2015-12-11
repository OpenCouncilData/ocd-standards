## Events 0.1
**([Comments welcome!](https://github.com/okfnau/open-council-data/issues))**

Public events such as concerts, festivals or workshops organised or promoted by the council.

####General recommendations

* Format: Various file formats have different benefits for different audiences. We recommend publishing in several formats if practical.
  * CSV: Very widely supported and easy to work with.
  * JSON: Preferred format for mobile and web developers.
  * GeoJSON: Preferred format for web map developers.
  * RSS/Atom: Useful for applications which can consume "feeds" of data.
* Dataset name: [Council name] events
* data.gov.au tag: `events`, `opencouncildata`, `ocd-events-0.1`

#### Required fields
Field | Description
------|------------
`date`           |The date on which the event begins, in `YYYY-MM-DD` format.
`title`          |A short name for the event, for example `Hamlet in the park`
`description`    |A longer description of the event. This could include HTML.

#### Recommended fields
Field | Description
------|------------
`lat`,`lon`            |Location using decimal degrees of latitude and longitude.
`location`             |Location given as text, such as a street address.
`time_start`,`time_end`|Start and end times, in `HH:MM` (24 hour) format.
`info_url`             | URL of a web page with more information about the event.

#### Optional fields

Field | Description
------|------------
`date_end`  | Date on which the event ends, if multiple days.
`image_url` | URL of an image to accompany the text.
`ref`       | Council-specific identifier.
`category`  | Council-specific classification of the event.
