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
|Description=The following code  example uses  the '''beginPath''' method to paint two paths  by using  different colors.
|LiveURL=
|Code=
 &lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
    &lt;title&gt;Canvas beginePath example&lt;/title&gt;
    &lt;script&gt;
    function beginDemo()
                  {
            var canvas {{=}} document.getElementById("demo")
            var ctx {{=}} canvas.getContext('2d');        
            ctx.beginPath();              
            ctx.lineWidth{{=}}"3";
            ctx.strokeStyle{{=}}"blue";  // This path is blue.
            ctx.moveTo(0,0);
            ctx.lineTo(150,150);
            ctx.lineTo(200,150);
            ctx.stroke();
            ctx.beginPath();
            ctx.strokeStyle{{=}}"red";   // This path is red.
            ctx.moveTo(0,0);
            ctx.lineTo(50,150);            
            ctx.stroke();           // Draw it.                      
            }
  		&lt;/script&gt;
&lt;/head&gt;
    &lt;body onload{{=}}"beginDemo();"&gt;
	    &lt;canvas id{{=}}"demo" width{{=}}"300" height{{=}}"300"&gt;&lt;/canvas&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
A path consists of a list of zero or more subpaths. Each subpath is a list of one or more points that are connected by straight or curved lines.  Each subpath also  contains a flag that indicates  whether the subpath is closed. If a subpath is closed, the last point of the subpath is connected to the first point by a straight line. Subpaths  that have  fewer than two points are ignored when the path is painted.
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