![MapmyIndia APIs](https://www.mapmyindia.com/api/img/mapmyindia-api.png)
# MapmyIndia Interactive Vector Maps JS SDK for Web !

You can get your api key to be used in this document here: [https://www.mapmyindia.com/api/signup](https://www.mapmyindia.com/api/signup)


## Raster Source Overlay

### Overlaying on map from a Raster Source

#### raster() Method

**`MapmyIndia.raster()`**

```js
var raster=MapmyIndia.raster({
	map:map,
	tiles:[
		'https://apis.mapmyindia.com/advancedmaps/v1/<key>/bhuvan_imagery/{z}/{x}/{y}.png'
		]
});
```

### Remove Raster Source

```js
MapmyIndia.remove({map:map_object,layer:rastersource_object});
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