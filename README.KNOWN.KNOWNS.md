# There are known knowns...

## Some records have no geometry or a centroid of 0,0

Which the exception of [Null Island](https://spelunker.whosonfirst.org/id/1/) these are records that need to be researched and updated. We use a default centroid of `0,0` to ensure as a way of tracking records that are still in need of editorial love and so that there is at least something to keep the more conversative GeoJSON parsers out there happy.

## Some polygon records contain 'buffered point' geometry

Some records represent point data as polygon data, such as: https://spelunker.whosonfirst.org/id/101873779, these records can be distinguished from actual geometries using the tag `qs:type="buffered point"`.

## See also

* https://en.wikipedia.org/wiki/There_are_known_knowns
