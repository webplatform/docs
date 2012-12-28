{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|An opaque object of the canvas API.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples={{Single Example
|Description=The following code example creates a gradient.
|Code=&lt;!DOCTYPE html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) {
 	  var ctx {{=}} canvas.getContext("2d");
      //create a gradient object from the canvas context
      gradient {{=}} ctx.createLinearGradient(0, 0, canvas.width, 0);
  // Add the colors with fixed stops at 1/4 of the width.
      gradient.addColorStop("0","magenta");
      gradient.addColorStop(".25","blue");
      gradient.addColorStop(".50","green");
      gradient.addColorStop(".75","yellow");
      gradient.addColorStop("1.0","red");
      
      // Use the gradient.
      ctx.fillStyle {{=}} gradient;
      ctx.fillRect (0,0,300,250);  
      ctx.fillRect(250,300,600,500);
    }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"500" border{{=}}"1"&gt; &lt;/canvas&gt;
    &lt;button onclick{{=}}"draw()"&gt;Click me&lt;/button&gt;        
&lt;/body&gt;
&lt;/html&gt;
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
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}