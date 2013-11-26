{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=pvarIndex|Data type=VARIANT|Description='''Variant''' of type '''Integer''' or '''String''' that specifies the object or collection to retrieve. If this parameter is an integer, it is the zero-based index of
the object. If this parameter is a string, all objects with matching
[[html/attributes/name|'''name''']] or [[html/attributes/id|'''id''']]
properties are retrieved, and a collection is returned if more than one match is made.|Optional=}}
|Method_applies_to=dom/TextRange
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Variant


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example uses the [[css/cssom/properties/item|'''item''']] method to retrieve each object from the document. In this case, the method parameter is a number, so the objects are retrieved in the order in which they appear in the document.
|LiveURL=
|Code=
&lt;script language{{=}}"JScript"&gt;
var oItem {{=}} document.all;
if (oItem!{{=}}null) {
    for (i{{=}}0; i&lt;oItem.length; i++) 
        alert(oItem.item(i).tagName);
}
&lt;/script&gt;
}}
{{Single_Example
|Description=The next example uses the [[css/cssom/properties/item|'''item''']] method to retrieve a collection of all objects in the document that have "Sample" as an [[html/attributes/id|'''ID''']]. It then uses '''item''' again to retrieve each object from the "Sample" collection.
|LiveURL=
|Code=
&lt;script language{{=}}"JScript"&gt;
var oItem {{=}} document.all.item("Sample");
If (oItem !{{=}} null) {
    for (i{{=}}0; i&lt;oItem.length; i++) {
        alert(oItem.item(i).tagName);
    }
}
&lt;/script&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Always check the IDispatch pointer returned by this call, even if the method returns S_OK. If the value of the pointer is null, the element was not found and the call was not successful.
Upon successful return, the ''pvarResult'' parameter contains an IDispatch interface pointer or an array of IDispatch interface pointers that can be queried for a specific interface, depending on the collection type.
'''item''' returns a '''Variant''' of type '''Object''' that can be queried for '''IHTMLTxtRange'''.
Microsoft Internet Explorer 5 does not provide multiple selection. The default implementation of this method returns a collection consisting of a single [[dom/traversal/TextRange|'''TextRange''']] object
Host applications can provide a multiple selection mechanism and can return a collection of [[dom/traversal/TextRange|'''TextRange''']] objects that represents discontinuous selections.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/properties/TextRange|TextRange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}