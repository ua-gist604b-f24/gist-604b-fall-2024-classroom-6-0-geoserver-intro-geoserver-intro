#### Q1: What is the URL of the WMS GetCapabilities request?
https://orange-barnacle-q77wwjv7vvp43476q-8080.app.github.dev/geoserver/ows?service=WMS&version=1.3.0&request=GetCapabilities

#### Q2: What is the URL of the WFS GetCapabilities request?
https://orange-barnacle-q77wwjv7vvp43476q-8080.app.github.dev/geoserver/ows?service=WFS&acceptversions=2.0.0&request=GetCapabilities


#### Q3: Submit a screenshot of your updated WFS Layer Preview
Q3.png

#### Q4: What does drawing order refer to? Which layer goes on `top`, the first or the last layer in the list?
Drawing order refers to which layers are displayed above others. The layer on the 'top' of the list is shown as the bottom layer on the preview, and the layer at the bottom of the list is shown at the top of the layer. When the dem is moved to the third position, the streams and roads are no longer visible where there is the dem.

#### Q5: Submit a screenshot of the Layer Preview of the Spearfish Layer Group when sf:sfdem is listed as the 3rd layer.
Q5.png

#### Q6: What is the WMS url for the single-tiled request?
https://orange-barnacle-q77wwjv7vvp43476q-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&SRS=EPSG%3A26713&WIDTH=769&HEIGHT=539&BBOX=585882.9353646475%2C4912739.313529556%2C615201.8963576788%2C4933316.032247321

#### Q7: What is the WMS url for one of the tiled requests? What is the image size?
https://orange-barnacle-q77wwjv7vvp43476q-8080.app.github.dev/geoserver/wms?SERVICE=WMS&VERSION=1.1.1&REQUEST=GetMap&FORMAT=image%2Fpng&TRANSPARENT=true&tiled=true&STYLES&LAYERS=spearfish&exceptions=application%2Fvnd.ogc.se_inimage&tilesOrigin=589425.9342365642%2C4913959.224611808&WIDTH=256&HEIGHT=256&SRS=EPSG%3A26713&BBOX=605925.1938559785%2C4920698.953330398%2C608368.4406053978%2C4923142.200079817

14.9kb is the image size.


#### Q8: What is the URL of your coarse resolution sample of a WMTS url? What level does this tile refer to? Notice the differences. What are some of the fields that are unique to this url?
https://orange-barnacle-q77wwjv7vvp43476q-8080.app.github.dev/geoserver/gwc/service/wmts?layer=spearfish&style=&tilematrixset=EPSG%3A4326&Service=WMTS&Request=GetTile&Version=1.0.0&Format=image%2Fpng&TileMatrix=EPSG%3A4326%3A11&TileCol=867&TileRow=518

Some fields that are unique to this is the tilematrixset which defines the grid, and the TileCol and TileRow which show tile coordinates

#### Q9: In the zoomed-out URL, what are the TileCol and TileRow?
In the zoomed-outURL, the TileCol and TileRow are much smaller numbers (258, 434)

#### Q10: In the zoomed-in URL, what are the TileCol and TileRow?
In the zoomed in URL they are much larger numbers (888671, 530911)

#### Q11: Why are they so different for the same location in the map?
Because they are showing much different levels and more or less information the zoomed out url has to stor info for the where the tiles are for the whole image.


#### Q12: Is there a difference in the TileMatrix? %3A is an HTML encoding for a colon, `:`.What does the number after EPSG:4326 mean?
Both have 4326 as the tile matrix which defines the matrix/coordinate system which is WGS 84.
