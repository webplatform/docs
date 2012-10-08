{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=identifier
|Description=The name of the counter, optionally followed by an
'''integer'''.
}}{{CSS Property Value
|Data Type=integer
|Description=The initial value of the counter. The default value is 0.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example demonstrates automatic
chapter and section numbering using
'''counter-reset''',
[[css/properties/counter-increment|'''counter-increment''']],
and [[css/properties/content|'''content''']].
The <code>chapter</code> counter is set to zero for the
'''body''' element,
and then incremented for each '''hn'''
element encountered. The <code>section</code> counter is
reset for each '''hn''' element and
incremented for each '''hn''' element.
When the page is viewed, each
'''hn''' element is preceded by
a chapter heading of the form
<code>"Chapter</code>''X''<code>."</code>,
while each '''hn''' element is preceded by
a section number of the form
<code>"</code>''X.N''<code>"</code>.
|Code=&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
&lt;style type{{=}}"text/css"&gt;
BODY {
    counter-reset: chapter;      /* Create a chapter counter */
}
H1 {
    counter-increment: chapter;  /* Add 1 to chapter */
    counter-reset: section;      /* Set section to 0 */
}
H1:before {
    content: "Chapter " counter(chapter) ". ";
}
H2 {
    counter-increment: section;
}
H2:before {
    content: counter(chapter) "." counter(section) " ";
}
&lt;/style&gt;
}}{{Single Example
|Description=Because of a conflicting set of style rules, in the following example
only the <code>imagenum</code> counter is reset.
To reset both counters, put them together in the same rule.
|Code=H1 { counter-reset: section -1 }
H1 { counter-reset: imagenum 99 }
}}
}}
{{Notes_Section
|Notes====Remarks===
The
'''counter-reset'''
attribute can contain a list of one or more counters,
each one optionally followed by an integer. The integer represents
the value that the counter is set to after each occurrence
of the element.
If an element both resets and increments a counter, the counter is
reset first and then incremented. If the same counter is specified
more than once, each reset or increment of the counter is processed
in the order specified.
The
[[css/properties/counter-increment|'''counter-increment''']]
and
'''counter-reset'''
attributes follow the rules of the CSS cascade. Given two style
declarations with the same specificity, only the last one encountered
will be processed. For more information about cascade and specificity,
see Understanding CSS Selectors.
An element that is not displayed
([[css/properties/display|'''display''']]
attribute set to 'none') and pseudo-elements that do not generate content
([[css/properties/content|'''content''']]
attribute set to 'normal') cannot increment or reset a counter.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>'''counter-reset: ''''''[''' ''
&lt;identifier&gt;
'' ''
&lt;integer&gt;
'' ''']''''''+'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 12.4
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
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
*<code>[[css/properties/counter-increment|counter-increment]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}