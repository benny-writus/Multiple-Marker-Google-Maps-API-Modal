# Marker-infowindow-Modal

# Requirements
Bootstrap 3
Google Maps API KEY

# Steps
Multiple markers in Google maps api with modal for infowindow

The index.html contains code to make Multiple Markers in Google Maps API to have Modal instead of infowindow that comes with the API
 
The Code used is taken from "Maps Javascript API tutorial Section"

https://developers.google.com/maps/documentation/javascript/mysql-to-maps

Add the code in javascript instead of  marker.addListener fucntion

```
google.maps.event.addListener(marker, 'click', (function(marker) {

return function() {

$(".modal-title").text(name);  //the 'name' is a Javascript variable

$(".modal-body").text(address); //the 'address' is a Javascript variable

$("#myModal").modal('show');

}})(marker));```


Add the Html Section inside Body Section
```
<div class="modal fade" id="myModal" role="dialog">
<div class="modal-dialog">
<div class="modal-content">
<div class="modal-header">
<h4 class="modal-title"></h4>
</div>
<div class="modal-body">
</div>
<div class="modal-footer">
<button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
</div>
</div>
</div>
</div>```



