{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add compatibility.
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''b''' element was originally used to tell the browser to make the enclosed text bold. While the '''b''' element is widely supported in browsers, its use is not recommended for this purpose since CSS can be used to achieve the same effect on a more semantically-appropriate element. In HTML5, '''b''' has been re-purposed to signify text this is offset in some way, but is of no greater significance than the surrounding text.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=The '''b''' element should be used as a last resort when no other element is more appropriate as it has no semantic value other than indicating that the contained text should be stylistically offset in some way (i.e. it’s like a shorter [[html/elements/span|'''span''' element]]).
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In the following example, objects in a text adventure are highlighted as being special by use of the '''b''' element.
|Code=&lt;p>You enter a small room. Your &lt;b>sword&lt;/b> glows
brighter. A &lt;b>rat&lt;/b> scurries past the corner wall.&lt;/p>
|LiveURL=http://code.webplatform.org/gist/7281844
}}{{Single Example
|Language=HTML
|Description=In this example, the '''b''' element is used to indicate both a company and a product name. Disambiguation via CSS is accomplished using the '''class''' attribute.
|Code=&lt;p>&lt;b class="org">Acme &lt;abbr title="Corporation">Corp&lt;/abbr>&lt;/b> 
is pleased to introduce the 
&lt;b class="product">Widget Blast 3000&lt;/b>. 
This is a miracle of modern science that will 
simplify your life, fry an egg, and even put 
your kids to bed.&lt;/p>
|LiveURL=http://code.webplatform.org/gist/321e5149c1e661e1de14
}}
}}
{{Notes_Section
|Usage=The '''b''' element makes a lot of sense for use as a wrapper for proper names (e.g. people, companies, products, locations) as they may be offset from the surrounding text in some way, but are not semantically meaningful.

Internationalization topics related to the '''b''' element:

* [[http://www.w3.org/International/techniques/authoring-html#bandi|Using b and i tags]]
|Notes=As the '''b''' element has no inherent meaning, you should not use it to convey meaning; there is probably a more appropriate element for that. Headings should use the '''h1''' to '''h6''' elements, stress emphasis should use the '''em''' element, importance should be denoted with the '''strong''' element, and contextually-important/highlighted text should use the '''mark''' element.
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-b-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/present/graphics.html#edef-B
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
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