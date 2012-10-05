{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=offset|Data type=float|Description=A floating point value between 0.0 and 1.0 that represents the position between the start and end points in a gradient.|Optional=}}
{{Method Parameter|Name=color|Data type=BSTR|Description=A CSS color string to  display  at the position  that the  ''offset'' parameter specifies.|Optional=}}
|Method_applies_to=canvas/objects/CanvasGradient
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example creates a gradient.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
&lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) {
 	  var ctx {{=}} canvas.getContext("2d");
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
}}}}
{{Notes_Section
|Notes=
===Remarks===
You can call the '''addColorStop'''  method  multiple times to  change  a gradient. If  you never call this method  for [[canvas/objects/CanvasGradient|'''CanvasGradient''']],  the gradient is not visible. You need to create at least one color stop to have a visible gradient.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/CanvasGradient|CanvasGradient]]</code>
*<code>Reference</code>
*<code>[[canvas/methods/createRadialGradient|createRadialGradient]]</code>
*<code>[[canvas/methods/createLinearGradient|createLinearGradient]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}