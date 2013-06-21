{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS Property
|Initial value=horizontal-tb
|Applies to=All elements except table row groups, table column groups, table rows, and table columns
|Inherited=Yes
|Media=visual
|Computed value=specified value
|Animatable=No
|CSS object model property=writingMode
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=lr-tb
|Description=Default. Content flows horizontally from left to right, top to bottom. The next horizontal line is positioned underneath the previous line. All glyphs are positioned upright. This layout is used by most writing systems.
}}{{CSS Property Value
|Data Type=rl-tb
|Description=Content flows horizontally from right to left, top to bottom. The next horizontal line is positioned underneath the previous line. All glyphs are positioned upright. This layout is used with right-to-left scripts like Arabic, Hebrew, Thaana, and Syriac.
}}{{CSS Property Value
|Data Type=tb-rl
|Description=Content flows vertically from top to bottom, right to left. The next vertical line is positioned to the left of the previous line. Wide-cell glyphs are positioned upright; nonwide-cell glyphs (also known as narrow Latin or narrow Kana glyphs) are rotated 90° clockwise. This layout is used in East Asian typography.
}}{{CSS Property Value
|Data Type=bt-rl
|Description=Content flows vertically from bottom to top, right to left. The next vertical line is positioned to the left of the previous line. Wide-cell glyphs are positioned upright; nonwide-cell glyphs (also known as narrow Latin or narrow Kana glyphs) are rotated 90° clockwise. This layout is used for right-to-left script blocks used in vertical East Asian typography.
}}{{CSS Property Value
|Data Type=tb-lr
|Description=Internet Explorer 8. Content flows vertically from top to bottom, left to right. The next vertical line is positioned to the right of the previous line.
}}{{CSS Property Value
|Data Type=bt-lr
|Description=Internet Explorer 8.	Content flows vertically from bottom to top, left to right.
}}{{CSS Property Value
|Data Type=lr-bt
|Description=Internet Explorer 8. Content flows horizontally from bottom to top, left to right. The next horizontal line is positioned above the previous line.
}}{{CSS Property Value
|Data Type=rl-bt
|Description=Internet Explorer 8. Content flows horizontally from bottom to top, right to left.
}}{{CSS Property Value
|Data Type=lr
|Description=Internet Explorer 9. For use on SVG and HTML elements. Equivalent to '''lr-tb'''.
}}{{CSS Property Value
|Data Type=rl
|Description=Internet Explorer 9. For use on SVG and HTML elements. Equivalent to '''rl-tb'''.
}}{{CSS Property Value
|Data Type=tb
|Description=Internet Explorer 9. For use on SVG and HTML elements. Equivalent to '''tb-rl'''.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''-ms-writing-mode''' property to nest horizontal text inside vertical text.
|Code=&lt;html&gt;&lt;head&gt;&lt;style&gt;
    .clsHorizLR { writing-mode:lr-tb }
    .clsHorizRL { writing-mode:rl-tb }
    .clsVertTB  { writing-mode:tb-rl }
    .clsVertBT  { writing-mode:bt-rl }
&lt;/style&gt;&lt;/head&gt;&lt;body&gt;
&lt;h1&gt;writing-mode Attribute&lt;/h1&gt;
&lt;p&gt;This example shows how to use the &lt;b&gt;writing-mode&lt;/b&gt; attribute to display horizontal text (&lt;span&gt;lr-tb&lt;/span&gt;) 
within vertical text (&lt;span&gt;tb-rl&lt;/span&gt;).&lt;/p&gt;
&lt;p&gt;The following &lt;b&gt;div&lt;/b&gt; element has a &lt;b&gt;writing-mode&lt;/b&gt; of tb-rl and contains text and &lt;b&gt;span&lt;/b&gt; child elements. 
The text flow alternates between vertical and horizontal. Be aware of the effect of the &lt;b&gt;BR&lt;/b&gt; element after the second 
set of vertical text.&lt;/p&gt;
&lt;div style{{=}}"writing-mode:tb-rl"&gt;First Set of Vertical Text&lt;span class{{=}}"clsHorizLR"&gt;First Set of Horizontal Text&lt;/span&gt;
Second Set of Vertical Text plus a line break&lt;BR&gt;&lt;span style{{=}}"writing-mode:lr-tb"&gt;Second Set of Horizontal Text&lt;/span&gt;
Third Set of Vertical Text&lt;span class{{=}}"clsHorizLR"&gt;Third Set of Horizontal Text&lt;/span&gt;
&lt;/div&gt;&lt;p&gt;This example shows how to use the new &lt;b&gt;writing-mode&lt;/b&gt; attribute to display horizontal text (&lt;span&gt;rl-tb&lt;/span&gt;).&lt;div class{{=}}"clsHorizRL"&gt;Fourth Set of Horizontal Text&lt;/div&gt;&lt;p&gt;This example makes use of the new&lt;b&gt;writing-mode&lt;/b&gt; attribute to display vertical text (&lt;span&gt;bt-rl&lt;/span&gt;).&lt;div class{{=}}"clsVertBT"&gt;Fourth Set of 
Vertical Text&lt;/div&gt;
&lt;/div&gt;&lt;/body&gt;&lt;/html&gt;
|LiveURL=Click to view sample.
}}
}}
{{Notes_Section
|Notes====Remarks===
The following diagram shows how the different values for the property appear on the screen.

Internet Explorer 8. The '''-ms-writing-mode''' attribute is an extension to CSS and can be used as a synonym for '''writing-mode''' in IE8 Standards mode.
The property does not accumulate.  That is, even if the '''-ms-writing-mode''' property, set to the same value, is applied to an object multiple times, the '''-ms-writing-mode''' property is effectively applied to the object only one time. For example, if a parent element has the '''-ms-writing-mode''' property set to '''tb-rl''', setting a child element's '''-ms-writing-mode''' property to '''tb-rl''' does not cause the child element to double the effect of the '''-ms-writing-mode''' property, or "rotate."
An element has its own layout if the value for the '''-ms-writing-mode''' property is different than its parent. When a change in layout flow is specified for a child element, the maximum logical height requirement (height in this element's coordinate system) is determined by the available space (width measurement) in the parent's coordinate system.  Based on this information, a logical width (width in the child's coordinate system) is computed to meet the maximum logical height requirement.  Depending on the amount of space needed by the child element, the actual logical height of the element can be less than the maximum logical height requirement.
When you use elements that have different values for the '''-ms-writing-mode''' property, you can have greater control over the layout of those elements by specifying fixed dimensions for each element.
Windows Internet Explorer 7.  The '''rl-tb''', and '''bt-rl''' values are available to the '''-ms-writing-mode'''.
Internet Explorer 7.  The '''-ms-writing-mode''' for the '''body''' element is limited to '''lr-tb''' and '''rl-tb'''.
Internet Explorer 8. Because '''-ms-writing-mode''' is currently defined by the World Wide Web Consortium (W3C) in a draft specification, '''-ms-writing-mode''' is preferred for style sheet validation, as in the following code example.
 <code>    .clsHorizLR { -ms-writing-mode:lr-tb }
     .clsHorizRL { -ms-writing-mode:rl-tb }
     .clsVertTB  { -ms-writing-mode:tb-rl }
     .clsVertBT  { -ms-writing-mode:bt-rl }</code>
|Import_Notes====Syntax===
<code>'''-ms-writing-mode: '''lr-tb '''{{!}}''' rl-tb '''{{!}}''' tb-rl '''{{!}}''' bt-rl '''{{!}}''' tb-lr '''{{!}}''' bt-lr '''{{!}}''' lr-bt '''{{!}}''' rl-bt '''{{!}}''' lr '''{{!}}''' rl '''{{!}}''' tb</code>
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Writing Modes Module Level 3
|URL=http://www.w3.org/TR/css3-writing-modes/#writing-mode
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Layout
|Manual_links=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
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