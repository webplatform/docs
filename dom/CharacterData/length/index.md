{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''length''' property to specify where a [[dom/TextNode|'''TextNode''']] is split by using the [[dom/methods/splitText|'''splitText''']] method.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnChangeValue(){
   var oListItem {{=}} document.createElement("LI");
   oList.appendChild(oListItem);
   var oNode {{=}} oList.firstChild.childNodes(0);
   var oTextNode {{=}} oList.firstChild.childNodes(0);
   var oSplit {{=}} oTextNode.splitText(oTextNode.length/2);
   oListItem.appendChild(oSplit);
}
&lt;/SCRIPT&gt;
&lt;UL ID {{=}} oList onclick {{=}} "fnChangeValue()"&gt;
&lt;LI&gt;Start Here
&lt;/UL&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 1.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/TextNode|TextNode]]</code>
*<code>[[dom/StaticNodeList|StaticNodeList]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}