{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=element|Data type=IHTMLElement|Description=Object|Optional=}}
{{Method Parameter|Name=before|Data type=VARIANT|Description='''Variant''' of type '''Integer''' that specifies the index position in the collection where the element is placed. If no value is given, the method places the element at the end of the collection.|Optional=}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
Internet Explorer 8. In IE8 Standards mode, ''before'' also accepts an '''Variant''' of type '''Object''' that specifies the object before which to insert the element.  For more information, see Defining Document Compatibility.
This method adds an '''option''' element to a '''select''' block.
Before you can add an element to a collection, you must create it first by using the [[dom/methods/createElement|'''createElement''']] method.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/properties/areas|areas]]</code>
*<code>[[dom/properties/controlRange|controlRange]]</code>
*<code>[[dom/properties/options|options]]</code>
*<code>select</code>
*<code>[[dom/methods/remove|remove]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}