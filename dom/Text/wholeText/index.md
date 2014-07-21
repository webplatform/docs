{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves the immediate text child nodes of the parent node, that are adjacent to the text node.}}
{{API_Object_Property
|Property_applies_to=dom/TextNode
|Read_only=Yes
|Example_object_name=textNode
|Return_value_name=text
|Javascript_data_type=String
|Return_value_description=The text of the node and its adjacent text nodes.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;body&gt;
&lt;p id="p"&gt;this is a text node that also has &lt;strong id="s"&gt;strong&lt;/strong&gt elements.&lt;/p&gt;
&lt;script type{{=}}"text/javascript"&gt;
alert(document.getElementById('p').firstChild.wholeText);
// displays 'this is a text node that also has' in an alert box.
&lt;/script&gt;
&lt;/body&gt;

}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}
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
|Internet_explorer_version=9
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Text.wholeText Text.wholeText]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974769(v=vs.85).aspx wholeText Property]
|HTML5Rocks_link=
}}