# Who's On First Changelog
_This is a human generated overview of significant changes to Who's On First place data 
across all repos. More recent changes are at the top, oldest changes at the bottom._

## 2019 October

### NORWAY:
- Updated locality and neighbourhood records in Norway (issue: #298)
- Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-admin-no/pull/6
- This pull request includes changes at the locality and neighbourhood placetypes in Norway. In summary, each locality record was updated with new geometries, property flags, and name translations. In addition, other administrative placetypes were updated as needed.
- Specific work included:
  - Updating geometries for two records at the region placetype, ensuring Who's On First has the most recent admin1 boundaries in Norway
  - Updating geometries for many records at the locality placetype, clipping geometries along parent boundaries 
  - Updating neighbourhood records, converting some existing locality records to neighbourhood records, and curating new neighbouhrood geometries in a handful of cases
  - Resetting all `lbl:bbox` values for records that received new Polygon or MultiPolygon geometries
  - Validating all geometries using osgeo, validating all records using Who's On First's `go-whosonfirst-validate` tool
  - Adding Wikipedia and Wikidata-sourced name translations to any record without a name translation
  - Completing PIP work to updating or confirming all `wof:hierarchy` properties for all records in the Poland admin repository

### FRANCE:
- Corrected postalcode hierarchies in France (issue: #1713)
- Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-postalcode-fr/pull/2
  - Updating "county_id" and "localadmin_id" values in dozens of postalcode records' `wof:hierarchy` properties, also updating `wof:belongsto` and `wof:parent_id` values
  - New postalcode hierarchies in France now maintain the appropriate, current parent administrative records

### ALTERNATE GEOMETRIES:
- Addition of `src:alt_label` property to each alt file (issue: #1714)
- Fixed by: Multiple, example: https://github.com/whosonfirst-data/whosonfirst-data-admin-ro/pull/9
  - In order for Who's On First to property publish public SQLite distribution files, each "alt" file in Who's On First needed a `src:alt_label` property added.
  - Alt files in each of the 260 per-country Who's On First repositories were given this property in a series of pull requests.

### POLAND:
- Updated county, localadmin, locality, borough, and neighbourhood records in Poland (issues: #1131)
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