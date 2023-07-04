GeoTiff Sample
==============

This repository contains a sample GeoTiff file created from Copernicus
Sentinel-2A data for training purposes.

![Sample GeoTiff File.](sample.png)


Meta Data
---------

    import rasterio
    dataset = rasterio.open('sample.tif')

    dataset.meta
    {'driver': 'GTiff',
     'dtype': 'uint16',
     'nodata': None,
     'width': 1001,
     'height': 1001,
     'count': 3,
     'crs': CRS.from_epsg(32631),
     'transform': Affine(10.0, 0.0, 590520.0,
	    0.0, -10.0, 5790630.0)}

    dataset.bounds
    BoundingBox(left=590520.0, bottom=5780620.0, right=600530.0, top=5790630.0)


`sample.tif` contains only 3 out of 13 Sentinel-2 bands: Blue (band
1), Green (band 2), and Red (band 3).
