{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Modifies the transformation matrix of this context by adding the scaling transformation described by the arguments to the transformation matrix. The arguments represent the scale factors in the horizontal (''x'') and vertical (''y'') directions. The factors are multiples.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=String
|Description=The value to add to horizontal (or x) coordinates.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=String
|Description=The value to add to vertical (or y) coordinates.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This short example translates the drawing matrixes by 50px to the right and 50px to the bottom
|Code=ctx.fillStyle = "lime";
ctx.fillRect(0,0,100,100);
ctx.translate(50,50);	// move the drawing coordinates by 50 px
ctx.fillStyle = "rgba(255,0,0,0.5)";
ctx.fillRect(0,0,100,100);	// note the x/y start positions at 0 (is actually 50)
}}{{Single Example
|Language=HTML
|Description=Full example that draws two rects, the second one 50x50px translated.
|Code=<!DOCTYPE html>
<html>
<head>
  <title>Canvas Textmetrics</title>
  <script>
    function draw() {
      var canvas = document.getElementById("MyCanvas");
      if (canvas.getContext) {  // check for support
        var ctx = canvas.getContext("2d"); 
        
        ctx.fillStyle = "lime";
        ctx.fillRect(0,0,100,100);
        ctx.translate(50,50);	// move the drawing coordinates by 50 px
        ctx.fillStyle = "rgba(255,0,0,0.5)";
        ctx.fillRect(0,0,100,100);	// note the x/y start positions at 0 (is actually 50)
        
      }
    }        
  </script>
</head>
<body onload="draw();">
  <canvas id="MyCanvas" width="400" height="400">This browser or document mode doesn't support canvas</canvas>
</body>
</html>
}}
}}
{{Notes_Section
|Notes=The ''translate'' method  effectively remaps the (0,0) origin on a canvas. You can specify one or both parameters. When  you call a canvas method such as  [[apis/canvas/CanvasRenderingContext2D/lineTo|lineTo]], the translate value is added to the respective x-coordinate  and y-coordinate values. ''translate'' does not return an error if either value or any derived value is out of the canvas dimensions.
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
{{Topics|API, Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}