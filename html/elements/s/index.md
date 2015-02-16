{{Page_Title|s – strikethrough}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name|s}}
{{Summary_Section|The '''s''' element represents contents that are no longer accurate and must be marked accordingly in order to allow keeping it in the document.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=Use the '''s''' element to represent things that are no longer relevant or no longer accurate. However, '''s''' is not appropriate when indicating document edits; for that, use the [[html/elements/del|'''del''']] and [[html/elements/ins|'''ins''']] elements, as appropriate.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the <code>&lt;s&gt;</code> element to render a text that no longer accurate.
|Code=&lt;ul&gt;
  &lt;li&gt;&lt;s&gt;today's special: Gouda Cheeseburger, .14&lt;/s&gt; SOLD OUT&lt;/li&gt;
  &lt;li&gt;Classic Cheeseburger, .50&lt;/li&gt;
&lt;/ul&gt;
|LiveURL=http://code.webplatform.org/gist/604bc1947f655fb863a1
}}{{Single Example
|Language=CSS
|Description=Typical browser default CSS properties for the <code>&lt;s&gt;</code> element.
|Code=text-decoration: line-through;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=While [[html/elements/s|'''s''']] and [[html/elements/del|'''del''']] appear to be similar, namely marking obsolete content, but they differ in semantics. [[html/elements/del|'''del''']] marks text that has been removed from the document, but [[html/elements/s|'''s''']] marks text that is to be kept in the document, but made clear that its content is no longer accurate.
|Notes=The information that the text inside the '''s''' element is not accurate is not indicated to assistive technologies, like screen readers. Instead it is interpreted like regular text which can lead to confusion. Add clear text that the information is invalid.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-s-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-s-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/present/graphics.html#edef-S
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=* [[html/elements/ins|<code>ins</code>]]
* [[html/elements/del|<code>del</code>]]
* [[html/elements/strike|<code>strike</code>]]
|External_links=* [https://developer.mozilla.org/en-US/docs/HTML/Element/s Mozilla Developer Network]
* [http://msdn.microsoft.com/en-us/library/ie/ms535890%28v=vs.85%29.aspx Microsoft Developer Network]
* http://www.w3.org/TR/html-markup/s.html#s
|Manual_sections=
}}
{{Topics|HTML}}
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