# ndviFromVRT

Since the calculation of the [NDVI (Normalized Difference Vegetation Index)](https://de.wikipedia.org/wiki/Normalized_Difference_Vegetation_Index) is a sometimes time consuming operation but still is needed for large datasets, it makes sense to implement it in a "lazy" way. 
This means, that it should be possible to directly load specific areas of an RGBIR image and be presented with a live display of the NDVI of the corresponding area.

By using the [**Derived Bands** function](http://www.gdal.org/gdal_vrttut.html) of GDAL's VRT files, it should be possible to achive exactly this result. The input files are specified as entries inside the VRT. The VRT file itself represents a valid GDAL input file format.


## Environment Variables

For security reasons, the execution of python code from within a VRT is disabled. This functionality can be enabled by setting a config-environment variable:

	export GDAL_VRT_ENABLE_PYTHON=YES

## NDVI as Derived Band

	np.divide( np.subtract(in_ar[1],in_ar[0]) , np.sum(in_ar,axis = 0), dtype = 'Float32', out = out_ar )
