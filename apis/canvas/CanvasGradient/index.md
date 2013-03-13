{{Page_Title}}
{{Flags
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|An opaque object of the canvas API.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following code example creates a gradient.
|Code=<!DOCTYPE html>
<html>
<head>
  <title>Canvas gradient test</title>
  <script>
    function draw() {
      var canvas = document.getElementById("MyCanvas");
      if (canvas.getContext) {  // check for support
        var ctx = canvas.getContext("2d"); 

        //create a gradient object from the canvas context
        gradient = ctx.createLinearGradient(0, 0, canvas.width, 0);

        //Add the colors with fixed stops at 1/4 of the width.
        gradient.addColorStop("0", "magenta");
        gradient.addColorStop(".25", "blue");
        gradient.addColorStop(".50", "green");
        gradient.addColorStop(".75", "yellow");
        gradient.addColorStop("1.0", "red");

        //Use the gradient.
        ctx.fillStyle = gradient;
        ctx.fillRect(0, 0, 300, 250);
        ctx.fillRect(250, 300, 600, 500);
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
|Notes=You can create a linear or radial  '''CanvasGradient'''  object  by using  the '''createLinearGradient''' or '''createRadialGradient''' method. A '''CanvasGradient'''  object  must  have at least one '''color stop''' or the gradient is not  visible.
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