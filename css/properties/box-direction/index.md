{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=normal
|Applies to=box elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=normal
|Description=Default. 
Child elements are displayed in the same order that they are declared in the source document. 

If the parent element has a computed value for [[css/properties/ms-box-orient|'''-ms-box-orient''']] of <code>horizontal</code>, the child elements are displayed from left to right. 

If the parent element has a computed value for [[css/properties/ms-box-orient|'''-ms-box-orient''']] of <code>vertical</code>, the child elements are displayed from top to bottom.
}}{{CSS Property Value
|Data Type=reverse
|Description=Child elements are displayed in the reverse order that they are declared in the source document. 

If the parent element has a computed value for [[css/properties/ms-box-orient|'''-ms-box-orient''']] of <code>horizontal</code>, the child elements are displayed from right to left. 

If the parent element has a computed value for [[css/properties/ms-box-orient|'''-ms-box-orient''']] of <code>vertical</code>, the child elements are displayed from bottom to top.
}}{{CSS Property Value
|Data Type=inherit
|Description=Child elements are displayed in the same order as the computed value of this property for the parent element.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Do not use. This property has been replaced by the [[-ms-flex-direction]] property, and is no longer recognized by Windows Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly. Gets or sets a value that specifies the display order (along the axis defined by the [[-ms-box-orient]] property) of all child elements of the object.

This property is read/write.

|Import_Notes====Syntax===
<code>'''-ms-box-direction: '''normal '''{{!}}''' reverse '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223142 Flexible Box Layout Module], Section 3
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