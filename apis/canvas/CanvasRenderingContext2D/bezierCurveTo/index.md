{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=cp1x|Data type=float|Description=The x-coordinate of the first Bézier control point.|Optional=}}
{{Method Parameter|Name=cp1y|Data type=float|Description=The y-coordinate of the first Bézier control point.|Optional=}}
{{Method Parameter|Name=cp2x|Data type=float|Description=The x-coordinate of the second Bézier control point.|Optional=}}
{{Method Parameter|Name=cp2y|Data type=float|Description=The y-coordinate of the second Bézier control point.|Optional=}}
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
|Description=The following code example draws a  Bézier  curve between two points. It also draws a reference line to  display  the deviation of the curve over a straight line between the beginning and ending points.
|LiveURL=
|Code=
 &lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
    &lt;title&gt;BezierCurveTo example&lt;/title&gt;
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
        // Draw a Bézier curve by using the same line cooridinates.
        ctx.beginPath();              
        ctx.lineWidth{{=}}"3";
        ctx.strokeStyle{{=}}"black"; 
        ctx.moveTo(100,100);
        ctx.bezierCurveTo(200,200,200,0,300,100);
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
A cubic bezier curve  must include  three points. The first two  points are control points  that are used in the cubic bezier calculation and the last point is the ending point for the curve. The first point on the curve is the last point in the existing current subpath. If a path does not exist, use the  [[canvas/methods/beginPath|'''beginPath''']] and [[canvas/methods/moveTo|'''moveTo''']]  methods to create a starting point.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
*<code>[[canvas/methods/quadraticCurveTo|quadraticCurveTo]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}