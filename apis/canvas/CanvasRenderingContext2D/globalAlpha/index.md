{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|An alpha value that is applied to shapes and images before they are composited onto the canvas.}}
{{API_Object_Property
|Property_applies_to=apis/canvas/CanvasRenderingContext2D
|Read_only=No
|Example_object_name=CanvasRenderingContext2D
|Javascript_data_type=Number
|Return_value_description=Default is 1.0.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example draws a semi-transparent white circle on a green background
|Code=function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  // draw background
  ctx.fillStyle = '#FD0';
  ctx.fillRect(0,0,150,150)

  //set transparency value
  ctx.globalAlpha = 0.2;

  //Draw a semi transparent circle
  ctx.beginPath();
  ctx.arc(75,75,50,0,Math.PI*2,true);
  ctx.fill();
}
}}
}}
{{Notes_Section
|Notes=If you set the ''globalAlpha'' property to a value outside the range (including infinity or not a number (NaN)), the previous value is preserved.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Specification
|URL=http://www.w3.org/TR/2012/CR-2dcontext-20121217/
|Status=W3C Candidate Recommendation
}}
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
{{See_Also_Section}}
{{Topics|Canvas}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/samples/canvas-tutorial/4_3_canvas_globalalpha.html
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}