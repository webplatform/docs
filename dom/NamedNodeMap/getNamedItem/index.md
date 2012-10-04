{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrName|Data type=BSTR|Description=A '''String''' that specifies the name of the [[dom/attributes|'''attribute''']] to get.|Optional=}}
|Method_applies_to=dom/attributecollection
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDOMAttribute'''

'''attribute'''


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''getNamedItem''' method to retrieve the value of an [[dom/attributes|'''attribute''']].
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/getNamedItemEx1.htm
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function Init()
{
    var oAttrColl {{=}} oElem.attributes;
    var oAttr {{=}} oAttrColl.getNamedItem("align");
    alert("ALIGN attribute value: " + oAttr.value);
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY ONLOAD{{=}}"Init()"&gt;
&lt;P ID{{=}}"oElem" ALIGN{{=}}"center"&gt;An element.&lt;/P&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
If the [[dom/attributes|'''attribute''']] applies to an element but is not specified, this method returns the '''attribute''' with the specified name set to an empty string.
If the [[dom/attributes|'''attribute''']] does not apply to the element and is not specified, then an error is returned.
If the [[dom/attributes|'''attribute''']] does not apply to the element and is specified, then the '''attribute''' with the specified name is returned.
Windows Internet Explorer 8 and later. In IE8 Standards mode, the '''getNamedItem''' method does not create [[dom/attributes|'''attribute''']] is not found. For more information on IE8 mode, see Defining Document Compatibility.
'''getNamedItem''' was introduced in Microsoft Internet Explorer 6.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/properties/attribute|attributes]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}