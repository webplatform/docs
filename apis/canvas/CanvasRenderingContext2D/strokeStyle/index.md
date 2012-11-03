{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The current style for stroking shapes. The style can be a [[canvas/objects/CanvasGradient|CanvasGradient]] object, a [[canvas/objects/CanvasPattern|CanvasPattern]], or a string containing a CSS color.}}
{{API_Object_Property
|Property_applies_to=canvas/objects/CanvasRenderingContext2D
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following  code example uses '''strokeStyle''' to change the colors of three subpaths.
|Code=&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) {
 	  var ctx {{=}} canvas.getContext("2d");
      ctx.beginPath();
      ctx.strokeStyle{{=}}"green";  // Use strokeStyle to set the color.
      ctx.rect (5,5,300,250); 
      ctx.stroke();
      ctx.beginPath();
      ctx.strokeStyle{{=}}"blue";  // Use strokeStyle to change the color.
      ctx.lineWidth {{=}} "5";
      ctx.moveTo(100,100);
      ctx.lineTo(130,100);
      ctx.moveTo(170,100);
      ctx.lineTo(200,100);
      ctx.stroke();
      ctx.beginPath();
      ctx.strokeStyle{{=}}"red";  // Use strokeStyle to change the color.
      ctx.arc(150,125,100,0,Math.PI, false);
      ctx.stroke();
    }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"600"&gt; &lt;/canvas&gt; 
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://www.w3.org/TR/2dcontext/ HTML Canvas 2D Context]

}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
*[[tutorials/canvas/Canvas_tutorial/Applying_styles_and_colors|Applying styles and colors]]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}