{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the type of quotation marks for embedded quotations.}}
{{CSS Property
|Initial value=depends on user agent
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=[&lt;string&gt;  &lt;string&gt;]+
|Description=The "open-quote" and "close-quote" values are taken from the specified list of pairs of quotation marks. The first (leftmost) pair represents the outermost level of quotation, the second pair the first level of embedding, etc.
}}{{CSS Property Value
|Data Type=none
|Description=The "open-quote" and "close-quote" values produce no quotation marks.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Here we demonstrate nested quotes.  Notice the syntax used to declare the quotes.  You can use any character for a quote, but here we used <code>'</code> and <code>"</code>.
|Code=q { quotes: '"' '"' "'" "'" }
q:before { content: open-quote }
q:after  { content: close-quote }
|LiveURL=http://code.webplatform.org/gist/5841933
}}{{Single Example
|Language=HTML
|Description=The HTML for the example above.
|Code=<p>
  <q>When I die, I'm donating my <q>body</q> to science fiction.</q>
  <em> ~ Stephen Wright</em>
</p>
}}
}}
{{Notes_Section
|Notes====Remarks===
Pairs of strings are required if the value is not <code>none</code>.
|Import_Notes====Standards information===
*[http://www.w3.org/TR/CSS21/generate.html#quotes CSS 2.1], Section 12.3
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
|Topic_clusters=Generated and Replaced Content
|Manual_sections====Related pages===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}