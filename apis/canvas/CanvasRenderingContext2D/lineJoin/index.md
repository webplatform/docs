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
|Description=The following  code example draws three sets of adjoining lines by using the three styles of the '''lineJoin''' property.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) 
    {
// Draw some lines with different line joins.
 	  var ctx {{=}} canvas.getContext("2d");
      var lStart {{=}} 50;
      var lEnd {{=}} 200;
      var yStart {{=}} 50;      
      ctx.beginPath();
      ctx.lineWidth {{=}} "25";
// Use a bevel corner.
      ctx.lineJoin {{=}} "bevel";
      ctx.moveTo (lStart,yStart);
      ctx.lineTo (lEnd,yStart);
      ctx.lineTo (lEnd,yStart+200);      
      ctx.stroke();
// Use a round corner.             
      ctx.beginPath();
      ctx.lineJoin {{=}} "round";
      ctx.moveTo (lStart+ 200 ,yStart);
      ctx.lineTo (lEnd + 200 , yStart);
      ctx.lineTo (lEnd +200 ,yStart + 200);
      ctx.stroke();
// Use a miter.      
      ctx.beginPath();
      ctx.lineJoin {{=}}"miter";
      ctx.moveTo (lStart + 400,yStart);
      ctx.lineTo (lEnd+ 400,yStart);
      ctx.lineTo (lEnd+ 400 ,yStart + 200);      
      ctx.stroke();      
// Annotate each corner.       
      addText("bevel",lStart +50 ,yStart+50,"blue");
      addText("round",lStart+250 ,yStart+50,"blue");
      addText("miter",lStart+450 ,yStart+50,"blue");
    }  
function addText(text,x,y,color)
    {
      ctx.save();
      ctx.font {{=}} "400 16px/2 Unknown Font, sans-serif";
      ctx.fillStyle {{=}} color;
      ctx.fillText(text,x,y );
      ctx.restore();
    }
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"800" height{{=}}"300"&gt; &lt;/canvas&gt; 
&lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''miter'''  option is affected by the [[canvas/properties/miterLimit|'''miterLimit''']] property.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 6


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