{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Gets or sets a value that specifies how a flexbox's lines align within the flexbox when there is extra space along the axis that is perpendicular to the axis defined by the -ms-flex-direction property.

}}
{{CSS Property
|Initial value=stretch
|Applies to=flexbox elements
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
}}{{CSS Property Value
|Data Type=distribute
|Description=Lines are evenly distributed in the flexbox, with half-size spaces on either end. If the leftover free space is negative or there is only a single line in the flexbox, this value is identical to [#center center]. Otherwise, the lines in the flexbox are distributed such that the empty space between any two adjacent lines is the same, and the empty space before the first and after the last lines in the flexbox are half the size of the other empty spaces.
}}{{CSS Property Value
|Data Type=stretch
|Description=Lines stretch to take up the remaining space. If the leftover free space is negative, this value is identical to [#start start]. Otherwise, the free space is split equally between all of the lines, increasing their cross size.
}}
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=This property is read/write.
|Import_Notes====Syntax===
<code>'''-ms-flex-line-pack: '''start '''{{!}}''' end '''{{!}}''' center '''{{!}}''' justify '''{{!}}''' distribute '''{{!}}''' stretch</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}223142 Flexible Box Layout Module], Section 8.4
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