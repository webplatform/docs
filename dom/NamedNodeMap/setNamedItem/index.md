{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=ppNode|Data type=IHTMLDOMAttribute|Description='''attribute'''|Optional=}}
|Method_applies_to=dom/attributes
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLDOMAttribute'''

'''attribute'''

attribute


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to add an attribute to an element using the '''setNamedItem''' method.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/setNamedItemEx1.htm
|Code=
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
function fnSetNamedItem(){
var nnm {{=}} myDIV.attributes;
var namedItem {{=}} document.createAttribute("title");
namedItem.value {{=}} "This is a ToolTip";
nnm.setNamedItem(namedItem);
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;BODY onload{{=}}"fnSetNamedItem();"&gt;
&lt;DIV ID{{=}}"myDIV"&gt;This DIV now has a ToolTip.&lt;/DIV&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
An [[dom/attributes|'''attribute''']] that is set with this method does not have to apply to the element.
If an [[dom/attributes|'''attribute''']] with the same name is already present, it is replaced by the new '''attribute'''.
'''setNamedItem''' was introduced in Microsoft Internet Explorer 6.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}182717 Document Object Model (DOM) Level 3 Core Specification], Section 1.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/properties/attribute|attributes]]</code>
*<code>Reference</code>
*<code>[[dom/methods/getNamedItem|getNamedItem]]</code>
*<code>[[dom/methods/removeNamedItem|removeNamedItem]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}