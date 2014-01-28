{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Retrieves an attribute node by name.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Element
|Example_object_name=element
|Return_value_name=attributeNode
|Javascript_data_type=DOM Node
|Return_value_description=An attribute node.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example uses '''getAttributeNode''' to create an attribute and populate its '''div''' element. Note how the call to [[dom/Element/setAttribute|'''setAttribute''']] changes the [[html/attributes/href|'''href''']] value for the content attribute but not for the DOM attribute.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;title&gt;Attribute Node Example&lt;/title&gt;
  &lt;base href{{=}}"http://msdn.microsoft.com/"&gt;
  &lt;script&gt;
function GetAttrNode() {
  //Retrieve an attribute node and a DOM attribute.
  var o {{=}} document.getElementById("msdn");
  var sDomAttr {{=}} o.href;

  o.setAttribute('href', 'en-us/ie/default.aspx');
  var sContentAttr {{=}} o.getAttributeNode("href");
  var sOutput {{=}} ("Content attribute node value: " + sContentAttr.value + 
              "&lt;br/&gt;DOM attribute value: " + sDomAttr);
              
  document.getElementById("output").innerHTML {{=}} sOutput;
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
   &lt;a id{{=}}"msdn" href{{=}}"en-us/default.aspx"&gt;Microsoft Developer Network&lt;/a&gt;
   &lt;div id{{=}}"output" onmouseover{{=}}"GetAttrNode()"&gt;Point here to display attribute values.&lt;/div&gt;
 &lt;/body&gt;
&lt;/html&gt;
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
|Internet_explorer_version=6
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=6 - 7
|Note=Boolean attributes (such as readonly) return a Boolean value, instead of "readonly".
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=6 - 7
|Note=Calling this method does not correctly populate the [[dom/HTMLElement/value|'''value''']] property of the returned '''attribute''' regardless of whether the [[dom/HTMLElement/specified|'''specified''']] property is set to true or false.
}}
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