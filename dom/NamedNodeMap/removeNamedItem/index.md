{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=bstrName|Data type=BSTR|Description=A '''String''' that specifies the name of an [[dom/attributes|'''attribute''']] to remove.|Optional=}}
|Method_applies_to=dom/attributes
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
|Description=The following example shows how to use this method to remove an [[dom/attributes|'''attribute''']] from an element.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/removeNamedItemEx1.htm
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function removeAttrib()
{
    var oAttrColl {{=}} myDIV.attributes;
    oAttrColl.removeNamedItem("TITLE");
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;DIV onclick{{=}}"removeAttrib();" ID{{=}}"myDIV" TITLE{{=}}"THIS IS A TOOLTIP"&gt;
Click this DIV and the ToolTip will be inactivated.&lt;/DIV&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
An [[dom/attributes|'''attribute''']] that is removed with this method reverts to the default value of the '''attribute''' when applicable. This method returns a script error if the user attempts to remove a non-existent attribute node.
'''removeNamedItem''' was introduced in Microsoft Internet Explorer 6.
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