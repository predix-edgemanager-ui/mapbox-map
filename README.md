#px-vis-pie-chart
==========================================

## Overview

px-map is a Predix UI component

## Usage

### Prerequisites
1. node.js
2. npm
3. bower
4. [webcomponents-lite.js polyfill](https://github.com/webcomponents/webcomponentsjs)

Node, npm and bower are necessary to install the component and dependencies. webcomponents.js adds support for web components and custom elements to your application.


## Getting Started

Install the app via git clone, go into the directory, bower install, run the app, go to px-map dropdown and click on the demo.
```bash
$ git clone 
$ cd px-map
$ bower install
$ polymer serve
go to px-map and click on demo to see a demo
```

Finally, use the component in your application:
Here is the over structure of the code:
The map is consist of two layers so far and in the future addition layer can be added to the existing two layers.
The main components used are located in 
* elements/px-map: Main map layer to display map and serve as the base to add more layers
* elements/px-map/map-side-menu: Side menu to display marker groups 
* elements/marker-layer: layer to display markers on the map 
* elements/map-legend: legend to display marker details and perform action on the markers.

to understand how to use the components, please see elements/user-usage to see how user would use the component

```html
  <head>
    <script src="bower_components/webcomponentsjs/webcomponents-lite.js"></script>
	  <link rel="import" href="bower_components/map-box/map-box.html">
	  <style>
    	html, body {
    		margin: 0;
    		height: 100%;
    	}
    	px-map {
    		height: 100%;
    	}
	  </style>
  </head>
  <body unresolved>
  <div style="flex flex--row">
    <div style="height:80vh;">  
      <px-map 
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
      </px-map>
    </div>
  <div style="height:20vh";> 
    <map-legend id="legendBox" legend-info="[[legendInfo]]" individual-feature-info="[[markerClicked]]" detail-title="All Devices" drop-down-config="{{dropDownConfig}}">
    </map-legend>
  </div>
</div>
  </body>
```

<br />
<hr />








License
-------
MIT
