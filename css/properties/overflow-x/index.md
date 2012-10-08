{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=visible
|Description=Default. Content is not clipped and scroll bars are not added. Elements are clipped to the size of the containing window or frame.
}}{{CSS Property Value
|Data Type=scroll
|Description=Content is clipped and scroll bars are added, even if the content does not exceed the dimensions of the object.
}}{{CSS Property Value
|Data Type=hidden
|Description=Content that exceeds the dimensions of the object is not shown.
}}{{CSS Property Value
|Data Type=auto
|Description=Content is clipped and scrolling is added only when necessary.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8. The '''-ms-overflow-x''' attribute is an extension to CSS, and can be used as a synonym for '''overflow-x''' in IE8 Standards mode.
With Microsoft Internet Explorer 6 and later, when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, this property applies to the '''html''' object.
|Import_Notes====Syntax===
<code>'''-ms-overflow-x: '''visible '''{{!}}''' scroll '''{{!}}''' hidden '''{{!}}''' auto</code>
===Standards information===
There are no standards that apply here.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/overflow|overflow]]</code>
*<code>[[css/properties/overflow-y|-ms-overflow-y]]</code>
*<code>[[css/properties/position|position]]</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}