{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLMediaElement
|Interface=dom/HTMLMediaElement
|Target=dom/Element
{{Method Parameter
|Name=type
|Data type=any
|Description=The type of media that the client can play.
|Optional=No
}}{{Method Parameter
|Name=canPlay
|Data type=any
|Description='''probably'''



The type of media that is most likely to be rendered.


'''maybe'''



The type of media that might be able to be rendered


'''[empty string]'''



The media type cannot be rendered.
|Optional=No
}}
|Method_applies_to=dom/HTMLMediaElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

String

The type of media that is most likely to be rendered.

The type of media that might be able to be rendered

The media type cannot be rendered.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.8.9.2
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
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/media|media]]</code>
*<code>audio</code>
*<code>audio</code>
*<code>video</code>
}}
{{Topics|API, Audio, DOM, Video}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}