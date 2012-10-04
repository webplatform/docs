{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=
|Values={{CSS_Property_Value|Data Type=horizontal |Description=Default. Content in the object flows from left to right, and the next horizontal line is positioned underneath the previous line.  This layout is used in most Roman-based documents.}}
{{CSS_Property_Value|Data Type=vertical-ideographic |Description=Content in the object flows from top to bottom, and the next vertical line appears to the left of the previous one.  This layout is used in East Asian typography.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8. The '''-ms-layout-flow''' attribute is an extension to CSS, and can be used as a synonym for '''layout-flow''' in IE8 Standards mode.
This is a deprecated property; use the [[css/properties/writing-mode|'''-ms-writing-mode''']] property instead.
This property is read-only for the
.
|Import_Notes=
===Syntax===
<code>'''-ms-layout-flow: '''horizontal '''{{!}}''' vertical-ideographic</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/writing-mode|-ms-writing-mode]]</code>
*<code>Other Resources</code>
*<code>[http://go.microsoft.com/fwlink/p/?linkid{{=}}203735 International Layout in CSS]</code>
|Topic_clusters=Text
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}