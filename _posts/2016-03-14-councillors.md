---
category: Non-spatial
path: '/councillors'
title: 'Councillors'
---
# Councillors 0.1
Councillors are the elected representatives of the council, usually representing a specific ward (area). The spreadsheet can include just the current elected councillors, or previous councillors too.

#### General recommendations

&nbsp;|Recommendation
----|----
Format|CSV, RSS
Dataset name| [Council name] councillors
data.gov.au tags| `opencouncildata`, `councillors`, `elections`

#### Required fields

Field|Description
----|----
`name`|Name of the councillor. Do not include "Cr" or "Councillor" prefix.

#### Recommended fields

Field|Description
----|----
`title`|The title of the councillor, such as "Lord Mayor", "Deputy Mayor", or "Councillor".
`ward_name`| Name of the ward the councillor represents.
`ward_id`| External ID of the ward. In Victoria, this should be the VicMap WARD_NUM (eg, Glenferrie is 50704)

#### Optional fields

Field|Description
----|----
`term_start`| Date the member's term began.
`term_end`| Date the member's term ends/ended. For currently serving councillors, this can be ommitted or be the date of the next election.
`portfolio`| The portfolio held by the councillor, if any. Multiple portfolios should be separated by semicolons.
`phone_office`| Office phone number.
`phone_mobile`| Mobile phone number.
`email`| Email address.
`url`| URL to page with more information about the councillor.
`image_url`| URL to image of the councillor.