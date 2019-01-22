# unite-schema
unite-schema is a common vector tile schema that takes these 9 layers.

1. nature
2. water
3. boundary
4. road
5. railway
6. route
7. structure
8. building
9. place

# the idea behind this vector tile schema
## Vector tile layers are for separation of work.
Consider layers as labels to divide data into 9 butkets. Do not consider layers as classes in object-oriented feature models.
## Do not distinguish between Point, LineString and Polygon/MultiPolygon
You can distinguish geometry types in Mapbox Style.
## Have a small number of layers
We likely compress the size of style.json if we take data-driven style granted. A huge style.json likely makes the start of the web map slow.
## Have more possibilities for interoperability between datasets
We expect more possibility for interoerabilities of vector tiles from different datasources.
## Properties depends on respective datasets
There are diversity in properties rather than feature types. OpenStreetMap data model is a tag-based open one. Therefore the unite-schema will not have any constraint on properties. Amount of the properties will probably be decided by the vector tile size optimization criteria. 
