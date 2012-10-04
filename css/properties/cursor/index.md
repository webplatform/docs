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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''cursor''' attribute and the '''cursor''' property to change the cursor as it passes over an object.

This example uses a call to an embedded (global) style sheet to set the cursor to '''hand''' as the cursor passes over all paragraphs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cursor_h.htm
|Code=
&lt;STYLE&gt;
    P { cursor : hand; }
&lt;/STYLE&gt;
}}
{{Single_Example
|Description=This example uses inline scripting to set the cursor to '''hand''' as the cursor passes over the paragraph.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cursor_s.htm
|Code=
&lt;P onmouseover{{=}}"this.style.cursor{{=}}'hand'"&gt;
}}
{{Single_Example
|Description=This example demonstrates setting a custom cursor, by using the '''url(uri)''' value.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cursor_c.htm
|Code=
&lt;STYLE&gt;
oBox.style.cursor {{=}} "url(" + Some_Uniform_Resource_Identifier + ")";
&lt;/STYLE&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The property handles a comma-separated list of cursor values. If the user agent does not understand or cannot find the first cursor specified, it looks at the next cursor in the comma-separated list and continues until it finds a usable cursor. If the user agent does not understand any of the cursors that are listed, the cursor does not change.
In Internet Explorer 6, The cursor property supports <code>progress, not-allowed, no-drop, vertical-text, all-scroll, col-resize, row-resize,</code> and <code>url(uri)</code> as new cursor styles.
Cursors support many shape, color and movement combinations.  This permits you to subtitute the default cursors with your preferred design.  For instance, you may want your company logo to display as the "progress" cursor;  or your country's flag waving in the wind to display as the "wait" cursor.
Cursors have been the subject of security bulletins and updates.  If your custom cursors are not behaving as expected, examine the security settings for your browser along with your cursors.  This is a common issue with animated cursors.  For an example, refer to [http://go.microsoft.com/fwlink/p/?linkid{{=}}203632 TechNet Security Resources] and search for "Microsoft Security Bulletin MS05-002".
|Import_Notes=
===Syntax===
<code>'''cursor: '''all-scroll '''{{!}}''' auto '''{{!}}''' col-resize '''{{!}}''' crosshair '''{{!}}''' default '''{{!}}''' hand '''{{!}}''' help '''{{!}}''' move '''{{!}}''' no-drop '''{{!}}''' not-allowed '''{{!}}''' pointer '''{{!}}''' progress '''{{!}}''' row-resize '''{{!}}''' text '''{{!}}''' url(uri) '''{{!}}''' vertical-text '''{{!}}''' wait '''{{!}}''' *-resize</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 18.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|Topic_clusters=Visual Effects
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}