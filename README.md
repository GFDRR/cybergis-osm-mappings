Nepal Earthquake Response OSM Mappings (cybergis-osm-mappings)
================

## Description

This repository contains OpenStreetmap (OSM) mappings for use by GeoGig.  See the "Using GeoGig with OpenStreetMap Data" page for more information at: [http://geogig.org/docs/interaction/osm.html](http://geogig.org/docs/interaction/osm.html).  The mappings folder includes the mappings in json format.  The mappings are broken out into namespaces/categories, mostly following ISO categories.  These are standardized mappings that should represent most basic OSM features, but also cover common mispellings and mistaggings.


This project was initially developed for use by the State Department Humanitarian Unit.  The repository you are looking at has been forked by GFDRR for use in supporting the response to the April 25 2015 Nepal Earthquake.

Please file any issues or support requests here: [https://github.com/GFDRR/cybergis-osm-mappings/issues](https://github.com/GFDRR/cybergis-osm-mappings/issues)

## Installation

These installation instructions are subject to change.  Right now, since there are no debian package dependencies, you can really extract the repo to whatever directory you want.  The instructions below are suggested as they mirror Linux best practices for external packages.

As root, execute the following commands:
```
cd /opt
git clone https://github.com/state-hiu/cybergis-osm-mappings.git cybergis-osm-mappings.git
```

The CyberGIS Scripts repo (cybergis-scripts) also contains some tools for automating the process of creating OpenStreetMap extracts.  See the installation guide at [https://github.com/state-hiu/cybergis-scripts](https://github.com/state-hiu/cybergis-scripts).

## Usage

Extents are currently limited to bounding boxes in the `S W N E` format to conform closely to the `osm download` command explained in the [Downloading data from an OSM Server](http://geogig.org/docs/interaction/osm.html#downloading-data-from-an-osm-serve) section of the GeoGig User Manual.  Complex geometry extents are possible but are not sufficiently integrated to work at scale.  You can do complex geometry extents, but it currently requires hand writing filters using the [Overpass Query Language](http://wiki.openstreetmap.org/wiki/Overpass_API/Language_Guide).

The easist mapping to start with is the `basic:buildings_and_roads` mapping available at [[link]](https://github.com/state-hiu/cybergis-osm-mappings/blob/master/mappings/basic/buildings_and_roads.json).

You can learn more about OSM mappings from the GeoGig User Manual at [http://geogig.org/docs/interaction/osm.html#data-mapping](http://geogig.org/docs/interaction/osm.html#data-mapping).

## License
This project constitutes a work of the United States Government and is not subject to domestic copyright protection under 17 USC § 105.

However, because the project utilizes code licensed from contributors and other third parties, it therefore is licensed under the MIT License. http://opensource.org/licenses/mit-license.php. Under that license, permission is granted free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the conditions that any appropriate copyright notices and this permission notice are included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
