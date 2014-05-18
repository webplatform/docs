{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''code''' element specifies a fragment of computer code.}}
{{Markup_Element
|DOM_interface=dom/HTMLElement
|Content=Content within a '''code''' element is used to indicate a selection of text that is computer programming code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This is a simple example of the '''code''' element to display a CSS snippet.
|Code=&lt;p>Now let’s set the color to red: &lt;code>color: #f00;&lt;/code>.&lt;/p>
}}{{Single Example
|Language=HTML
|Description=This is another take on the example above, but includes a '''class''' to indicate the type of code being written.
|Code=&lt;p>Now let’s set the color to red: 
&lt;code class="language-css">color: #f00;&lt;/code>.&lt;/p>
}}
}}
{{Notes_Section
|Usage=The '''code''' element is a phrasing-level element used to indicate a selection of code. It must not contain block-level elements, but it may contain other phrasing-level elements.

Often, authors will use a '''class''' attribute to indicate the language being used in the '''code''' element (see Example 2).
|Notes=While the '''code''' element is often visually-presented in a monospace font like the '''pre''' element, unlike '''pre''' white space (spaces, tabs, etc.) inside a '''code''' element is **not preserved**.

When representing HTML code within a '''code''' element, remember to encode the reserved characters &lt; and &gt; with their HTML entity equivalents (&amp;lt; and &amp;gt;, respectively).
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
*<code>samp</code>
}}
{{Topics|HTML, XHTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}