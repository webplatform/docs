{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example shows how to assign to a variable the '''childNodes''' collection of the '''body''' object.
|Code=&lt;SCRIPT&gt;
var aNodeList {{=}} oBody.childNodes;
&lt;/SCRIPT&gt;
:
&lt;BODY ID{{=}}"oBody"&gt;
&lt;SPAN ID{{=}}"oSpan"&gt;A Span&lt;/SPAN&gt;
&lt;/BODY&gt;
}}{{Single Example
|Description=This example shows how to assign to a variable the '''childNodes''' collection of a node created with the [[dom/Document/createElement|'''createElement''']] method.
|Code=var oParentNode {{=}} document.createElement("DIV");
var oNode {{=}} document.createElement("B");
document.body.insertBefore(oParentNode);
oParentNode.insertBefore(oNode);
var aNodeList {{=}} oParentNode.childNodes;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''childNodes''' collection can contain [[dom/HTMLElement|'''HTML Element''']] and [[dom/TextNode|'''TextNode''']] objects.
If you check the '''childNodes''' collection of an element created through standard HTML, you  encounter [[dom/TextNode|'''TextNode''']] objects in unexpected places—in place of line breaks, for example. Alternately, if you create an element using the Document Object Model (DOM), Windows Internet Explorerdoesn't create extraneous '''TextNode''' objects.

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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}