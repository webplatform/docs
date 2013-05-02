{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
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
|Data Type=single
|Description=Default. 
All child elements are displayed in a single row or column. The [[css/properties/overflow|'''overflow''']] property of the object determines whether the child elements are hidden, clipped, or scrollable.
}}{{CSS Property Value
|Data Type=multiple
|Description=Child elements are wrapped and displayed in successive, parallel rows or columns. The object expands in height or width, perpendicular to the axis defined by the [[css/properties/ms-box-orient|'''-ms-box-orient''']] property, to accommodate the additional rows or columns.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Do not use. This property has been replaced by the [[-ms-flex-wrap]] property, and is no longer recognized by Windows Internet Explorer. To ensure compatibility in the future, applications using this property should be updated accordingly. Gets or sets a value that specifies whether child elements wrap onto multiple lines or columns based on the space available in the object. 

This property is read/write.
|Notes====Remarks===
Each child element is resized to its minimum width or height before the object is resized to accomodate additional rows or columns.
Each successive rows is inserted below the previous row when [[css/properties/ms-box-direction|'''-ms-box-direction''']] is set to <code>normal</code> or above the previous row when '''-ms-box-direction''' is set to <code>reverse</code>.
Each successive column is inserted to the right of the previous column when [[css/properties/ms-box-direction|'''-ms-box-direction''']] is set to <code>normal</code> or to the left of the previous column when '''-ms-box-direction''' is set to <code>reverse</code>.
|Import_Notes====Syntax===
<code>'''-ms-box-lines: '''single '''{{!}}''' multiple</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223142 Flexible Box Layout Module], Section 7
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