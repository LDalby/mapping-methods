# Mapping methods

## Process summary
The overall process follows these steps:
+ Convert vector to raster maps where the map has:
    * Value 1 where the feature is absent.
    * Where the feature is present, it gets a value corresponding to the layers ranking in the following stacking into thematic layers (see below).
+ Combine individual raster maps in theme maps (e.g., various road types, paths and railway tracks in a transportation theme). The stacking order of the individual layers within a theme is determined by the value in the raster where the feature was present.
+ Stack the themes in a reasonable order (i.e. roads on top of fields etc.). 




## Input data
We used publicly available vector map layers from the common public geographical administration data (FOT-data version 4.0, downloaded month year, insert URL). The FOT-data was used to map 41 different landscape features (see table X). The Danish AgriFish Agency (DAFA, under the Ministry of Food, Agriculture and Fisheries) provided vector maps of individual agricultural fields. Lastly, in the rare cases where an area was not covered by a field nor the FOT-data, we used the Area Information System data, which is a surface covering map with xxx different landcover types for Denmark.

### Special section about fields
The Danish AgriFish Agency ( under the Ministry of Food, Agriculture and Fisheries) maintains a map of all fields and a database of crops grown in Denmark. The database is updated annually. Farmers are obliged to report for each individual field the crop they intend to grow the following year. The data set used for this study stems from 2012 where more than 45.000 farmers contributed to the database. The data set makes it possible to identify the  owner (or manager) of each field and the actual crop grown on it.

## Conversion
Each of the vector maps were initially converted to raster maps with a resolution of 1 m * 1 m. 
Linear features are described as their centre line in the FOT-data. To get a meaningful raster representation of these features, a buffer was added when converting to raster. For example for large roads (width 10m) we added a 5m buffer around the centre line. Same procedure was followed for other linear features (e.g. streams and hedgerows). A similar procedure was followed for  point features such as wind turbines, tele masts and individual trees which are represented as their centre points in the FOT-data.

A line about how polygons were converted (in some cases a buffer was added, in others not...)


All input data  initially used the UTM zone 32/ETRS89 coordinate system.




#### The handling of the actual field polygons
+ How was it processed?


## Combining the layers
Map layers were organized into thematic layers before combining to the final map. E.g. all layers with roads, road verges, road side slopes, tracks, railroads etc. were combined in to a *road* theme. Same for built up areas, nature, wet nature, water and cultural areas. 

## Final map
Landscape maps for ALMaSS are surface covering and have a resolution of 1 m * 1 m. 

## Mapping Tools
All handling and analysis of spatial data was done using ArcGIS and the python library *arcpy*. 

The pyton script used to generate the maps used here is freely available on Github (url).

## Classification of farms



# Junk yard:

To avoid gaps between feature layers, a buffer was added around all linear features (#ld: hmm also the top one? Check up). In most cases this buffer will be covered by other layers. In the final map only XXX cells are buffers. 

A buffer was also added around point features such as wind mills, pylons and individual trees to get a meaningfull raster representation of these features (vector points have no area).

We added a buffer around features represented as lines in the FOT-data to  

For example roads are represented as their centre line - (NB - hvor ikke kun vejmidten, men også kanterne er digitaliserede, bruger vi dem. I de tilfælde er vejene jo reelt polygoner. Men det komplicerer jo, at det kan gøres på begge måder, så måske skal vi holde os til den simple, der jo under alle omstændigheder gælder for hele landet)
