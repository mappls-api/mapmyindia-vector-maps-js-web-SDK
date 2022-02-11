![MapmyIndia APIs](https://www.mapmyindia.com/api/img/mapmyindia-api.png)
# MapmyIndia Interactive Vector Maps JS SDK for Web !

You can get your api key to be used in this document here: [https://www.mapmyindia.com/api/signup](https://www.mapmyindia.com/api/signup)


## KML Overlay

### Supported Object Types

#### 1. Markers
#### 2. Polylines
#### 3. Polygons


### Overlaying KML on map

#### [KML Properties](#KML-Properties)

### *Required*

- **Map**
- **url:** URL of the KML file.

### *Optional*

- **fitbounds:** Fits in the map layer automatically to a bound on which geoJson has made. By default it is false.

```js
	{
		fitbounds: true
	}
```

- **fitboundOptions:** This shows the options aailable on the fitBound property.

```js
	{
		fitboundOptions: {padding: 120,duration:1000}
	}
```

- **cType:** It is for geojson data geometry<br>
    - 0: for lat,lng combination (Default)<br>
    - 1: for lng,lat conbination

```js
    {
        cType: 1
    }
```

#### KmlLayer Method

**`MapmyIndia.KmlLayer()`**

```js
	var url="https://www.mapmyindia.com/api/advanced-maps/doc/sample/mmi.kml"; 
	new MapmyIndia.KmlLayer({
		map:map_object,
		url:url,
		cType:1,
		preserveViewport:true
	});
```

### Remove KML Overlay

```js
	MapmyIndia.remove({map:map_object,layer:KmlLayer_object});
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