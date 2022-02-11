![MapmyIndia APIs](https://www.mapmyindia.com/api/img/mapmyindia-api.png)
# MapmyIndia Interactive Vector Maps JS SDK for Web !

You can get your api key to be used in this document here: [https://www.mapmyindia.com/api/signup](https://www.mapmyindia.com/api/signup)

## Marker Methods Quick Reference: 

- **setIcon:** Setting the URL of the icon. It replaces the icon URL.

```js
    marker.setIcon("https://apis.mapmyindia.com/map_v3/1.png");
```

- **setDraggable:** To make the marker draggable.

```js
    marker.setDraggable();
```

- **setPosition:** Setting the Position of the marker.

```js
    marker.setPosition({lat:28.454,lng:77.5454});
```

- **setZIndex:** Setting the priority index of the marker.

```js
    marker.setZIndex(1);
```

- **setPopup:**

```js
    marker.setPopup("html",popupOptions(optional));
    ie. marker.setPopup("India",{openPopup:true});
```

- **getPosition:** Returns the compass heading of aerial imagery.

```js
    marker.getPosition();
```

### Example

```js
    marker.setPosition({lat:28.454,lng:77.5454});
    marker.setIcon("https://apis.mapmyindia.com/map_v3/1.png");
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