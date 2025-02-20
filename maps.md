---
layout: page
title: "Maps"
permalink: /maps2/
---

## Maps Embedded JavaScript

<div id="map" style="width: 100%; height: 500px;"></div>
<script src="https://cdn.apple-mapkit.com/mk/5.x.x/mapkit.js"></script>
<script>
  mapkit.init({ authorizationCallback: function(done) { done('YOUR_TOKEN_HERE'); } });
  const map = new mapkit.Map('map', { center: new mapkit.Coordinate(37.7749, -122.4194), zoom: 11 });
  const trainData = [...];
  trainData.forEach(train => {
    const annotation = new mapkit.MarkerAnnotation(new mapkit.Coordinate(train.latitude, train.longitude), {
      title: train.name, subtitle: train.detail,
    });
    map.addAnnotation(annotation);
  });
</script>