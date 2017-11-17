# ndviFromVRT

Since the calculation of the [NDVI (Normalized Difference Vegetation Index)](https://de.wikipedia.org/wiki/Normalized_Difference_Vegetation_Index) is a sometimes time consuming operation but still is needed for large datasets, it makes sense to implement it in a "lazy" way. 
This means, that it should be possible to directly load specific areas of an RGBIR image and be presented with a live display of the NDVI of the corresponding area.

By using the [**Derived Bands** function](http://www.gdal.org/gdal_vrttut.html) of GDAL's VRT files, it should be possible to achive exactly this result. The input files are specified as entries inside the VRT. The VRT file itself represents a valid GDAL input file format.

## VRT Files


## Derived Bands with functions


## NDVI as Derived Band
