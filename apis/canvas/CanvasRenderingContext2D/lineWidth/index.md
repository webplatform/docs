{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The current line width, in pixels.}}
{{API_Object_Property
|Property_applies_to=canvas/objects/CanvasRenderingContext2D
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example draws a series of lines by using increasing values for the '''lineWidth''' property.
|Code=&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) 
    {
 	  var ctx {{=}} canvas.getContext("2d");
      var lStart {{=}} 0;
      var lEnd {{=}} 200;
      var yStart {{=}} 5;           
      for(i{{=}}1;i&lt;16;i++)
      {
        ctx.lineWidth {{=}} i;
        ctx.beginPath();
        yStart {{=}} yStart + (i*2) + ctx.lineWidth;            
        ctx.moveTo (lStart,yStart);      
        ctx.lineTo (lEnd,yStart);
        ctx.stroke();   
        ctx.textBaseline {{=}} "middle";
        ctx.fillText(ctx.lineWidth,lEnd + 10,yStart);
      }
    }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"300" height{{=}}"600"&gt; &lt;/canvas&gt; 
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