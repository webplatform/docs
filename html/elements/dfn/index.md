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
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''dfn''' element to indicate the defining instance of a new term.
|Code=&lt;p>The &lt;dfn title="Garage Door Opener">GDO&lt;/dfn>
is a device that allows off-world teams to open the iris.&lt;/p>
}}{{Single Example
|Language=HTML
|Description=This example uses the '''dfn''' element to indicate the defining instance of a new term that is an abbreviation.
|Code=&lt;p>The &lt;dfn>&lt;abbr title="Garage Door Opener">GDO&lt;/abbr>&lt;/dfn>
is a device that allows off-world teams to open the iris.&lt;/p>
&lt;!-- ... later in the document: -->
&lt;p>Teal'c activated his &lt;abbr>GDO&lt;/abbr>
and so Hammond ordered the iris to be opened.&lt;/p>
}}{{Single Example
|Language=HTML
|Description=This example uses the '''dfn''' element to indicate the defining instance of a new term and then uses an anchor to provide a reference to that instance.
|Code=&lt;p>The &lt;dfn id="dfn-gdo">&lt;abbr title="Garage Door Opener">GDO&lt;/abbr>&lt;/dfn>
is a device that allows off-world teams to open the iris.&lt;/p>
&lt;!-- ... later in the document: -->
&lt;p>Teal'c activated his &lt;a href="#dfn-gdo">&lt;abbr>GDO&lt;/abbr>&lt;/a>
and so Hammond ordered the iris to be opened.&lt;/p>
}}
}}
{{Notes_Section
|Usage=The '''dfn''' is a phrasing-level element and can’t contain block-level elements, but it can contain other phrasing type elements like '''abbr''', read on…

If the '''dfn''' element has a [[html/attributes/title|'''title''' attribute]], then the value of that attribute serves as the definition for the text inside the element (see Example 1).

If the '''dfn''' contains exactly one child element (and no other text) //and// that child element is an [[html/elements/abbr|'''abbr''' element]] with a [[html/attributes/title|'''title''' attribute]], then the exact value of that '''title''' attribute serves as the definition for the text inside the '''abbr''' (see Example 2).

If the '''dfn''' only contains text, the exact text content of the element gives the term being defined.

If the [[html/attributes/title|'''title''' attribute]] of the '''dfn''' element is present, then it must contain only the definition of the term being defined.
|Notes=If given an [[html/attributes/id|'''id''' attribute]], a '''dfn''' may serve as a reference for other elements on the page by anchoring to the '''dfn''' (see Example 3).
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
|Topic_clusters=HTML, Text
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>cite</code>
*<code>i</code>
}}
{{Topics|HTML, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}