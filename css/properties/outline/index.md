{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{CSS_Selector}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=div { outline:1px solid #000; }
}}
}}
{{Notes_Section
|Notes====Remarks===
Displaying an outline does not cause reflow, no matter how wide the
outline is. The outline frame is drawn over an element, and does
not influence the position or size of the box, or of any other boxes.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>'''outline: ''''''[''' color '''{{!}}{{!}}''' style '''{{!}}{{!}}''' width ''']'''</code>

===Standards information===
*[http://www.w3.org/TR/CSS2/ui.html#dynamic-outlines CSS 2.1], Section 18.4
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
|Topic_clusters=Visual Effects
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>[[css/selectors/outline-color|outline-color]]</code>
*<code>[[css/selectors/outline-style|outline-style]]</code>
*<code>[[css/selectors/outline-width|outline-width]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}