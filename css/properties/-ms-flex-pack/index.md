{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Gets or sets a value that specifies how excess space is distributed (along the axis defined by the [[-ms-flex-direction]] property) between child elements of the object.

}}
{{CSS Property
|Initial value=start
|Applies to=flexbox elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=start
|Description=Initial value. Flexbox items are packed toward the start of the line. The starting edge of the first child element is placed at the start of the parent element; the starting edge of the next child element is placed edge to edge with the ending edge of the first child element; and so on along the layout axis direction. All space that remains along the layout axis is placed at the end of the layout axis.
}}{{CSS Property Value
|Data Type=end
|Description=Flexbox items are packed toward the end of the line. The ending edge of the first child element is placed at the end of the parent element; the ending edge of the next child element is placed edge to edge with the starting edge of the first child element; and so on along the layout axis direction. All space remaining along the layout axis is placed at the start of the layout axis.
}}{{CSS Property Value
|Data Type=center
|Description=Flexbox items are packed toward the center of the line. All child elements are placed edge to edge with each other, as described in the descriptions for the [#start start] or [#end end] keywords. However, the group of child elements is centered between the starting and ending edges of the parent element so that all remaining space is evenly distributed before the first child element and after the last child element.
}}{{CSS Property Value
|Data Type=justify
|Description=Flexbox items are evenly distributed in the line. The starting edge of the first child element is placed at the start of the parent element; the ending edge of the last child element is placed edge to edge with the end of the parent box; and all remaining children are placed between the first and last child elements, so that any space that remains along the layout axis is equally distributed between child elements.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=This property is read/write.

|Notes====Remarks===
Be aware that these are [[css/properties/writing-mode|'''writing-mode''']] dependent keywords; the starting and ending edges of the parent element and child elements depend on the layout direction. For instance, for a left-to-right layout, the starting edge is the left edge of the parent element, for a top-to-bottom layout the starting edge is the top edge, and so on. Likewise, the ending edge of a child element is the right edge in a left-to-right layout, the bottom edge in a top-to-bottom layout, and so on.
|Import_Notes====Syntax===
<code>'''-ms-flex-pack: '''start '''{{!}}''' end '''{{!}}''' center '''{{!}}''' justify</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223142 Flexible Box Layout Module], Section 8.1
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
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}