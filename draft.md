# Mapping methods

## Process summary
The overall process follows these steps:
+ Convert vector to raster maps where the map has:
    * Value 1 where the feature is absent.
    * Where the feature is present it gets a value corresponding to the layers ranking in the following stacking (see below).
+ Stack the rasters in a sensible order (i.e. roads on top of fields etc.). This is determined by the value of layers, where higher values stack on top of lower ones.  


## Input data
Publicly available vector map layers from the FOT (insert proper name and ref) were used. In total 43 (- de to marklag og ais) different layers was used (see appendix 1 for details).
## Conversion
Each of the vector maps were initially converted to raster maps with a resolution of 1 m * 1 m.

## Making mosaic

## Final map
Landscape maps for ALMaSS are surface covering and have a resolution of 1 m * 1 m. 



## Tools
All handling and analysis of spatial data was done using ArcGIS and the python library *arcpy*. 