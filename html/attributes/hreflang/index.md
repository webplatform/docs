{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
|Content=Internationalization topics related to the <code>hreflang</code> attribute:
* [http://www.w3.org/International/techniques/authoring-html#linkdestination Indicating the language of a link destination]

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the [[html/elements/a|'''a''']] element in the following example, the '''HREFLANG''' attribute specifies the language code of the U.S. version of English.
|Code=&lt;A HREF{{=}}"http://example.microsoft.com/..." HREFLANG{{=}}"en-US"&gt;anchor text&lt;/A&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
You must set the value of this property before you can retrieve it.
Language codes identify natural languages that are spoken, written, or otherwise used for the communication of information among people, and are defined and explained in [http://go.microsoft.com/fwlink/p/?linkid{{=}}203649 Tags for the Identification of Languages (RFC1766)].  Computer languages are explicitly excluded from language codes.
'''hreflang''' was introduced in Microsoft Internet Explorer 6
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
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
*<code>[[html/elements/a|a]]</code>
*<code>link</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}