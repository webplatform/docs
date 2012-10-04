{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example uses the  [[canvas/methods/lineTo|'''lineTo''']] and [[canvas/methods/closePath|'''closePath''']]  methods to create a shape and then fills the shape.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
    &lt;title&gt;Canvas fill example&lt;/title&gt;
    &lt;script&gt;
    function fillDemo()
                  {
            var canvas {{=}} document.getElementById("demo")
			var ctx {{=}} canvas.getContext('2d');        
            ctx.beginPath();              
            ctx.lineWidth{{=}}"3";
            ctx.strokeStyle{{=}}"blue";  // This path is blue.
            ctx.fillStyle{{=}}"red";    // The fill is red.
            ctx.moveTo(0,0);
            ctx.lineTo(150,150);
            ctx.lineTo(200,150);
            ctx.closePath();
            ctx.fill();            
            ctx.stroke();           // Draw it.                      
            }
  		&lt;/script&gt;
&lt;/head&gt;
    &lt;body onload{{=}}"fillDemo();"&gt;
	    &lt;canvas id{{=}}"demo" width{{=}}"300" height{{=}}"300"&gt;&lt;/canvas&gt;
  &lt;/body&gt;
&lt;/html&gt; 
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 9


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