{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=No
|Initial value=
|Values={{CSS_Property_Value|Data Type=string |Description=Text content, in either double quotation marks (")
or single quotation marks (').}}
{{CSS_Property_Value|Data Type=counter |Description=Possible values include the following:}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example generates braces before and after
all the '''hn''' elements on a page.
|LiveURL=
|Code=
&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
&lt;style type{{=}}"text/css"&gt;
H1:before {
    content: "{ ";
}
H1:after {
	content: " }";
}
&lt;/style&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''content'''
attribute is used in conjunction with
[[css/selectors/pseudo-elements/::before|'''::before''']] and
[[css/selectors/pseudo-elements/::after|'''::after''']] pseudo-classes
to generate content in a document.
Strings can written with either double quotation marks (") or
with single quotation marks ('). Double quotation marks cannot occur
inside other double quotation marks, unless they are preceded by
a backslash (\) escape character. For example, the string
<code>"\""</code> is interpreted as containing
one double quotation character.
It is possible to break strings over several lines, for esthetic or
other reasons, by use of the backslash as a continuation character;
however, the newline character itself is ignored.
Authors may include line breaks in the generated content
by writing the <code>\A</code> escape sequence in any
of the strings after the
'''content'''
property. The generated line break is displayed in accordance
with the value of the
[[css/properties/white-space|'''white-space''']]
attribute.
The backslash is also used to generate escape characters that
cannot be represented in the current character encoding.
In this case, the backslash is followed by at most
six hexadecimal digits (from the range 0–9 and A–F)
to indicate the	Unicode character with that number.
This property requires Windows Internet Explorer
to be in IE8 Standards mode rendering.
|Import_Notes=
===Syntax===
<code>'''content: ''''''[''' string '''{{!}}''' counter ''']''''''+'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 12.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/counter-increment|counter-increment]]</code>
*<code>[[css/properties/counter-reset|counter-reset]]</code>
|Topic_clusters=Generated and Replaced Content, Multi-Column
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}