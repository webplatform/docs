{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_At_Rule
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
You can use the '''@-ms-viewport''' rule in tandem with media queries to help optimize your layout. Typically, you nest the '''@-ms-viewport''' rule inside the media query, as shown in the following pseudocode snippet:
<code>@media [media query logic here] {
@-ms-viewport {
[viewport properties here]
}
[CSS for this layout combination here]
}</code>
|Import_Notes=
===Syntax===
<code>'''@-ms-viewport '''{ ''viewport-properties'' }</code>
===Parameters===
;''viewport-properties'':One or more property declarations, each with a trailing semicolon. Only the following viewport properties are supported.<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"width"/><a id{{=}}"WIDTH"/><dl><dt>'''width'''</dt></dl></td><td width{{=}}"60%">Indicates the preferred viewport width used in determining the size of the initial containing block. Can be one of the following values:<dl><dt>'''auto'''</dt><dd>The value is calculated based on the display device's normal mode of operation.</dd><dt>'''device-width'''</dt><dd>The width of the screen in CSS pixels at a zoom factor of 100%.</dd><dt>'''device-height'''</dt><dd>The height of the screen in CSS pixels at a zoom factor of 100%.</dd><dt>''length''</dt><dd>A positive absolute or relative length.</dd><dt>''percentage''</dt><dd>A positive percentage value relative to the width or height of the initial viewport at a zoom factor of 100%, for horizontal and vertical lengths respectively. </dd></dl></td></tr><tr><td width{{=}}"40%"><a id{{=}}"height"/><a id{{=}}"HEIGHT"/><dl><dt>'''height'''</dt></dl></td><td width{{=}}"60%">Indicates the preferred viewport width used in determining the size of the initial containing block.  See '''width''' for  a list of possible values.</td></tr></table> 
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}233011 CSS Device Adaptation], Section 4


}}
{{See_Also_Section
|Topic_clusters=Syntax
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}