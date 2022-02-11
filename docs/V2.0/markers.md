![MapmyIndia APIs](https://www.mapmyindia.com/api/img/mapmyindia-api.png)
# MapmyIndia Interactive Vector Maps JS SDK for Web !

You can get your api key to be used in this document here: [https://www.mapmyindia.com/api/signup](https://www.mapmyindia.com/api/signup)


## Markers

Markers are effortless way of pointing to a location, so getting right to it, you can go ahead and add markers that we provide out of the box but just in case you want to add your own, we’ve got that covered for you as well. There are 3 main categories of markers that you can add namely,  
-  **Stock Markers**: The one you get out of the box using our Interactive Vector Maps SDK and you can select from a lot of choices.  
-  **Custom Marker**: Just in case you want to provide your own markers, we’ve handled that for you as well.  
-  **HTML Marker**: In case you don’t want to add in an image you can use HTML to create a marker and then plot it on the map as well.

### Add Markers

```js
var marker = new MapmyIndia.Marker({
    map: map,
    position: {"lat": 28.519467,"lng":77.223150}
	});
```
#### Detailed Code:

```js
	marker = new MapmyIndia.Marker({
			map: object,
			id: id(optional),
			class: class(optional),
			position: {"lat": "28.519467","lng":"77.223150"},
			fitbounds: true, // or false
			fitboundOptions: {padding: 120,duration:1000}, /*if fitbound true*/
			icon: icon(url),
			offset: [0,10],
			width: 35,
			height: 20,
			html: <div style="white-space:nowrap;font-size:10px;padding l					eft:15px;color:#fff">Hello World</div>,
			popupOptions: true, //or false 
			popupHtml: 'Mapmyindia',
			draggable: true, //or false
			clustersOptions: {"color": "blue","bgcolor":"red"},
		})
```

[**Multiple Marker With cluster**](#Multiple-Marker-With-cluster)

[Live Demo](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/multiple-marker) | [JS Fiddle](https://jsfiddle.net/mapmyindia_map/efo0cn2r/)

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

#### GeoJSON bulk Markers

[Live Demo](https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/addgeojson)

```js
	var geoData={
				"type": "FeatureCollection",
				"features": [{
				"type": "Feature",
				"properties":
					{
						"description":"noida",
						"icon":"https://apis.mapmyindia.com/map_v3/1.png",
						"icon-size":.75,
						"icon-offset":[0,-10],
						"text":"1",
						"text-size":10,
						"text-offset":[0,.6]
				},
				"geometry": {"type": "Point",
				"coordinates": [28.544,77.5454]}
				},{
				"type": "Feature",
				"properties": {"description":"faridabad","icon":"https://apis.mapmyindia.com/map_v3/1.png"},
				"geometry": {"type": "Point",
				"coordinates": [28.27189158,77.2158203125]}
				},{
				"type": "Feature",
				"properties": {"description":"delhi","icon":"https://apis.mapmyindia.com/map_v3/1.png"},
				"geometry": {"type": "Point",
				"coordinates": [28.549511,77.2678250]}
				}]
			};
	var marker=MapmyIndia.addGeoJson({map:map,data:geoData,fitbounds:true,cType:0});
```


### Remove Markers

**`MapmyIndia.remove()`**

```js
	MapmyIndia.remove({map: map_object, layer: marker_object});
```


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