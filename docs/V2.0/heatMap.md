![MapmyIndia APIs](https://www.mapmyindia.com/api/img/mapmyindia-api.png)
# MapmyIndia Interactive Vector Maps JS SDK for Web !

You can get your api key to be used in this document here: [https://www.mapmyindia.com/api/signup](https://www.mapmyindia.com/api/signup)


## Heat Map Overlay

### Overlaying Heat Maps on map

#### [Heatmap Properties](#heatmap-properties)

### *Required*

- **Map**
- **data** This could be be the array of lat lng.

### *Optional*

- **opacity:** Set the opacity of the heatmap overlays.

```js
	{
		opacity: 0.8
	}
```

- **radius:** Set the radius of the heatmap overlays.

```js
	{
		radius: 50
	}
```

- **maxIntensity:** Set the intensity of the heatmap overlays.

```js
	{
		maxIntensity: 50
	}
```

- **fitbounds:** Fit map to layer. By default the value is false

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

- **gradient:** The color gradient of the heatmap, specified as an array of CSS color strings. All CSS3 colors are supported except for extended named colors.

```js
	{
		gradient: [ 'rgba(0, 255, 255, 0)', 'rgba(0, 255, 255, 1)', 'rgba(0, 191, 255, 1)', 'rgba(0, 127, 255, 1)', 'rgba(0, 63, 255, 1)', 'rgba(0, 0, 255, 1)', 'rgba(0, 0, 223, 1)', 'rgba(0, 0, 191, 1)', 'rgba(0, 0, 159, 1)', 'rgba(0, 0, 127, 1)', 'rgba(63, 0, 91, 1)', 'rgba(127, 0, 63, 1)', 'rgba(191, 0, 31, 1)', 'brown' ]               
	}
```


#### HeatmapLayer Method

**`MapmyIndia.HeatmapLayer()`**

```js
	var pts=[{lat: 28.774, lng: 80.190}, {lat: 28.466, lng: 76.118},{lat: 27.321, lng: 77.757}, {lat: 27.774, lng: 80.190}];
	var gradient = ['rgba(0, 255, 255, 0)', 'rgba(0, 255, 255, 1)', 'rgba(0, 191, 255, 1)', 'rgba(0, 127, 255, 1)', 'rgba(0, 63, 255, 1)', 'rgba(0, 0, 255, 1)', 'rgba(0, 0, 223, 1)', 'rgba(0, 0, 191, 1)', 'rgba(0, 0, 159, 1)', 'rgba(0, 0, 127, 1)', 'rgba(63, 0, 91, 1)', 'rgba(127, 0, 63, 1)', 'rgba(191, 0, 31, 1)', 'brown' ]; 
	heat_map=new MapmyIndia.HeatmapLayer({
		map:map_object,
		data:pts,
		opacity:1,
		radius:10,
		maxIntensity:10,
		fitbounds:true, // or false
		gradient1:gradient
	});
```

### Remove HeatMap

```js
	MapmyIndia.remove({map:map,layer:HeatmapLayer});
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