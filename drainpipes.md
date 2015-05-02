## Drainpipes 0.1 ([comments welcome](https://github.com/okfnau/open-council-data/issues))

Drain pipes known about or maintained by the council.

####General recommendations:

* Format: Polyline geospatial data. GeoJSON (preferred), Shapefile
* Dataset name: [Council name] council drain pipes
* data.gov.au tag: `opencouncildata-drainpipes-0.1`

#### Required fields

#### Reccommended fields
* `material`: The main construction material used to create the drain pipe. One of: `PVC` (pvc pipe), `RCP` (concrete rienforced), `STEL` (steel pipe), `SUB` (sub soil drain),`ACP` (aspestos cement), `ARM` (Armourcore Steel wire reinforced polyethylene pipe), `BB` (black brute), `BC` (box culvert), `BLUESTONE` (Bluestone), `BRK` (brick), `CI` (cast iron), `CONC` (concrete unrienforced), `CULV` (free standing culvert), `DI` (ducile iron), `EARTH` (open earth drain), `EWP` (earthernware pipe), `FRC` (fibre rienforced cement), `GRATE` (Grated pipe), `GRP` (Glass fiber reinforced plastics), `HDPVC` (high density pvc), `LINED` (Geotextile lining), `PE` (polyethylene pipe), `UNK` (Unknown pipe material).
* `width`: The width in millimetres of the drain pipe.
* `unit_type`: The type of unit. One of: `ABAN` (abandoned), `CULV` (freestanding culvert), `DRAIN` (null), `MAJCUL` (major culvet), `OPEN` (open).

#### Optional fields
* `height`: The height in millimetres of the drain pipe if it's not symmetrical.
* `FUPINV`: Upstream Invert.
* `FDNINV`: Downstream Invert.
* `construction_date`: The date the drain pipe was constructed.
* `compkey`: Council specific reference id for the drain pipe segment.
