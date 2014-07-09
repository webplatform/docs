{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets a reference to the last child in the childNodes collection of an object. }}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example implements the '''lastChild''' property to obtain a reference to the last child element of an object.
|Code=&lt;body&gt;
&lt;ul id {{=}} "oList"&gt;
&lt;li&gt;List Item 1&lt;/li&gt;
&lt;li&gt;List Item 2&lt;/li&gt;
&lt;li&gt;List Item 3&lt;/li&gt;
&lt;/ul&gt;
&lt;script type{{=}}"text/javascript"&gt;
var olastChild {{=}} oList.lastChild;
&lt;/script&gt;
&lt;body&gt;
}}
}}
{{Notes_Section
|Usage=Used to remove and append nodes to user lists and tables.
|Import_Notes====Syntax===
var last_child = element.lastChild
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 1.2
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Core
|URL=http://www.w3.org/TR/2000/REC-DOM-Level-2-Core-20001113/core.html#ID-61AD09FB
|Status=Recommendation
}}
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.lastChild Node.lastChild]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms533943(v=vs.85).aspx lastChild Property]
|HTML5Rocks_link=
}}