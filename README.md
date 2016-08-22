&lt;mapbox-map&gt; element &lt;/mapbox-map&gt;
==========================================

Make Open Street Maps using declarative Polymer web components. To get started read the [&lt;mapbox-doc&gt;&lt;/mapbox-doc&gt;] or checkout the [&lt;mapbox-demo&gt;&lt;/mapbox-demo&gt;].


Tech
-----------

`<mapbox-map></mapbox-map>` use:
* [Mapbox] - Awesome library for use Open Maps
* [Polymer] - Awesome framework for web components.

Use guide
--------------
```bash
$ git clone 
$ cd mapbox-map
$ bower install
$ polymer serve
```



##### Configure Polymer and the new component.

```html
  <head>
    <script src="bower_components/webcomponentsjs/webcomponents-lite.js"></script>
	  <link rel="import" href="bower_components/map-box/map-box.html">
	  <style>
    	html, body {
    		margin: 0;
    		height: 100%;
    	}
    	mapbox-map {
    		height: 100%;
    	}
	  </style>
  </head>
  <body unresolved>
  <div style="flex flex--row">
    <div style="height:80vh;">  
      <mapbox-map 
        id="mapContainer"
        zoom="3"
        latitude="37.77493" 
        longitude="-122.41942"
        layer="roadtrippers.ijjip7cb"
        selected-features="{{selectedFeatures}}"
        zoomable
        side-menu-dropdown="{{sideMenuDropdown}}">
        <marker-layer 
          selected-marker="{{markerClicked}}" 
          cluster-marker legend-info="{{legendInfo}}" 
          custom-pie-color-function="myMap.customPieColorFunction" 
          custom-legend-function="myMap.customizedLegendInfo"
          data='{{inputData}}' 
          selected-icon="{{selectedIcon}}">
        </marker-layer>
      </mapbox-map>
    </div>
  <div style="height:20vh";> 
    <map-legend id="legendBox" legend-info="[[legendInfo]]" individual-feature-info="[[markerClicked]]" detail-title="All Devices" drop-down-config="{{dropDownConfig}}">
    </map-legend>
  </div>
</div>
  </body>
```


License
-------
MIT


[&lt;mapbox-demo&gt;&lt;/mapbox-demo&gt;]:http://gnurub.github.io/mapbox-map/components/map-box/
[&lt;mapbox-doc&gt;&lt;/mapbox-doc&gt;]:http://gnurub.github.io/mapbox-map/components/map-box/
[Polymer]:http://www.polymer-project.org/
[MapBoxEditor]:https://www.mapbox.com/editor
[MapBoxStudio]:https://www.mapbox.com/mapbox-studio/
[Mapbox]:https://www.mapbox.com/
[Events mapbox]:https://www.mapbox.com/mapbox.js/api/v2.2.1/l-map-class/#map-events
[Events marker]:https://www.mapbox.com/mapbox.js/api/v2.2.1/l-marker/#marker-events
[maki]:https://www.mapbox.com/maki/
[bower]:http://bower.io/
[1]:http://pix.toile-libre.org/upload/original/1439212072.png
[2]:http://i.imgur.com/Eclrm2ul.jpg
[3]:http://i.imgur.com/P8HXkrFl.jpg
