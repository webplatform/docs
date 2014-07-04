{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, examples needed
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=css/cssom/properties
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 7 and later. If given a string that is not a numeric index, this method throws an error if no [[html/attributes/id|'''id''']] property with that string value is found.
Always check the IDispatch pointer returned by this call, even if the method returns S_OK. If the value of the pointer is null, the element was not found and the call was not successful.
Upon successful return, the ''pvarResult'' parameter contains an IDispatch interface pointer or an array of IDispatch interface pointers that can be queried for a specific interface, depending on the collection type.
'''item''' returns a '''Variant''' of type '''Object''' that can be queried for '''IHTMLStyleSheet'''.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.

===Parameters===
;''pvarIndex'' [in]:Type: '''VARIANT''''''Variant''' of type '''Integer''' or '''String''' that specifies the object or collection to retrieve. If this parameter is an integer, it is the zero-based index ofthe object. If this parameter is a string, all objects with matching [[html/attributes/id|'''id''']]properties are retrieved, and a collection is returned if more than one match is made.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/imports|imports]]</code>
*<code>[[css/cssom/styleSheets|styleSheets]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}