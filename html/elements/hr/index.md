{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''hr''' element represents a paragraph-level thematic break in text.}}
{{Markup_Element
|DOM_interface=dom/HTMLHRElement
|Content=The '''hr''' element represents a paragraph-level thematic break. That sounds kinda strange, I know, but a good example what that means comes from the world of fiction where the text in a given chapter might shift from one location to another or from one period of time to another. The '''hr''' is a great way to indicate a shift like that.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''hr''' element to create a paragraph-level thematic break.
|Code=&lt;p>This is a paragraph in a section about Topic A.&lt;/p>
&lt;hr/>
&lt;p>This paragraph is part of a section concerning Topic B.&lt;/p>
}}
}}
{{Notes_Section
|Usage=The '''hr''' element is a “replaced element” which means it is comprised of a single tag with no content. You can apply attributes (e.g. '''class''') to the tag, but it must not contain text.

As a replaced element, the '''hr''' will be automatically closed by browsers, but you can also explicitly close the element with a trailing slash: '''&lt;hr/&gt;'''
|Notes=In HTML 4.01, the '''hr''' element represented a horizontal rule. And while the '''hr''' element may still be displayed as a horizontal rule in visual browsers, it is now defined in semantic terms, rather than presentational ones.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 15.3
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html-markup/hr.html
|Status=W3C Working Draft
|Relevant_changes=Semantic meaning to “paragraph-level thematic break”.
}}{{Related Specification
|Name=HTML 4.01 Specification
|URL=http://www.w3.org/TR/html401/present/graphics.html#edef-HR
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=0.2
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=0.8
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=1
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
}}
{{Topics|HTML, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}