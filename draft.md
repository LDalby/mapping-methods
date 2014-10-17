# Mapping methods

## Process summary
The overall process follows these steps:
+ Convert vector to raster maps where the map has:
    * Value 1 where the feature is absent.
    * Where the feature is present it gets a value corresponding to the layers ranking in the following stacking (see below).
+ Stack the rasters in a sensible order (i.e. roads on top of fields etc.). This is determined by the value of layers, where higher values stack on top of lower ones.  


## Input data
Publicly available vector map layers from the FOT (insert proper name and ref) were used. In total XX different layers were used (see appendix 1 for details).

## Conversion
Each of the vector maps were initially converted to raster maps with a resolution of 1 m * 1 m. To avoid gaps between feature layers, a buffer was added around all linear features (#ld: hmm also the top one? Check up). In most cases this buffer will be covered by other layers. In the final map only XXX cells are buffers. 

### Special section about fields
#### The handling of the actual field polygons

#### Stuff about 

## Combining the layers
Map layers were organized into thematic layers before combining to the final map. E.g. all layers with roads, road verges, road side slopes, tracks, railroads etc. were combined in to a *road* theme. Same for built up areas, nature, wet nature, water and cultural areas. 

## Final map
Landscape maps for ALMaSS are surface covering and have a resolution of 1 m * 1 m. 

## Mapping Tools
All handling and analysis of spatial data was done using ArcGIS and the python library *arcpy*. 

## Classification of farms
