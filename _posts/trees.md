## Trees 1.3

Trees registers contain locations and information about individual trees within the council boundaries. They usually include "street trees", sometimes "park trees", but rarely trees on private property or in bushland. Reasons for collecting the data including planning future growth or maintenance of canopy cover, and managing risk of falling branches.

[OpenTrees.org](http://opentrees.org) shows council tree inventories already published:

<iframe src="http://opentrees.org?embed" style="height: 600px; width: 800px;"></iframe>

####General recommendations:

&nbsp;| Recommendation
------|------------
Format| CSV (preferred), Shapefile, GeoJSON
Dataset name| [Council name] Street and Park Trees
data.gov.au tag| `trees`, `opencouncildata`, `ocd-trees-1.3`

When information is available only as a range (eg, diameter is recorded as 100-150cm), the middle of the range should be presented as the field name, with an additional `_min` and `_max`. For example, `dbh`: 125, `dbh_min`: 100, `dbh_max`, 150. 

If the information is only available as an unbounded range (eg, height greater than 5 metres), then do the same with no `_max`. For example, `height`: 5, `height_min`: 5.

####Required fields:

Field | Description
------|------------
`lat`, `lon`| Latitude, longitude, decimal degrees. (EPSG:4326)

####Recommended fields:

Field | Description
------|------------
`genus`| Botanical genus, in title case. eg: `Eucalyptus`
`species`| Botanical genus, in title case. Leave blank if not known (not "Sp."). eg: `Regnans`
`dbh`| Diameter at breast height (130cm above ground), in centimetres. eg: `60`. (See *General recommendations* for ranges.)
`year_min`| Lower bound on year that tree is expected to live to. (That is, a tree surveyed in 2008 with useful life expectancy range of 10-15 years would be `2018`).
`year_max`| Upper bound on year that tree is expected to live to. (`2023` in this example)

####Optional fields:

Field | Description
------|------------
`crown`| Width in metres of the tree's foliage (also known as crown spread). eg: `6` (See *General recommendations* for ranges.) 
`height`| Height in metres. eg: `4`. (See *General recommendations* for ranges.)
`common`| Common name for species (non-standardised), in title case. eg: `Myrtle Beech`
`location`| Where the tree is located: `park`, `street`, `council`
`ref`| Council-specific identifier, enabling joining to other datasets. eg `9128`
`maintenance`| number of months, how often the tree is inspected. eg `24`
`maturity`| one of `young`, `semi-mature`, `mature`, `over-mature`
`planted`| date of planting, in ISO8601. eg `1998-04-02`
`updated`| date of addition to database or most recent revision, in ISO8601. eg `2012-06-08`
`health`| Health of tree growth: one of `stump`, `dead`, `poor`,`fair`,`good`
`structure`| Solidity of tree, unlikelihood of falling. One of `failed`, `poor`, `fair`, `good`
`variety`| Any part of the scientific name below species level, including subspecies or variety.
`description`| Other information about the tree that is not its scientific name or species.
`family`| Botanical family.
`dbh_min`, `dbh_max`, `height_min`, `height_max`, `crown_min`, `crown_max`|  See *General recommendations*.
`ule_min`, `ule_max`| Lower and upper bound on useful life expectancy, when surveyed, in years. eg: `15`. *See also `year_max`,`year_min`* 
`address`| Street address.
