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
|Description=The following  code example draws lines with the three  '''lineCap'''  styles  and adds guidelines to  display the additional length  that the  lines add.
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
// Draw some lines with different line caps.
 	  var ctx {{=}} canvas.getContext("2d");
      var lStart {{=}} 50;
      var lEnd {{=}} 200;
      var yStart {{=}} 50;
      ctx.beginPath();
      ctx.lineWidth {{=}} "25";
      ctx.lineCap {{=}} "butt";
      ctx.moveTo (lStart,yStart);
      ctx.lineTo (lEnd,yStart);
      ctx.stroke();
      ctx.beginPath();
      ctx.lineCap {{=}} "round";
      ctx.moveTo (lStart,yStart + 75);
      ctx.lineTo (lEnd,yStart + 75);
      ctx.stroke();
      ctx.beginPath();
      ctx.lineCap {{=}}"square";
      ctx.moveTo (lStart,yStart + 150);
      ctx.lineTo (lEnd,yStart + 150);
      ctx.stroke();      
// Add visualizer guidelines.      
      var x{{=}} lStart + ((lEnd-lStart)/2);
      var capSize {{=}} ctx.lineWidth/2;
      ctx.beginPath();  
      ctx.lineWidth {{=}} "1";
      // Line length guidelines.
      ctx.strokeStyle {{=}} "blue";
      ctx.moveTo(lStart,10);
      ctx.lineTo(lStart,200);
      ctx.moveTo(lEnd,10);
      ctx.lineTo(lEnd,200);
      ctx.stroke();      
      // Total line length guidelines.
      ctx.beginPath();        
      ctx.strokeStyle {{=}} "red";
      ctx.moveTo(lStart-capSize,yStart + 25);
      ctx.lineTo(lStart-capSize, 240);
      ctx.moveTo(lEnd + capSize,yStart + 25);
      ctx.lineTo(lEnd + capSize,240);
      ctx.stroke();      
      // Annotate each line.      
      addText("&lt;- line length -&gt;",x,20,"blue");      
      addText("butt lineCap",x,yStart,"white");
      addText("round lineCap",x,yStart+75,"white");
      addText("square lineCap",x,yStart+ 150,"white");
      addText("&lt;- Total line length -&gt;",x,yStart+ 180,"red");
    }  
function addText(text,x,y,color)
    {
      ctx.save();
      ctx.font {{=}} "400 16px/2 Unknown Font, sans-serif";
      ctx.textBaseline {{=}} "middle";
      var tMetric {{=}} ctx.measureText(text);      
      ctx.fillStyle {{=}} color;
      ctx.fillText(text,(x - tMetric.width/2),y );
      ctx.restore();
    }
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"300" height{{=}}"300"&gt; &lt;/canvas&gt; 
&lt;/body&gt;
&lt;/html&gt;
 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''round''' and '''square''' styles for the  '''lineCap'''  property  make the lines slightly longer. For round ends, the cap diameter equals the  [[canvas/properties/lineWidth|'''lineWidth''']] value. The '''square''' style  adds a rectangle with a width of 1/2  of  '''lineWidth'''. Both the '''round''' and '''square''' styles add approximately 1/2 of the current '''lineWidth'''  value to the end of a line. You should consider this addition if your graphics accuracy is critical.


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