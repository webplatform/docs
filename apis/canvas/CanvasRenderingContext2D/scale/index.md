{{Page_Title}}
{{Flags
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Adds the scaling transformation described by the arguments to the transformation matrix. The ''x'' argument represents the scale factor in the horizontal direction; the ''y'' argument represents the scale factor in the vertical direction. The factors are multiples.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description=The horizontal scaling factor, where 1 equals unity or 100% scale.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=The vertical scaling factor.
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
|Description=This basic example draws two rects, the second scaled 1.5 times
|Code=ctx.fillStyle = "lime";
ctx.fillRect(0,0,100,100);
ctx.scale(1.5, 1.5);	// draws the second rect 2.5 times larger
ctx.fillStyle = "rgba(255,0,0,0.5)";
ctx.fillRect(25,25,100,100);	// note the width & height are 1.5 times bigger than 100 px
}}{{Single Example
|Language=HTML
|Description=This full example draws two rects, the second scaled 1.5 times
|Code=<!DOCTYPE html>
<html>
<head>
  <title>Canvas Example</title>
  <script>
    function draw() {
      var canvas = document.getElementById("MyCanvas");
      if (canvas.getContext) {  // check for support
        var ctx = canvas.getContext("2d"); 
        
        ctx.fillStyle = "lime";
        ctx.fillRect(0,0,100,100);
        ctx.scale(1.5, 1.5);	// draws the second rect 2.5 times larger
        ctx.fillStyle = "rgba(255,0,0,0.5)";
        ctx.fillRect(25,25,100,100);	// note the width & height are 1.5 times bigger than 100 px
        
      }
    }        
  </script>
</head>
<body onload="draw();">
  <canvas id="MyCanvas" width="600" height="500">This browser or document mode doesn't support canvas</canvas>
</body>
</html>
}}
}}
{{Notes_Section
|Notes=When  you create a [[apis/canvas/CanvasRenderingContext2D|CanvasRenderingContext2D]] object, it has a transformation matrix that identifies the current state.  The ''scale'' method  modifies the transformation by multiplying the matrix by the  specified  factor. 

For example, <code>context.scale(1,.5)</code> halves the vertical (or y-axis) values  that are used in context and  leaves  the horizontal (or x-axis) values the same. Similarly, <code>context.scale(2,2)</code>  doubles  the size of the graphics.
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