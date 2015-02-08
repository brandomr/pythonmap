# pythonmap
## A guide to creating filled maps (or chloropleths) with Python
<img src='pymap3.png'>

First, big thanks to Stephan Hügel for his excellent [guide to mapping with Python](http://sensitivecities.com/so-youd-like-to-make-a-map-using-python-EN.html#.VNZHhVXF8kR). 
To create this guide, I heavily borrowed from Stephan's work, but tried to provide more 
contextualizing comment to ensure that a less advanced user can create their own filled map.

For this guide, I focus on creating a filled map of Sri Lanka. I use some basic demographic data plus a shapefile that includes the first level of administration (for example, in the United States this is a state) to demonstrate how to create and manipulate a filled map with Python.

The shapefile I obtained is from the [Spatial Data Repository](http://spatialdata.dhsprogram.com/boundaries/#countryId=LK&view=map&surveyId=19&level=1) 
where you can find detailed shapefiles for most countries. 

## Requirements
* pandas
* numpy
* matplotlib
* mpl_toolkits.basemap (Basemap)
* shapely
* pysal
* descartes
* fiona
* itertools

Up front, you are going to need to install some packages you might not have used before. I had to install pysal, descartes, shapely, and Basemap. Install Basemap with:

    pip install basemap --allow-external basemap --allow-unverified basemap