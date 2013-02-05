{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The overflow property controls how extra text  exceeding the bounding box of an element is rendered. The overflow property can be used in conjunction with an element that has a fixed width and height, to eliminate text-induced page distortion.}}
{{CSS Property
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=visible
|Description=Default. Content is not clipped and scroll bars are not added.
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
The default value for the '''body''' element is '''auto'''.
Setting the '''overflow''' property to '''hidden''' on a '''textArea''' object hides its scroll bars.
Setting the '''overflow''' property to '''visible''' causes the content to clip to the size of the window or frame that contains the object.
With Microsoft Internet Explorer 6 and later, when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, this property applies to the '''html''' object.
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
|Topic_clusters=Box Model, Visual Effects
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/properties/overflow-x|-ms-overflow-x]]</code>
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