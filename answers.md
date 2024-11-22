Geoff Maas
GIST 604B – Lesson 6-0

Q1: What is the URL of the WMS GetCapabilities request?
https://friendly-space-chainsaw-4jwv5vg77wvpcq5wj-8080.app.github.dev/geoserver/ows?service=WMS&version=1.3.0&request=GetCapabilities

Q2: What is the URL of the WFS GetCapabilities request?
https://friendly-space-chainsaw-4jwv5vg77wvpcq5wj-8080.app.github.dev/geoserver/ows?service=WFS&acceptversions=2.0.0&request=GetCapabilities

Q3: Submit a screenshot of your updated WFS Layer Preview
Question3_Image.png 

Q4: What does drawing order refer to? Which layer goes on top, the first or the last layer in the list?
Drawing order refers to the order in which features are stacked in the display in the map view or interface.
First layers on top, last layers on the bottom.
Points generally go above the lines and polygons.
Lines generally go below points and above polygons.
Road lines go above river lines (except if they are a tunnel)

Q5: Submit a screenshot of the Layer Preview of the Spearfish Layer Group when sf:sfdem is listed as the 3rd layer.
I don’t understand the question, but have attached what I think is being asked for: Question5_Image.png 

Q6: What is the WMS url for the single-tiled request?
https://friendly-space-chainsaw-4jwv5vg77wvpcq5wj-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&SRS=EPSG%3A26713&WIDTH=768&HEIGHT=539&BBOX=592143.7551600345%2C4915879.267359864%2C606803.23565655%2C4926167.6267187465

Q7: What is the WMS url for one of the tiled requests?
https://friendly-space-chainsaw-4jwv5vg77wvpcq5wj-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A12&TileCol=1735&TileRow=1038

What is the image size?
42.6 kb

Q8: What is the URL of your coarse resolution sample of a WMTS url?
https://friendly-space-chainsaw-4jwv5vg77wvpcq5wj-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A12&TileCol=1735&TileRow=1037

What level does this tile refer to?
Size of tile based on zoom and view level.

What are some of the fields that are unique to this url?
I don’t understand the question or how to answer it.

Q9: In the zoomed-out URL, what are the TileCol and TileRow?
TileCol=1735, TileRow=1037

Q10: In the zoomed-in URL, what are the TileCol and TileRow?
Tile Col=-867, Tile Row=518

Q11: Why are they so different for the same location in the map?
They refer to different sizes and zoom level of the view.

Q12: Is there a difference in the TileMatrix?
Tile Matrix is 11 in zoomed in one

%3A is an HTML encoding for a colon, what does the number after EPSG:4326 mean?
The number of times you have divided up (sliced out) divisions of the globe.
