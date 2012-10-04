{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=canvas/objects/CanvasRenderingContext2D
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example creates a series of squares  that have  different vertical shadow offsets.
|LiveURL=
|Code=
 &lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) {
 	  var ctx {{=}} canvas.getContext("2d");
      // Define the shadow parameters.
      ctx.shadowColor{{=}}"black";
      ctx.shadowBlur {{=}} "5";
      ctx.shadowOffsetX {{=}} "5";
      ctx.shadowOffsetY {{=}} "5";      
        
      // Change the offsetY value.
      ctx.strokeRect(25,25,200,200);
      ctx.shadowOffsetY {{=}} "10";
      ctx.strokeRect(75,75,200,200);
      ctx.shadowOffsetY {{=}} "15";
      ctx.strokeRect(125,125,200,200);
      ctx.shadowOffsetY {{=}} "20";
      ctx.strokeRect(175,175,200,200);  
      ctx.shadowOffsetY {{=}} "25";
      ctx.strokeRect(225,225,200,200);      
      }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"500"&gt; &lt;/canvas&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can use positive or negative values  to control the position of a shadow. If you do not specify the  '''shadowOffsetY'''  property,  the default value is zero.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 7


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}