{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>‘font-language-override’</code> property allows authors to explicitly specify the language system of the font, overriding the language system implied by the content language.}}
{{CSS Property
|Initial value=normal
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=font
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=specifies that when rendering with OpenType fonts, the content language of the element is used to infer the OpenType language system
}}{{CSS Property Value
|Data Type=<string>
|Description=single three-letter case-sensitive OpenType language system tag, specifies the OpenType language system to be used instead of the language system implied by the language of the element
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=OpenType supports language-specific glyph selection and positioning, so that text can be displayed correctly in cases where the language dictates a specific display behavior. Authors can control the use of language-specific glyph substitutions and positioning by setting the content language of an element.

<code>&lt;!-- Display text using S'gaw Karen specific features --&gt;
&lt;p lang="ksw"&gt;...&lt;/p&gt;</code>
|Notes=Use of invalid OpenType language system tags must not generate a parse error but must be ignored when doing glyph selection and placement.
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
|Topic_clusters=CSS Font, Fonts, Text
|External_links=[http://www.microsoft.com/typography/otspec/languagetags.htm Microsoft OpenType Layout Tag Registry]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}