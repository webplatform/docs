{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=cmdID|Data type=BSTR|Description='''String''' that specifies a command identifier.|Optional=}}
|Method_applies_to=dom/traversal/TextRange
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Variant

'''Variant''' that returns the command value for the document, range, or current selection, if supported. Possible values  depend on ''cmdID''. If not supported, this method returns a '''Variant''' of type '''Boolean''' set to false.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
This method is a wrapper function for the command constants. You can obtain an '''IHTMLDocument2''' interface using IID_IHTMLDocument2 for the IID.
This method is a wrapper function for the command constants. You can obtain an '''IHTMLControlRange''' interface using IID_IHTMLControlRange for the IID.
This method is a wrapper function for the command constants. You can obtain an '''IHTMLTxtRange''' interface using IID_IHTMLTxtRange for the IID.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>[[dom/properties/controlRange|controlRange]]</code>
*<code>[[dom/traversal/TextRange|TextRange]]</code>
*<code>Reference</code>
*<code>execCommand</code>
*<code>[[dom/traversal/methods/queryCommandEnabled|queryCommandEnabled]]</code>
*<code>[[dom/traversal/methods/queryCommandIndeterm|queryCommandIndeterm]]</code>
*<code>[[dom/traversal/methods/queryCommandState|queryCommandState]]</code>
*<code>[[dom/traversal/methods/queryCommandSupported|queryCommandSupported]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}