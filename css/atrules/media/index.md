{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets the media types for a set of rules in a [[css/cssom/properties/styleSheet|styleSheet]] object.}}
{{CSS_At_Rule}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following example,  the '''@media''' rule is used to specify the [[css/properties/font-size|'''font-size''']] attribute of the '''body''' element for two media types.
|Code=// For computer screens, the font size is 12pt.
@media screen {
   BODY {font-size:12pt;}
}
// When printed, the font size is 8pt.
@media print {
   BODY {font-size:8pt;}
}
}}{{Single Example
|Description=The following declaration is a typical media query. In this case, <code>screen</code> indicates the target media type, and <code>max-width</code> is the target media property. The declaration states that the specified rules (no border on '''div''' elements) are only to be applied when the page is displayed on a screen in a browser window with a width of at most 400 pixels.
|Code=@media screen and (max-width:400px) {
   div {border:none;}
}
}}{{Single Example
|Description=You can use media properties together to create even more specific queries, such as the following. This declaration applies the specified rules when the medium is a screen and the browser window has a width of no more than 400 pixels ''and'' a height of no more than 600 pixels.
|Code=@media screen and (max-width:400px) and (max-height:600px) {
   ...
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The rule has no default value.
Dynamic HTML (DHTML) expressions can be used in place of the preceding value(s). As of Windows Internet Explorer 8, expressions are not supported in IE8 Standards mode. For more information, see About Dynamic Properties.
Windows Internet Explorer 9 introduces support for media queries. Media queries enable you to scope a style sheet to a set of precise device capabilities. For instance, you might want to design pages differently for users browsing on a mobile device (that has a very small screen, limited color palette, low resolution, and so on) versus a netbook (that has a small screen, full color palette, high resolution, and so on) versus a standard computer (that has a large screen, full color palette, high resolution, and so on).
A media query consists of a media type (''sMediaType'') and zero or more expressions (''sMediaFeatures'') that check for the conditions of particular media features. A media query is a logical expression that is either true or false. A media query is true if the media type of the media query matches the media type of the computer on which Windows Internet Explorer is running, and all expressions in the media query are true. The following media features are supported:
*[[css/media queries/width|width]]
*[[css/media queries/height|height]]
*[[css/media queries/device-width|device-width]]
*[[css/media queries/device-height|device-height]]
*[[css/media queries/orientation|orientation]]
*[[css/media queries/aspect-ratio|aspect-ratio]]
*[[css/media queries/device-aspect-ratio|device-aspect-ratio]]
*[[css/media queries/colors by|color]]
*[[css/media queries/color-index|color-index]]
*[[css/media queries/monochrome|monochrome]]
*[[css/media queries/resolution|resolution]]
|Import_Notes====Syntax===
<code>'''@media '''''sMediaType'' { ''Media-Rule'''''+''' }</code>
'''Media-Rule'''
<code>'''@media '''''sRules''</code>
===Parameters===
;''sMediaType'':'''String''' that specifies one of the following media types:<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"screen"/><a id{{=}}"SCREEN"/><dl><dt>'''screen'''</dt></dl></td><td width{{=}}"60%">Output is intended for computer screens.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"print"/><a id{{=}}"PRINT"/><dl><dt>'''print'''</dt></dl></td><td width{{=}}"60%">Output is intended for printed material and for documents viewed in Print Preview mode.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"all"/><a id{{=}}"ALL"/><dl><dt>'''all'''</dt></dl></td><td width{{=}}"60%">Output is intended for all devices.</td></tr></table> 
;''sRules'':'''String''' that specifies one or more rules in a [[css/cssom/styleSheet|'''styleSheet''']] object.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0 - 28.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5 - 21.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9 and 10
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=5.5 - 8.0 with polyfill
|Opera_supported=Yes
|Opera_version=9.5 - 12.1
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4.0 - 6.0
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=Partial support for 3.1 and 3.2
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1 - 4.2
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0 and 10.0 
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=25.0
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=19.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10.0 - 12.1 
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0 - 7.0 
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2 - 6.2 
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Syntax
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/properties/media|media]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}