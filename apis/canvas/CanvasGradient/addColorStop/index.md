{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Adds a new stop to a gradient. If the offset is less than 0 or greater than 1 then an IndexSizeError exception must be thrown. If the color cannot be parsed as a CSS <color> value, then a SyntaxError exception must be thrown. Otherwise, the gradient must have a new stop placed, at offset offset relative to the whole gradient, and with the color obtained by parsing color as a CSS <color> value.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=offset
|Data type=any
|Description=A floating point value between 0.0 and 1.0 that represents the position between the start and end points in a gradient.
|Optional=No
}}{{Method Parameter
|Name=color
|Data type=any
|Description=A CSS color string to  display  at the position  that the  ''offset'' parameter specifies.
|Optional=No
}}
|Method_applies_to=apis/canvas/CanvasGradient
|Example_object_name=CanvasGradient
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example creates a gradient.
|Code=&lt;!DOCTYPE html&gt;
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
}}
}}
{{Notes_Section
|Notes=You can call the '''addColorStop'''  method  multiple times to  change  a gradient. If  you never call this method  for [[apis/canvas/CanvasGradient|CanvasGradient]],  the gradient is not visible. You need to create at least one color stop to have a visible gradient.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C HTML Canvas 2D Specification
|URL=http://www.w3.org/TR/2012/CR-2dcontext-20121217/
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}