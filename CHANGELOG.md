# Who's On First Changelog

_This is a human generated overview of significant changes to Who's On First place data
across all repos. More recent changes are at the top, oldest changes at the bottom._

## 2020 January

### BRAZIL
- Add 5 macroregion records for statistical purposes ([issue #1128](https://github.com/whosonfirst-data/whosonfirst-data/issues/1128))

### CANADA
- Add missing Alberta "unitary" counties around Edmonton, Calgary, and Drumheller to ensure continuous fabric ([issue #1765](https://github.com/whosonfirst-data/whosonfirst-data/issues/1765))

### EGYPT
- Deprecate bunk "testing" locality ([issue #1771](https://github.com/whosonfirst-data/whosonfirst-data/issues/1771))

### INDIA
- Resolve duplicate New Delhi locality ([issue #1785](https://github.com/whosonfirst-data/whosonfirst-data/issues/1785))
- Fix Damunda and Laxmapur locality names ([issue #1788](https://github.com/whosonfirst-data/whosonfirst-data/issues/1788))
- Correct neighbourhood records in Mumbai to have `hierarchy_label=1` ([issue #1783](https://github.com/whosonfirst-data/whosonfirst-data/issues/1783))

### LAOS
- Add missing Nong district ([issue #1782](https://github.com/whosonfirst-data/whosonfirst-data/issues/1782))

### PORTUGAL
- Cleanup regions to ensure Azores and Madeira have features; dissolve 4 existing region geometries into 2 region geometries ([issue #1173](https://github.com/whosonfirst-data/whosonfirst-data/issues/1173))
- Add ~5,000 localadmin level features in Portugal ([issue #1740](https://github.com/whosonfirst-data/whosonfirst-data/issues/1740))

### SERBIA
- Fix Sabac locality name ([issue #1781](https://github.com/whosonfirst-data/whosonfirst-data/issues/1781))

### VENEZUELA
- Add missing Atures municipality ([issue #1767](https://github.com/whosonfirst-data/whosonfirst-data/issues/1767))

### VARIOUS
- Clean up records with a megacity tag ([issue #701](https://github.com/whosonfirst-data/whosonfirst-data/issues/701))
- Ensure megacities have `population` and `population_rank` ([issue #797](https://github.com/whosonfirst-data/whosonfirst-data/issues/797))


## 2019 December

### BRAZIL
- Update Portugese localized names of around 4,500 counties, and correct names of 3 ([issue #1756](https://github.com/whosonfirst-data/whosonfirst-data/issues/1756))

### CANADA
- Update geometry of Quebec to high precision ([issue #1719](https://github.com/whosonfirst-data/whosonfirst-data/issues/1719))

### COSTA RICA
- Correct Liverpool population and Wikidata concordance ([issue #1759](https://github.com/whosonfirst-data/whosonfirst-data/issues/1759))

### FRANCE
- Fix name translations of Barbas locality ([issue #1747](https://github.com/whosonfirst-data/whosonfirst-data/issues/1747))

### INDIA
- Add additional 242,827 name localizations to 18,679 admin places ([issue #1763](https://github.com/whosonfirst-data/whosonfirst-data/issues/1763))
- Add polygons for "100" largest cities in India ([issue #1592](https://github.com/whosonfirst-data/whosonfirst-data/issues/1592))
- Add detailed admin subdivisions for largest localities in India, including: Ahmedabad, Bangalore, Chandigarh, Chennai, Delhi, Hyderabad, Jaipur, Kolkata, Mumbai, and Pune. ([issue #1593](https://github.com/whosonfirst-data/whosonfirst-data/issues/1593))
- Upgrade neighbourhood records in Hyderabad, India ([issue #661](https://github.com/whosonfirst-data/whosonfirst-data/issues/661))
- Correct name of wof:name is "Nekowal" (from "Dadra and Nagar Haveli") ([issue #1722](https://github.com/whosonfirst-data/whosonfirst-data/issues/1722))

### UNITED STATES
- Deprecate duplicate Washington DC record ([issue #1758](https://github.com/whosonfirst-data/whosonfirst-data/issues/1758))
- Fix names in South Park neighbourhood to Dogtown ([Pull #31](https://github.com/whosonfirst-data/whosonfirst-data-admin-us/pull/31))

### VARIOUS
- For localization, add missing `wof:{lang}_x_*` property to macroregion, region, or macrocounty records ([issue #1718](https://github.com/whosonfirst-data/whosonfirst-data/issues/1718))
- Fix invalid JSON in single alt file ([issue #1764](https://github.com/whosonfirst-data/whosonfirst-data/issues/1764))


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
- Updated the properties of two county records in **Germany** ([issue](https://github.com/whosonfirst-data/whosonfirst-data/issues/1697))
  - Fixed by: https://github.com/whosonfirst-data/whosonfirst-data-admin-de/pull/17
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
