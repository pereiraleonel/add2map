# What is add2map?
add2map is a code sample to use [Folium](https://github.com/python-visualization/folium) geolocation capabilities without running python.
# How does it work?
- download the add2map.html file
- open in the browser
- enter coordinates to add a pointer on the map.
# Who uses it?
Those who wants to add geolocation capabilities to their project.
# What is it goals?
Facilitate the use of Folium geolocation.
# Screenshot
<table>
  <tr>
    <td>
      <img alt="homepage" src="docs/add2map.jpg">
    </td>
  </tr>
</table>

## main code
### head
    <script src="https://cdn.jsdelivr.net/npm/leaflet@1.2.0/dist/leaflet.js"></script>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/leaflet@1.2.0/dist/leaflet.css" />
    ...
    <style>
        #map {
            position : relative;
            width : 100.0%;
            height: 100.0%;
            left: 0.0%;
            top: 0.0%;
        }
    </style>
### body
    <form id="latLonForm" name="latLonForm">
        <input type="text" id="lat" name="lat" placeholder="Latitude e.g. 29.7787" required>
        <input type="text" id="lon" name="lon" placeholder="Longitude e.g. -95.4218" required>
        <button type="button" onclick="add2map();">add2map</button>
    </form>
    <div class="folium-map" id="map" ></div>
### footer
    <script>
        var map = L.map(
            'map',
            {center: [30,-30],
            zoom: 2,
            maxBounds: bounds,
            layers: [],
            worldCopyJump: false,
            crs: L.CRS.EPSG3857
            });
            ...
    </script>
