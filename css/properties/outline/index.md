{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Selector
|Content=
}}
{{Topics|CSS}}
{{Notes_Section
|Notes=
===Remarks===
Displaying an outline does not cause reflow, no matter how wide the
outline is. The outline frame is drawn over an element, and does
not influence the position or size of the box, or of any other boxes.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes=
===Syntax===
<code>'''outline: ''''''[''' color '''{{!}}{{!}}''' style '''{{!}}{{!}}''' width ''']'''</code>
===Example===
<code> div { outline:1px solid #000; }</code>
===Standards information===
*[http://www.w3.org/TR/CSS2/ui.html#dynamic-outlines CSS 2.1], Section 18.4


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/selectors/outline-color|outline-color]]</code>
*<code>[[css/selectors/outline-style|outline-style]]</code>
*<code>[[css/selectors/outline-width|outline-width]]</code>
|Topic_clusters=Visual Effects
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}