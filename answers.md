### Q1: What is the URL of the WMS GetCapabilities request?
https://humble-fortnight-jvpgv979jp635rj4-8080.app.github.dev/geoserver/ows?service=WMS&version=1.3.0&request=GetCapabilities

### Q2: What is the URL of the WFS GetCapabilities request?
https://humble-fortnight-jvpgv979jp635rj4-8080.app.github.dev/geoserver/wcs?service=wfs&version=1.1.0&request=GetCapabilities

### Q3: Submit a screenshot of your updated WFS Layer Preview
WFSlayer.png and WFSlayer1.png added to repository. Triangles are not visible at default scale, but are as it zooms closer, as shown in the screencaps.

### Q4: What does drawing order refer to? Which layer goes on top, the first or the last layer in the list?
The drawing order refers to the order the layers are listed in the Layer Group or the Map Context. The last layer in the list is drawn on top.

### Q5: Submit a screenshot of the Layer Preview of the Spearfish Layer Group when sf:sfdem is listed as the 3rd layer.
SpearfishLayerGroup.png added to repository.

### Q6: What is the WMS url for the single-tiled request?
https://humble-fortnight-jvpgv979jp635rj4-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&tiled=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&tilesOrigin=589425.9342365642%2C4913959.224611808&WIDTH=500&HEIGHT=500&SRS=EPSG%3A26713&BBOX=594930.5834835917%2C4916423.271518914%2C595541.3951709465%2C4917034.083206269

### Q7: What is the WMS url for one of the tiled requests? What is the image size?
https://humble-fortnight-jvpgv979jp635rj4-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&tiled=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&tilesOrigin=589425.9342365642%2C4913959.224611808&WIDTH=256&HEIGHT=256&SRS=EPSG%3A26713&BBOX=593708.96010888%2C4920698.953330398%2C596152.2068582992%2C4923142.200079817

Image size: width 256, height 256

### Q8: What is the URL of your coarse resolution sample of a WMTS url? What level does this tile refer to? Notice the differences. What are some of the fields that are unique to this url?
https://humble-fortnight-jvpgv979jp635rj4-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A13&TileCol=3468&TileRow=2073

The TileMatrix parameter (EPSG:4326:13) indicates that the tile belongs to a set at zoom level 13.

The WMTS URL includes fields that define the tiling system (tilematrixset, TileMatrix, TileCol, TileRow) and is more tile-specific, while the WMS URL focuses on map rendering for a bounding box with defined dimensions.

### Q9: In the zoomed-out URL, what are the TileCol and TileRow?
https://humble-fortnight-jvpgv979jp635rj4-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A13&TileCol=3468&TileRow=2073

TileCol=3468, TileRow=2073

### Q10: In the zoomed-in URL, what are the TileCol and TileRow?
https://humble-fortnight-jvpgv979jp635rj4-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A16&TileCol=27749&TileRow=16592

TileCol=27749, TileRow=16592

### Q11: Why are they so different for the same location in the map?
At higher zoom levels, each tile represents a smaller geographic area, which means the number of tiles needed to cover the same extent grows exponentially.

### Q12: Is there a difference in the TileMatrix? %3A is an HTML encoding for a colon, :.What does the number after EPSG:4326 mean?
Yes, there is a difference between the two. In the first URL, the TileMatrix=EPSG:4326:13, while in the second URL the TileMatrix=EPSG:4326:16. The number after EPSG:4326 is the zoom level, 13 in the first URL and 16 in the second.