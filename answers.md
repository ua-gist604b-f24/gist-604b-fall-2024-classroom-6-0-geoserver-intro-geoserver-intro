Q1: What is the URL of the WMS GetCapabilities request?
https://bug-free-space-telegram-x55xw5595wgwcpwqv-8080.app.github.dev/geoserver/ows?service=WMS&version=1.3.0&request=GetCapabilities

Q2: What is the URL of the WFS GetCapabilities request?
https://bug-free-space-telegram-x55xw5595wgwcpwqv-8080.app.github.dev/geoserver/ows?service=WFS&acceptversions=2.0.0&request=GetCapabilities

Q3: Submit a screenshot of your updated WFS Layer Preview
See uploaded files

Q4: What does drawing order refer to? Which layer goes on top, the first or the last layer in the list?
Drawing order refers to the sequence in which layers are drawn on the map. The sequence determines how layers overlap, and which ones are visible in the case of overlapping and the last layer in the list is shown on top of other layers. Once the DEM layer was moved below streams and roads, the streams and roads were covered by the DEM raster layer, hiding them. If DEM is moved to the top of the list item (1 of 6) it will sit behind all vector layers and if it is moved to the last layer (6 of 6) it will sit on top of all other layers.

Q5: Submit a screenshot of the Layer Preview of the Spearfish Layer Group when sf:sfdem is listed as the 3rd layer.
see uploaded files

Q6: What is the WMS url for the single-tiled request?
https://bug-free-space-telegram-x55xw5595wgwcpwqv-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&SRS=EPSG%3A26713&WIDTH=768&HEIGHT=540&BBOX=595999.5039364618%2C4918744.833127493%2C599664.3740605906%2C4921316.922967214

Q7: What is the WMS url for one of the tiled requests? What is the image size?
each tile is 256x256 pixels and only shows the area requested (the tile) not the full image.

Q8: What is the URL of your coarse resolution sample of a WMTS url? What level does this tile refer to? Notice the differences. What are some of the fields that are unique to this url?
https://bug-free-space-telegram-x55xw5595wgwcpwqv-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A14&TileCol=6936&TileRow=4147
EPSG level 14 
TileCOl and TileRow are unique to this URL

Q9: In the zoomed-out URL, what are the TileCol and TileRow?
https://bug-free-space-telegram-x55xw5595wgwcpwqv-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A900913&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A900913%3A11&TileCol=436&TileRow=739
TileCol=436
TileRow=739

Q10: In the zoomed-in URL, what are the TileCol and TileRow?
https://bug-free-space-telegram-x55xw5595wgwcpwqv-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A900913&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A900913%3A18&TileCol=55516&TileRow=94875
TileCol=55516
TileRow=94875

Q11: Why are they so different for the same location in the map?
TileCol and TileRow values are different for the same location in the map because they depend on the zoom level

Q12: Is there a difference in the TileMatrix? %3A is an HTML encoding for a colon, :.What does the number after EPSG:4326 mean?
the zoom level