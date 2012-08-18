{{Flags
|High-level issues=Stub
|Content=Outdated, Incomplete, Needs Best Practices
|Compatibility=Missing
|Examples=Examples have errors
}}
{{CSS Property
|Summary=The <code>font-size</code> CSS properties specifies the size of the font used for text in the object. Setting the font size may, in turn, change the size of other items, since it is used to compute the value of <code>em</code> and <code>ex</code> length units.
|Initial value=medium
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=absolute length
|Animatable=No
|CSS object model property=fontSize
|CSS percentages=Relative to parent element's font size
|Values={{CSS Property Value
|Data Type=xx-small, x-small, small, medium, large, x-large, xx-large
|Description=A set of absolute size keywords based on the user's default font size (which is medium). Similar to presentational HTML's &lt;font size="1"> through &lt;font size="7"> where the user's default font size is &lt;font size="3">.
}}{{CSS Property Value
|Data Type=larger, smaller
|Description=Larger or smaller than the parent element's font size, by roughly the ratio used to separate the absolute size keywords above.
}}{{CSS Property Value
|Data Type=length
|Description=A positive length. When the units are specified in em or ex,  the size is defined relative to the size of the font on the parent element of the element in question. For example, 0.5em is half the font size of the parent of the current element.
}}{{CSS Property Value
|Data Type=percentage
|Description=A positive percentage of the parent element's font size.
}}
|Syntax=font-size: xx-small
|Value_Name=percentage
}}