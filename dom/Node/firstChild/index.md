{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets a reference to the first child node in the childNodes collection of the object.

If the node is childless, null is returned.
}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=No
|Javascript_data_type=Element
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following code example implements the '''firstChild''' attribute to get the first child element of an object.
|Code=
&lt;body&gt;
&lt;ul id {{=}}" oList"&gt;
&lt;li&gt;List Item 1&lt;/li&gt;
&lt;li&gt;List Item 2&lt;/li&gt;
&lt;li&gt;List Item 3&lt;/li&gt;
&lt;/ul&gt;
&lt;script type{{=}}"text/javascript"&gt;
var oFirstChild {{=}} oList.firstChild;
&lt;/script&gt;
&lt;/body&gt;
}}{{Single Example
|Description=The following example shows how the firstChild method will include white space nodes #text.
|Code=&lt;p id{{=}}"para-01"&gt;
  &lt;span&gt;First span&lt;/span&gt;
&lt;/p&gt;
&lt;p id{{=}}"p2"&gt;&lt;span&gt;first span, no whitespace&lt;/span&gt;&lt;/p&gt;
&lt;script type{{=}}"text/javascript"&gt;
  var p01 {{=}} document.getElementById('para-01');
  alert(p01.firstChild.nodeName);// #text
  var p2{{=}}document.getElementById('p2');
  alert(p2.firstChild.nodeName);// SPAN
&lt;/script&gt;
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 1.2
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.firstChild Node.firstChild]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms533755(v=vs.85).aspx firstChild Property]
|HTML5Rocks_link=
}}