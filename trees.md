### Trees

Trees registers contain locations and information about individual trees within the council boundaries. They usually include "street trees", sometimes "park trees", but rarely trees on private property or in bushland. Reasons for collecting the data including planning future growth or maintenance of canopy cover, and managing risk of falling branches.

Format: CSV (preferred), Shapefile, GeoJSON

Required fields:

* `lat`: Latitude, decimal degrees.
* `lon`: Longitude, decimal degrees.

Recommended fields:

* `genus`: Botanical genus, in title case. eg: `Eucalyptus`
* `species`: Botanical genus, in title case. eg: `Regnans`
* `dbh`: Diameter at breast height (130cm above ground), in centimetres. eg: `60`
* `ule_min`: Lower bound on useful life expectancy, when surveyed, in years. eg: `15`
* `ule_max`: Upper bound on useful life expectancy, when surveyed, in years. Blank means an unbounded range, like "20+ 
years". eg: `25`

Optional fields:

* `crown`: Width in metres of the tree's foliage (also known as crown spread). eg: `6`
* `height`: Height in metres. eg: `4`
* `common`: Common name for species (non-standardised), in title case. eg: `Myrtle Beech`
* `location`: Where the tree is located: `park`, `street`, `council`
* `ref`: Council-specific identifier, enabling joining to other datasets. eg `9128`
* `maintenance`: number of months, how often the tree is inspected. eg `24`
* `maturity`: one of `young`, `semi-mature`, `mature`, `over-mature`
* `planted`: date of planting, in ISO8601. eg `1998-04-02`
* `captured`: date of addition to database, in ISO8601. eg `2012-06-08`
* `health`: Health of tree growth: one of `dead`, `poor`,`fair`,`good`
* `structure`: Solidity of tree, unlikelihood of falling. One of `failed`, `poor`, `fair`, `good 
