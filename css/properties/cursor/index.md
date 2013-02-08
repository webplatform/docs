{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The cursor CSS property specifies the mouse cursor displayed when the mouse pointer is over an element.}}
{{CSS Property
|Initial value=auto
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=as specified (if a keyword)
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=url [x, y]
|Description=Optional.
A <code>url(…)</code> or a comma separated list <code>url(…), url(…), …</code> , pointing to an image file. More than one <code><uri></code> may be provided as fallback, in case some cursor image types are not supported. A non-URL fallback (one ore more of the other values) must be at the end of the fallback list. See Using URL values for the cursor property for more details.

The <x>, <y> values are optional and experimental. Two unit-less numbers.
}}{{CSS Property Value
|Data Type=standard values
|Description=There are many standard cursors available.
'''''Available standard cursors''''': 
auto, default, none, context-menu, help, pointer, progress, wait, cell, crosshair, text, vertical-text, alias, copy, move, no-drop, not-allowed, e-resize, n-resize, ne-resize, nw-resize, s-resize, se-resize, sw-resize, w-resize, ew-resize, ns-resize, nesw-resize, nwse-resize, col-resize, row-resize, all-scroll, zoom-in, zoom-out

Check out the Examples.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''cursor''' attribute and the '''cursor''' property to change the cursor as it passes over an object.

This example uses a call to an embedded (global) style sheet to set the cursor to '''hand''' as the cursor passes over all paragraphs.


<div style="background: grey; cursor: help; padding: 1em; border-radius: 4px; color: white;">cursor: help</div>
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cursor_h.htm
}}{{Single Example
|Description=This example uses inline scripting to set the cursor to '''hand''' as the cursor passes over the paragraph.
|Code=&lt;div onmouseover{{=}}"this.style.cursor{{=}}'hand'"&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cursor_s.htm
}}{{Single Example
|Description=This example demonstrates setting a custom cursor, by using the '''url(uri)''' value.
|Code=&lt;style&gt;
oBox.style.cursor {{=}} "url(" + Some_Uniform_Resource_Identifier + ")";
&lt;/style&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/cursor_c.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The property handles a comma-separated list of cursor values. If the user agent does not understand or cannot find the first cursor specified, it looks at the next cursor in the comma-separated list and continues until it finds a usable cursor. If the user agent does not understand any of the cursors that are listed, the cursor does not change.
In Internet Explorer 6, The cursor property supports <code>progress, not-allowed, no-drop, vertical-text, all-scroll, col-resize, row-resize,</code> and <code>url(uri)</code> as new cursor styles.
Cursors support many shape, color and movement combinations.  This permits you to subtitute the default cursors with your preferred design.  For instance, you may want your company logo to display as the "progress" cursor;  or your country's flag waving in the wind to display as the "wait" cursor.
Cursors have been the subject of security bulletins and updates.  If your custom cursors are not behaving as expected, examine the security settings for your browser along with your cursors.  This is a common issue with animated cursors.  For an example, refer to [http://go.microsoft.com/fwlink/p/?linkid{{=}}203632 TechNet Security Resources] and search for "Microsoft Security Bulletin MS05-002".
|Import_Notes===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 18.1
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.2
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Visual Effects
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/cursor
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
==Syntax==
<code>
cursor: ''value'';
</code>