Supplying a CSS ''fallback property'' is a common technique	to ensure
cross-browser compatibility. In	the example below, the first
[[css/properties/background-image|'''background-image''']] specifies an
image file, which all browsers are able	to render. The additional ones
after that specify the more recent
[[css/functions/linear-gradient|'''linear-gradient()''']] function,
which not all browsers support.	The browser uses those values only if
it is able to interpret them,	otherwise reverting to the image file
value as a fallback.

 div {
     background-image: url(img/gradient.png);
     background-image: -webkit-linear-gradient(to bottom, #dddddd, #aaaaaa);
     background-image: -moz-linear-gradient(to bottom, #dddddd, #aaaaaa);
     background-image: linear-gradient(to bottom, #dddddd, #aaaaaa);
 }

Note here that you can use this fallback technique to apply	a mix of
standardized or vendor-prefixed properties, whichever works.