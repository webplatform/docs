{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the type of quotation marks for embedded quotations.}}
{{CSS Property
|Initial value=depends on user agent/element
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=
|Animatable=No
|CSS object model property=
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
|Description=Here we demonstrate nested quotes.  Notice the syntax used to declare the quotes.  Any character can be used for a quote, but this example uses <code>'</code> and <code>"</code>.  If we wanted to declare <code>quotes: "«" "»" "!" "@"</code>, that would work, too.  You can also escape the characters (e.g. <code>quotes: "\""</code>), if that is your preference.
|Code=q { quotes: '"' '"' "'" "'" }
q:before { content: open-quote }
q:after  { content: close-quote }
|LiveURL=http://code.webplatform.org/gist/5841933
}}{{Single Example
|Language=HTML
|Description=The HTML for the example above.
|Code=<nowiki><p>
  <q>When I die, I'm donating my <q>body</q> to science fiction.</q>
  <em> ~ Stephen Wright</em>
</p></nowiki>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=Pairs of strings are required if the value is not <code>none</code>.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS21/generate.html#quotes
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
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
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Version=37 and earlier
|Note=Supports the nonstandard single string syntax (<code>quotes: 'red'</code>).
}}
}}