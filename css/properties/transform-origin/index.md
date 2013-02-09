{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Allows you to change the position on transformed elements.}}
{{CSS Property
|Initial value=50% 50%
|Applies to=transformable elements
|Inherited=No
|Media=visual
|Computed value=For <length> the absolute value, otherwise a percentage 
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=A floating-point number, followed by either an absolute units designator
(<code>cm</code>,
<code>mm</code>,
<code>in</code>,
<code>pt</code>,
or <code>pc</code>)
or a relative units designator
(<code>em</code>,
<code>ex</code>,
or <code>px</code>), that indicates the origin of transformation.
For more information about the supported length units,
see CSS Values and Units.
}}{{CSS Property Value
|Data Type=percentage
|Description=An integer, followed by a %. The value is a percentage of the total box length (for the first value) or the total box height (for the second value, if specified).
}}{{CSS Property Value
|Data Type=left
|Description=First value only. Equal to 0% or a zero length.
}}{{CSS Property Value
|Data Type=center
|Description=First value only. Equal to 50% or half the length of the box.
}}{{CSS Property Value
|Data Type=right
|Description=First value only. Equal to 100% or the full box length.
}}{{CSS Property Value
|Data Type=top
|Description=Second value only. Equal to 0% or a zero height.
}}{{CSS Property Value
|Data Type=center
|Description=Second value only. Equal to 50% or a half the height of the box.
}}{{CSS Property Value
|Data Type=bottom
|Description=Second value only. Equal to 100% or the full box height.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The version of this property using a vendor prefix, '''-ms-transform-origin''', has been deprecated in Internet Explorer 10 and later. To ensure compatibility in the future, applications using this property with a vendor prefix should be updated accordingly. However, be aware that '''-ms-transform-origin''' is the only form of this property that is recognized by Windows Internet Explorer 9, which supports 2-D Cascading Style Sheets (CSS) transforms.
If the '''transform-origin''' property is not set, the transform begins in the center (equal to a '''transform-origin''' value of <code>50% 50%</code>).
If only one value is specified, the second value is assumed to be <code>center</code>.
3-D transforms are only supported in Internet Explorer 10 and later.
|Import_Notes====Syntax===
<code>'''transform-origin: ''''''[''' '''[''' '''[''' ''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' left '''{{!}}''' center '''{{!}}''' right ''']''' '''[''' ''
&lt;percentage&gt;
'' '''{{!}}''' ''
&lt;length&gt;
'' '''{{!}}''' top '''{{!}}''' center '''{{!}}''' bottom ''']''' ? ''']''' ''
&lt;length&gt;
'' ''']''' '''{{!}}''' '''[''' '''[''' '''[''' left '''{{!}}''' center '''{{!}}''' right ''']''' {{!}}{{!}} '''[''' top '''{{!}}''' center '''{{!}}''' bottom ''']''' ''']''' ''
&lt;length&gt;
'' ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?LinkID{{=}}223145 CSS Transforms Module, Level 3], Section 8
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=22.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=15.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Transforms
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/transforms/transform|transform]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}