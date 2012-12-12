{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Increments one or more counter values.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=identifier
|Description=The name of the counter, optionally followed by an
'''increment'''.
}}{{CSS Property Value
|Data Type=integer
|Description=An integer that indicates by how much the counter is
incremented for every occurrence of the element.
Zero and negative integers are allowed.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example demonstrates automatic
chapter and section numbering using
[[css/properties/counter-reset|'''counter-reset''']],
'''counter-increment''',
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
}}
}}
{{Notes_Section
|Notes====Remarks===
The
'''counter-increment'''
attribute can contain a list of one or more counters,
each one optionally followed by an integer. The integer	represents
the amount that the counter is incremented after each occurrence
of an element.
This property is used to generate numbered content for each occurrence
of an element. The counter need not be defined before it is incremented.
To reset a counter value, use the
[[css/properties/counter-reset|'''counter-reset''']]
attribute.
An element that is not displayed
([[css/properties/display|'''display''']]
attribute set to 'none') and pseudo-elements that do not generate content
([[css/properties/content|'''content''']]
attribute set to 'normal') cannot increment or reset a counter.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>'''counter-increment: ''''''[''' ''
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
*<code>[[css/properties/counter-reset|counter-reset]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}