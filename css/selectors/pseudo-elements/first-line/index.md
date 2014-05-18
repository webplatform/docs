{{Page_Title|::first-line}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Represents the first line of an element. Note that the content of the first line varies depending on the available width and the styling of text (size, spacing).}}
{{CSS_Selector
|Content====Syntax===
{{Single Example
|Language=CSS
|Code=::first-line {}
}}
===Usage===
The ::first-line pseudo-element can be attached to block-level elements. It can be attached to inline elements if you set the corresponding display property to block.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example puts the first line of any paragraph in bold text
|Code=p::first-line {
	font-weight: bold;
}
|LiveURL=https://code.webplatform.org/gist/fe1382a764e07a9c7917
}}
}}
{{Notes_Section
|Notes====Remarks===
The [[css/cssom/properties/background|'''background''']], [[css/properties/clear|'''clear''']], [[css/properties/color|'''color''']], [[css/properties/font|'''font''']], 
[[css/properties/font-family|'''font-family''']], [[css/properties/font-size|'''font-size''']], [[css/properties/font-style|'''font-style''']], [[css/fonts/font-variant|'''font-variant''']], [[css/properties/font-weight|'''font-weight''']], 
[[css/properties/line-height|'''line-height''']], [[css/properties/text-decoration|'''text-decoration''']], 
[[css/properties/text-transform|'''text-transform''']], [[css/properties/vertical-align|'''vertical-align''']], and [[css/text/word-spacing/word-spacing|'''word-spacing''']] properties apply to the '''::first-line''' pseudo-element.


|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.12.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=< 9
|Note=Only the one-colon form of this pseudo-element is recognized—that is, ''':first-line'''. Beginning with Internet Explorer 9, the '''::first-line''' pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form.
}}
}}
{{See_Also_Section
|Topic_clusters=Pseudo-Elements, Selectors
|Manual_sections====Related pages (MSDN)===
*<code>[[css/selectors/pseudo-elements/::first-letter|::first-letter]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}