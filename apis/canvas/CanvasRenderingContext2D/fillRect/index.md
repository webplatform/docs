{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=String
|Description=The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=String
|Description=The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=w
|Data type=String
|Description=The width, in pixels, of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}{{Method Parameter
|Name=h
|Data type=String
|Description=The height, in pixels, of the rectangle in relation to the coordinates of the canvas.
|Optional=No
}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following  code example  fills  rectangles  by using a linear gradient and a solid color.
|Code=&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
    if (canvas.getContext) 
      //get a context       
      var ctx {{=}} canvas.getContext("2d");
      //create a gradient object
      var gradient {{=}} ctx.createLinearGradient(0, 0, canvas.width, 0);
      // Add the colors with fixed stops at 1/4 of the width.
      gradient.addColorStop("0","magenta");
      gradient.addColorStop(".25","blue");
      gradient.addColorStop(".50","green");
      gradient.addColorStop(".75","yellow");
      gradient.addColorStop("1.0","red");      
      // Use the gradient as a fill pattern
      ctx.fillStyle {{=}} gradient;
      ctx.fillRect (0,0,300,250);  
      ctx.fillStyle {{=}} "blue";
      ctx.fillRect(250,300,600,500);
    }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"500"&gt; &lt;/canvas&gt; 
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
If the  ''w'' or ''h'' parameter is  zero, the  '''fillRect''' method does not draw the rectangle.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197019 HTML Canvas 2D Context], Section 8
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
|Manual_sections====Related pages (MSDN)===
*<code>[[canvas/objects/CanvasRenderingContext2D|CanvasRenderingContext2D]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
}