# Who's On First Changelog

_This is a human generated overview of significant changes to Who's On First place data
across all repos. More recent changes are at the top, oldest changes at the bottom._

## 2020 April

### AFGHANISTAN
- Update Fatah record to remove funky name translation. ([Pull request #11](https://github.com/whosonfirst-data/whosonfirst-data-admin-af/pull/11))

### CZECHIA
- Add name and label localizations for 14 region records, in Czech and English. ([Pull request #10](https://github.com/whosonfirst-data/whosonfirst-data-admin-cz/pull/10) related to [Issue #1640](https://github.com/whosonfirst-data/whosonfirst-data/issues/1640))

### DENMARK
- Update Denmark region name translations and `wof:name` values. ([Issue #1453](https://github.com/whosonfirst-data/whosonfirst-data/issues/1453))

### GERMANY
- Update Korzendorf record's German and English names. ([Pull request #24](https://github.com/whosonfirst-data/whosonfirst-data-admin-de/pull/24))

### INDIA
- Update Gandhuan record's default and English names. ([Pull request #42](https://github.com/whosonfirst-data/whosonfirst-data-admin-in/pull/42))
- Update Jhanbke record's default and English names. ([Pull request #43](https://github.com/whosonfirst-data/whosonfirst-data-admin-in/pull/43))

### ITALY
- Update Fie allo Sciliar to resolve funky `�` character in names. ([Pull request #18](https://github.com/whosonfirst-data/whosonfirst-data-admin-it/pull/18) related to [Issue #1830](https://github.com/whosonfirst-data/whosonfirst-data/issues/1830))

### NORWAY
- Update Norway region name translations and `wof:name` values. ([Issue #1445](https://github.com/whosonfirst-data/whosonfirst-data/issues/1445))

### PORTUGAL
- Add name and label localizations for 18 region records, in Portuguese and English. ([Pull request #11](https://github.com/whosonfirst-data/whosonfirst-data-admin-pt/pull/11) related to [Issue #1640](https://github.com/whosonfirst-data/whosonfirst-data/issues/1640))

### ROMANIA
- Add name and label localizations for 42 region records, in Romanian and English. ([Pull request #13](https://github.com/whosonfirst-data/whosonfirst-data-admin-ro/pull/13) related to [Issue #1640](https://github.com/whosonfirst-data/whosonfirst-data/issues/1640))

### SWITZERLAND
- Update Schaffhausen record's English names. ([Pull request #16](https://github.com/whosonfirst-data/whosonfirst-data-admin-ch/pull/16))

### UKRAINE
- Update Polyakhova reocrd to remove bad name variant. ([Pull request #10](https://github.com/whosonfirst-data/whosonfirst-data-admin-ua/pull/10))

### UNITED STATES
- Resolve duplicate Kansas City, MO records. ([Issue #1791](https://github.com/whosonfirst-data/whosonfirst-data/issues/1791))
- Update Cheektowasa record's default and English names. ([Pull request #55](https://github.com/whosonfirst-data/whosonfirst-data-admin-us/pull/55))

### VARIOUS
- Run wiki names script on "high priority" places. ([Issue #1821](https://github.com/whosonfirst-data/whosonfirst-data/issues/1821))
- Fix `ST_GeogFromGeoJSON` fails on a handful of country geometries. ([Issue #1819](https://github.com/whosonfirst-data/whosonfirst-data/issues/1819))
- Add name translations to continent records. ([Issue #1818](https://github.com/whosonfirst-data/whosonfirst-data/issues/1818))
- Fix Spratley Islands names and concordances. ([Issue #1459](https://github.com/whosonfirst-data/whosonfirst-data/issues/1459))
- Update locality names for Schaffhausen, Bachowali, Charik, and Ballyhisky. ([Issue #1805](https://github.com/whosonfirst-data/whosonfirst-data/issues/1805))
- Fix 2,031 cases of bunk new lines/whitespaces newline in wof:name values (this makes it easier to import into Postgres). ([Issue #1796](https://github.com/whosonfirst-data/whosonfirst-data/issues/1796))
- Goodbye old Tempelhof Central Airport. ([Pull request #18](https://github.com/whosonfirst-data/whosonfirst-data-admin-xy/pull/18))


## 2020 March

### GAMBIA
- Update names for Banjul. ([Issue #1802](https://github.com/whosonfirst-data/whosonfirst-data/issues/1802))

### INDIA
- Resolve Devli duplicate of Delhi. ([Issue #1784](https://github.com/whosonfirst-data/whosonfirst-data/issues/1784))
- Update Bajowali English and default names. ([Pull request #38](https://github.com/whosonfirst-data/whosonfirst-data-admin-in/pull/38))
- Update Chirak English and default names. ([Pull request #39](https://github.com/whosonfirst-data/whosonfirst-data-admin-in/pull/39))

### IRELAND
- Update Ballylusky English and default names. ([Pull request #12](https://github.com/whosonfirst-data/whosonfirst-data-admin-ie/pull/12))

### ITALY
- Updates English, Italian, and French label properties on `region` records, population and src properties, and concordances. ([Pull request #14](https://github.com/whosonfirst-data/whosonfirst-data-admin-it/pull/14))

### NORWAY
- Adds/updates `label` properties to Norway `region` records. ([Pull request #13](https://github.com/whosonfirst-data/whosonfirst-data-admin-no/pull/13))
    - Also updates `wof:lang*` properties in all `region` and `country` records
    - Corrects `name` property values, storing variant names when applicable

### POLAND
- Update Roznowo with English and Polish names. ([Pull request #16](https://github.com/whosonfirst-data/whosonfirst-data-admin-pl/pull/16))

### UNITED KINGDOM
- Update to ONS Feb 2020 data release for `postalcode` records. ([Issue #1685](https://github.com/whosonfirst-data/whosonfirst-data/issues/1685))

### UNITED STATES
- Update East Side, Kansas City neighbourhood. ([Issue #1789](https://github.com/whosonfirst-data/whosonfirst-data/issues/1789))
- Update Minnewawa, MN English and default names. ([Issue #1799](https://github.com/whosonfirst-data/whosonfirst-data/issues/1799))
- Update Place Shawnee. ([Pull request #49](https://github.com/whosonfirst-data/whosonfirst-data-admin-us/pull/49))

### VARIOUS
- Import DigitalEnvoy concordances for `country`, `region`, `localadmin`, and `marketarea` records (eg `digitalenvoy:country_code`). ([Issue #1807](https://github.com/whosonfirst-data/whosonfirst-data/issues/1807))
- Add `README` and `ISSUE_TEMPLATE` to all the new admin repos. ([Issue #1667](https://github.com/whosonfirst-data/whosonfirst-data/issues/1667))
- Add `wof:repo` property to all alt files. ([Issue #1729](https://github.com/whosonfirst-data/whosonfirst-data/issues/1729))
- Add missing `src:alt_label` properties. ([Issue #1804](https://github.com/whosonfirst-data/whosonfirst-data/issues/1804))
- Add new `wof:geom_alt` property. ([Issue #1793](https://github.com/whosonfirst-data/whosonfirst-data/issues/1793))
- Remove whosonfirst-data-{country code} repos as we went with different naming convention. ([Issue #1806](https://github.com/whosonfirst-data/whosonfirst-data/issues/1806))


## 2020 February

### AFGHANISTAN
- Remove 2 funk temporary files from repp. ([Issue #1800](https://github.com/whosonfirst-data/whosonfirst-data/issues/1800))

### INDIA
- Update Place Zerakpur. ([Pull request #37](https://github.com/whosonfirst-data/whosonfirst-data-admin-in/pull/37))

### NORWAY
- Update Norway regions and add new localadmin ("counties") to reflect 2020 boundary changes. ([Issue #1757](https://github.com/whosonfirst-data/whosonfirst-data/issues/1757))

### OMAN
- Add 2 missing country records. ([Issue #1773](https://github.com/whosonfirst-data/whosonfirst-data/issues/1773))

### SWITZERLAND
- Update Rothenburg. ([Pull request #9](https://github.com/whosonfirst-data/whosonfirst-data-admin-ch/pull/9))

### VARIOUS
- Generate licenses file from whosonfirst-sources. ([Issue #1081](https://github.com/whosonfirst-data/whosonfirst-data/issues/1081))
- Licensing information - link targets not available. ([Issue #1651](https://github.com/whosonfirst-data/whosonfirst-data/issues/1651))
- Add back LICENSE file as pointer. ([Issue #1795](https://github.com/whosonfirst-data/whosonfirst-data/issues/1795))


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
