{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Needs Review
|Content=Incomplete, Compatibility Incomplete
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
|Language=HTML
|Code=&lt;!DOCTYPE html&gt;
&lt;html lang="en"&gt;
  &lt;head&gt;
      &lt;meta http-equiv="X-UA-Compatible" content="IE=8"/&gt;
    &lt;title&gt;QUOTES Example&lt;/title&gt;
    &lt;style type="text/css"&gt;
    /* Define quote characters */
      q { quotes: '"' '"' }
    /* Define pseudo-class triggers */
      q:before { content: open-quote }
      q:after  { content: close-quote }
    &lt;/style&gt;
  &lt;/head&gt;
  &lt;body&gt;
  &lt;p&gt;&lt;q&gt;When I die, I'm donating my body to science fiction.&lt;/q&gt;&lt;em&gt; ~ Stephen Wright&lt;/em&gt;&lt;/p&gt;
  &lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://code.webplatform.org/gist/5841933
}}
}}
{{Notes_Section
|Notes====Remarks===
Pairs of strings are required if the value is not <code>none</code>.
|Import_Notes====Syntax===
<code>'''quotes: ''''''[''' &lt;string&gt; &lt;string&gt; ''']''''''+''' '''{{!}}''' none</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 12.3
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
|Manual_sections====Related pages (MSDN)===
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