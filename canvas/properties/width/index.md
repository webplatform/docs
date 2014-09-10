{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes={{Editorial/Move_Candidate
| Probably should be under HTML5 canvas element. See [http://www.w3.org/html/wg/drafts/html/master/single-page.html#the-canvas-element HTML5 specification].
}}
|Checked_Out=No
|High-level issues=Move Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Width property of canvas element.}}
{{API_Object_Property
|Property_applies_to=dom/HTMLCanvasElement
|Read_only=No
|Example_object_name=
|Return_value_name=
|Javascript_data_type=
|Return_value_description=
|Example_value_name=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=The following  code example uses the  '''width''' and [[canvas/properties/height (canvas)|'''height''']]  property to get and set the attributes of a  [[canvas/objects/canvas|'''canvas''']]  element on the document.
|Code=&lt;!DOCTYPE html&gt;
&lt;head&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function draw()
{
  var canvas {{=}} document.getElementById("MyCanvas");
  if (canvas.getContext) 
    {
 	var ctx {{=}} canvas.getContext("2d");
    ctx.fillStyle {{=}} "blue";
    ctx.fillRect(0,0,canvas.width,canvas.height);  
    }  
}
function change(val)
    {
    var canvas {{=}} document.getElementById("MyCanvas");
    canvas.width {{=}} canvas.width + val;
    canvas.height {{=}} canvas.height + val;
    draw();
    }
  &lt;/script&gt;
&lt;/head&gt;
&lt;body onload{{=}}"draw()" bgcolor{{=}}"lightgray" &gt;
      &lt;div&gt;
      &lt;button onclick{{=}}"change(10)"&gt;Make canvas larger&lt;/button&gt;
      &lt;button onclick{{=}}"change(-10)"&gt;Make canvas smaller&lt;/button&gt;
      &lt;/div&gt;      
      &lt;div&gt;
        &lt;canvas id{{=}}"MyCanvas" width{{=}}"500" height{{=}}"500" &gt; &lt;/canvas&gt;
      &lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.10
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}