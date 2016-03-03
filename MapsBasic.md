## Google Map API
```html
<script src="http://maps.googleapis.com/maps/api/js"></script>
```

## Map Properties
```javascript
function initialize(){
}
```
```javascript
var mapProp = {
  center:new google.maps.LatLng(24.1510393, 120.6637024),
  zoom: 18,
  mapTypeId: google.maps.MapTypeId.ROADMAP
};
```
mapTypeId：
  + ROADMAP (normal, default 2D map)
  + SATELLITE (photographic map)
  + HYBRID (photographic map + roads and city names)
  + TERRAIN (map with mountains, rivers, etc.)


### Create Map
在 initialize() 內，建立地圖物件，將剛剛參數指定進去。
```javascript
var map = new google.maps.Map(document.getElemtentById("googleMap"), mapProp );
```

 
  
## Map Container
```html
<div id="googleMap" style="width:500px;height:380px;"></div>
```

## Add an Event
```javascript
google.map.event.addDomListener(window, 'load', initianlize);
```

## Asynchronously Loading
此方法為將 initialize() 參數轉為 parameter 帶入 url，檔頭不須引用 api


於 callback 後串接 function：
```javascript
function loadScript(){
  var script = document.createElement("script");
  script.src = "http://maps.googleapis.com/maps/api/js?callback=initialize";
  document.body.appendChild(script);
}

window.onload = loadScript;
```

## Map Demo
[CodePen](http://codepen.io/ta7382/pen/ONVvyq?editors=1010 "asd"  target="_blank")
