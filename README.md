# WebMapping
Assignments for Web Mapping
## Assignment_One
<!DOCTYPE html>
<html>

  <head>
    <meta charset='utf-8' />
    <title>University of Oregon Mapping</title>
    <meta name='viewport' content='initial-scale=1,maximum-scale=1,user-scalable=no' />
    <!--    Include the reference to the Mapbox JavaScript here in the <head> of the page  (Part I.1)  -->
     <script src="https://api.mapbox.com/mapbox-gl-js/v3.20.0/mapbox-gl.js"></script>


          
    <!--    Include the reference to the Mapbox CSS here in between <head> tags    (Part I.2) -->
     <link href="https://api.mapbox.com/mapbox-gl-js/v3.20.0/mapbox-gl.css" rel="stylesheet">

    <style>
        /* Insert the additional CSS code here between the <style> tags  (Part I.4)   */
         body { margin:0; padding:0; }

    #map {
      position:absolute;
      top:0;
      bottom:0;
      width:100%;
    }

    #banner {
      z-index: 9999;
      background-color: white;
      opacity: 0.8;
      text-align: center;
      color: darkgreen;
      padding: 10px;
    }



    </style>
  </head>

  <body>
    <!--  Insert the map div here in the <body> of the page  (Part I)  -->
   <div id='map'></div>
    <!--  Insert the title div here (part VI) -->
 <div id='banner'>
    <h1>My Map of Portland</h1>
    <h2>By: Makenna Phillips</h2>
  </div>
    <script>
        // Insert the JavaScript within the <script> tags, within the body   
        // Start with the Mapbox access token here (Part 2.1)
mapboxgl.accessToken = 'pk.eyJ1IjoibWFrZW5uYWFwaGlsbGlwcyIsImEiOiJjbW5wNGk0dDgyYzlrMnJxNXI4dDdzMHc1In0.iFOEbvb6cI1ZBb1o0Qcl8g';

const map = new mapboxgl.Map({
  container: 'map',
  style: 'mapbox://styles/mapbox/navigation-day-v1',
  center: [-122.6788, 45.5212],
  zoom: 10
});

        // Add the zoom contols here (part V)
   map.addControl(new mapboxgl.NavigationControl({
      showCompass: false
    }), 'bottom-left');
        // Add popups for markers here. Yes, before the markers!  (part IV)
        var popup = new mapboxgl.Popup({ offset: 25 })
      .setHTML('<a href="https://www.powells.com/?srsltid=AfmBOopD1jNtIIB4Srj1bZ9xgqt_2-7t8LaaK77hVepBaVjtsiAoW0XH">Powells Books</a>');

        // Add any other variables such as markers here (part III)
 var marker = new mapboxgl.Marker({ color: 'green' })
      .setLngLat([-122.6788, 45.5212])
      .setPopup(popup)
      .addTo(map);
        // Add any other variables such as markers here (part III)
 var marker = new mapboxgl.Marker({ color: 'pink' })
      .setLngLat([-122.6814, 45.5232])
      .setPopup(popup)
      .addTo(map);
        // Add optional advanced "On load" function here
        
    </script>

  </body>

</html>
