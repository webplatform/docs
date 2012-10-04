{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to assign to a variable the '''childNodes''' collection of the '''body''' object.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
var aNodeList {{=}} oBody.childNodes;
&lt;/SCRIPT&gt;
:
&lt;BODY ID{{=}}"oBody"&gt;
&lt;SPAN ID{{=}}"oSpan"&gt;A Span&lt;/SPAN&gt;
&lt;/BODY&gt;
}}
{{Single_Example
|Description=This example shows how to assign to a variable the '''childNodes''' collection of a node created with the [[dom/methods/createElement|'''createElement''']] method.
|LiveURL=
|Code=
var oParentNode {{=}} document.createElement("DIV");
var oNode {{=}} document.createElement("B");
document.body.insertBefore(oParentNode);
oParentNode.insertBefore(oNode);
var aNodeList {{=}} oParentNode.childNodes;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''childNodes''' collection can contain [[dom/HTMLElement|'''HTML Element''']] and [[dom/TextNode|'''TextNode''']] objects.
If you check the '''childNodes''' collection of an element created through standard HTML, you  encounter [[dom/TextNode|'''TextNode''']] objects in unexpected places—in place of line breaks, for example. Alternately, if you create an element using the Document Object Model (DOM), Windows Internet Explorerdoesn't create extraneous '''TextNode''' objects.
In Microsoft Internet Explorer 6, This collection now applies to the [[dom/attributes|'''attribute''']] object.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>About the W3C Document Object Model</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}