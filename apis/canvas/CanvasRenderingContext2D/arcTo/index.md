{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=x1|Data type=float|Description=The x-coordinate for the first tangent that intersects with the current path point.|Optional=}}
{{Method Parameter|Name=y1|Data type=float|Description=The y-coordinate for the first tangent that intersects with the current point.|Optional=}}
{{Method Parameter|Name=x2|Data type=float|Description=The x-coordinate for the second tangent that intersects with  the ''x1'' and ''y1'' points.|Optional=}}
{{Method Parameter|Name=y2|Data type=float|Description=The y-coordinate for the second tangent that intersects with  the ''x1'' and ''y1'' points.|Optional=}}
{{Method Parameter|Name=radius|Data type=float|Description=The radius of the arc to create.|Optional=}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|IndexSizeError
|The radius given is negative.
|}
 

Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|IndexSizeError
|The radius given is negative.
|}
 


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example shows how  '''arcTo'''  creates two different arcs of the same radius based on the angle of the tangents. The difference  between the arcs is the position of the last path point. For illustrative purposes, the  example uses the [[canvas/methods/translate|'''translate''']] method  to move the second  arc  down on the screen while preserving the same basic coordinate values.

The second arc has  the same radius as the first arc.  But because  [[canvas/methods/moveTo|'''moveTo''']] moves the tangential lines, the arc  appears in a different position.

Because  the radius is a fixed value,  '''arcTo'''  calculates the tangential lines and moves the arc to a position where it fits.
|LiveURL=Both examples include  blue lines  to show the tangential lines  that '''arcTo''' uses.
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;ArcTo example&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;canvas id{{=}}"foo" width{{=}}"300" height{{=}}"600"&gt;&lt;/canvas&gt;
    &lt;script&gt;
			var ctx {{=}} document.getElementById('foo').getContext('2d');
// Draw the imaginary tangents in blue.
            ctx.beginPath();
            ctx.lineWidth{{=}}"3";
            ctx.strokeStyle{{=}}"blue";
            ctx.moveTo(80,100);
            ctx.lineTo(240,100);
            ctx.moveTo(200,60);
            ctx.lineTo(200,220);
            ctx.stroke();           // Draw it.
            
// Create two lines that have a connecting arc that could be used as a start to a rounded rectangle.
			ctx.beginPath();     
            ctx.strokeStyle{{=}}"black";            
            ctx.lineWidth {{=}} "5";
            ctx.moveTo(120, 100);   // Create a starting point.
            ctx.lineTo(180, 100);   // Draw a horizontal line. 
            ctx.arcTo(200, 100, 200, 120, 20); // Create an arc.
            ctx.lineTo(200,180);    // Continue with a vertical line of the rectangle.    
            ctx.stroke();           // Draw it.           
// Use the translate method to move the second example down. 
            ctx.translate(0,220);   // Move all y-coordinates down 220 pixels to see more clearly.
   // Draw the imaginary tangents in blue.            
            ctx.beginPath();
            ctx.strokeStyle{{=}}"blue";
            ctx.lineWidth{{=}}"3";
            ctx.moveTo(200,60);
            ctx.lineTo(200,220);            
            ctx.moveTo(220,80);
            ctx.lineTo(120,180);
			ctx.stroke();     
// Create a line, move the last path point to a point below, and then create an arc.
   			ctx.beginPath();        
            ctx.strokeStyle{{=}}"black";
            ctx.lineWidth {{=}} "5";                        
            ctx.moveTo(120, 100);   // Same starting point as above.
            ctx.lineTo(180, 100);   // Same horizontal line as above.
            ctx.moveTo(180,120);    // Move the last path point down 20 pixels.
            ctx.arcTo(200, 100, 200, 120, 20); // Create an arc.
            ctx.lineTo(200,180);    // Continue with a vertical line of the rectangle.                			                       
            ctx.stroke();                                  
  		&lt;/script&gt;
  &lt;/body&gt;
&lt;/html&gt;
 
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''arcTo'''  method creates an arc of ''radius'' radius between two tangents. The first tangent is defined by an imaginary line  that is drawn through the last point in a path and the point (''x1'', ''y1''). The second tangent is defined by an imaginary line  that is drawn through the point (''x1'', ''y1'') and the point (''x2'', ''y2'').
The arc is drawn between the two tangents using ''radius'' as the radius. ArcTo will draw a straight line from the last point of the path to the start of the arc which lies on the tangent that contains the last point on the path and ''x1'' and ''y1''.
When  '''arcTo'''  draws an arc, it tries to fit the arc  between the two tangents. The following illustration  shows two graphics. Both graphics create a path, and both draw horizontal and vertical lines and use the same parameters for '''arcTo'''.  However,  the second  graphic  moves the last point on the path down by 20 pixels,  which  changes  the angle between the two tangents. In the first graphic, the values  make  the arc complete a  rounded corner.

In the second example, because the angle of the intersecting tangents is narrower, arcTo needs to move the fixed radius arc to a point where it fits.

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