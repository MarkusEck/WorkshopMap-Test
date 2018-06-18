<!DOCTYPE html>
<html>
  <head>
  <style>
    #map-canvas { width:1000px; height:700px; }
    .layer-wizard-search-label { font-family: sans-serif };
  </style>
  <script type="text/javascript"
    src="http://maps.google.com/maps/api/js?sensor=false">
  </script>
  <script type="text/javascript">
    var map;
    var layer_0;
    var layer_1;
    function initialize() {
      map = new google.maps.Map(document.getElementById('map-canvas'), {
        center: new google.maps.LatLng(52.45874446186184, 13.330655170305818),
        zoom: 10,
        mapTypeId: google.maps.MapTypeId.ROADMAP
      });
      layer_0 = new google.maps.FusionTablesLayer({
        query: {
          select: "col2>>0",
          from: "1Ce0h6WuFW5nP60EhgU7Nzj6s0vvTM7MZxfd02lx0"
        },
        map: map,
        styleId: 2,
        templateId: 2
      });
      layer_1 = new google.maps.FusionTablesLayer({
        query: {
          select: "col8",
          from: "1nteEAwOcPdiP4tZR7Rp-eJuJW1-3xMFfeJb0QxfK"
        },
        map: map,
        styleId: 2,
        templateId: 2
      });
    }
    google.maps.event.addDomListener(window, 'load', initialize);
  </script>
  </head>
  <body>
    <div id="map-canvas"></div>
  </body>
</html>
