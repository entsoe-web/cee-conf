---
title: venue
order: 4
---

<div class="small-12 columns">
<div class="large-8" markdown="1">
# {{page.title | capitalize}}
{:id="{{page.title | append: '_1'}}"}
</div>
</div>

{% raw %}
<style type="text/css">
    .bleed-section .address {
    background-color: white;
    padding: 40px;
    position: absolute;
    z-index: 4;
    border-radius: 8px;
    top: 80px;
    right: 20px;
    font-weight: 900;
}
</style>

<div class="bleed-section" style="min-height:1px;position: relative;">

<div class="address hide-for-small-only">
    <a href="https://goo.gl/maps/czETZzEoqom">Grand Hotel River Park,<br>Dvorakovo Nabrezie 6,<br> Bratislava 81102,<br> Slovakia</a>
    
</div>
<div id='map'></div>
</div>

<script src='https://api.tiles.mapbox.com/mapbox-gl-js/v0.17.0/mapbox-gl.js'></script>
<link href='https://api.tiles.mapbox.com/mapbox-gl-js/v0.17.0/mapbox-gl.css' rel='stylesheet' />
<style>
    body { margin:0; padding:0; }
    #map { position:relative; top:0; bottom:0; width:100%; height:500px; }
</style>
<script type="text/javascript">

mapboxgl.accessToken = 'pk.eyJ1IjoiZW50c29lIiwiYSI6ImNpbWxxYXJocDAwMG53Ymx3N2JxNGhtZDYifQ.YjNgK9usqRNrzxWXnR152g';
var map = new mapboxgl.Map({
    container: 'map',
    style: 'mapbox://styles/mapbox/streets-v8',
    center: [17.0902620,48.141673],
    zoom: 15
});

map.scrollZoom.disable();
map.addControl(new mapboxgl.Navigation({position:'top-left'}))

map.on('style.load', function () {
    map.addSource("markers", {
        "type": "geojson",
        "data": {
            "type": "FeatureCollection",
            "features": [{
                "type": "Feature",
                "geometry": {
                    "type": "Point",
                    "coordinates": [17.0902620,48.141673]
                },
                "properties": {
                    "title": "Grand Hotel River Park",
                    "description": 'Dvorakovo Nabrezie 6, Bratislava, 81102, Slovakia',
                    "marker-symbol": "monument"
                }
            }]
        }
    });

    map.addLayer({
        "id": "markers",
        "type": "symbol",
        "source": "markers",
        "layout": {
            "icon-image": "{marker-symbol}-15",
            "text-field": "{title}",
            "text-font": ["Open Sans Bold", "Arial Unicode MS Bold"],
            "text-offset": [0, 0.6],
            "text-anchor": "top"
        }
    });
});

// When a click event occurs near a marker icon, open a popup at the location of
// the feature, with description HTML from its properties.
map.on('click', function (e) {
    var features = map.queryRenderedFeatures(e.point, { layers: ['markers'] });

    if (!features.length) {
        return;
    }

    var feature = features[0];

    // Populate the popup and set its coordinates
    // based on the feature found.
    var popup = new mapboxgl.Popup()
        .setLngLat(feature.geometry.coordinates)
        .setHTML(feature.properties.description)
        .addTo(map);
});

</script>
{% endraw %}