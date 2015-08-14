{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Removes an attribute with a given name.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of an [[dom/HTMLElement|'''attribute''']] to remove.
|Optional=No
}}
|Method_applies_to=dom/NamedNodeMap
|Example_object_name=attributes
|Return_value_name=attribute
|Javascript_data_type=DOM Node
|Return_value_description=The removed attribute.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows how to use this method to remove an [[dom/HTMLElement|'''attribute''']] from an element.
|Code=&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
&lt;title&gt;removeNamedItem example&lt;/title&gt;
  &lt;script&gt;
function removeAttrib() {
    var attributes {{=}} document.getElementById("ex").attributes;
    attributes.removeNamedItem("title");
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
 &lt;div onclick{{=}}"removeAttrib();" id{{=}}"ex" title{{=}}"This is a tooltip"&gt;
Click this DIV and the tooltip will be deactivated.&lt;/div&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeNamedItemEx1.htm
}}
}}
{{Notes_Section
|Notes=An '''attribute''' that is removed with this method reverts to the default value of the '''attribute''' when applicable. This method returns a script error if the user attempts to remove a non-existent attribute node.
'''removeNamedItem''' was introduced in Microsoft Internet Explorer 6.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Core
|URL=http://www.w3.org/TR/DOM-Level-3-Core/
|Status=Recommendation
|Relevant_changes=Section 1.4
}}
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NamedNodeMap NamedNodeMap]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}