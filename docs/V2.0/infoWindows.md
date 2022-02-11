![MapmyIndia APIs](https://www.mapmyindia.com/api/img/mapmyindia-api.png)
# MapmyIndia Interactive Vector Maps JS SDK for Web !

You can get your api key to be used in this document here: [https://www.mapmyindia.com/api/signup](https://www.mapmyindia.com/api/signup)


## Info Windows Quick Reference

### Drawing Info Windows

### [InfoWindow Properties](#InfoWindow-Properties)

### *Required*

- **Map Object**
- **Position**

**Example:**

```js
    Var infowindow =new MapmyIndia.InfoWindow({
            map:map,
            position: {"lng":"77.64534","lat":"28.5454"},
        });
```

### *Optional*

- **Content:** It shows the popup content on the Info Window.

```js
    {
		content: "MapmyIndia"
	}
```

- **Class:** It shows the custom class name on the Info Window.

```js
    {
		class: info_class
	}
```

- **Offset:** It sets the exact location of the Info Window.

```js
    {
		offset: [0,10]
	}
```

- **MaxWidth:** It sets the width in pixels of the Info Window.

```js
    {
		maxWidth: 200
	}
```

- **closeButton:** It shows the Close button on the Info Window. By default it is `true`

```js
    {
		closeButton: true
	}
```

**Example**

```js
	infoWindow_object =new MapmyIndia.InfoWindow({
		position: {"lng":"77.64534","lat":"28.5454"},
		class: info_class ( optional ),
		map: map_object,
		content: "MapMyindia",
		offset: [0,10],
		maxWidth: 200
	});
```

### [Remove InfoWindow](#Remove-InfoWindow)

```js
	MapmyIndia.remove({map: map_object, layer: infoWindow_object);
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