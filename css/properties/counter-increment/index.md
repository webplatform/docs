{{Page_Title}}
{{Flags
|High-level issues=Unreviewed Import
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The counter-increment property accepts one or more names of counters (identifiers), each one optionally followed by an integer which specifies the value by which the counter should be incremented (e.g. if the value is 2, the counter increases by 2 each time it is invoked). }}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=identifier
|Description=The name of the counter.  The counter can then be invoked by using '''counter(<identifier>)'''.
}}{{CSS Property Value
|Data Type=integer
|Description=An integer that indicates by how much the counter is
incremented for every occurrence of the element.
Zero and negative integers are allowed.  If no value is specified, the value defaults to 1.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=This example uses '''counter-increment''' and the '''content''' properties to prepend headers with an outline-esque, identifier, similar to an ordered list.  (Note that the numbering does not reset between the two headers: this can be handled with {{css/properties/counter-reset}}.)
|Code=/*
 * Using the CSS 'counter-increment' property.
 */

h1 {
	counter-increment: header;
}

h1:before {
 	content: counter(header) ". ";
}

h2 {
	counter-increment: subheader;
}

h2:before {
	content: counter(header) "." counter(subheader) ". ";
} 
|LiveURL=http://code.webplatform.org/gist/5841845
}}{{Single Example
|Language=CSS
|Description=This example shows how to specify an integer in the '''counter-increment''' property and allow the CSS to increment the counter by values besides 1.  
|Code=/*
 * Using the CSS 'counter-increment' property with a non-default increment JavaScript.
 */

/* In this example, we specify both an identifier and an integer -- the integer is the number
 * which the counter is increased by every time it is used.
 */
h1 {
	counter-increment: header 3;
}

/* Using the pseudo-element `:after`, we place the counter after each valid `h1` tag. */
h1:after {
 	content: counter(header) ". ";
}
|LiveURL=http://code.webplatform.org/gist/5841870
}}
}}
{{Notes_Section
|Usage=It is important to note that '''counter-increment''' can handle multiple counters and non-positive integers, though best practices often dictates that counters should be defined separately.
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