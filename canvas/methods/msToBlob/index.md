{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes={{Editorial/Move_Candidate
| Probably should be under HTML5 canvas element (as '''toBlob'''). See [http://www.w3.org/html/wg/drafts/html/master/single-page.html#the-canvas-element HTML5 specification].
}}
|Checked_Out=No
|High-level issues=Move Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=
|Name=retVal
|Data type=Blob
|Description=A blob object.
|Optional=No
}}
|Method_applies_to=dom/HTMLCanvasElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

This method can return one of these values.

{| class="wikitable"
|-
!Return code/value
!Description
|-
|S_OK
|
|-
|DOMException.SECURITY_ERR
18
|The image is not of the same origin or domain as the destination.
|}
 

Blob

A blob object.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections====Related pages (MSDN)===
*<code>[[canvas/objects/canvas|HTMLCanvasElement]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}