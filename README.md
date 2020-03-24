![MapmyIndia APIs](https://www.mapmyindia.com/api/img/mapmyindia-api.png)
# MapmyIndia Interactive Vector Maps JS SDK for Web !

You can get your api key to be used in this document here: [https://www.mapmyindia.com/api/signup](https://www.mapmyindia.com/api/signup)

## Introduction
The Interactive Maps JavaScript SDK for Web helps render and display map tiles while customizing the map's look and feel on mobile or web browser. MapmyIndia is India's leading Map provider, and produces various SDKs, including Web SDKs (JavaScript libraries) for mobile-friendly interactive maps which are easy to use & high on performance. 
This SDK is a collection of classes and functions that can be used to implement a host of map features.

**Features:**

-   **Zoom**: Pan-able map of India with 19 zoom levels, 22 being the highest (most detailed) and 4 being the lowest (country level) map display.
-   **Overlays**: The map is the key for any sort of business and understanding this, we at MapmyIndia provide quick default overlays to reduce the boiler plate code for your code base.
    -   **Map Markers (Pushpins)**: Point to any location using default pushpin behaviours and provide it your own style to make it look more tailored for your application. Note: Have a look at the Plug-ins section to find out what makes it cooler.
    -   **Info Windows (Pop-ups)**: On a Map Clicking is a native behaviour understanding this, we provide out of the box info windows such that if a pushpin is clicked an info window pops up open and you can show your content related to that location there. You can style it to make it behave as required for your UI to be magnificent.
    -   **Polylines**: Connect any two points or even more with out of the box MapmyIndia polylines dedicated to high customizability and performance to suit your use cases. Note: Have a look at the plug-ins we provide to make your polylines have an edge up and suit your use cases in a more integrated manner.
    -   **Polygons**: Show a region in a spotlight with a polygon and show various localized data based on it.
    -   **Circles:** Show instant radial areas of inter
-   **Controls**: because we understand the use cases with a map we provide the below out of the box controls that can be turned off or on based on your requirement and because we care, we provide you to override our controls outlook by providing your own styles or CSS so that you can move them or customize them completely. Controls include:
    -   **Zoom Bar**: (appears by default at the centre on the right side). Helps to provide zoom in and zoom out functionality to the map by default.
    -   **Map Layer Control**: Allows to change the map view from basic to hybrid and regional. Also allows to show traffic layer on map.
  -   **Fullscreen Control**: Allows to view a fullscreen map.
  -   **Current Location Control**: Scopes the Map to the viewer’s current location.**  
	
        Note:**  The location settings must be turned on and must allow the site to fetch the location for this control to work.

**Please Note**: MapmyIndia may extend and enhance functionality for its interactive map API in future, which will be clearly documented in this section, and which will be available through the MapmyIndia.Map class and MapmyIndia.* set of classes generally.

## Getting Started

Now that you’re all caught up with the features let’s get down right to them and look at how can you integrate our Interactive Map to your Website from scratch.


### Initializing The Map

[Live Demo](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/mapInitialization) | [JS Fiddle](https://jsfiddle.net/mapmyindia_map/7fqyshoc/)

The easiest way to start loading maps in a web page is with a “Hello World” sample code, you can download or view a working “Hello World” sample from the links for adding your first marker below.

#### Adding the Map Script to your web page

Follow the below steps to integrate MapmyIndia interactive Maps into your existing code base or even a File -> New Project.
- Declare application as HTML5:
Define `<!DOCTYPE html>` on top of your HTML.
- Integrate Interactive maps from MapmyIndia into your browser application by simply including MapmyIndia's interactive map API in your script source in the head section.

```html
    <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?v=2.0&layer=vector"></script>
```

    **Important**: 

    - *bearer token* in place of `<key>`
    - *layer*: Vector/raster default vector

- Define a style in the head section to load in your CSS.
   
```html
    <style> html, body, #map1 {margin: 0;padding: 0;width: 100%;height: 100%;} </style>
```

- Define a div object in the body tag of the HTML where you want the MapmyIndia Map to show up.

```html
    <div id="map"></div>;
```

- Initialize a MapmyIndia Map by simply calling new MapmyIndia.Map() in the JavaScript and passing it at the minimum, the div object in which you want the map populated. (All other parameters are optional.)

```js
    map = new MapmyIndia.Map('map', {center:{lat:28.612964,lng:77.229463} });
```	

- **Hello World** 

```html    
  <html>
      <head>
      <title>Hello, World</title>
      <meta name="viewport" content="initial-scale=1.0">
      <meta charset="utf-8">
      <style>
          html,
          body,
          #map {
              margin: 0;
              padding: 0;
              width: 100%;
              height: 100vh;
              }
      </style>
      <script src="https://apis.mapmyindia.com/advancedmaps/api/<key>/map_sdk?layer=vector&v=2.0&callback=loadMap" defer async></script>
      </head>
      <body>
          <div id="map"></div>
          <script>
              var map;
              function loadMap()
              { 
                  map = new MapmyIndia.Map('map', {center: [28.544,77.5454]});
              } 
          </script>
      </body>
  </html>   
```
	
## Map Quick Reference:

- [**Map Properties**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/mapProperties)
    

- [**Map Methods**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/mapMethods)

	
- [**Map Events**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/mapEvents)

### Markers


Markers are effortless way of pointing to a location, so getting right to it, you can go ahead and add markers that we provide out of the box but just in case you want to add your own, we’ve got that covered for you as well. There are 3 main categories of markers that you can add namely,  
-  **Stock Markers**: The one you get out of the box using our Interactive Vector Maps SDK and you can select from a lot of choices.  
-  **Custom Marker**: Just in case you want to provide your own markers, we’ve handled that for you as well.  
-  **HTML Marker**: In case you don’t want to add in an image you can use HTML to create a marker and then plot it on the map as well.

For more details on Markers, please read article in [wiki](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/markers)
  
Now, that you have a basic understanding of Markers, Functions and Events let’s talk about Info Windows or Pop-Ups.

### Adding Your First Marker

[LIVE DEMO](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/single-marker) | [JS Fiddle](https://jsfiddle.net/mapmyindia_map/7uyafxjn/)

The easiest way to start loading maps with simple markers in a web page is with a “Hello World” sample code, you can download or view a working “Hello World” sample from the links above. 
  
In the sample, we have a case of a map scenario where objective is plotting a pushpin that says hello world on click. 

#### Method to add marker on map

**`new MapmyIndia.Marker`**

##### Code to add marker on Map

```js
var marker = new MapmyIndia.Marker({
    map: map,
    position: {"lat": 28.519467,"lng":77.223150}
	});
```

## Example

```html    
<html>
    <head>
    <title>First Marker</title>
    <meta name="viewport" content="initial-scale=1.0">
    <meta charset="utf-8">
    <style>
        html,
        body,
        #map {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100vh;
            }
    </style>
    <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?layer=vector&v=2.0&callback=loadMap" defer async></script>
    </head>
    <body>
        <div id="map"></div>
        <script>
            var map;
            function loadMap()
            { 
                map = new MapmyIndia.Map('map', {center: [28.544,77.5454]});
                map.addListener('load', function () {
                    var marker= new MapmyIndia.Marker({
                    map: map,
                    position: {"lat": 28.544,"lng":77.5454}
                    });
                }); 
            }
            </script>
        </body>
    </html>
```

### Knowing Properties And Methods

You can interact with properties of the Map we provide to suite your use case and add additional customizability to your Map layer using the features it has to offer. These functions are a quick go to in case of an event. 

For details on Map Methods, please read article in [wiki](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/mapMethods)

## Marker Quick Reference:

- [**Marker Properties**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/markerProperties)
    
- [**Marker Methods**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/markerMethods)

- [**Marker Events**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/markerEvents)

- [**Multiple Marker with cluster**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/markers#Multiple-Marker-With-cluster)

- [**GeoJSON Bulk Marker**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/markers#GeoJSON-Bulk-Marker)

```js
    var geoData={
                "type": "FeatureCollection",
                "features": [{
                "type": "Feature",
                "properties": {"htmlPopup":"noida"},
                "geometry": {"type": "Point",
                "coordinates": [28.544,77.5454]}
                },{
                "type": "Feature",
                "properties": {"htmlPopup":"faridabad"},
                "geometry": {"type": "Point",
                "coordinates": [28.27189158,77.2158203125]}
                },{
                "type": "Feature",
                "properties": {"htmlPopup":"delhi"},
                "geometry": {"type": "Point",
                "coordinates": [28.549511,77.2678250]}
                }]
            };
    var marker=MapmyIndia.Marker({map:map,position:geoData,icon_url:'https://apis.mapmyindia.com/map_v3/1.png',clusters:true,fitbounds:true,fitboundOptions:{padding: 120,duration:1000},popupOptions:{offset: {'bottom': [0, -20]}}});
```


### Info Windows

[LIVE DEMO](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/infowindow) | [JS Fiddle](https://jsfiddle.net/mapmyindia_map/wcto9g0n/)

Info Windows are a convenient way of showing data about a marker or in simple words: what that marker stands for. The Native behaviour of a user to know about any marker is to try and click on it to know what it’s all about and showing an info window would be the way to go about it:

**Please Note**: MapmyIndia interactive map SDK supports a default info window that you can leverage but we want you to have an option to customize your info window to fit in with your UI and you can do so in the CSS.

For a quick sample or a demo you can follow up with the links on top. 

You can declare an info window in your CSS and write up a quick function to generate data in that info window and on marker click event simple open that info window.

For details on Info Windows, please read article in [wiki](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/infoWindows)

## Example

```html    
    <html>
        <head>
        <title>Infowindow</title>
        <meta name="viewport" content="initial-scale=1.0">
        <meta charset="utf-8">
        <style>
            html,
            body,
            #map {
                margin: 0;
                padding: 0;
                width: 100%;
                height: 100vh;
                }
        </style>
        <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?layer=vector&v=2.0&callback=loadMap" defer async></script>
        </head>
        <body>
            <div id="map"></div>
            <script>
                var map;
                function loadMap()
                { 
                    map = new MapmyIndia.Map('map', {center: [28.544,77.5454]});
                    map.addListener('load', function () {
                        var window=new MapmyIndia.InfoWindow({map:map,content:"Balmukand",position:{lat: 28.529467 ,lng: 77.223150}});
                    }); 
                }
            </script>
        </body>
    </html>
```

## Info Window Quick Reference

- [**InfoWindow Properties**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/infoWindows#InfoWindow-Properties)

- [**Remove InfoWindow**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/infoWindows#Remove-InfoWindow)


### Polylines

[LIVE DEMO](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/polyline) | [JS Fiddle](https://jsfiddle.net/mapmyindia_map/15faq7j2/)

Polylines are a way of showing movement or transit on a map. We at MapmyIndia understand the ways you can leverage the features offered by a map and one among them is a Polyline.

Polylines are continuous lines consisting of one or more line segments (preferably a geopath). To add a polyline, initialize map as shown in the previous sections and then create a data set. What is a data set? The Data set is the collection of points (latitude and longitude) over which you want the polyline to be drawn.

For details on Polylines, please read article in [wiki](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polyline)

### Polyline Quick Reference

- [**Polyline Properties**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polyline#Polyline-Properties)

## Example:

 ```html    
	<html>
    <head>
    <title>Polyline</title>
    <meta name="viewport" content="initial-scale=1.0">
    <meta charset="utf-8">
    <style>
        html,
        body,
        #map {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100vh;
            }
    </style>
    <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?layer=vector&v=2.0&callback=loadMap" defer async></script>
    </head>
    <body>
        <div id="map"></div>
        <script>
            var map;
            function loadMap()
            { 
                map = new MapmyIndia.Map('map', {center: [28.544,77.5454]});
                map.addListener('load', function () {
                    
                    var pts=[{lat:28.55108, lng:77.26913},{lat:28.55106,lng: 77.26906},{lat:28.55105,lng: 77.26897},{lat:28.55101,lng:77.26872},{lat:28.55099, lng:77.26849},{lat:28.55097, lng:77.26831},{lat:28.55093, lng:77.26794},{lat:28.55089, lng:77.2676},{lat:28.55123, lng:77.26756},{lat:28.55145, lng:77.26758},{lat:28.55168, lng:77.26758},{lat:28.55175, lng:77.26759},{lat:28.55177, lng:77.26755},{lat:28.55179, lng:77.26753}];
                    var polyline = new MapmyIndia.Polyline({
                        map:map,
                        paths: pts,
                        strokeColor: '#333',
                        strokeOpacity: 1.0,
                        strokeWeight: 5,
                        fitbounds:true
			        });
                }); 
            }
        </script>
    </body>
</html>
```

- [**Draw Editable Polyline**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polyline#Editable-Polyline)

*Drag polyline from anywhere & get callback polyline data. By default the value is false.*

```js
    editable: true 
```

- [**Draw Gradient In Polyline**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polyline#Gradient-Polyline)

- [**Draw Animated Polyline**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polyline#Animated-Polyline)

*Polyline draw point by point with speed*

```js
    animate: {path:true/false,speed:5}
```

- [**Animated Marker Along With Polyline**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polyline#Animated-Marker-Along-With-Polyline)

```js
    animate: { 
        speed:5 
        icon_width: 35 / “35”,
        icon_height: 15 / “15”,,
        icon_url: (icon_url),
        repeat: true/false,
    },
```

- [**Multi Colored Polyline**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polyline#Multi-Colored-Polyline)

- [**Polyline Marker Animation Methods**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polyline#polyline-marker-animation-methods)

- [**Polyline Events**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polyline#polyline-events)

**Remove Polyline**
```js
    MapmyIndia.remove({map: map, layer: polyline);
```


In real case scenarios, you’ll need to get the data set on the fly or from a service and then you can leverage the events and functions we’ve learnt about how to plot the polyline. You also might need to beautify your polyline or add transitions for your UI to look marvellous. 

The polyline is just the beginning, but sometimes you’ll need to mark a territory to properly showcase your information. In such cases a polyline might not be the perfect fit but Polygons and Circles may be the apt choice.

### Polygons

Polygons are a way of showing a territory. In cases where you want to showcase data over an area, polygons are your best pick. You can use them to show Geozones as well.

It’s very like generating a polyline, the basic steps remain the same, create a Data set, generate a polygon and add it to the map.

For details on Polygons, please read article in [wiki](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polygon)


**Simple Polygon**

[LIVE DEMO](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/polygon) | [JS Fiddle](https://jsfiddle.net/mapmyindia_map/tmyexuz0/)

## Example

```html    
    <html>
        <head>
        <title>Polygon</title>
        <meta name="viewport" content="initial-scale=1.0">
        <meta charset="utf-8">
        <style>
            html,
            body,
            #map {
                margin: 0;
                padding: 0;
                width: 100%;
                height: 100vh;
                }
        </style>
        <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?layer=vector&v=2.0&callback=loadMap" defer async></script>
        </head>
        <body>
            <div id="map"></div>
            <script>
                var map;
                function loadMap()
                { 
                    map = new MapmyIndia.Map('map', {center: [28.544,77.5454]});
                    map.addListener('load', function () {
                        var pts=[{lat: 28.774, lng: 80.190},{lat: 28.466, lng: 76.118},{lat: 27.321, lng: 77.757},{lat: 27.771, lng: 80.757}];
                        new MapmyIndia.Polygon({map:map,paths: pts,fillColor:"blue"});
                    }); 
                }
            </script>
        </body>
    </html>
```

- [**Polygon Properties**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polygon#polygon-properties)

- [**Polygon Events**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/polygon#polygon-events)

### Draw Polyline/Polygons 

This method can draw polyline or polygon directly from map with click event. with callback methods.

Double Click to finish draw event.

```js
//Polyline

    var polylineoptions={strokeColor: "blue",strokeOpacity:1.0,strokeWeight: 9,lineGap:0,popupHtml:'Route 1',popupOptions:{offset: {'bottom': [0, -20]}}} 

    MapmyIndia.draw({map:map,type:'polyline',callback:draw_callback,options:polylineoptions});

//Polygon
var polygonoptions={fillColor:'#333'}
MapmyIndia.draw({map:map,type:'polygon',callback:draw_callback,options:polygonoptions});

function draw_callback(data)
{
 console.log(data);
}
```

*Now that we’ve covered polygons let’s have a look at **Circles** which provide another way of showcasing territory.*

### Circles

Circles are way of marking a territory without too much interaction by the user. A circle only has two important values:

-   The Centre point of the circle (in this case it’ll be a latitude with a longitude).
-   The Radius of the circle.

With the two values, you can easily define a quick area of interest on a map.

For details on Circles, please read article in [wiki](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/circle)

```js
    MapmyIndia.Circle()
```

[LIVE DEMO](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/circle) | [JS Fiddle](https://jsfiddle.net/mapmyindia_map/24pgv9qw/)

## Example

```html    
	<html>
    <head>
    <title>Circle</title>
    <meta name="viewport" content="initial-scale=1.0">
    <meta charset="utf-8">
    <style>
        html,
        body,
        #map {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100vh;
            }
    </style>
    <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?layer=vector&v=2.0&callback=loadMap" defer async></script>
    </head>
    <body>
        <div id="map"></div>
        <script>
            var map;
            function loadMap()
            { 
                map = new MapmyIndia.Map('map', {center: [28.544,77.5454]});
                map.addListener('load', function () {
                    var mapmyindia_circle = new MapmyIndia.Circle({
                    map: map,
                    center: {"lat": 28.544 ,"lng": 77.5454},
                    radius: 1000});
                }); 
            }
        </script>
    </body>
</html>
```
- [**Circle Properties**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/circle#circle-properties)

- [**Circle Events**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/circle#circle-events)



## Heatmap Overlays

For details on Heatmap Overlays, please read article in [wiki](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/heatMap)

```js
    var pts=[ {lat: 28.774, lng: 80.190}, {lat: 28.466, lng: 76.118}, {lat: 27.321, lng: 77.757}, {lat: 27.774, lng: 80.190} ];

    var heat_map=new MapmyIndia.HeatmapLayer({map:map,data:pts,fitbounds:true});
```

- [**Heatmap Properties**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/heatMap#Heatmap-Properties)

[LIVE DEMO](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/heatmaplayer)

## Example

```html    
    <html>
        <head>
        <title>Heatmap</title>
        <meta name="viewport" content="initial-scale=1.0">
        <meta charset="utf-8">
        <style>
            html,
            body,
            #map {
                margin: 0;
                padding: 0;
                width: 100%;
                height: 100vh;
                }
        </style>
        <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?layer=vector&v=2.0&callback=loadMap" defer async></script>
        </head>
        <body>
            <div id="map"></div>
            <script>
                var map;
                function loadMap()
                { 
                    map = new MapmyIndia.Map('map', {center: [28.544,77.5454]});
                    map.addListener('load', function () {
                        var pts=[{lat:28.55108, lng:77.26913},{lat:28.55106,lng: 77.26906},{lat:28.55105,lng: 77.26897},{lat:28.55101,lng:77.26872},{lat:28.55099, lng:77.26849},{lat:28.55097, lng:77.26831},{lat:28.55093, lng:77.26794},{lat:28.55089, lng:77.2676},{lat:28.55123, lng:77.26756},{lat:28.55145, lng:77.26758},{lat:28.55168, lng:77.26758},{lat:28.55175, lng:77.26759},{lat:28.55177, lng:77.26755},{lat:28.55179, lng:77.26753}];

                        var gradient = [ 'rgba(0, 255, 255, 0)', 'rgba(0, 255, 255, 1)', 'rgba(0, 191, 255, 1)', 'rgba(0, 127, 255, 1)', 'rgba(0, 63, 255, 1)', 'rgba(0, 0, 255, 1)', 'rgba(0, 0, 223, 1)', 'rgba(0, 0, 191, 1)', 'rgba(0, 0, 159, 1)', 'rgba(0, 0, 127, 1)', 'rgba(63, 0, 91, 1)', 'rgba(127, 0, 63, 1)', 'rgba(191, 0, 31, 1)', 'brown' ]; 

                        var heat_map=new MapmyIndia.HeatmapLayer({map:map,data:pts,gradient:gradient,fitbounds:true});
                    }); 
                }
            </script>
        </body>
    </html>
```


### Add geojson layer

For details on GeoJSON layer, please read article in [wiki](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/geoJson)

[Live Demo](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/addgeojson) | [JS Fiddle](https://jsfiddle.net/mapmyindia_map/19hotbck/)

*GeoJSON Supports marker, polyline and polygon*

***Marker Propery support in geojson***

1. description
2. icon 
3. icon-size 
4. icon-offset
5. text 
6. text-size
7. text-offset

***polyline Propery support in geojson:***

1. stroke
2. stroke-opacity
3. stroke-width

***polygon Propery support in geojson:***

1. stroke
2. fill color
3. fill opacity

```js
    new MapmyIndia.addGeoJson({map:map,data:geoData,fitbounds:true,cType:0});
```

- [**Add GeoJSON Properties**](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/geoJson#Add-GeoJSON-Properties)

## Example

```html    
    <html>
        <head>
        <title>Geojson Layer</title>
        <meta name="viewport" content="initial-scale=1.0">
        <meta charset="utf-8">
        <style>
            html,
            body,
            #map {
                margin: 0;
                padding: 0;
                width: 100%;
                height: 100vh;
                }
        </style>
        <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?layer=vector&v=2.0&callback=loadMap" defer async></script>
        </head>
        <body>
            <div id="map"></div>
            <script>
                var map;
                function loadMap()
                { 
                    map = new MapmyIndia.Map('map', {center: [28.544,77.5454]});
                    map.addListener('load', function () {
                        var mixjson={
                            "type": "FeatureCollection",
                            "features": [
                                {
                                    "type": "Feature",
                                    "geometry": {"type": "Point","coordinates": [28.54950,77.2678540]
                                    },
                                    "properties": {
                                        "name": "MapmyIndia old Office",
                                        "description": "Okhla delhi",
                                        "icon": "https://apis.mapmyindia.com/map_v3/1.png",
                                        "icon-size":1,
                                        "text":"",
                                        "text-size":20,
                                        "text-offset":[0,0],
                                        "text-color":"red",
                                    }
                                },
                                {
                                    "type": "Feature",
                                    "geometry": {
                                        "type": "Point",
                                        "coordinates": [28.5510446,77.268952]
                                    },
                                    "properties": {
                                        "name": "<div onclick=\"function1()\">MapmyIndia New Office</div>",
                                        "description": "68,Okhla delhi",
                                        "icon": "https://apis.mapmyindia.com/map_v3/1.png",
                                        "icon-size":0.55,
                                        "text":"1",
                                        "icon-offset":[0,-20],
                                    }
                                },
                                {
                                    "type": "Feature",
                                    "geometry": {
                                        "type": "LineString",
                                        "coordinates": [
                                            [28.551042,77.268953],
                                            [28.551005,77.268649],
                                            [28.550986,77.268392],
                                            [28.550967,77.268231],
                                            [28.550967,77.268177],
                                            [28.550958,77.268016],
                                            [28.55092,77.267587],
                                            [28.550722,77.267651],
                                            [28.55042,77.267823],
                                            [28.550128,77.267802],
                                            [28.549751,77.267995],
                                            [28.549652,77.268039]
                                        ]
                                    },
                                    "properties": {
                                        "name": "Direction1",
                                        "description": "Direction2",
                                        "stroke": "#33CC00",
                                        "stroke-opacity": 0.6509803921568628,
                                        "stroke-width": 10,
                                    }
                                },
                                {
                                    "type": "Feature",
                                    "geometry": {
                                        "type": "Polygon",
                                        "coordinates": [[
                                                [28.550868798522835,77.26878225803375],
                                                [28.550868798522835,77.26899683475493],
                                                [28.550383454405356,77.26903975009918],
                                                [28.550388166494926,77.26883590221404]
                                        ]]
                                    
                                    },
                                    "properties": {
                                        "name": "MapmyIndia Head Office",
                                        "stroke": "#33CC00",
                                        "stroke-opacity": 0.6509803921568628,
                                        "stroke-width": 3,
                                        "fill": "#33CC00",
                                        "fill-opacity": 0.6509803921568628
                                    }
                                }
                            ]
                        };
                    var jsonData=MapmyIndia.addGeoJson({map:map,data:mixjson,fitbounds:true});
                    }); 
                }
            </script>
        </body>
    </html>
```

**Remove Layer**
```js
    new MapmyIndia.remove({map:map,layer:jsonData});
```


### KML Overlay

**KML**: [Keyhole Markup Language](https://www.opengeospatial.org/standards/kml) is a file format used to display geographic data on maps.
Using this plugin, you can overlay KML data over MapmyIndia Maps for web.

[LIVE DEMO](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/kml) | [JS Fiddle](https://jsfiddle.net/mapmyindia_map/7zabxp3d/)

#### Important Notes to remember
1. Only KML data supported.
2. KML file **must** have absolute path or raw KML string 
(in variable or in textbox)
3. All internal URL's path **must** be absolute. 
(for icon path etc)
4. File must not be password protected.
5. File must be CORS enabled from the server where they are hosted.
6. File must follow KML standard strictly.

**How to allow**
add libraries=kml in initial load
ie.

```js
    <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?v=2.0&layer=vector&libraries=kml"></script>
```

- **KML Method**

```js
    var url="https://www.mapmyindia.com/api/advanced-maps/doc/sample/mmi.kml";
    MapmyIndia.KmlLayer({map:map,url:url,cType:1,fitbounds:true,fitboundOptions:{padding:200}});
```

- [**KML Properties**:](https://github.com/MapmyIndia/MapmyIndia-Interactive-Vector-Maps-JS-SDK/wiki/kml#KML-Properties)


```html    
    <html>
        <head>
        <title>Geojson Layer</title>
        <meta name="viewport" content="initial-scale=1.0">
        <meta charset="utf-8">
        <style>
            html,
            body,
            #map {
                margin: 0;
                padding: 0;
                width: 100%;
                height: 100vh;
                }
        </style>
        <script src="https://apis.mapmyindia.com/advancedmaps/api/<key or token>/map_sdk?layer=vector&v=2.0&libraries=kml&callback=loadMap" defer async></script>
        </head>
        <body>
            <div id="map"></div>
            <script>
                var map;
                function loadMap()
                { 
                    map = new MapmyIndia.Map('map', {center: [28.544,77.5454]});
                    map.addListener('load', function () {
                        var url="https://www.mapmyindia.com/api/advanced-maps/doc/sample/mmi.kml";
                        MapmyIndia.KmlLayer({map:map,url:url,fitbounds:true,fitboundOptions:{padding:200}});
                    }); 
                }
            </script>
        </body>
    </html>
```


**Please Note**: For a more detailed code snippet follow the links provided above to see the sample code or see a live demo.

For any queries and support, please contact: 

![Email](https://www.google.com/a/cpanel/mapmyindia.co.in/images/logo.gif?service=google_gsuite) 

Email us at [apisupport@mapmyindia.com](mailto:apisupport@mapmyindia.com)

![](https://www.mapmyindia.com/api/img/icons/stack-overflow.png)
[Stack Overflow](https://stackoverflow.com/questions/tagged/mapmyindia-api)
Ask a question under the mapmyindia-api

![](https://www.mapmyindia.com/api/img/icons/support.png)
[Support](https://www.mapmyindia.com/api/index.php#f_cont)
Need support? contact us!

![](https://www.mapmyindia.com/api/img/icons/blog.png)
[Blog](http://www.mapmyindia.com/blog/)
Read about the latest updates & customer stories


> © Copyright 2019. CE Info Systems Pvt. Ltd. All Rights Reserved. | [Terms & Conditions](http://www.mapmyindia.com/api/terms-&-conditions)
