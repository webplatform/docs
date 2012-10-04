{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=fragment|Data type=DOMString|Description=String containing HTML to be parsed.|Optional=}}
{{Method Parameter|Name=retVal|Data type=DocumentFragment|Description=A document fragment representing the parsed HTML.|Optional=}}
|Method_applies_to=dom/Element
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code
!Description
|-
|S_OK
|The operation completed successfully.
|-
|W3CException_INVALID_STATE_ERR
|Throws this exception if the range has been detached.
|}
 

DocumentFragment

A document fragment representing the parsed HTML.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
When inserting elements into a DOM structure, some elements behave according to their context. Using createContextualFragment, you can ensure the parsed HTML will work as expected when inserted or added to the document.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML]


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/Range|Range]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}