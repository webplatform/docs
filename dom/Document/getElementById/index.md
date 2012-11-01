{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets an element with a specified ID.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=id
|Data type=String
|Description=The ID to match.
|Optional=No
}}
|Method_applies_to=dom/document
|Example_object_name=document
|Return_value_name=element
|Javascript_data_type=DOM Node
|Return_value_description=An element that matches the specified ID. If there are multiple matches, the first is returned.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example uses '''getElementById''' to display the content of the first '''div''' element in a collection with the [[html/attributes/id|'''ID''']] attribute value, <code>div1</code>, when a button is clicked.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;title&gt;"Show First DIV Content"&lt;/title&gt;
  &lt;meta charset{{=}}"utf-8"/&gt;
  &lt;script type{{=}}"text/javascript"&gt;
function getID() {
   // Display the content of the first DIV element in the collection.
   var div {{=}} document.getElementById("div1");
   alert("The content of the first DIV element is " + "\"" + div.innerHTML + "\".");
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
  &lt;div id{{=}}"div1"&gt;Div #1&lt;/div&gt;
  &lt;div id{{=}}"div2"&gt;Div #2&lt;/div&gt;
  &lt;div id{{=}}"div3"&gt;Div #3&lt;/div&gt;
  &lt;input type{{=}}"button" value{{=}}"Show First DIV Content" onclick{{=}}"getID()"&gt; 
 &lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Core
|URL=http://www.w3.org/TR/DOM-Level-2-Core/core.html#ID-getElBId
|Status=Recommendation
|Relevant_changes=Section 1.2. Fundamental Interfaces
}}{{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5 (eariler?)
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=16
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5.5 - 7
|Note=The method also considers results of searches for elements with ID or name attributes that match the the specified value in a case insensitive manner as valid matches.
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>About the W3C Document Object Model</code>
}}
{{Topics|DOM, HTML, XHTML, XML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}