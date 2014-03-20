{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Gets an attribute with a given name from an element.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=name
|Data type=String
|Description=The name of the [[dom/HTMLElement|'''attribute''']] to get.
|Optional=No
}}
|Method_applies_to=dom/NamedNodeMap
|Example_object_name=attributes
|Return_value_name=attribute
|Javascript_data_type=DOM Node
|Return_value_description=The attribute node with the given name.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example shows how to use the '''getNamedItem''' method to retrieve the value of an [[dom/HTMLElement|'''attribute''']].
|Code=&lt;!doctype html&gt;
&lt;html&gt;
&lt;head&gt;
&lt;script&gt;
function Init()
{
    var oAttrColl {{=}} document.getElementById("oElem").attributes;
    var oAttr {{=}} oAttrColl.getNamedItem("align");
    console.log("ALIGN attribute value: " + oAttr.value);
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body onload{{=}}"Init()"&gt;
  &lt;p id{{=}}"oElem" align{{=}}"center"&gt;An element.&lt;/P&gt;
 &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getNamedItemEx1.htm
}}
}}
{{Notes_Section
|Notes=If the '''attribute''' applies to an element but is not specified, this method returns the '''attribute''' with the specified name set to an empty string.
If the '''attribute''' does not apply to the element and is not specified, then an error is returned.
If the '''attribute''' does not apply to the element and is specified, then the '''attribute''' with the specified name is returned.

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
|Desktop_rows=
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