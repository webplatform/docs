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
|Description=This example uses the '''data''' property to change the value of a text node.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function fnChangeValue(){
   var oNode {{=}} oList.firstChild.childNodes(0);
   var oNewText {{=}} document.createTextNode();
   oNewText.data{{=}}"Create Data";
   oNode.replaceNode(oNewText);
   oNode.data {{=}} "New Node Value";
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
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}