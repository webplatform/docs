{{Page_Title}}
{{Flags}}
{{Summary_Section}}
{{Tutorial
|Content=The SVG image element allows for raster images to be rendered within an SVG object.
 
In this basic example, a .jpg image will be rendered inside an SVG object:
 
<pre>&lt;?xml version="1.0" standalone="no"?&gt;
&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;
&lt;svg width="5cm" height="4cm" version="1.1"
     xmlns="http://www.w3.org/2000/svg" xmlns:xlink= "http://www.w3.org/1999/xlink"&gt;
	&lt;image xlink:href="firefox.jpg" x="0" y="0" height="50px" width="50px"/&gt;
&lt;/svg&gt;</pre>
 
There are some important things to take note of (referenced from the [[W3 specs]])
 
* If you do not set the x or y attributes, they will be set to 0
* If you do not set the height or width attributes, they will be set to 0
* Having a height or width attribute of 0 will disable rendering of the image
 
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/SVG/Tutorial/SVG_Image_Tag
|MSDN_link=
|HTML5Rocks_link=
}}