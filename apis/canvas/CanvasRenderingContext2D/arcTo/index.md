{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Check to be sure there's a subpath for (x1, y1). Then, the behavior depends on the arguments and the last point in the subpath. See Notes.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x1
|Data type=Number
|Description=The x-coordinate for the first tangent that intersects with the current path point.
|Optional=No
}}{{Method Parameter
|Name=y1
|Data type=Number
|Description=The y-coordinate for the first tangent that intersects with the current point.
|Optional=No
}}{{Method Parameter
|Name=x2
|Data type=Number
|Description=The x-coordinate for the second tangent that intersects with  the ''x1'' and ''y1'' points.
|Optional=No
}}{{Method Parameter
|Name=y2
|Data type=Number
|Description=The y-coordinate for the second tangent that intersects with  the ''x1'' and ''y1'' points.
|Optional=No
}}{{Method Parameter
|Name=radius
|Data type=Number
|Description=The radius of the arc to create.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example creates an arc 
|Code=<html>
  <head>
    <title>ArcTo example</title>
  </head>

    <script type="text/javascript">
      function draw(){
        var canvas = document.getElementById("myCanvas");
        if (canvas.getContext) {
            var ctx = canvas.getContext("2d");
            // Draw the imaginary tangents in blue.
            ctx.beginPath();
            ctx.lineWidth = "3";
            ctx.strokeStyle = "blue";
            ctx.moveTo(80, 100);
            ctx.lineTo(240, 100);
            ctx.moveTo(200, 60);
            ctx.lineTo(200, 220);
            ctx.stroke();           // Draw it.

            // Create two lines that have a connecting arc that could be used as a start to a rounded rectangle.
            ctx.beginPath();
            ctx.strokeStyle = "black";
            ctx.lineWidth = "5";
            ctx.moveTo(120, 100);   // Create a starting point.
            ctx.lineTo(180, 100);   // Draw a horizontal line. 
            ctx.arcTo(200, 100, 200, 120, 20); // Create an arc.
            ctx.lineTo(200, 180);    // Continue with a vertical line of the rectangle.    
            ctx.stroke();           // Draw it.           
            // Use the translate method to move the second example down. 
            ctx.translate(0, 220);   // Move all y-coordinates down 220 pixels to see more clearly.
            // Draw the imaginary tangents in blue.            
            ctx.beginPath();
            ctx.strokeStyle = "blue";
            ctx.lineWidth = "3";
            ctx.moveTo(200, 60);
            ctx.lineTo(200, 220);
            ctx.moveTo(220, 80);
            ctx.lineTo(120, 180);
            ctx.stroke();
            // Create a line, move the last path point to a point below, and then create an arc.
            ctx.beginPath();
            ctx.strokeStyle = "black";
            ctx.lineWidth = "5";
            ctx.moveTo(120, 100);   // Same starting point as above.
            ctx.lineTo(180, 100);   // Same horizontal line as above.
            ctx.moveTo(180, 120);    // Move the last path point down 20 pixels.
            ctx.arcTo(200, 100, 200, 120, 20); // Create an arc.
            ctx.lineTo(200, 180);    // Continue with a vertical line of the rectangle.                                                   
            ctx.stroke();
        }
        }
          </script>
  <body onload="draw();">
    <canvas id="myCanvas" width="300" height="600">This browser or document mode doesn't support canvas</canvas>

  </body>
</html>
}}
}}
{{Notes_Section
|Notes=The '''arcTo'''  method creates an arc of ''radius'' radius between two tangents. The first tangent is defined by an imaginary line that is drawn through the last point in a path and the point ''(x1, y1)''. The second tangent is defined by an imaginary line that is drawn through the point ''(x1, y1)'' and the point ''(x2, y2)''.

The arc is drawn between the two tangents using ''radius'' as the radius. '''arcTo''' will draw a straight line from the last point of the path to the start of the arc which lies on the tangent that contains the last point on the path and ''x1'' and ''y1''.
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
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}