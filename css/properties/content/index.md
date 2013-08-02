{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The content property is used with the pseudo-elements ::before and ::after. }}
{{CSS Property
|Initial value=normal
|Applies to=pseudo-elements :before and :after
|Inherited=No
|Media=visual
|Computed value=On elements, always computes to 'normal'. On ::before and ::after, if 'normal' is specified, computes to 'none'; if ‘icon’ is specified, computes to ‘icon’. Otherwise, for URI values, the absolute URI; for attr() values, the resulting string; for other keywords, as specified.
|Animatable=Yes
|Values={{CSS Property Value
|Data Type=none
|Description=Pseudo element is not generated.
}}{{CSS Property Value
|Data Type=normal
|Description=Equivalent to "none" for :before and :after pseudo-elements, which are the only places the content property currently applies.
}}{{CSS Property Value
|Data Type=string
|Description=Text content, in either double quotation marks (") or single quotation marks (').
}}{{CSS Property Value
|Data Type=counter
|Description=Counters may be specified with two different functions: 
* 'counter()'  
Two forms: 'counter(name)' or 'counter(name, style)'. The generated text is the value of the innermost counter of the given name in scope at this pseudo-element; it is formatted in the indicated style ('decimal' by default). 
* 'counters()' 
Two forms: 'counters(name, string)' or 'counters(name, string, style)'. The generated text is the value of all counters with the given name in scope at this pseudo-element, from outermost to innermost separated by the specified string. 

The counters are rendered in the indicated style ('decimal' by default). The name must not be 'none', 'inherit' or 'initial'. Such a name causes the declaration to be ignored.
}}{{CSS Property Value
|Data Type=open-quote
|Description=Sets the content to be the appropriate string from the quotes property.
}}{{CSS Property Value
|Data Type=close-quote
|Description=Sets the content to be the appropriate string from the quotes property.
}}{{CSS Property Value
|Data Type=no-open-quote
|Description=If set, removes the opening quote from the content.
}}{{CSS Property Value
|Data Type=no-close-quote
|Description=If set, removes the closing quote from the content.
}}{{CSS Property Value
|Data Type=uri
|Description=URI designates an external resource, such as an image. If the user agent cannot display the resource it must either leave it out as if it were not specified or display some indication that the resource cannot be displayed.{{cn}} 
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example generates braces before and after
all the '''hn''' elements on a page.
|Code=&lt;meta http-equiv{{=}}"X-UA-Compatible" content{{=}}"IE{{=}}8" /&gt;
&lt;style type{{=}}"text/css"&gt;
H1:before {
    content: "{ ";
}
H1:after {
	content: " }";
}
&lt;/style&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
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
|Import_Notes====Syntax===
<code>'''content: ''''''[''' string '''{{!}}''' counter ''']''''''+'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 12.2
* CSS2.1 uses a single colon, and most browsers still support this. CSS3 introduces the use of double colons to avoid confusion with pseudo-classes.

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
|Topic_clusters=Generated and Replaced Content, Multi-Column
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/counter-increment|counter-increment]]</code>
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