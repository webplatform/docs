{{Page_Title}}
{{Flags
|High-level issues=Move Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Editorial notes={{Editorial/Move_Candidate
| Probably should be under HTML5 canvas element. See [http://www.w3.org/html/wg/drafts/html/master/single-page.html#the-canvas-element HTML5 specification].
}}

}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=contextId
|Data type=any
|Description=The identifier (ID) of the type of canvas to create.
|Optional=No
}}
|Method_applies_to=dom/HTMLCanvasElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''ICanvasRenderingContext2D'''

The context object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following  code example uses '''getContext''' to get a context to use to show a filled rectangle and filled text.
|Code=&lt;!DOCTYPE html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
  if (canvas.getContext) 
    {
 	var ctx {{=}} canvas.getContext("2d");
    ctx.font {{=}} "italic 36px/2 Unknown Font, sans-serif";
    ctx.fillStyle {{=}} "blue";
    ctx.fillRect(0,0,canvas.width,canvas.height);  
    ctx.fillStyle {{=}} "white";
    ctx.fillText ("Hello World",canvas.width/2,canvas.height*.8);
    }  
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw()" bgcolor{{=}}"lightgray" &gt;
      &lt;div&gt;
        &lt;canvas id{{=}}"MyCanvas" width{{=}}"500" height{{=}}"500" &gt; &lt;/canvas&gt;
      &lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''getContext'''  method returns  null if  the ''contextId''  value is not supported.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}197017 The canvas element], Section 4.8.11
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[canvas/objects/canvas|canvas]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}