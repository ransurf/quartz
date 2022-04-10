---
aliases:
started: 2021-10-07
finished:
---
Status: #📥/🟩 
Tags: [[GEOG 150 Inputs]] #archivedCards/geog150

Links: [[' Classes]]
___

# ' GEOG 150 Week 5
Class:: GEOG150

## Notes

### [Exploring GIS: Georeferencing](https://www.youtube.com/watch?v=8QRlfV7UCRE&t=13s&ab_channel=GISVideosTV)
Mapping the earth refers to two aspects
?
- Georeferencing
	- Scientific principles, process of transforming spatial data
- Symbolizing the map
<!--SR:!2021-12-07,9,130-->

###### Categories of spatial referencing systems
?
- Census geography (postal codes, DA, EA)
- Location specified by a label or code
- Location types are hierarchically aranged
<!--SR:!2021-12-05,2,130-->

###### Geocoding (postal address, COGO)
?
- Linear reference system
- Location specific by reference to a segment of a linear geographic feature and distance from that segment to a point
- Turning physical address into geographical point
<!--SR:!2021-12-05,7,130-->

###### Latitude, Longitude, UTM
?
- Coordinate reference system
- Location specified with respect to a datum
- Allows GPS point measurements
<!--SR:!2021-12-05,7,130-->

###### Georeferencing
What is georeferencing
?
- the principles and processes of transforming spatial data from an arbritrary system into a geographic or projected system
<!--SR:!2021-12-07,9,130-->

- Georeferencing process
?
1. Define correct shape of earth
2. Make it flat
3. Add coordinates
4. Group objects into communities
<!--SR:!2021-12-07,4,130-->

###### Models of earth
**Globes**
?
- Highly accurate
- Difficult to move around, time consuming to make, convenient for small scales
<!--SR:!2022-01-02,35,270-->

**Ellipsoid**
?
- Ellipsoid is more accurate than a sphere, takes flattening of earth into consideration
	- Each country used a different elipsoid `4:01`
<!--SR:!2021-12-05,4,146-->

GEOID
?
- Accurate representation of earth's shape and size
- Based on equipotential gravity surfaces at mean sea level
- Rock densitites cause the geoid to deviate from the elipsoid
<!--SR:!2021-12-05,2,130-->

- Datum is;; an accurate arrangement of ground points
<!--SR:!2021-12-06,8,130-->
- Horizontal datum;; provides a frame of reference for measuring locations on surface of earth
<!--SR:!2021-12-14,11,150-->
- Vertical datum;; provides a frame of reference for measuring elevations with respect to the mean sea level
<!--SR:!2021-12-08,10,167-->
- Removing datum results in 7 years in prison lmao

###### Geographic coordinate systems composition
?
- Key lines
	- Meridian, equator
- Related to 3d earth shape
<!--SR:!2021-12-11,8,130-->

###### Projected Coordinate Systems
- Mapping involves
?
- Determining geographic locations of features on earth's curved surface, transforming locations into positions on a flat map
	- skinning the earth and laying it flat
<!--SR:!2021-12-10,12,162-->

- Earth projection can lead to distortion, but we can still preserve
?
- Angles (conformal/orthomorphic)
- Areas (equal-area or equivalent projections)
- Distances (equidistant projections)
- Directions (azimuthal and gnomonic projections)
<!--SR:!2021-12-04,6,130-->

- How to project earth
?
- Plane
	- Azimuthal projections
- Cylinder
	- Cylindrical projections
- Cone
	- Conic projections
- Each projection saves different properties
<!--SR:!2021-12-09,11,160-->

###### Universal Transverse Mercator (UTM) grid system
?
- world-wide system defined in meters
- Divided into
	- 60 zones, 6 degrees longitude each, 84 to 80
	- zone 1 is international date line
<!--SR:!2021-12-06,8,130-->

### [Spatial Data Representation](https://www.youtube.com/watch?v=lelnsbJ7VWo&ab_channel=GISVideosTV)
Real world to computer model
- Levels of conceptualization
?
1. Reality
2. Information model (Conceptual model)
	- (Objects/discrete features, fields/continuous features)
3. Representation of data model (Logical model)
4. Databases (Physical model)
5. File structures (Binary model)
<!--SR:!2021-12-05,2,130-->

###### Objects and fields
Objects
?
- Spatially referenced objects
- Boundaries defined
- Space is only occupied where objects exist
- Identified and described through attribute table
<!--SR:!2021-12-07,4,150-->

Field
?
- Vary across geographic space
- Fuzzy boundaries
- Exhaustive and exclusive
- Represented by category/value
<!--SR:!2021-12-05,7,130-->

###### Vector Data Model
?
- Points, vector lines, vector polygon
	- Names in spatial database
	- One geometry per layer
<!--SR:!2021-12-09,11,170-->

###### Specifying geometry for vector model (human world)
- Good for
?
- data with definite boundaries
- Network analysis capabilities
- Graphic output
- Used for census analysis, routing problems
- Branch of mathematics describing shape, size, and relative configurations of objects
<!--SR:!2021-12-07,4,150-->

- Topology focuses on properties of objects that don't change when distorted
?
- Expresses spatial relationships between connected or adjacent vector features in a GIS database
	- Missing, system, user-defined
	- [![Image from Gyazo](https://i.gyazo.com/914eb97b5c3441a3e5a504255c55dc02.png)](https://gyazo.com/914eb97b5c3441a3e5a504255c55dc02)
- Attribute table is linked to geometry
<!--SR:!2021-12-06,8,140-->

###### Raster data model (natural world)
- Good for
?
- Continuous data
- Good representation of spatial variability
- Good for data derived from remote sensing
- Forest change, landslide modeling
- Arranged in rows and column, each cell has a value
<!--SR:!2021-12-09,6,150-->

###### Choropleth map
?
- Used to show relative quantity by symbolizing area units such as countries, municipalities, using colour intensities
<!--SR:!2021-12-05,7,130-->

## Thoughts/Questions
-
___

# Backlinks
```dataview
list from [[' GEOG 150 Week 5]] and !outgoing([[' GEOG 150 Week 5]])
```
___

Created:: 2021-10-07 16:10
