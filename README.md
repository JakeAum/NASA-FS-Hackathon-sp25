# NASA-FS-Hackathon-sp25
I &lt;3 NASA &amp; USDA

---
## Mission
Make forests accessible!

Given multi-modal data, find a way to identify hidden road networks within forests and add them to the map.

---
## Understanding the Multi-Modal Data

What does DEM mean?
- Digital Elevation Model, a rasterized representation of the elevation of the earth's surface from Lidar point clouds.

What is NAIP data?
- Aerial imagery collected by the National Agricultural Imagery Program 
- Products have with 4 channels: blue, green, red, and near-infrared (nir). 
- Exactly aligned with the lidar-derived dem's and can be stacked for analysis. 
- Visualization of RGB channels will show true color representation. 
- Visualization where the red band is replaced with nir, the green band is replaced with red, and the blue band is replaced with green will highlight areas with vegetation. 
- This file and its metadata can be read with Python packages like Rasterio, Rioxarray, and gdal among others.


What is the Hillshade transformation?
- The Hillshade transformation is a technique used in Geographic Information Systems (GIS) to visualize terrain as shaded relief, enhancing the three-dimensional appearance of the landscape by simulating the effects of light and shadow. Here's a detailed explanation of how it works:
- This is computed using the DEM for elevation then a "simulated sun": A virtual light source is set at a specific azimuth (direction) and altitude (angle above the horizon). Commonly, the light source is positioned at an azimuth of 315° (northwest) and an altitude of 45°.

What is GeoTIFF Metadata and coordinate system?

What are ESRI shapefiles and extensions?

 
## What are the interesting features of this problem?
- Ground Structures "Skid Roads" are hard to see under the dense forest canopy.
- Hillshade transformation is easy and commonly used but might not be the best for this problem.
  - "This method has the disadvantage, however, that certain ground structures cannot be seen, depending on the simulated position of the sun"
- I read a paper about the U-Net model architecture that seems to be more sensitive to these types of features.
    - https://www.waldwissen.net/en/technique-and-planning/forest-technology/forest-roads/using-lidar-to-look-for-skid-trails-in-the-forest
    - https://arxiv.org/pdf/1505.04597
    - https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/

    