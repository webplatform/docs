{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=cp1x|Data type=float|Description=The x-coordinate of the Bézier control point.|Optional=}}
{{Method Parameter|Name=cp1y|Data type=float|Description=The y-coordinate of the Bézier control point.|Optional=}}
{{Method Parameter|Name=x|Data type=float|Description=The x-coordinate of the point to add to the current path.|Optional=}}
{{Method Parameter|Name=y|Data type=float|Description=The y-coordinate of the point to add to the current path.|Optional=}}
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
|Description=The following  code example uses '''quadraticCurveTo''' to draw an arc.
|LiveURL=
|Code=
 &lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
    &lt;title&gt;QuadraticCurveTo example&lt;/title&gt;
  &lt;script&gt;
    function beginDemo()
      {
        var canvas {{=}} document.getElementById("demo")
        var ctx {{=}} canvas.getContext('2d');        
        // Draw a straight reference line.
        ctx.beginPath();
        ctx.strokeStyle{{=}}"blue"; 
        ctx.moveTo(100,100);
        ctx.lineTo(300,100);
        ctx.stroke();                
        // Draw a quadratic curve by using the same line coordinates.
        ctx.beginPath();              
        ctx.lineWidth{{=}}"3";
        ctx.strokeStyle{{=}}"black"; 
        ctx.moveTo(100,100);
        ctx.quadraticCurveTo(200,300,300,100);
        ctx.stroke();        
      }
  		&lt;/script&gt;
&lt;/head&gt;
    &lt;body onload{{=}}"beginDemo();"&gt;
	    &lt;canvas id{{=}}"demo" width{{=}}"400" height{{=}}"400"&gt;&lt;/canvas&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
A quadratic Bézier curve  requires  two points. The first  point is a control point  that  is used in the quadratic Bézier calculation and the second  point is the ending point for the curve. The starting point for the curve is the last point in the existing current subpath. If a path does not exist, use the  [[canvas/methods/beginPath|'''beginPath''']] and [[canvas/methods/moveTo|'''moveTo''']]  methods to set a starting point.
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