{{Page_Title|CSS images: url()}}
{{Flags}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|CSS has a variety of different properties that can reference an image file, displaying that file on a web page normally as part of an element's background. This is done using the CSS image syntax, which is <code>url()</code>.}}
{{CSS_Function
|Content===Usage==

Usage is simple — you insert the path to the image you want to include in your page inside the brackets of <code>url()</code>, some for example

<pre>background-image: url(images/my-image.png);</pre>

This will cause <code>my-image.png</code> to be displayed in the background of whatever element or elements the <code>background-image</code> property is applied to. Accepted image formats are:

* .bmp
* .gif
* .png
* .svg (this includes references to in-page SVG elements, for example <code>url(#mySVGElement)</code>)
* data URIs
* .webp

==Browser support notes==

* IE < 9: doesn't support SVG for background-images, or multiple background images, or gradients
* IE6: doesn't support PNG transparency properly; result looks buggy and malformed
* Only Opera and Chrome support .webp

== Properties that accept URL as a value ==

* [[css/properties/background-image|background-image]]
* [[css/properties/border-image|border-image]]
* [[css/properties/content|content]]
* [[css/properties/list-style-image|list-style-image]]
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}