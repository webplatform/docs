{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Deprecated}}
{{CSS Property
|Initial value=single
|Applies to=box elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. 
Successive rows or columns of child elements flow in the direction specified by the [[css/properties/writing-mode|'''writing-mode''']] and [[css/properties/ms-box-lines|'''-ms-box-lines''']] properties.
}}{{CSS Property Value
|Data Type=reverse
|Description=Successive rows or columns of child elements flow in the reverse direction specified by the [[css/properties/writing-mode|'''writing-mode''']] and [[css/properties/ms-box-lines|'''-ms-box-lines''']] properties.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Do not use. This property has been replaced by the [[-ms-flex-wrap]] property, and is no longer recognized by Windows Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly. Gets or sets a value that specifies the direction to add successive rows or columns when the value of [[-ms-box-lines]] is set to multiple.

This property is read/write.
|Import_Notes====Syntax===
<code>'''-ms-box-line-progression: '''normal '''{{!}}''' reverse</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223142 Flexible Box Layout Module]
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
|Topic_clusters=Flexbox
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}