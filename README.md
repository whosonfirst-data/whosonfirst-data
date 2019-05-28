# whosonfirst-data

## Disclaimer

As of May 2019, the whosonfirst-data repository has split into per-country repositories. You can read more about that change [here](https://whosonfirst.org/blog/2019/05/09/changes/). While we still track all issues in this repository, the data itself will live in the per-country repositories for the foreseeable future.

Per-country repositories have the following repository naming convention:

`whosonfirst-data-admin-{2-char country code}`

Meaning administrative data for Mexico, for example, would live in the following repository:

[whosonfirst-data-admin-mx](https://github.com/whosonfirst-data/whosonfirst-data-admin-mx)

At the [bottom of this README](https://github.com/whosonfirst-data/whosonfirst-data#whosonfirst-data/#repositories), you will find a full list of per-country repositories.

## whosonfirst-data

Who's On First is a gazetteer of places. Not quite _all_ the places in the world but a whole lot of them and, we hope, the kinds of places that we mostly share in common.

A gazetteer is a big list of places, each with a stable identifier and some number of descriptive properties about that location. An interesting way to think about a gazetteer is to consider it as the space where debate about a place is _managed_ but not decided. We call our gazetteer "Who's On First" (or sometimes "WOF" for short).

According to [Wikipedia](https://en.wikipedia.org/wiki/Who's_on_First%3F), Who’s on First:

```
...is a comedy routine made famous by Abbott and Costello. The premise of the
sketch is that Abbott is identifying the players on a baseball team for
Costello, but their names and nicknames can be interpreted as non-responsive
answers to Costello's questions. For example, the first baseman is named "Who";
thus, the utterance "Who's on first" is ambiguous between the question ("Which
person is the first baseman?") and the answer ("The name of the first baseman is
'Who'"). "Who's on First?" is descended from turn-of-the-century burlesque
sketches that used plays on words and names. Examples are "The Baker Scene" (the
shop is located on Watt Street) and "Who Dyed" (the owner is named Who). In the
1930 movie Cracked Nuts, comedians Bert Wheeler and Robert Woolsey examine a map
of a mythical kingdom with dialogue like this: "What is next to Which." "What is
the name of the town next to Which?" "Yes." In English music halls (Britain's
equivalent of vaudeville theatres), comedian Will Hay performed a routine in the
early 1930s (and possibly earlier) as a schoolmaster interviewing a schoolboy
named Howe who came from Ware but now lives in Wye.
```

Which sort of sums up the “problem” of geo, nicely. It might be easier, perhaps, if we all understood and [experienced the world as coordinate data](https://github.com/google/open-location-code) but we don’t, so the burden of “place” and its many meanings is one we trundle along with to this day.

Our gazetteer is absolutely not finished – both in terms of data coverage as well as data quality – so, in the near-term, you should adjust your expectations accordingly when you approach the data. We are releasing the data now because _we believe it is important not just to articulate our goals and intentions around the project but also to back them up with tangible proofs_.

Learn more about the Who’s On First data model over at [https://whosonfirst.org/docs/](https://whosonfirst.org/docs/).

## First Principles

The gazetteer starts from a series of first principles:

### Who's On First has an opinion

It is important that Who's On First have an opinion not about any one place but rather
about _the nature of place_ itself. It is important for us to know and
understand the boundaries of our project in order to know what the project is
for and, critically, what the project is not.

### Leave as many decisions as possible to the "edges"

The world is a complicated place and we would like the gazetteer to be a project
that can support, or act as a scaffolding for, the sometimes contradictory
opinions that people have about it. We aim to leave as much meaning or
inference, as we can, about a place to individual users and applications. How
this will manifest itself in concrete terms remains to be seen but this is a
goal we have set for ourselves.

### Portability

The canonical source for a place is a text file, specifically GeoJSON with a
unique 64-bit numeric ID. This is because all computers speak "text files" and
"numbers". Text files can be inspected or updated in any old text editor. Text
files can be printed. Numbers are fast and cheap for databases to index.

We use text files because our primary concern for the data is: Ease of use,
robustness and portability _over time_. On measure, the benefits of plain old
text files outweigh both the costs and in many cases the benefits of other
formats.

Google's [Protocol Buffers](https://developers.google.com/protocol-buffers/) for
example are awesome but require that you install a whole lot of Google on your
computer in order to use them. ESRI's
[Shapefiles](https://en.wikipedia.org/wiki/Shapefile) are equally awesome and
their ubiquity and longevity is a testament to their utility but they too
require bespoke applications for even the most trivial of updates.

That does not mean that plain text or static files are necessarily the optimal
choice for delivery or distribution. We will account for that on a case-by-case
basis. If we need to pre-process all the data into a smaller and nimbler format
for a specific use-case then we will, but you will always be able to access the
data as simple text files.

### GeoJSON

We use [GeoJSON](http://www.geojson.org) as the primary exchange format for the
gazetteer for two interconnected and complementary reasons:

* It is structured data with the least amount of markup _today_. If someone
creates another markup language with even less scaffolding we might use that
instead but for now GeoJSON is a good happy medium.

* There are lots of tools for working with GeoJSON and, importantly, for
converting it into all the other formats that different people use.

## Some Very Very (Very Very) Important Caveats

### Who’s On First is a work in progress

This means a few things:

1. Some (maybe even a lot) of the data will be wrong.

2. Some things are missing. Some things are missing in a [known unknown](https://github.com/TileStache/TileStache/blob/fb60b32439ebf108f983eaa4556627b07848d7ad/TileStache/Core.py#L772-L821) kind of way in which case they’ll be addressed shortly. Some things may still be missing in an [unknown unknown](https://en.wikipedia.org/wiki/There_are_known_knowns) kind of way in which case they’ll be addressed as the errors become apparent.

3. Some (probably most) of the data will change in some way, if only to account for #1.

4. We have not formalized or finalized the tools for updating all the ancestors or dependencies of a record when that record is updated. This means that in the short-term it is possible there will be inconsistencies between a record and its relations. We’ll get there.

The purpose of releasing the data now is not to sound the trumpets and
herald a new dawn of perfect data but rather to give substance to
everything we’ve been talking about and to have a meaningful dataset
with which to prove or disprove those assumptions and to work through
the practicalities of working with that data.

If you don’t have the time or the temperament (personally or
institutionally) to deal with a little bit of on-going [bad
craziness](http://www.ralphsteadmanprints.com/images/00art/gonzo/02badcrazy.jpg)
as we work through the issues diving in to the data now is probably
premature. We intend to continue working in public and discussing the
project openly so keep an eye on the blog and we’ll let you know as
things improve.

### Git and GitHub

Don’t get too attached to working with or managing Who’s On First data
in GitHub (or Git in general). We haven’t quite figured out what the
best way of both distributing the Who’s On First data and of accepting
corrections or suggestions from community.

Even though the nice people at GitHub continue to do excellent work at
making Git easier for a broader population to use, the reality remains
that Git is a significant barrier to participation for many
people. Absent a more formal decision about an alternative GitHub at
least allows us to point in the general direction of:

* An open and readily distributed dataset that people can download and
work with

* A way for people to contribute corrections (and general nuance)
about a place

* A way for us to be able to do everything above while still assuring
us a measure of authority around the assertions we make about the data  
* Also a way for us to think about how and where we store an audit
trail (of sorts) for updates to a place

#### Git and large files

We have started using [git-lfs](https://github.com/github/git-lfs) for managing large files. For example, the record for New Zealand which contains a _very very very very very_ detailed coastline is fast approaching the 100MB filesize limit for any individual file on GitHub.

You can see the current list of files being managed by invoking the `git lfs ls-files` command, like this:

```
$> cd /usr/local/mapzen/whosonfirst-data
$> git lfs ls-files
65ccc4825e * data/856/333/45/85633345.geojson
```

When you clone this repo the files (managed by git-lfs) only contain metadata, like this:

```
$> cat data/856/333/45/85633345.geojson
version https://git-lfs.github.com/spec/v1
oid sha256:65ccc4825e65c30f00fcebf1f3d57f4385f18a47e3c5e524114a67050186ae48
size 71879893
```

In order to fetch the file itself you will need to run `git lfs fetch` and then `git lfs checkout`. Because computers... but anyway, like this:

```
$> git lfs fetch
Fetching master
(1 of 1 files) 68.54 MB / 68.55 MB                                                                                               

$> cat data/856/333/45/85633345.geojson
version https://git-lfs.github.com/spec/v1
oid sha256:65ccc4825e65c30f00fcebf1f3d57f4385f18a47e3c5e524114a67050186ae48
size 71879893

$> git lfs checkout
(1 of 1 files) 68.55 MB / 68.55 MB                                                                                               

$> cat data/856/333/45/85633345.geojson
{
  "id": 85633345,
  "type": "Feature",
  "properties": {
    "edtf:cessation":"u",
    "edtf:inception":"u",
    "geom:area":29.187792061074827,
    "geom:bbox":"166.426148,-47.289992,178.577244,-33
```

Woosh! We're still working through the details on this so suggestions, tips and (gentle) cluebats are welcome.

## Theory (or "the even-longer version")

Where appropriate we have moved the theory (and sometimes history) around decisions for specific Who's On First properties in to dedicated GitHub repositories. They are:

### [whosonfirst-dates](https://github.com/whosonfirst/whosonfirst-dates)

### [whosonfirst-geometries](https://github.com/whosonfirst/whosonfirst-geometries)

### [whosonfirst-names](https://github.com/whosonfirst/whosonfirst-names)

### [whosonfirst-placetypes](https://github.com/whosonfirst/whosonfirst-placetypes)

### [whosonfirst-properties](https://github.com/whosonfirst/whosonfirst-properties)

### [whosonfirst-sources](https://github.com/whosonfirst/whosonfirst-sources)

### [whosonfirst-tests](https://github.com/whosonfirst/whosonfirst-tests)

### Blog posts and related musings

* [Who's On First](https://whosonfirst.org/blog/2015/08/18/who-s-on-first/) - 2015-08-18
* [Spelunker - Jumping into Who's On First](https://whosonfirst.org/blog/2015/09/28/spelunker-jumping-into-who-s-on-first/) - 2015-09-28
* [I Am Here](https://whosonfirst.org/blog/2016/02/19/iamhere/) - 2016-02-19
* [Yes No Fix](https://whosonfirst.org/blog/2016/04/08/yesnofix/) - 2016-04-08
* [Missing the Point - GeoIP's, Points, Polygons, and a Precarious Farm in Kansas](https://whosonfirst.org/blog/2016/04/14/missing-the-point/) - 2016-04-14
* [Updating Neighbourhood Records in Who's on First](https://whosonfirst.org/blog/2016/06/24/sf-neighbourhood-updates/) - 2016-06-24
* [Concordances with Wikipedia Data](https://whosonfirst.org/blog/2016/07/13/wikipedia-data/) - 2016-07-13
* [Mapping with Bias](https://whosonfirst.org/blog/2016/08/15/mapping-with-bias/) - 2016-08-15
* [All of the Places](https://whosonfirst.org/blog/2016/08/24/all-of-the-places/) - 2016-08-24
* [Boundary Issues: Editing Properties in Who's On First Records](https://whosonfirst.org/blog/2016/10/05/boundary-issues-properties/) - 2016-10-05
* [Who's On First Life Cycle Documentation](https://whosonfirst.org/blog/2016/10/06/wof-lifecycle-documentation/) - 2016-10-06
* [Venues, Postal Codes... and All Those GitHub Repositories](https://whosonfirst.org/blog/2016/10/07/whosonfirst-venues/) - 2016-10-07
* [Improving county coverage in Who's On First](https://whosonfirst.org/blog/2016/12/08/mesoshapes/) - 2016-12-08
* [Bundling up descendants into GeoJSON](https://whosonfirst.org/blog/2017/02/10/bundler/) - 2017-02-10
* [The Who's On First API](https://whosonfirst.org/blog/2017/04/04/whosonfirst-api/) - 2017-04-04
* [The world is weird and wonderful!](https://whosonfirst.org/blog/2017/04/17/weird-and-wonderful/) - 2017-04-17
* [Updating Who's On First Neighbourhoods - Part II](https://whosonfirst.org/blog/2017/04/20/neighbourhood-updates-two/) - 2017-04-21
* [The Who's On First API Explorer](https://whosonfirst.org/blog/2017/04/28/whosonfirst-api-explorer/) - 2017-04-28
* [Simple is hard](https://whosonfirst.org/blog/2017/05/10/simple-is-hard/) - 2017-05-10
* [Tackling Space and Time in Who's On First](https://whosonfirst.org/blog/2017/06/29/tackling-space-and-time-in-whosonfirst/) - 2017-06-29
* [Redesigning and Rebuilding the Who's On First website](https://whosonfirst.org/blog/2017/07/28/wof-website-redesign/) - 2017-07-28
* [Geotagging WOF venues](https://whosonfirst.org/blog/2017/08/01/geotagging-wof-venues/) - 2017-08-01
* [Increasing Name Translations in Who's On First](https://whosonfirst.org/blog/2017/08/22/summer-2017-wof/) - 2017-08-22
* [Statoids, Mesoshapes, and Who's On First](https://whosonfirst.org/blog/2017/09/19/introducing-statoids/) - 2017-09-19
* [Mapzen Places is here! And there! And everywhere](https://whosonfirst.org/blog/2017/10/05/mapzen-places/) - 2017-09-19
* [maîtres chez nous](https://whosonfirst.org/blog/2017/10/17/whosonfirst-nacis-2017/) - 2017-10-17
* [Who’s On First ꞉fist-bump꞉ OpenStreetMap](https://whosonfirst.org/blog/2017/10/24/whosonfirst-sotmus-2017/) - 2017-10-24
* [Whos On First Updates, 2017](https://whosonfirst.org/blog/2017/12/14/updating-whosonfirst/) - 2017-12-14
* [WOF in a Box (part 1)](https://whosonfirst.org/blog/2017/12/21/wof-in-a-box/) - 2017-12-21
* [Updating Who’s On First Neighbourhoods - Part III](https://whosonfirst.org/blog/2017/12/22/neighbourhood-updates-three/) - 2017-12-22
* [WOF in a Box (part 2)](https://whosonfirst.org/blog/2017/12/29/wof-in-a-box-part2/) - 2017-12-29
* [Who’s On First, Chapter Two](https://whosonfirst.org/blog/2018/01/02/chapter-two/) - 2018-01-02
* [Privatezen](https://whosonfirst.org/blog/2018/02/02/privatezen/) - 2018-02-02
* [WOF in a Box (part 3)](https://whosonfirst.org/blog/2018/02/20/wof-in-a-box-part3/) - 2018-02-20
* [The Why of the How](https://whosonfirst.org/blog/2018/02/27/why-of-the-how/) - 2018-02-27
* [Three Steps Backwards, One Step Forwards; a Tale of Data Consistency and JSON Schema](https://whosonfirst.org/blog/2018/05/25/three-steps-backwards/) - 2018-05-25

_All of the blog posts can be found over here: [https://whosonfirst.org/blog/](https://whosonfirst.org/blog/)._

## Practice

### The spelunker

There is a read-only "spelunker" for viewing Who's On First online at:

https://spelunker.whosonfirst.org/

## Venues

For the time being Who's On First maintains separate repositories with venues and points-of-interest. The starting point for venue data is:

https://<span></span>github.com/whosonfirst-data/whosonfirst-data-venue-*

Note: The `*` should be replaced with country code (ex: `ca`) and/or country code and region code (ex: `us-ny`).

Repository examples:

- https://github.com/whosonfirst-data/whosonfirst-data-venue-us-ca
- https://github.com/whosonfirst-data/whosonfirst-data-venue-us-ny
- https://github.com/whosonfirst-data/whosonfirst-data-venue-ca


## License

Crediting Who's On First is recommended and linking back to this License is required.

```
Data from Who's On First. <a href="https://whosonfirst.org/docs/licenses/">License</a> and <a href="https://github.com/whosonfirst/whosonfirst-sources/blob/master/sources/README.md">Sources</a>.
```

The Who's On First dataset is both original work and a modification of existing open data. Some of those open data projects **do** require attribution. We have listed some sources below.

When we [source](https://github.com/whosonfirst/whosonfirst-sources/) other open data projects we make best effort to indicate them (e.g.: `'src:geom':naturalearth`) and we also include the original source's properties prefixed with the following names spaces:

* `gn` - [GeoNames](http://www.geonames.org) (CC-BY)
* `gp` - [GeoPlanet](https://developer.yahoo.com/geo/geoplanet/) Where on Earth, aka `woe` (CC-BY)
* `ne` - [Natural Earth](http://www.naturalearthdata.com) (Public Domain)
* `oa` - [OurAirports](http://ourairports.com/) (Public Domain)
* `qs` - [Quattroshapes](https://github.com/foursquare/quattroshapes/) (CC-BY)
* `zs` - [Zetashapes](http://zetashapes.com/) (CC-BY)

See an up-to-date list of sources [here](https://github.com/whosonfirst/whosonfirst-sources/blob/master/sources/README.md).

Please notify us if you believe that an open data project has not been properly noted.

Our original work is generally indicated with properties prefixed with `wof` or is not prefixed (like `name`).

Remember, some sources **require attribution**, some do not. Mapzen's original work, including the format and structure that allows Who's On First to operate, is made available under the [Creative Commons Zero](https://creativecommons.org/publicdomain/zero/1.0/) designation, and a shout out would be lovely.

Read the full [License](https://github.com/whosonfirst/whosonfirst-data/blob/master/LICENSE.md#sources) file for more details per data source.

## Caveats and "known knowns"

We've add a separate document called [README.KNOWN.KNOWNS.md](README.KNOWN.KNOWNS.md) that lists the current state of known knowns and other gotchas you might encounter working with the Who's On First data.

## See also:

* https://whosonfirst.org/
* https://whosonfirst.org/download/

## Repositories

* [whosonfirst-data-admin-ad](https://github.com/whosonfirst-data/whosonfirst-data-admin-ad) - Andorra
* [whosonfirst-data-admin-ae](https://github.com/whosonfirst-data/whosonfirst-data-admin-ae) - United Arab Emirates
* [whosonfirst-data-admin-af](https://github.com/whosonfirst-data/whosonfirst-data-admin-af) - Afghanistan
* [whosonfirst-data-admin-ag](https://github.com/whosonfirst-data/whosonfirst-data-admin-ag) - Antigua and Barbuda
* [whosonfirst-data-admin-ai](https://github.com/whosonfirst-data/whosonfirst-data-admin-ai) - Anguilla
* [whosonfirst-data-admin-al](https://github.com/whosonfirst-data/whosonfirst-data-admin-al) - Albania
* [whosonfirst-data-admin-am](https://github.com/whosonfirst-data/whosonfirst-data-admin-am) - Armenia
* [whosonfirst-data-admin-ao](https://github.com/whosonfirst-data/whosonfirst-data-admin-ao) - Angola
* [whosonfirst-data-admin-aq](https://github.com/whosonfirst-data/whosonfirst-data-admin-aq) - Antarctica
* [whosonfirst-data-admin-ar](https://github.com/whosonfirst-data/whosonfirst-data-admin-ar) - Argentina
* [whosonfirst-data-admin-as](https://github.com/whosonfirst-data/whosonfirst-data-admin-as) - American Samoa
* [whosonfirst-data-admin-at](https://github.com/whosonfirst-data/whosonfirst-data-admin-at) - Austria
* [whosonfirst-data-admin-au](https://github.com/whosonfirst-data/whosonfirst-data-admin-au) - Australia
* [whosonfirst-data-admin-aw](https://github.com/whosonfirst-data/whosonfirst-data-admin-aw) - Aruba
* [whosonfirst-data-admin-ax](https://github.com/whosonfirst-data/whosonfirst-data-admin-ax) - Åland Islands
* [whosonfirst-data-admin-az](https://github.com/whosonfirst-data/whosonfirst-data-admin-az) - Azerbaijan
* [whosonfirst-data-admin-ba](https://github.com/whosonfirst-data/whosonfirst-data-admin-ba) - Bosnia and Herzegovina
* [whosonfirst-data-admin-bb](https://github.com/whosonfirst-data/whosonfirst-data-admin-bb) - Barbados
* [whosonfirst-data-admin-bd](https://github.com/whosonfirst-data/whosonfirst-data-admin-bd) - Bangladesh
* [whosonfirst-data-admin-be](https://github.com/whosonfirst-data/whosonfirst-data-admin-be) - Belgium
* [whosonfirst-data-admin-bf](https://github.com/whosonfirst-data/whosonfirst-data-admin-bf) - Burkina Faso
* [whosonfirst-data-admin-bg](https://github.com/whosonfirst-data/whosonfirst-data-admin-bg) - Bulgaria
* [whosonfirst-data-admin-bh](https://github.com/whosonfirst-data/whosonfirst-data-admin-bh) - Bahrain
* [whosonfirst-data-admin-bi](https://github.com/whosonfirst-data/whosonfirst-data-admin-bi) - Burundi
* [whosonfirst-data-admin-bj](https://github.com/whosonfirst-data/whosonfirst-data-admin-bj) - Benin
* [whosonfirst-data-admin-bl](https://github.com/whosonfirst-data/whosonfirst-data-admin-bl) - Saint Barthélemy
* [whosonfirst-data-admin-bm](https://github.com/whosonfirst-data/whosonfirst-data-admin-bm) - Bermuda
* [whosonfirst-data-admin-bn](https://github.com/whosonfirst-data/whosonfirst-data-admin-bn) - Brunei
* [whosonfirst-data-admin-bo](https://github.com/whosonfirst-data/whosonfirst-data-admin-bo) - Bolivia
* [whosonfirst-data-admin-bq](https://github.com/whosonfirst-data/whosonfirst-data-admin-bq) - Bonaire
* [whosonfirst-data-admin-br](https://github.com/whosonfirst-data/whosonfirst-data-admin-br) - Brazil
* [whosonfirst-data-admin-bs](https://github.com/whosonfirst-data/whosonfirst-data-admin-bs) - Bahamas
* [whosonfirst-data-admin-bt](https://github.com/whosonfirst-data/whosonfirst-data-admin-bt) - Bhutan
* [whosonfirst-data-admin-bw](https://github.com/whosonfirst-data/whosonfirst-data-admin-bw) - Botswana
* [whosonfirst-data-admin-by](https://github.com/whosonfirst-data/whosonfirst-data-admin-by) - Belarus
* [whosonfirst-data-admin-bz](https://github.com/whosonfirst-data/whosonfirst-data-admin-bz) - Belize
* [whosonfirst-data-admin-ca](https://github.com/whosonfirst-data/whosonfirst-data-admin-ca) - Canada
* [whosonfirst-data-admin-cc](https://github.com/whosonfirst-data/whosonfirst-data-admin-cc) - Cocos (Keeling) Islands
* [whosonfirst-data-admin-cd](https://github.com/whosonfirst-data/whosonfirst-data-admin-cd) - Democratic Republic of the Congo
* [whosonfirst-data-admin-cf](https://github.com/whosonfirst-data/whosonfirst-data-admin-cf) - Central African Republic
* [whosonfirst-data-admin-cg](https://github.com/whosonfirst-data/whosonfirst-data-admin-cg) - Congo
* [whosonfirst-data-admin-ch](https://github.com/whosonfirst-data/whosonfirst-data-admin-ch) - Switzerland
* [whosonfirst-data-admin-ci](https://github.com/whosonfirst-data/whosonfirst-data-admin-ci) - Ivory Coast
* [whosonfirst-data-admin-ck](https://github.com/whosonfirst-data/whosonfirst-data-admin-ck) - Cook Islands
* [whosonfirst-data-admin-cl](https://github.com/whosonfirst-data/whosonfirst-data-admin-cl) - Chile
* [whosonfirst-data-admin-cm](https://github.com/whosonfirst-data/whosonfirst-data-admin-cm) - Cameroon
* [whosonfirst-data-admin-cn](https://github.com/whosonfirst-data/whosonfirst-data-admin-cn) - China
* [whosonfirst-data-admin-co](https://github.com/whosonfirst-data/whosonfirst-data-admin-co) - Colombia
* [whosonfirst-data-admin-cr](https://github.com/whosonfirst-data/whosonfirst-data-admin-cr) - Costa Rica
* [whosonfirst-data-admin-cu](https://github.com/whosonfirst-data/whosonfirst-data-admin-cu) - Cuba
* [whosonfirst-data-admin-cv](https://github.com/whosonfirst-data/whosonfirst-data-admin-cv) - Cabo Verde
* [whosonfirst-data-admin-cw](https://github.com/whosonfirst-data/whosonfirst-data-admin-cw) - Curaçao
* [whosonfirst-data-admin-cx](https://github.com/whosonfirst-data/whosonfirst-data-admin-cx) - Christmas Island
* [whosonfirst-data-admin-cy](https://github.com/whosonfirst-data/whosonfirst-data-admin-cy) - Cyprus
* [whosonfirst-data-admin-cz](https://github.com/whosonfirst-data/whosonfirst-data-admin-cz) - Czechia
* [whosonfirst-data-admin-de](https://github.com/whosonfirst-data/whosonfirst-data-admin-de) - Germany
* [whosonfirst-data-admin-dj](https://github.com/whosonfirst-data/whosonfirst-data-admin-dj) - Djibouti
* [whosonfirst-data-admin-dk](https://github.com/whosonfirst-data/whosonfirst-data-admin-dk) - Denmark
* [whosonfirst-data-admin-dm](https://github.com/whosonfirst-data/whosonfirst-data-admin-dm) - Dominica
* [whosonfirst-data-admin-do](https://github.com/whosonfirst-data/whosonfirst-data-admin-do) - Dominican Republic
* [whosonfirst-data-admin-dz](https://github.com/whosonfirst-data/whosonfirst-data-admin-dz) - Algeria
* [whosonfirst-data-admin-ec](https://github.com/whosonfirst-data/whosonfirst-data-admin-ec) - Ecuador
* [whosonfirst-data-admin-ee](https://github.com/whosonfirst-data/whosonfirst-data-admin-ee) - Estonia
* [whosonfirst-data-admin-eg](https://github.com/whosonfirst-data/whosonfirst-data-admin-eg) - Egypt
* [whosonfirst-data-admin-eh](https://github.com/whosonfirst-data/whosonfirst-data-admin-eh) - Western Sahara
* [whosonfirst-data-admin-er](https://github.com/whosonfirst-data/whosonfirst-data-admin-er) - Eritrea
* [whosonfirst-data-admin-es](https://github.com/whosonfirst-data/whosonfirst-data-admin-es) - Spain
* [whosonfirst-data-admin-et](https://github.com/whosonfirst-data/whosonfirst-data-admin-et) - Ethiopia
* [whosonfirst-data-admin-fi](https://github.com/whosonfirst-data/whosonfirst-data-admin-fi) - Finland
* [whosonfirst-data-admin-fj](https://github.com/whosonfirst-data/whosonfirst-data-admin-fj) - Fiji
* [whosonfirst-data-admin-fk](https://github.com/whosonfirst-data/whosonfirst-data-admin-fk) - Falkland Islands
* [whosonfirst-data-admin-fm](https://github.com/whosonfirst-data/whosonfirst-data-admin-fm) - Federated States of Micronesia
* [whosonfirst-data-admin-fo](https://github.com/whosonfirst-data/whosonfirst-data-admin-fo) - Faroe Islands
* [whosonfirst-data-admin-fr](https://github.com/whosonfirst-data/whosonfirst-data-admin-fr) - France
* [whosonfirst-data-admin-ga](https://github.com/whosonfirst-data/whosonfirst-data-admin-ga) - Gabon
* [whosonfirst-data-admin-gb](https://github.com/whosonfirst-data/whosonfirst-data-admin-gb) - United Kingdom
* [whosonfirst-data-admin-gd](https://github.com/whosonfirst-data/whosonfirst-data-admin-gd) - Grenada
* [whosonfirst-data-admin-ge](https://github.com/whosonfirst-data/whosonfirst-data-admin-ge) - Georgia
* [whosonfirst-data-admin-gf](https://github.com/whosonfirst-data/whosonfirst-data-admin-gf) - French Guiana
* [whosonfirst-data-admin-gg](https://github.com/whosonfirst-data/whosonfirst-data-admin-gg) - Guernsey
* [whosonfirst-data-admin-gh](https://github.com/whosonfirst-data/whosonfirst-data-admin-gh) - Ghana
* [whosonfirst-data-admin-gi](https://github.com/whosonfirst-data/whosonfirst-data-admin-gi) - Gibraltar
* [whosonfirst-data-admin-gl](https://github.com/whosonfirst-data/whosonfirst-data-admin-gl) - Greenland
* [whosonfirst-data-admin-gm](https://github.com/whosonfirst-data/whosonfirst-data-admin-gm) - Gambia
* [whosonfirst-data-admin-gn](https://github.com/whosonfirst-data/whosonfirst-data-admin-gn) - Guinea
* [whosonfirst-data-admin-gp](https://github.com/whosonfirst-data/whosonfirst-data-admin-gp) - Guadeloupe
* [whosonfirst-data-admin-gq](https://github.com/whosonfirst-data/whosonfirst-data-admin-gq) - Equatorial Guinea
* [whosonfirst-data-admin-gr](https://github.com/whosonfirst-data/whosonfirst-data-admin-gr) - Greece
* [whosonfirst-data-admin-gs](https://github.com/whosonfirst-data/whosonfirst-data-admin-gs) - South Georgia and the South Sandwich Islands
* [whosonfirst-data-admin-gt](https://github.com/whosonfirst-data/whosonfirst-data-admin-gt) - Guatemala
* [whosonfirst-data-admin-gu](https://github.com/whosonfirst-data/whosonfirst-data-admin-gu) - Guam
* [whosonfirst-data-admin-gw](https://github.com/whosonfirst-data/whosonfirst-data-admin-gw) - Guinea-Bissau
* [whosonfirst-data-admin-gy](https://github.com/whosonfirst-data/whosonfirst-data-admin-gy) - Guyana
* [whosonfirst-data-admin-hk](https://github.com/whosonfirst-data/whosonfirst-data-admin-hk) - Hong Kong
* [whosonfirst-data-admin-hm](https://github.com/whosonfirst-data/whosonfirst-data-admin-hm) - Heard Island and McDonald Islands
* [whosonfirst-data-admin-hn](https://github.com/whosonfirst-data/whosonfirst-data-admin-hn) - Honduras
* [whosonfirst-data-admin-hr](https://github.com/whosonfirst-data/whosonfirst-data-admin-hr) - Croatia
* [whosonfirst-data-admin-ht](https://github.com/whosonfirst-data/whosonfirst-data-admin-ht) - Haiti
* [whosonfirst-data-admin-hu](https://github.com/whosonfirst-data/whosonfirst-data-admin-hu) - Hungary
* [whosonfirst-data-admin-id](https://github.com/whosonfirst-data/whosonfirst-data-admin-id) - Indonesia
* [whosonfirst-data-admin-ie](https://github.com/whosonfirst-data/whosonfirst-data-admin-ie) - Ireland
* [whosonfirst-data-admin-il](https://github.com/whosonfirst-data/whosonfirst-data-admin-il) - Israel
* [whosonfirst-data-admin-im](https://github.com/whosonfirst-data/whosonfirst-data-admin-im) - Isle of Man
* [whosonfirst-data-admin-in](https://github.com/whosonfirst-data/whosonfirst-data-admin-in) - India
* [whosonfirst-data-admin-io](https://github.com/whosonfirst-data/whosonfirst-data-admin-io) - British Indian Ocean Territory
* [whosonfirst-data-admin-iq](https://github.com/whosonfirst-data/whosonfirst-data-admin-iq) - Iraq
* [whosonfirst-data-admin-ir](https://github.com/whosonfirst-data/whosonfirst-data-admin-ir) - Iran
* [whosonfirst-data-admin-is](https://github.com/whosonfirst-data/whosonfirst-data-admin-is) - Iceland
* [whosonfirst-data-admin-it](https://github.com/whosonfirst-data/whosonfirst-data-admin-it) - Italy
* [whosonfirst-data-admin-je](https://github.com/whosonfirst-data/whosonfirst-data-admin-je) - Jersey
* [whosonfirst-data-admin-jm](https://github.com/whosonfirst-data/whosonfirst-data-admin-jm) - Jamaica
* [whosonfirst-data-admin-jo](https://github.com/whosonfirst-data/whosonfirst-data-admin-jo) - Jordan
* [whosonfirst-data-admin-jp](https://github.com/whosonfirst-data/whosonfirst-data-admin-jp) - Japan
* [whosonfirst-data-admin-ke](https://github.com/whosonfirst-data/whosonfirst-data-admin-ke) - Kenya
* [whosonfirst-data-admin-kg](https://github.com/whosonfirst-data/whosonfirst-data-admin-kg) - Kyrgyzstan
* [whosonfirst-data-admin-kh](https://github.com/whosonfirst-data/whosonfirst-data-admin-kh) - Cambodia
* [whosonfirst-data-admin-ki](https://github.com/whosonfirst-data/whosonfirst-data-admin-ki) - Kiribati
* [whosonfirst-data-admin-km](https://github.com/whosonfirst-data/whosonfirst-data-admin-km) - Comoros
* [whosonfirst-data-admin-kn](https://github.com/whosonfirst-data/whosonfirst-data-admin-kn) - Saint Kitts and Nevis
* [whosonfirst-data-admin-kp](https://github.com/whosonfirst-data/whosonfirst-data-admin-kp) - North Korea
* [whosonfirst-data-admin-kr](https://github.com/whosonfirst-data/whosonfirst-data-admin-kr) - South Korea
* [whosonfirst-data-admin-kw](https://github.com/whosonfirst-data/whosonfirst-data-admin-kw) - Kuwait
* [whosonfirst-data-admin-ky](https://github.com/whosonfirst-data/whosonfirst-data-admin-ky) - Cayman Islands
* [whosonfirst-data-admin-kz](https://github.com/whosonfirst-data/whosonfirst-data-admin-kz) - Kazakhstan
* [whosonfirst-data-admin-la](https://github.com/whosonfirst-data/whosonfirst-data-admin-la) - Laos
* [whosonfirst-data-admin-lb](https://github.com/whosonfirst-data/whosonfirst-data-admin-lb) - Lebanon
* [whosonfirst-data-admin-lc](https://github.com/whosonfirst-data/whosonfirst-data-admin-lc) - Saint Lucia
* [whosonfirst-data-admin-li](https://github.com/whosonfirst-data/whosonfirst-data-admin-li) - Liechtenstein
* [whosonfirst-data-admin-lk](https://github.com/whosonfirst-data/whosonfirst-data-admin-lk) - Sri Lanka
* [whosonfirst-data-admin-lr](https://github.com/whosonfirst-data/whosonfirst-data-admin-lr) - Liberia
* [whosonfirst-data-admin-ls](https://github.com/whosonfirst-data/whosonfirst-data-admin-ls) - Lesotho
* [whosonfirst-data-admin-lt](https://github.com/whosonfirst-data/whosonfirst-data-admin-lt) - Lithuania
* [whosonfirst-data-admin-lu](https://github.com/whosonfirst-data/whosonfirst-data-admin-lu) - Luxembourg
* [whosonfirst-data-admin-lv](https://github.com/whosonfirst-data/whosonfirst-data-admin-lv) - Latvia
* [whosonfirst-data-admin-ly](https://github.com/whosonfirst-data/whosonfirst-data-admin-ly) - Libya
* [whosonfirst-data-admin-ma](https://github.com/whosonfirst-data/whosonfirst-data-admin-ma) - Morocco
* [whosonfirst-data-admin-mc](https://github.com/whosonfirst-data/whosonfirst-data-admin-mc) - Monaco
* [whosonfirst-data-admin-md](https://github.com/whosonfirst-data/whosonfirst-data-admin-md) - Moldova
* [whosonfirst-data-admin-me](https://github.com/whosonfirst-data/whosonfirst-data-admin-me) - Montenegro
* [whosonfirst-data-admin-mf](https://github.com/whosonfirst-data/whosonfirst-data-admin-mf) - Saint Martin
* [whosonfirst-data-admin-mg](https://github.com/whosonfirst-data/whosonfirst-data-admin-mg) - Madagascar
* [whosonfirst-data-admin-mh](https://github.com/whosonfirst-data/whosonfirst-data-admin-mh) - Marshall Islands
* [whosonfirst-data-admin-mk](https://github.com/whosonfirst-data/whosonfirst-data-admin-mk) - North Macedonia
* [whosonfirst-data-admin-ml](https://github.com/whosonfirst-data/whosonfirst-data-admin-ml) - Mali
* [whosonfirst-data-admin-mm](https://github.com/whosonfirst-data/whosonfirst-data-admin-mm) - Myanmar
* [whosonfirst-data-admin-mn](https://github.com/whosonfirst-data/whosonfirst-data-admin-mn) - Mongolia
* [whosonfirst-data-admin-mo](https://github.com/whosonfirst-data/whosonfirst-data-admin-mo) - Macao
* [whosonfirst-data-admin-mp](https://github.com/whosonfirst-data/whosonfirst-data-admin-mp) - Northern Mariana Islands
* [whosonfirst-data-admin-mq](https://github.com/whosonfirst-data/whosonfirst-data-admin-mq) - Martinique
* [whosonfirst-data-admin-mr](https://github.com/whosonfirst-data/whosonfirst-data-admin-mr) - Mauritania
* [whosonfirst-data-admin-ms](https://github.com/whosonfirst-data/whosonfirst-data-admin-ms) - Montserrat
* [whosonfirst-data-admin-mt](https://github.com/whosonfirst-data/whosonfirst-data-admin-mt) - Malta
* [whosonfirst-data-admin-mu](https://github.com/whosonfirst-data/whosonfirst-data-admin-mu) - Mauritius
* [whosonfirst-data-admin-mv](https://github.com/whosonfirst-data/whosonfirst-data-admin-mv) - Maldives
* [whosonfirst-data-admin-mw](https://github.com/whosonfirst-data/whosonfirst-data-admin-mw) - Malawi
* [whosonfirst-data-admin-mx](https://github.com/whosonfirst-data/whosonfirst-data-admin-mx) - Mexico
* [whosonfirst-data-admin-my](https://github.com/whosonfirst-data/whosonfirst-data-admin-my) - Malaysia
* [whosonfirst-data-admin-mz](https://github.com/whosonfirst-data/whosonfirst-data-admin-mz) - Mozambique
* [whosonfirst-data-admin-na](https://github.com/whosonfirst-data/whosonfirst-data-admin-na) - Namibia
* [whosonfirst-data-admin-nc](https://github.com/whosonfirst-data/whosonfirst-data-admin-nc) - New Caledonia
* [whosonfirst-data-admin-ne](https://github.com/whosonfirst-data/whosonfirst-data-admin-ne) - Niger
* [whosonfirst-data-admin-nf](https://github.com/whosonfirst-data/whosonfirst-data-admin-nf) - Norfolk Island
* [whosonfirst-data-admin-ng](https://github.com/whosonfirst-data/whosonfirst-data-admin-ng) - Nigeria
* [whosonfirst-data-admin-ni](https://github.com/whosonfirst-data/whosonfirst-data-admin-ni) - Nicaragua
* [whosonfirst-data-admin-nl](https://github.com/whosonfirst-data/whosonfirst-data-admin-nl) - Netherlands
* [whosonfirst-data-admin-no](https://github.com/whosonfirst-data/whosonfirst-data-admin-no) - Norway
* [whosonfirst-data-admin-np](https://github.com/whosonfirst-data/whosonfirst-data-admin-np) - Nepal
* [whosonfirst-data-admin-nr](https://github.com/whosonfirst-data/whosonfirst-data-admin-nr) - Nauru
* [whosonfirst-data-admin-nu](https://github.com/whosonfirst-data/whosonfirst-data-admin-nu) - Niue
* [whosonfirst-data-admin-nz](https://github.com/whosonfirst-data/whosonfirst-data-admin-nz) - New Zealand
* [whosonfirst-data-admin-om](https://github.com/whosonfirst-data/whosonfirst-data-admin-om) - Oman
* [whosonfirst-data-admin-pa](https://github.com/whosonfirst-data/whosonfirst-data-admin-pa) - Panama
* [whosonfirst-data-admin-pe](https://github.com/whosonfirst-data/whosonfirst-data-admin-pe) - Peru
* [whosonfirst-data-admin-pf](https://github.com/whosonfirst-data/whosonfirst-data-admin-pf) - French Polynesia
* [whosonfirst-data-admin-pg](https://github.com/whosonfirst-data/whosonfirst-data-admin-pg) - Papua New Guinea
* [whosonfirst-data-admin-ph](https://github.com/whosonfirst-data/whosonfirst-data-admin-ph) - Philippines
* [whosonfirst-data-admin-pk](https://github.com/whosonfirst-data/whosonfirst-data-admin-pk) - Pakistan
* [whosonfirst-data-admin-pl](https://github.com/whosonfirst-data/whosonfirst-data-admin-pl) - Poland
* [whosonfirst-data-admin-pm](https://github.com/whosonfirst-data/whosonfirst-data-admin-pm) - Saint Pierre and Miquelon
* [whosonfirst-data-admin-pn](https://github.com/whosonfirst-data/whosonfirst-data-admin-pn) - Pitcairn
* [whosonfirst-data-admin-pr](https://github.com/whosonfirst-data/whosonfirst-data-admin-pr) - Puerto Rico
* [whosonfirst-data-admin-ps](https://github.com/whosonfirst-data/whosonfirst-data-admin-ps) - Palestine
* [whosonfirst-data-admin-pt](https://github.com/whosonfirst-data/whosonfirst-data-admin-pt) - Portugal
* [whosonfirst-data-admin-pw](https://github.com/whosonfirst-data/whosonfirst-data-admin-pw) - Palau
* [whosonfirst-data-admin-py](https://github.com/whosonfirst-data/whosonfirst-data-admin-py) - Paraguay
* [whosonfirst-data-admin-qa](https://github.com/whosonfirst-data/whosonfirst-data-admin-qa) - Qatar
* [whosonfirst-data-admin-re](https://github.com/whosonfirst-data/whosonfirst-data-admin-re) - Réunion
* [whosonfirst-data-admin-ro](https://github.com/whosonfirst-data/whosonfirst-data-admin-ro) - Romania
* [whosonfirst-data-admin-rs](https://github.com/whosonfirst-data/whosonfirst-data-admin-rs) - Serbia
* [whosonfirst-data-admin-ru](https://github.com/whosonfirst-data/whosonfirst-data-admin-ru) - Russia
* [whosonfirst-data-admin-rw](https://github.com/whosonfirst-data/whosonfirst-data-admin-rw) - Rwanda
* [whosonfirst-data-admin-sa](https://github.com/whosonfirst-data/whosonfirst-data-admin-sa) - Saudi Arabia
* [whosonfirst-data-admin-sb](https://github.com/whosonfirst-data/whosonfirst-data-admin-sb) - Solomon Islands
* [whosonfirst-data-admin-sc](https://github.com/whosonfirst-data/whosonfirst-data-admin-sc) - Seychelles
* [whosonfirst-data-admin-sd](https://github.com/whosonfirst-data/whosonfirst-data-admin-sd) - Sudan
* [whosonfirst-data-admin-se](https://github.com/whosonfirst-data/whosonfirst-data-admin-se) - Sweden
* [whosonfirst-data-admin-sg](https://github.com/whosonfirst-data/whosonfirst-data-admin-sg) - Singapore
* [whosonfirst-data-admin-sh](https://github.com/whosonfirst-data/whosonfirst-data-admin-sh) - Saint Helena
* [whosonfirst-data-admin-si](https://github.com/whosonfirst-data/whosonfirst-data-admin-si) - Slovenia
* [whosonfirst-data-admin-sj](https://github.com/whosonfirst-data/whosonfirst-data-admin-sj) - Svalbard
* [whosonfirst-data-admin-sk](https://github.com/whosonfirst-data/whosonfirst-data-admin-sk) - Slovakia
* [whosonfirst-data-admin-sl](https://github.com/whosonfirst-data/whosonfirst-data-admin-sl) - Sierra Leone
* [whosonfirst-data-admin-sm](https://github.com/whosonfirst-data/whosonfirst-data-admin-sm) - San Marino
* [whosonfirst-data-admin-sn](https://github.com/whosonfirst-data/whosonfirst-data-admin-sn) - Senegal
* [whosonfirst-data-admin-so](https://github.com/whosonfirst-data/whosonfirst-data-admin-so) - Somalia
* [whosonfirst-data-admin-sr](https://github.com/whosonfirst-data/whosonfirst-data-admin-sr) - Suriname
* [whosonfirst-data-admin-ss](https://github.com/whosonfirst-data/whosonfirst-data-admin-ss) - South Sudan
* [whosonfirst-data-admin-st](https://github.com/whosonfirst-data/whosonfirst-data-admin-st) - Sao Tome and Principe
* [whosonfirst-data-admin-sv](https://github.com/whosonfirst-data/whosonfirst-data-admin-sv) - El Salvador
* [whosonfirst-data-admin-sx](https://github.com/whosonfirst-data/whosonfirst-data-admin-sx) - Sint Maarten
* [whosonfirst-data-admin-sy](https://github.com/whosonfirst-data/whosonfirst-data-admin-sy) - Syrian Arab Republic
* [whosonfirst-data-admin-sz](https://github.com/whosonfirst-data/whosonfirst-data-admin-sz) - Eswatini
* [whosonfirst-data-admin-tc](https://github.com/whosonfirst-data/whosonfirst-data-admin-tc) - Turks and Caicos Islands
* [whosonfirst-data-admin-td](https://github.com/whosonfirst-data/whosonfirst-data-admin-td) - Chad
* [whosonfirst-data-admin-tf](https://github.com/whosonfirst-data/whosonfirst-data-admin-tf) - French Southern Territories
* [whosonfirst-data-admin-tg](https://github.com/whosonfirst-data/whosonfirst-data-admin-tg) - Togo
* [whosonfirst-data-admin-th](https://github.com/whosonfirst-data/whosonfirst-data-admin-th) - Thailand
* [whosonfirst-data-admin-tj](https://github.com/whosonfirst-data/whosonfirst-data-admin-tj) - Tajikistan
* [whosonfirst-data-admin-tk](https://github.com/whosonfirst-data/whosonfirst-data-admin-tk) - Tokelau
* [whosonfirst-data-admin-tl](https://github.com/whosonfirst-data/whosonfirst-data-admin-tl) - Timor-Leste
* [whosonfirst-data-admin-tm](https://github.com/whosonfirst-data/whosonfirst-data-admin-tm) - Turkmenistan
* [whosonfirst-data-admin-tn](https://github.com/whosonfirst-data/whosonfirst-data-admin-tn) - Tunisia
* [whosonfirst-data-admin-to](https://github.com/whosonfirst-data/whosonfirst-data-admin-to) - Tonga
* [whosonfirst-data-admin-tr](https://github.com/whosonfirst-data/whosonfirst-data-admin-tr) - Turkey
* [whosonfirst-data-admin-tt](https://github.com/whosonfirst-data/whosonfirst-data-admin-tt) - Trinidad and Tobago
* [whosonfirst-data-admin-tv](https://github.com/whosonfirst-data/whosonfirst-data-admin-tv) - Tuvalu
* [whosonfirst-data-admin-tw](https://github.com/whosonfirst-data/whosonfirst-data-admin-tw) - Taiwan
* [whosonfirst-data-admin-tz](https://github.com/whosonfirst-data/whosonfirst-data-admin-tz) - Tanzania
* [whosonfirst-data-admin-ua](https://github.com/whosonfirst-data/whosonfirst-data-admin-ua) - Ukraine
* [whosonfirst-data-admin-ug](https://github.com/whosonfirst-data/whosonfirst-data-admin-ug) - Uganda
* [whosonfirst-data-admin-um](https://github.com/whosonfirst-data/whosonfirst-data-admin-um) - United States Minor Outlying Islands
* [whosonfirst-data-admin-un](https://github.com/whosonfirst-data/whosonfirst-data-admin-un) - United Nations
* [whosonfirst-data-admin-us](https://github.com/whosonfirst-data/whosonfirst-data-admin-us) - United States of America
* [whosonfirst-data-admin-uy](https://github.com/whosonfirst-data/whosonfirst-data-admin-uy) - Uruguay
* [whosonfirst-data-admin-uz](https://github.com/whosonfirst-data/whosonfirst-data-admin-uz) - Uzbekistan
* [whosonfirst-data-admin-va](https://github.com/whosonfirst-data/whosonfirst-data-admin-va) - Vatican City
* [whosonfirst-data-admin-vc](https://github.com/whosonfirst-data/whosonfirst-data-admin-vc) - Saint Vincent and the Grenadines
* [whosonfirst-data-admin-ve](https://github.com/whosonfirst-data/whosonfirst-data-admin-ve) - Venezuela
* [whosonfirst-data-admin-vg](https://github.com/whosonfirst-data/whosonfirst-data-admin-vg) - Virgin Islands (British)
* [whosonfirst-data-admin-vi](https://github.com/whosonfirst-data/whosonfirst-data-admin-vi) - Virgin Islands (U.S.)
* [whosonfirst-data-admin-vn](https://github.com/whosonfirst-data/whosonfirst-data-admin-vn) - Vietnam
* [whosonfirst-data-admin-vu](https://github.com/whosonfirst-data/whosonfirst-data-admin-vu) - Vanuatu
* [whosonfirst-data-admin-wf](https://github.com/whosonfirst-data/whosonfirst-data-admin-wf) - Wallis and Futuna
* [whosonfirst-data-admin-ws](https://github.com/whosonfirst-data/whosonfirst-data-admin-ws) - Samoa
* [whosonfirst-data-admin-xk](https://github.com/whosonfirst-data/whosonfirst-data-admin-xk) - Kosovo
* [whosonfirst-data-admin-xn](https://github.com/whosonfirst-data/whosonfirst-data-admin-xn) - Null Island
* [whosonfirst-data-admin-xs](https://github.com/whosonfirst-data/whosonfirst-data-admin-xs) - Somaliland
* [whosonfirst-data-admin-xx](https://github.com/whosonfirst-data/whosonfirst-data-admin-xx) - Placeholder for "unknown"
* [whosonfirst-data-admin-xy](https://github.com/whosonfirst-data/whosonfirst-data-admin-xy) - Placeholder for "unknown"
* [whosonfirst-data-admin-xz](https://github.com/whosonfirst-data/whosonfirst-data-admin-xz) - Placeholder for "unknown"
* [whosonfirst-data-admin-ye](https://github.com/whosonfirst-data/whosonfirst-data-admin-ye) - Yemen
* [whosonfirst-data-admin-yt](https://github.com/whosonfirst-data/whosonfirst-data-admin-yt) - Mayotte
* [whosonfirst-data-admin-za](https://github.com/whosonfirst-data/whosonfirst-data-admin-za) - South Africa
* [whosonfirst-data-admin-zm](https://github.com/whosonfirst-data/whosonfirst-data-admin-zm) - Zambia
* [whosonfirst-data-admin-zw](https://github.com/whosonfirst-data/whosonfirst-data-admin-zw) - Zimbabwe
