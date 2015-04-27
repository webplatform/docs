{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Add compatibility.
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''strong''' element indicates text that is of great importance, seriousness, or urgency.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=required
|CSS_display=inline
|Content=The relative level of importance of a piece of content is given by its number of ancestor strong elements.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''strong''' element to indicate important information.
|Code=<nowiki><p>Please fill in the form below.
<strong>Note: all fields are required.</strong></p>
}}{{Single Example
|Language=HTML
|Description=Example with nested '''strong''' elements.
|Code=<nowiki><p><strong><strong>Warning.</strong> This dungeon is dangerous.</strong></p></nowiki>
}}
}}
{{Notes_Section
|Usage=The '''strong''' element is a phrasing-level element. It must not contain block-level elements, but it can contain other phrasing-level elements.
|Notes=By default, most browsers render the '''strong''' element with bold text, but you can change that in CSS.

If you are looking to emphasize a word or phrase, the [[html/elements/em|'''em''' element]] would be a better choice.

If you want to bold text, but the text is not important, you should use the CSS rule [[css/properties/font-weight|'''font-weight: bold''']] on the appropriate element enclosing the text.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-strong-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-strong-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-STRONG
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>b</code>
*<code>cite</code>
}}
{{Topics|HTML, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}