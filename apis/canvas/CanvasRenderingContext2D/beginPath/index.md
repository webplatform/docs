{{Page_Title}}
{{Flags
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Empties the list of subpaths in the context's current default path so that it once again has zero subpaths.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/canvas/CanvasRenderingContext2D
|Example_object_name=context
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This is a full example that uses beginPath to create two stroked lines.
|Code=<html>
<head>
    <title>Canvas beginPath example</title>
    <script>
        function beginDemo() {
            var canvas = document.getElementById("demo")
            if (canvas.getContext) {
                var ctx = canvas.getContext('2d');
                ctx.beginPath();
                ctx.lineWidth = "3";
                ctx.strokeStyle = "blue";  // This path is blue.
                ctx.moveTo(0, 0);
                ctx.lineTo(150, 150);
                ctx.lineTo(200, 150);
                ctx.stroke();
                ctx.beginPath();
                ctx.strokeStyle = "red";   // This path is red.
                ctx.moveTo(0, 0);
                ctx.lineTo(50, 150);
                ctx.stroke();           // Draw it.                      
            }
        }
          </script>
</head>
    <body onload="beginDemo();">
        <canvas id="demo" width="300" height="300">This browser or document mode doesn't support canvas</canvas>
  </body>
</html>
|LiveURL=http://code.webplatform.org/gist/5022033/58ee0dfab60f4ee6d22c14881d9708708f45e2b2
}}{{Single Example
|Language=JavaScript
|Description=This snippet shows the basis syntax for beginPath() using the canvas context.
|Code=var ctx = canvas.getContext('2d');
                ctx.beginPath();
}}
}}
{{Notes_Section
|Notes=A path consists of a list of zero or more subpaths. Each subpath is a list of one or more points that are connected by straight or curved lines.  Each subpath also  contains a flag that indicates  whether the subpath is closed. If a subpath is closed, the last point of the subpath is connected to the first point by a straight line. Subpaths  that have  fewer than two points are ignored when the path is painted.
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