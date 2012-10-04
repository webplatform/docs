{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=index|Data type=Integer|Description=The zero-based index of the item in the collection.|Optional=}}
{{Method Parameter|Name=startTime|Data type=VARIANT|Description=The start position of the range, in seconds, from the beginning of the timeline.|Optional=}}
|Method_applies_to=apis/audio-video/HTMLTimeRanges
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
|IndexSizeError
|The specified index is out of range.
|}
 

Variant

The start position of the range, in seconds, from the beginning of the timeline.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Time ranges do not overlap. The '''start''' time is guaranteed to be greater than the [[apis/audio-video/methods/end|'''end''']] of the range that precedes it.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.9.11


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/audio-video/HTMLTimeRanges|TimeRanges]]</code>
*<code>Reference</code>
*<code>[[apis/audio-video/methods/end|end]]</code>
*<code>[[apis/audio-video/properties/length (TimeRanges)|length]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}