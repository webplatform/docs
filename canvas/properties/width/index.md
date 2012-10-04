{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLCanvasElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following  code example uses the  '''width''' and [[canvas/properties/height (canvas)|'''height''']]  property to get and set the attributes of a  [[canvas/objects/canvas|'''canvas''']]  element on the document.
|LiveURL=
|Code=
&lt;!DOCTYPE html&gt;
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
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.10


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[canvas/objects/canvas|canvas]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}