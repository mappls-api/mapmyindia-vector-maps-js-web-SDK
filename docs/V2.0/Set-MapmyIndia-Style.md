![MapmyIndia APIs](https://www.mapmyindia.com/api/img/mapmyindia-api.png)

# [Set MapmyIndiaMaps style](#Set-MapmyIndiaMaps-style)

MapmyIndia offers a range of preset styles to rendering the map. The user has to retrieve a list of styles for a specific account. 
The listing api would help in rendering specific style as well as facilitate the switching of style themes. 

From the below reference code it would become quite clear that user has to specify style names and not URLs to use them. 

A default style is set for all account users to start with. 
To know more about available styles, kindly contact apisupport@mapmyindia.com

**This feature is available from version v2.0**

## [List of Available Styles](#list-of-available-styles)

To get the list of available styles :

**Method:**

MapmyIndia.getStyles();

Click for Live Demo: https://www.mapmyindia.com/api/advanced-maps/WebSDK-LiveDemo/map_style

`MapmyIndiaStyle` contains below parameters:

 1. `description(String)`: Description of the style
 2. `displayName(string)`: Generic Name of style mostly used in MapmyIndia content.
 3. `imageUrl(String)`: Preview Image of style
 4. `name(String)`: Name of style used to change the style.

## [Set MapmyIndia Styles](#Set-MapmyIndia-Styles)


To set the MapmyIndia style refer the code below :

**Method:**

MapmyIndia.setStyles();

For eg:

```
MapmyIndia.setStyle(‘grey-day’);
```

That's all!

For any queries and support, please contact: 

![Email](https://www.google.com/a/cpanel/mapmyindia.co.in/images/logo.gif?service=google_gsuite)
