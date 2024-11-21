Q1: What is the URL of the WMS GetCapabilities request?

https://animated-fishstick-jjq7qx69w57g3p45r-8080.app.github.dev/geoserver/ows?service=WMS&version=1.3.0&request=GetCapabilities

Q2: What is the URL of the WFS GetCapabilities request?

https://animated-fishstick-jjq7qx69w57g3p45r-8080.app.github.dev/geoserver/ows?service=WFS&acceptversions=2.0.0&request=GetCapabilities

Q3: Submit a screenshot of your updated WFS Layer Preview

Tried this multiple times, probably 20+, with help from online research, discussion boards, emails to instructor, with no resolve. This is as far as this assignment would work in Geoserver.  Could not upload sld file in any way possible. Could not save or preview. The Publish feature will not work in Geoserver, it is a white/blank screen with nothing on it. I’ve tried all of these steps, repeating this assignment from the beginning on 3 different browsers, without Geoserver functioning the way it shows in this lab.

 see screenshot_exhibit_1.png

 See screenshot_exhibit_2.png


Q4: What does drawing order refer to? Which layer goes on `top`, the first or the last layer in the list?

Drawing order refers to the order that the layers are rendered. The last layer in the list will be on top.

Q5: Submit a screenshot of the Layer Preview of the Spearfish Layer Group when sf:sfdem is listed as the 3rd layer.

Here is a screen shot of my attempt to do this step. I was able to move sf:sdem down to be the third layer, but when I click save or save and then preview, I get a blank white screen.

see screenshot_exhibit_3.png

This is what I get with preview:

see screenshot_exhibit_4.png


Q6: What is the WMS url for the single-tiled request?

https://animated-fishstick-jjq7qx69w57g3p45r-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image/png&TRANSPARENT=true&STYLES=&LAYERS=spearfish&exceptions=application/vnd.ogc.se_inimage&SRS=EPSG:26713&WIDTH=1900&HEIGHT=1000&BBOX=590025.0021195225,4909551.640036173,626291.9460562146,4928639.505266011



Q7: What is the WMS url for one of the tiled requests? What is the image size?


https://animated-fishstick-jjq7qx69w57g3p45r-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image/png&TRANSPARENT=true&tiled=true&STYLES=&LAYERS=spearfish&exceptions=application/vnd.ogc.se_inimage&tilesOrigin=589425.9342365642,4913959.224611808&WIDTH=256&HEIGHT=256&SRS=EPSG:26713&BBOX=601038.7003571391,4901152.979335044,605925.1938559776,4906039.472833882

image size = 256 x 256


Q8: What is the URL of your coarse resolution sample of a WMTS url? What level does this tile refer to? Notice the differences. What are some of the fields that are unique to this url?

https://animated-fishstick-jjq7qx69w57g3p45r-8080.app.github.dev/geoserver/gwc/service/wmts?VERSION=1.0.0&LAYER=spearfish&STYLE=&TILEMATRIX=EPSG:4326:11&TILEMATRIXSET=EPSG:4326&SERVICE=WMTS&FORMAT=image/png&SERVICE=WMTS&REQUEST=GetFeatureInfo&INFOFORMAT=text/html&TileCol=950&TileRow=568&I=222&J=65

This link is unique because it refers to the tile column and row numbers.


Q9: In the zoomed-out URL, what are the TileCol and TileRow?

TileCol = 870 TileRow = 520


Q10: In the zoomed-in URL, what are the TileCol and TileRow?

TileCol = 3470 TileRow = 2075

Q11: Why are they so different for the same location in the map?

They’re different because the zoom in/out request of the map is different.


Q12: Is there a difference in the TileMatrix? %3A is an HTML encoding for a colon, `:`.What does the number after EPSG:4326 mean?

Yes, there’s a difference. EPSG:4326 refers to a coordinate reference system.
