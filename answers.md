Q1: What is the URL of the WMS GetCapabilities request?
https://redesigned-giggle-7vpwp57x9xx7cv5-8080.app.github.dev/geoserver/ows?SERVICE=WMS&

Q2: What is the URL of the WFS GetCapabilities request?
https://redesigned-giggle-7vpwp57x9xx7cv5-8080.app.github.dev/geoserver/ows?service=WFS&acceptversions=2.0.0&request=GetCapabilities

Q3: Submit a screenshot of your updated WFS Layer Preview
(I can't edit GeoServer. I do not have permission)

Q4: What does drawing order refer to? Which layer goes on top, the first or the last layer in the list?
It is the order that the layers appear in the Layers section. The first layer goes on top. 

Q5: Submit a screenshot of the Layer Preview of the Spearfish Layer Group when sf:sfdem is listed as the 3rd layer
screenshot_spearfish_dem3_unsaved (I can't edit GeoServer. I do not have permission)

Q6: What is the WMS url for the single-tiled request?
https://redesigned-giggle-7vpwp57x9xx7cv5-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&SRS=EPSG%3A26713&WIDTH=1900&HEIGHT=1000&BBOX=593767.8143631879%2C4913132.205425384%2C611898.1050142997%2C4922672.956723069

Q7: What is the WMS url for one of the tiled requests? What is the image size?
https://redesigned-giggle-7vpwp57x9xx7cv5-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&tiled=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&tilesOrigin=589425.9342365642%2C4913959.224611808&WIDTH=256&HEIGHT=256&SRS=EPSG%3A26713&BBOX=613254.934104234%2C4908482.719583303%2C615698.1808536532%2C4910925.966332722

Q8: What is the URL of your coarse resolution sample of a WMTS url? What level does this tile refer to? Notice the differences. What are some of the fields that are unique to this url?
https://redesigned-giggle-7vpwp57x9xx7cv5-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A12&TileCol=1734&TileRow=1035
I have trouble discerning what is read in the url. But I think it's zoom level 12. I have noticed it is half the lenght of the Single tile and Tiled images. 

Q9: In the zoomed-out URL, what are the TileCol and TileRow?
https://redesigned-giggle-7vpwp57x9xx7cv5-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A12&TileCol=1737&TileRow=1035
TileCol:1737
TileRow:1035

Q10: In the zoomed-in URL, what are the TileCol and TileRow?
https://redesigned-giggle-7vpwp57x9xx7cv5-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A13&TileCol=3468&TileRow=2075
TileCol:3468
TileRow:2075

Q11: Why are they so different for the same location in the map?
If I understand correctly the tiles do not represent resolution, but rather locations within a matrix. 
There are different levels with different number of tiles per level. 

Q12: Is there a difference in the TileMatrix? %3A is an HTML encoding for a colon, :.What does the number after EPSG:4326 mean?
I think the difference in the TileMatrix is the number of tiles per level?
I think EPSG: 4326 is the CRS for the map.