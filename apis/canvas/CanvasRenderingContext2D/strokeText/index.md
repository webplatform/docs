{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=text|Data type=BSTR|Description=The text characters to paint on the canvas.|Optional=}}
{{Method Parameter|Name=x|Data type=float|Description=The horizontal coordinate to start painting the text relative to the canvas.|Optional=}}
{{Method Parameter|Name=y|Data type=float|Description=The vertical coordinate of the baseline for the text to start painting, relative to the canvas.|Optional=}}
{{Method Parameter|Name=maxWidth|Data type=VARIANT|Description=The maximum possible text width. If the value is less than [[canvas/properties/width (canvasTextMetrics)|'''width''']], the text  is scaled to fit.|Optional=}}
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
|SecurityError
|The current font is not of the same origin or domain as the document that owns the canvas element.
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
|SecurityError
|The current font is not of the same origin or domain as the document that owns the canvas element.
|}
 


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example paints "Hello World" by  using '''strokeText'''.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt; &lt;html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
 	if (canvas.getContext) {
 	  var ctx {{=}} canvas.getContext("2d");
      ctx.font {{=}} "italic 200 36px/2 Unknown Font, sans-serif";
      ctx.strokeStyle {{=}} "blue";
      var i;
      for (i{{=}}0;i&lt;450; i+{{=}}45){
      ctx.strokeText("Hello World",i,i);  
      }
    }  
}
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw();"&gt;
  &lt;canvas id{{=}}"MyCanvas" width{{=}}"600" height{{=}}"500" border{{=}}"1"&gt; &lt;/canvas&gt;
&lt;/body&gt;
&lt;/html&gt;
}}}}
{{Notes_Section
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