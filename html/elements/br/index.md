{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Modify DOM Interface information.
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The line break element, '''br''', forces the current line of text to end and the text that follows it will being on a new line.}}
{{Markup_Element
|DOM_interface=dom/HTMLBRElement
|Content=The '''br''' element forcibly breaks (ends) the current line of text, without starting a new paragraph.

'''br''' elements must be used only for line breaks that are actually part of the content, as in poems or addresses, but must not be used for separating thematic groups in a paragraph. For that you should use the [[html/elements/p|'''paragraph''' element]].

Any content inside '''br''' elements (i.e. attributes) must not be considered part of the surrounding text.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following example is correct usage of the '''br''' element
|Code=&lt;p>P. Sherman&lt;br>
42 Wallaby Way&lt;br>
Sydney&lt;/p>
|LiveURL=http://code.webplatform.org/gist/7282007
}}
}}
{{Notes_Section
|Usage=The '''br''' element is a “replaced element” which means it is comprised of a single tag with no content. You can apply attributes (e.g. '''class''') to the tag, but it must not contain text.

As a replaced element, the '''br''' will be automatically closed by browsers, but you can also explicitly close the element with a trailing slash: '''&lt;br/&gt;'''
|Notes=No closing tag is needed.
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-br-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-br-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-BR
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
}}
{{Topics|HTML, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}