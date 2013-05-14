{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Summary_Section|The outline-color CSS property sets the color of the [[css/properties/outline|outline]] of an element. An outline is a line that is drawn around elements, outside the border edge, to make the element stand out.}}
{{CSS Property
|Initial value=medium
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=absolute length; ‘0’ if the outline style is ‘none’.
|Animatable=Yes
|CSS object model property=outlineWidth
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=medium
|Description=Default.  
}}{{CSS Property Value
|Data Type=thin
|Description=Less than the default width.
}}{{CSS Property Value
|Data Type=thick
|Description=Greater than the default width.
}}{{CSS Property Value
|Data Type=<width>
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=inherit
|Description=This is a keyword indicating that all four values are inherited from their parent's element calculated value.
}}
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
Displaying an outline does not cause reflow, no matter how wide the
outline is. The outline frame is drawn over an element, and does
not influence the position or size of the box, or of any other boxes.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 UI, 7.2. ‘outline-width’ property
|URL=http://dev.w3.org/csswg/css-ui/#outline-width0
|Status=Working Draft
}}{{Related Specification
|Name=CSS 2.1, 18.4 Dynamic outlines: the 'outline' property
|URL=http://www.w3.org/TR/CSS2/ui.html#dynamic-outlines
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/selectors/outline|outline]]</code>
*<code>[[css/selectors/outline-color|outline-color]]</code>
*<code>[[css/selectors/outline-style|outline-style]]</code>
|Topic_clusters=Visual Effects
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}