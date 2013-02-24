{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Draws the specified arc.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description=The x-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description=The y-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.
|Optional=No
}}{{Method Parameter
|Name=radius
|Data type=Number
|Description=The radius or distance from the point (x,y) that the arc's path  follows.
|Optional=No
}}{{Method Parameter
|Name=startAngle
|Data type=Number
|Description=The starting angle, in radians, where 0 is at the 3 o'clock position of the arc's circle.
|Optional=No
}}{{Method Parameter
|Name=endAngle
|Data type=Number
|Description=The ending angle, in radians.
|Optional=No
}}{{Method Parameter
|Name=anticlockwise
|Data type=Number
|Description=''true'': The arc is drawn in a counterclockwise direction from start to end.

''false'': The arc  is drawn in a clockwise direction from start to end.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=String
|Return_value_description=Type: '''string'''

This method can return the following value.

{{{!}} class="wikitable"
{{!}}-
!Return code
!Description
{{!}}-
{{!}}IndexSizeError
{{!}}The  specified radius value  is negative.
{{!}}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example shows several different arcs.
|Code=<html>
<head>
      <title>Arc example</title>
  <script type="text/javascript">
      function curves() {
          var canvas = document.getElementById("canvas");
          if (canvas.getContext) {
              var ctx = canvas.getContext("2d");
              for (var i = 0; i < 2; i++)                            // Step through two rows.
              {
                  for (var j = 0; j < 3; j++)                        // Step through three versions.    
                  {
                      ctx.beginPath();
                      var x = 25 + j * 50;               // The x-coordinate.
                      var y = 25 + i * 50;               // The y-coordinate.
                      var radius = 20;                    // The arc radius.
                      var startAngle = 0;                     // The starting point on the circle.
                      var endAngle = Math.PI + (Math.PI * j) / 2; // The end point on the circle.
                      var anticlockwise = i % 2 == 0 ? false : true; // The direction of drawing.
                      ctx.arc(x, y, radius, startAngle, endAngle, anticlockwise); // Create the arc path.
                      ctx.stroke();                               // Display the work.
                  }
              }
          }
      }// Curves      
  </script>
</head>
<body onload="curves();">
  <canvas id="canvas" width="300" height="300">This browser or document mode doesn't support canvas</canvas> 
</body>
</html>
|LiveURL=http://result.dabblet.com/gist/5024626/e8999ad1cd338a601a3d75c139e92d8ee68b2ca3
}}
}}
{{Notes_Section
|Notes=If the ''startAngle'' and ''endAngle''  angles are equal,  the '''arc'''  method  creates a circle. To convert degrees to radians use:
 <code>var radians {{=}} degrees * Math.PI/180</code>
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