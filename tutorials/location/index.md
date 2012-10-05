{{Page_Title}}
{{Flags}}
{{Byline}}
{{Summary_Section|Geolocation lets you identify a user's location by returning their latitude and longitude. Applications can use this to offer localized experiences such as driving directions, nearby points of interest, local deals, etc. In the past few years, smartphones with dedicated GPS chips have exploded in popularity.}}
{{Tutorial
|Content=Devices base location on a number of things, including

* The user's internet access point or Wi-Fi connection
* The user's phone operator's cell-tower locations
* An Embedded GPS chip in the user's phone

== Detecting Support ==

Geolocation is supported by all modern browsers, including Chrome 5.0+, Firefox 3.5+, IE 9.0+, Opera 10.6+, Safari 5.0+, and smartphone platforms including iPhone 3.0+, Android 2.0+, Windows Mobile 7. For up-to-date compatibility support, check out [http://www.caniuse.com/#search=geolocation CanIUse.com].

You can use the [http://www.modernizr.com/ Modernizr JavaScript library] to detect support for the geolocation API. For example,

 if (Modernizr.geolocation) {
   // geolocation is supported
 } else {
   // no  geolocation support available
 }

== Location Functions ==

Geolocation functions are exposed under the <code>geolocation</code> property of the global navigator object.

 navigator.geolocation.getCurrentPosition(callback_function, error_handler, PositionOptions_interface_object)

This will asynchronously fetch and pass the user's current location to the <code>callback_function</code>. The location is only provided via callback to the callback function. If user has not yet authorized your app, a permission info bar/dialog will be rendered to the user.  Here's what it looks like:
 

=== Success callback function ===

When the user's location is available, your callback function will receive a bundle of information.  It's passed <code>position</code>, with two properties including <code>coords</code> and <code>timestamp</code>.

<table>
  <tr>
   <th> Property </th>
   <th> Returned </th>
   <th> Type </th>
   <th> Description </th>
   <th> Example data </th>
  </tr>
  <tr>
    <td> coords.latitude </td>
    <td> Always </td>
    <td> double </td>
    <td> decimal degrees </td>
    <td> 37.774929 </td>
  </tr>
  <tr>
    <td> coords.longitude </td>
    <td> Always </td>
    <td> double </td>
    <td> decimal degrees </td>
    <td> -122.419415 </td>
  </tr>
  <tr>
    <td> coords.accuracy </td>
    <td> Always </td>
    <td> double </td>
    <td> meters </td>
    <td> 50 </td>
  </tr>
  <tr>
    <td> coords.altitude </td>
    <td> Optional </td>
    <td> double or null </td>
    <td> meters </td>
    <td> 150 </td>
  </tr>
  <tr>
    <td> coords.altitudeAccuracy </td>
    <td> Optional </td>
    <td> double or null </td>
    <td> meters </td>
    <td> 8 </td>
  </tr>
  <tr>
    <td> coords.heading </td>
    <td> Optional </td>
    <td> double or null </td>
    <td> degrees, calculated based on previous position. </td>
    <td> 20 </td>
  </tr>
  <tr>
    <td> coords.speed </td>
    <td> Optional </td>
    <td> double or null </td>
    <td> meters/second, calculated based on previous position. </td>
    <td> 10 </td>
  </tr>
  <tr>
    <td> timestamp </td>
    <td> Optional </td>
    <td> DOMTimeStamp </td>
    <td> bound to the <code>Date</code> type </td>
    <td> 1314300437317 </td>
  </tr>
</table>

=== Error callback function ===

If there is an error while fetching location or user denied permission to your app, the <code>error_handler</code> callback function is called with the <code>PositionError</code> object with following properties.

<table>
  <tr>
 	<th> Property </th>
    <th> Type </th>
    <th> Description </th>
  </tr>
  <tr>
    <td> code </td>
    <td> short </td>
    <td> enumerated value: <code>error.PERMISSION_DENIED</code> (1), <code>error.POSITION_UNAVAILABLE</code> (2), <code>error.TIMEOUT</code> (3), or <code>error.UNKNOWN_ERROR</code> (0) </td>
  </tr>
  <tr>
    <td> message </td>
    <td> DOMString </td>
    <td> not to be presented to the end user. </td>
  </tr>
</table>

=== Control how the location is fetched ===

The optional parameter, <code>PositionOptions_interface_object</code>, provides more control over how location is fetched, timeout or cached location via the following three optional properties.

<table>
  <tr>
 	<th> Property </th>
    <th> Type </th>
    <th> Default </th>
    <th> Description </th>
  </tr>
  <tr>
    <td> enableHighAccuracy </td>
    <td> boolean </td>
    <td> false </td>
    <td> true will seek exact location if device supports it, else coarse location. </td>
  </tr>
  <tr>
    <td> timeout </td>
    <td> long </td>
    <td> none </td>
    <td> the time in milliseconds before the request should time out. Note that this is calculated after user has allowed sharing location.</td>
  </tr>
  <tr>
    <td> maximumAge </td>
    <td> long </td>
    <td> 0 </td>
    <td> in milliseconds. If provided, function returns cached location if available in the [(current - maximumAge) to current] time window</td>
  </tr>
</table>

== Monitoring Location ==

This function is exactly like the <code>getCurrentPosition</code> function except that the callback function will be automatically called every time user's location changes.  It's useful in a service like turn-by-turn direction. The interval is optimally defined by the browser and can't be changed.

 int navigator.geolocation.watchPosition(callback_function, error_handler, PositionOptions_interface_object)

Unlike <code>getCurrentPosition</code>, this function returns an integer value which can be used to cancel the watch process and stop invoking any callbacks by calling the <code>clearWatch</code> function.  This is how you call the <code>clearWatch</code> function:

 navigator.geolocation.clearWatch(int watch_number)

== Additional Resources ==

* [http://html5demos.com/geo HTML5 Geolocation Demo]
* [http://diveintohtml5.info/geolocation.html Dive Into HTML5: You are here (and so is everybody else)]
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Geolocation, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=Facebook HTML5 Resource Center
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}