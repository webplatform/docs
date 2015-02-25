{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''dfn''' element indicates the defining instance of a term.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Tag_omissions=Closing tag required
|CSS_display=inline
|Content=*If the dfn element is specified, nearest parent of the dfn element(paragraph, description list group, or section) must also contain the definitions for the defining term.
*The priority level of defining term is as follow:
*# Value of the title attribute in the dfn element.
*# Value of the title attribute in the abbr element. (if the dfn element contains exactly one element child node and no child text nodes, and that child element is the abbr element
*# TextContent of the dfn element
*If the title attribute of the dfn element is present, then it must contain only the term being defined.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''dfn''' element to indicate the defining instance of a new term.
|Code=&lt;p>The &lt;dfn title="Garage Door Opener">GDO&lt;/dfn>
is a device that allows off-world teams to open the iris.&lt;/p>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example uses the '''dfn''' element to indicate the defining instance of a new term that is an abbreviation.
|Code=&lt;p>The &lt;dfn>&lt;abbr title="Garage Door Opener">GDO&lt;/abbr>&lt;/dfn>
is a device that allows off-world teams to open the iris.&lt;/p>
&lt;!-- ... later in the document: -->
&lt;p>Teal'c activated his &lt;abbr>GDO&lt;/abbr>
and so Hammond ordered the iris to be opened.&lt;/p>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example uses the '''dfn''' element to indicate the defining instance of a new term and then uses an anchor to provide a reference to that instance.
|Code=&lt;p>The &lt;dfn id="dfn-gdo">&lt;abbr title="Garage Door Opener">GDO&lt;/abbr>&lt;/dfn>
is a device that allows off-world teams to open the iris.&lt;/p>
&lt;!-- ... later in the document: -->
&lt;p>Teal'c activated his &lt;a href="#dfn-gdo">&lt;abbr>GDO&lt;/abbr>&lt;/a>
and so Hammond ordered the iris to be opened.&lt;/p>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=The '''dfn''' is a phrasing-level element and can’t contain block-level elements, but it can contain other phrasing type elements like '''abbr''', read on…

If the '''dfn''' element has a [[html/attributes/title|'''title''' attribute]], then the value of that attribute serves as the definition for the text inside the element (see Example 1).

If the '''dfn''' contains exactly one child element (and no other text) //and// that child element is an [[html/elements/abbr|'''abbr''' element]] with a [[html/attributes/title|'''title''' attribute]], then the exact value of that '''title''' attribute serves as the definition for the text inside the '''abbr''' (see Example 2).

If the '''dfn''' only contains text, the exact text content of the element gives the term being defined.

If the [[html/attributes/title|'''title''' attribute]] of the '''dfn''' element is present, then it must contain only the definition of the term being defined.
|Notes=If given an [[html/attributes/id|'''id''' attribute]], a '''dfn''' may serve as a reference for other elements on the page by anchoring to the '''dfn''' (see Example 3).
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/text-level-semantics.html#the-dfn-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/text-level-semantics.html#the-dfn-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-DFN
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML, Text
|Manual_links=*<code>[[html/elements/acronym|acronym]]</code>
*<code>[[html/elements/address|address]]</code>
*<code>[[html/elements/cite|cite]]</code>
*<code>[[html/elements/i|i]]</code>
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