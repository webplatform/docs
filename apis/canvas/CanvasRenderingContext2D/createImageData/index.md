{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Depending on how it is called, returns either an '''ImageData''' object with the given ''sw, sh'' dimensions or an '''ImageData''' object with the same dimensions as the ''imagedata'' argument. See Notes.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=sw
|Data type=Number
|Description=The width of the new object, in CSS pixels.
|Optional=No
}}{{Method Parameter
|Index=1
|Name=sh
|Data type=Number
|Description=The height of the new object, in CSS pixels.
|Optional=No
}}{{Method Parameter
|Index=2
|Name=imagedata
|Data type=Object
|Description=An '''ImageData''' object of the desired width and height.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=An '''ImageData''' object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example creates an ImageData object, then sets all its data pixels to yellow (at half intensity), then puts the object onto the canvas at a specified position.
|Code=<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var imgdata = ctxt.createImageData(150, 100);
for (var i = 0; i < imgdata.data.length; i += 4) {
    imgdata.data[i+0] = 255;
    imgdata.data[i+1] = 255;
    imgdata.data[i+2] = 0;
    imgdata.data[i+3] = 128;
}
ctxt.putImageData(imgdata, 10, 10);
</script>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=When this method is invoked with two arguments, ''sw'' and ''sh'', it returns an '''ImageData''' object representing a rectangle with a width in CSS pixels equal to the absolute magnitude of ''sw'' and a height in CSS pixels equal to the absolute magnitude of ''sh''. When invoked with a single ''imagedata'' argument, it returns an '''ImageData''' object representing a rectangle with the same dimensions as the '''ImageData''' object passed as the argument. The object returned is filled with transparent black.

This method is never called with all three arguments.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Context
|URL=http://www.w3.org/TR/2dcontext/
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|API, Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0-7.0 (partial)
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}