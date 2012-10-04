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
|Description=The following  code example shows the anchor point and the effect of each alignment keyword.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
&lt;head&gt;
    &lt;title&gt;TextAlign example&lt;/title&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) {
 	  var ctx {{=}} canvas.getContext("2d");
      // Create a line at the anchor point.
      ctx.strokeStyle{{=}}"red";
      ctx.textAlign {{=}} "center";
      ctx.strokeText("Anchor point",200,60);
      ctx.moveTo(200,60);
      ctx.lineTo(200,210);
      ctx.stroke();
      // Show the demo.
      ctx.strokeStyle{{=}}"blue";
      ctx.font {{=}} "italic 100 24px/2 Unknown Font, sans-serif";    
      ctx.textAlign {{=}} "start";      
      ctx.strokeText("Hello Start",200,100);        
      ctx.textAlign {{=}} "end";      
      ctx.strokeText("Hello End",200,120);                  
      ctx.textAlign {{=}} "left";      
      ctx.strokeText("Hello Left",200,140);
      ctx.textAlign {{=}} "center";     
      ctx.strokeText("Hello center",200,160);              
      ctx.textAlign {{=}} "right";      
      ctx.strokeText("Hello Right",200,180);       
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
The exact alignment depends on whether the direction of '''IHTMLCanvasElement''' is left-to-right (ltr) or right-to-left (rtl). The [[canvas/properties/textBaseline|'''textBaseline''']] value also determines the  anchor point of  the  text.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 11


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