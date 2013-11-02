{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''b''' element (&lt;b&gt;) historically was used to tell the browser to make the nested text bold. While the &lt;b&gt; element is widely supported in browsers, its use is not recommended, as CSS can be used to achieve the same effect. In HTML5, it merely signifies that the text should be stylistically distinguished in some way.


Internationalization topics related to the <code>b</code> element:
* [http://www.w3.org/International/techniques/authoring-html#bandi Using b and i tags]
}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=The &lt;b&gt; element is used to make the nested tag bolded. The use of the &lt;b&gt; is not recommended according to HTML 5 standards as the bold effect can achieved using CSS.

The b element should be used as a last resort when no other element is more appropriate. In particular, headings should use the h1 to h6 elements, stress emphasis should use the em element, importance should be denoted with the strong element, and text marked or highlighted should use the mark element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=In the following example, objects in a text adventure are highlighted as being special by use of the ""b"" element.
|Code=<p>You enter a small room. Your <b>sword</b> glows
brighter. A <b>rat</b> scurries past the corner wall.</p>
|LiveURL=http://code.webplatform.org/gist/7281229
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5 - 4.6 Text-level Semantics
|URL=http://www.w3.org/TR/html5/text-level-semantics.html
|Status=W3C Candidate Recommendation
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
|Topic_clusters=HTML
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}