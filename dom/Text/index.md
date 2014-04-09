{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Represents a section of text content (character data) within the document.  It is not an element and cannot contain any child elements.}}
{{API_Object
|Subclass_of=dom/CharacterData, dom/Node, dom/EventTarget
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''TextNode''' object to change the text of an '''li''' object.
|Code=&lt;script&gt;
function fnChangeText(){
   var oTextNode {{=}} document.createTextNode("New List Item 1");
   var oReplaceNode {{=}} oItem1.firstChild.replaceNode(oTextNode);
}
&lt;/script&gt;

&lt;ul onclick {{=}} "fnChangeText()"&gt;
&lt;li id {{=}} "oItem1"&gt;List Item 1&lt;/li&gt;
&lt;/ul&gt;
}}
}}
{{Notes_Section
|Notes=Use the [[dom/Document/createTextNode|'''createTextNode''']] method to create a '''TextNode''' object. After you create the '''TextNode''', you can add to it using the [[dom/Node/appendChild|'''appendChild''']] or [[dom/Node/insertBefore|'''insertBefore''']] methods.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
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