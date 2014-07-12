{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the text content of a node and any child nodes.}}
{{API_Object_Property
|Property_applies_to=dom/Node
|Read_only=No
|Example_object_name=node
|Return_value_name=textContent
|Javascript_data_type=String
|Return_value_description=The text content of a node and its child nodes, if any.
|Example_value_name=newText
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Code=// Given the following HTML fragment:
//   <div id="divA">This is <span>some</span> text</div>

// Get the text content:
var text = document.getElementById("divA").textContent;
// |text| is set to "This is some text".

// Set the text content:
document.getElementById("divA").textContent = "This is some text";
// The HTML for divA is now:
//   <div id="divA">This is some text</div>
}}{{Single Example
|Description=The following example displays the textContent property of a &lt;script&gt; tag.
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;&lt;head&gt;
&lt;meta http-equiv{{=}}"Content-Type" content{{=}}"text/html; charset{{=}}utf-8"&gt;
&lt;script id{{=}}"scrtest" type{{=}}"text/javascript"&gt;
function gettextContent(el){
alert(el.textContent);
}
&lt;/script&gt;
&lt;title&gt;textContent example&lt;/title&gt;
&lt;/head&gt;

&lt;body&gt;
&lt;script type{{=}}"text/javascript"&gt;
gettextContent(document.getElementById('scrtest'));
&lt;/script&gt;



&lt;/body&gt;&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes=textContent returns null if the element is a document, a document type, or a notation. To grab all of the text and CDATA data for the whole document, one could use document.documentElement.textContent.

If the node is a CDATA section, a comment, a processing instruction, or a text node, textContent returns the text inside this node (the nodeValue).

For other node types, textContent returns the concatenation of the textContent attribute value of every child node, excluding comments and processing instruction nodes. This is an empty string if the node has no children.

Setting this property on a node removes all of its children and replaces them with a single text node with the given value.
}}
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
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
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
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and earlier
|Note=Supported a similar functionality using the [[dom/HTMLElement/innerText|innerText]] property.
}}
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Node.textContent Node.textContent]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974773(v=vs.85).aspx textContent Property]
|HTML5Rocks_link=
}}