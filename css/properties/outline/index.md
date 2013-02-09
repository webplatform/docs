{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The CSS <code>outline</code> property is a shorthand property for setting one or more of the individual outline properties [[css/properties/outline-style|outline-style]], [[css/properties/outline-width|outline-width]] and [[css/properties/outline-color|outline-color]] in a single rule. In most cases the use of this shortcut is preferable and more convenient.}}
{{CSS_Selector
|Content=Outlines differ from [[css/properties/border|borders]] in the following ways:

* Outlines do not take up space, they are drawn above the content.
* Outlines may be non-rectangular. They are rectangular in Gecko/Firefox. But e.g. Opera draws a non-rectangular shape around a construct like this:

<strong style="color: orange; outline: 1px dotted;">TEXT<span style="font-size: xx-large;">TEXT</span>TEXT</strong>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Remove the outline of a link on hover
|Code=a:hover { outline: 0; }
}}{{Single Example
|Language=CSS
|Code=:focus { outline: solid; } /* outline-width and outline-color are the default ones when nothing but the outline-style is specified */

:focus { outline: dashed red; } /* outline-style and outline-color */

:focus { outline: dashed 1px; } /* outline-style and outline-width */

:focus { outline: ridge thick violet; } /* outline-style, outline-width and outline-color */
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
<code>outline:  [ &lt;outline-width&gt; {{!}}{{!}} &lt;outline-style&gt; {{!}}{{!}} &lt;outline-color&gt; ] {{!}} inherit</code>

===Standards information===
*[http://www.w3.org/TR/CSS2/ui.html#dynamic-outlines CSS 2.1], Section 18.4
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
|Topic_clusters=Visual Effects
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}