# Who's On First Changelog
_This is a human generated overview of significant changes to Who's On First place data 
across all repos. More recent changes are at the top, oldest changes at the bottom._

## 2019 November

### INDIA
- Updated administrative records in select localities in India ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1593))
- Fixed by:
  - https://github.com/whosonfirst-data/whosonfirst-data-admin-in/pull/12
  - https://github.com/whosonfirst-data/whosonfirst-data-admin-in/pull/11
- This work is ongoing and will update neighbourhood, borough, locality, county, and region geometries in and around ten of the most populous localities in India. Two of the ten localities were updated this month, the remaining eight will be completed in December.
- Specific work included:
  - Updating geometries for neighbourhood, borough, locality, county, and region records in Chandigarh and Kolkata
  - Updating properties for these records, including name translations, `mz:` property flags, and `wof:` properties
  - PIP work to update `wof:hierarchy` and `wof:parent_id` properties for all records
  - Validating all geometries using osgeo, validating all records using Who's On First's `go-whosonfirst-validate` tool
  - Completing PIP work to updating or confirming all `wof:hierarchy` properties for all records in the India admin repository

### FRANCE
- Updated French `label:` properties in region records ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1734))
- Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-admin-fr/pull/18
  - Verifying and fixing each unique `"label:fra_x_preferred_longname"` property values for each of the 101 region records

### SCOTLAND
- Updated neighbourhood geometries in Glasgow ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1724))
- Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-admin-gb/pull/18
  - Clipping existing geometries to the Glasgow locality geometry
  - Flagging each updated record with a `mz:is_current` property value of `1`
  - Storing existing geometries in alt-geometry files

### VARIOUS
- Fixed incorrect concordances and name translations in a locality record in **Norway** ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1730))
  - Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-admin-no/pull/7
- Updated the locality geometry of a locality in **Honduras** ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1736)):
  - Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-admin-hn/pull/6
- Minor updates to locality records in **Poland** ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1738))
  - Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-admin-pl/pull/14
- Updated name translations in various locality records ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1743))
  - Fixed locality records in the **Angola**, **Austria**, **Hungary**, **India**, **Lithuania**, **Poland**, **Spain**, and the **United States**.
  - See issue for PR fixes


## 2019 October

### NORWAY
- Updated locality and neighbourhood records in Norway ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/298))
- Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-admin-no/pull/6
- This pull request includes changes at the locality and neighbourhood placetypes in Norway. In summary, each locality record was updated with new geometries, property flags, and name translations. In addition, other administrative placetypes were updated as needed.
- Specific work included:
  - Updating geometries for two records at the region placetype, ensuring Who's On First has the most recent admin1 boundaries in Norway
  - Updating geometries for many records at the locality placetype, clipping geometries along parent boundaries 
  - Updating neighbourhood records, converting some existing locality records to neighbourhood records, and curating new neighbouhrood geometries in a handful of cases
  - Resetting all `lbl:bbox` values for records that received new Polygon or MultiPolygon geometries
  - Validating all geometries using osgeo, validating all records using Who's On First's `go-whosonfirst-validate` tool
  - Adding Wikipedia and Wikidata-sourced name translations to any record without a name translation
  - Completing PIP work to updating or confirming all `wof:hierarchy` properties for all records in the Norway admin repository

### FRANCE
- Corrected postalcode hierarchies in France ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1713))
- Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-postalcode-fr/pull/2
  - Updating "county_id" and "localadmin_id" values in dozens of postalcode records' `wof:hierarchy` properties, also updating `wof:belongsto` and `wof:parent_id` values
  - New postalcode hierarchies in France now maintain the appropriate, current parent administrative records

### ALTERNATE GEOMETRIES
- Addition of `src:alt_label` property to each alt file ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1714))
- Fixed by: Multiple, example: https://github.com/whosonfirst-data/whosonfirst-data-admin-ro/pull/9
  - In order for Who's On First to property publish public SQLite distribution files, each "alt" file in Who's On First needed a `src:alt_label` property added.
  - Alt files in each of the 260 per-country Who's On First repositories were given this property in a series of pull requests.

### POLAND
- Updated county, localadmin, locality, borough, and neighbourhood records in Poland ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1131))
- Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-admin-pl/pull/11
- This pull request includes various changes at five placetypes in Poland. In summary, each localadmin and locality record was updated with updated geometries, property flags, and name translations.
- Specific work included:
  - Adding new source geometries to each localadmin record
  - Adding new source geometries to some locality records, storing some source geometries as "alt" files
  - Adding source concordances to region, county, localadmin records
  - Flagging localadmin and locality as coterminous using the `wof:coterminous` property, as necessary
  - Demoting some locality records to the neighbourhood placetype, as needed
  - Adding new borough records to two localities in Poland - Krakow and Warsaw
  - Adding concordances to the `wof:concordances` propert
  - Validating all geometries using osgeo, validating all records using Who's On First's `go-whosonfirst-validate` tool
  - Adding Wikipedia and Wikidata-sourced name translations to any record without a name translation
  - Completing PIP work to updating or confirming all `wof:hierarchy` properties for all records in the Poland admin repository

_NOTE: This document was created 2019 November. Earlier changes have not been 
retroactively cataloged._