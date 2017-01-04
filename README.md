# Elrond
Dstl Satellite Imagery Feature Detection

### Image Files
File Name | Available Format
--------- | ----------------
sixteen_band | [.zip (7.30 gb)] (https://www.kaggle.com/c/dstl-satellite-imagery-feature-detection/download/sixteen_band.zip)
three_band | [.zip (12.87 gb)] (https://www.kaggle.com/c/dstl-satellite-imagery-feature-detection/download/three_band.zip)

## Imagery Details
* Sensor : WorldView 3
* Wavebands :
  * Panchromatic: 450-800 nm
  * 8 Multispectral: (red, red edge, coastal, blue, green, yellow, near-IR1 and near-IR2) 400 nm - 1040 nm
  * 8 SWIR: 1195 nm - 2365 nm
* Sensor Resolution (GSD) at Nadir :
  * Panchromatic: 0.31m 
  * Multispectral: 1.24 m
  * SWIR: Delivered at 7.5m
* Dynamic Range
  * Panchromatic and multispectral : 11-bits per pixel
  * SWIR : 14-bits per pixel
  
## Object types

In a satellite image, you will find lots of different objects like roads, buildings, vehicles, farms, trees, water ways, etc. We have labeled 10 different classes in Dstl:

 1. Buildings - large building, residential, non-residential, fuel storage facility, fortified building
 2. Misc. Manmade structures 
 3. Road 
 4. Track - poor/dirt/cart track, footpath/trail
 5. Trees - woodland, hedgerows, groups of trees, standalone trees
 6. Crops - contour ploughing/cropland, grain (wheat) crops, row (potatoes, turnips) crops
 7. Waterway 
 8. Standing water
 9. Vehicle Large - large vehicle (e.g. lorry, truck,bus), logistics vehicle
 10. Vehicle Small - small vehicle (car, van), motorbike

Every object class is described in the form of Polygons and MultiPolygons, which are simply a list of polygons. There are two different formats for these shapes: GeoJson and WKT. These are both open source formats for geo-spatial shapes. 

The submission has to be in the WKT format. 

Geo Coordinates

In this provided dataset, we create a set of geo-coordinates that are in the range of x = [0,1] and y = [-1,0]. These coordinates are transformed such that we can obscure the location of where the satellite images are taken from. The images are from the same region on Earth.

To utilize these images, the grid coordinates are provided of each image so we know how to scale them and align them with the images in pixels. We need the Xmax and Ymin for each image to do the scaling (provided in our grid_sizes.csv) Please refer to this [tutorial](https://www.kaggle.com/c/dstl-satellite-imagery-feature-detection/details/data-processing-tutorial) on how to programmatically view the images.

