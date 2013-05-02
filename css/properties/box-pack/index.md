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
|Initial value=start
|Applies to=box elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=start
|Description=The starting edge of the first child element is placed at the start of the parent element; the starting edge of the next child element is placed edge to edge with the ending edge of the first child element; and so on along the layout axis direction. All space that remains along the layout axis is placed at the end of the layout axis.
}}{{CSS Property Value
|Data Type=end
|Description=The ending edge of the first child element is placed at the end of the parent element; the ending edge of the next child element is placed edge to edge with the starting edge of the first child element; and so on along the layout axis direction. All space remaining along the layout axis is placed at the start of the layout axis.
}}{{CSS Property Value
|Data Type=center
|Description=All child elements are placed edge to edge with each other, as described in the descriptions for the [#start start] or [#end end] keywords. However, the group of child elements is centered between the starting and ending edges of the parent element so that all remaining space is evenly distributed before the first child element and after the last child element.
}}{{CSS Property Value
|Data Type=justify
|Description=The starting edge of the first child element is placed at the start of the parent element; the ending edge of the last child element is placed edge to edge with the end of the parent box; and all remaining children are placed between the first and last child elements, so that any space that remains along the layout axis is equally distributed between child elements.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Do not use. This property has been replaced by the [[-ms-flex-pack property]], and is no longer recognized by Windows Internet Explorer.

Be aware that these are [[css/properties/writing-mode|'''writing-mode''']] dependent keywords; the starting and ending edges of the parent element and child elements depend on the layout direction. For instance, for a left-to-right layout, the starting edge is the left edge of the parent element, for a top-to-bottom layout the starting edge is the top edge, and so on. Likewise, the ending edge of a child element is the right edge in a left-to-right layout, the bottom edge in a top-to-bottom layout, and so on.
|Import_Notes====Syntax===
<code>'''&#150;ms-box-pack: '''start '''{{!}}''' end '''{{!}}''' center '''{{!}}''' justify</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223142 Flexible Box Layout Module], Section 6
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
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}