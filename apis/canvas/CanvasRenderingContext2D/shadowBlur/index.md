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
|Description=The following  code example creates a series of squares  that have  different degrees of shadow blur.
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
      ctx.lineWidth {{=}} "3";
      ctx.strokeStyle {{=}} "blue";
      // Define the shadow parameters.
      ctx.shadowColor{{=}}"black";
      ctx.shadowOffsetX {{=}} "10";
      ctx.shadowOffsetY {{=}} "10";      
        
      // Change the blur value.
      ctx.shadowBlur {{=}} "0";
      ctx.strokeRect(25,25,200,200);
      ctx.shadowBlur {{=}} "5";
      ctx.strokeRect(100,100,200,200);
      ctx.shadowBlur {{=}} "10";
      ctx.strokeRect(175,175,200,200);
      ctx.shadowBlur {{=}} "15";
      ctx.strokeRect(250,250,200,200);  
      ctx.shadowBlur {{=}} "20";
      ctx.strokeRect(325,325,200,200);      
      }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"600"&gt; &lt;/canvas&gt;
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
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