{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Modifies the transformation matrix of this context.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=String
|Description=The value to add to horizontal (or x) coordinates.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=String
|Description=The value to add to vertical (or y) coordinates.
|Optional=No
}}
|Method_applies_to=canvas/objects/CanvasRenderingContext2D
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following  code example uses  '''translate'''  to create two squares  that are offset by 50 pixels.
|Code=&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
    &lt;title&gt;Canvas Translate example&lt;/title&gt;
    &lt;script&gt;
    function twoSquares()
            {
            var canvas {{=}} document.getElementById("demo")
			var ctx {{=}} canvas.getContext('2d');
            canvas.style.border {{=}} "2px solid";  // Put a border around the canvas.
            ctx.beginPath();
            ctx.lineWidth{{=}}"3";
            ctx.strokeStyle{{=}}"blue";           
            ctx.strokeRect(50,50,150,150);                        
            ctx.translate(50,50);   // Move the square down by 50 pixels.
            ctx.strokeRect(50,50,150,150);
            ctx.stroke();           // Draw it.                      
            }
  		&lt;/script&gt;
&lt;/head&gt;
    &lt;body onload{{=}}"twoSquares();"&gt;
	    &lt;canvas id{{=}}"demo"  width{{=}}"300" height{{=}}"300"&gt;&lt;/canvas&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes=The '''translate''' method  effectively remaps the  (0,0)  origin on a canvas.  You can specify one or both parameters. When  you call a canvas method such as  [[canvas/methods/lineTo|'''lineTo''']], the translate value is added to the respective x-coordinate  and y-coordinate values.  '''translate'''  does not return an error if either value or any derived value is out of the canvas dimensions.
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
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}