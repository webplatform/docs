{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information. Add HTML information section.
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''i''' element indicates that the contained text is in an alternate voice, mood, or language from the surrounding text.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=
|CSS_display=
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example of the '''i''' element in use.
|Code=&lt;p>The car wouldn't start yesterday 
no matter what I did, but today it works 
just fine. &lt;i>Go figure!&lt;/i>&lt;/p>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example uses the '''I''' element to indicate the transition to an alternate language. Note that the [html/attributes/lang|'''lang''' attribute] is used to indicate the language being used
|Code=&lt;p>HTML has that certain 
&lt;i lang="fr" title="I don’t know what">je ne 
sais quoi&lt;/i>&lt;/p>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=The '''i''' element is a phrasing-level element. It must not contain block-level elements, but it can contain other phrasing-level elements.
|Notes=The '''i''' element was historically used to indicate that the text should be rendered in Italic type, where available. By default, most browsers still render the '''i''' element in italics, but you can change that in CSS.

If you are looking to emphasize a word or phrase, the [[html/elements/em|'''em''' element]] would be a better choice.

If you wish to italicize the name of a creative work (e.g. a magazine, book, or film title), use the [[html/elements/cite|'''cite''' element]] instead.

Internationalization topics related to the '''i''' element:

* [http://www.w3.org/International/techniques/authoring-html#bandi Using b and i tags]
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-i-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-i-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/present/graphics.html#edef-I
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML, XHTML}}
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