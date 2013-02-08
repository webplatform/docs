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
'''Available standard cursors''': 
auto, default, none, context-menu, help, pointer, progress, wait, cell, crosshair, text, vertical-text, alias, copy, move, no-drop, not-allowed, e-resize, n-resize, ne-resize, nw-resize, s-resize, se-resize, sw-resize, w-resize, ew-resize, ns-resize, nesw-resize, nwse-resize, col-resize, row-resize, all-scroll, zoom-in, zoom-out

Check out the Examples.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''cursor''' attribute and the '''cursor''' property to change the cursor as it passes over an object.

This example uses a call to an embedded (global) style sheet to set the cursor to '''hand''' as the cursor passes over all paragraphs.


		General
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: auto; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: auto;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: default; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: default;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: none; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: none;</div>
		Links & status
		<div style="width: 25%; float: left; background: #ffffff; cursor: context-menu; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: context-menu;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: help; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: help;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: pointer; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: pointer;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: progress; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: progress;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: wait; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: wait;</div>
		Selection
		<div style="width: 25%; float: left; background: #ffffff; cursor: cell; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: cell;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: crosshair; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: crosshair;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: text; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: text;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: vertical-text; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: vertical-text;</div>
		Drag & drop
		<div style="width: 25%; float: left; background: #ffffff; cursor: alias; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: alias;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: copy; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: copy;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: move; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: move;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: no-drop; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: no-drop;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: not-allowed; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: not-allowed;</div>
		Resize & scrolling
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: all-scroll; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: all-scroll;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: col-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: col-resize;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: row-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: row-resize;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: n-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: n-resize;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: e-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: e-resize;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: s-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: s-resize;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: w-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: w-resize;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: ne-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: ne-resize;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: nw-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: nw-resize;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: se-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: se-resize;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: sw-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: sw-resize;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: ew-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: ew-resize;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: ew-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: ew-resize;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: ns-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: ns-resize;</div>
		<div style="width: 25%; float: left; background: #f4f5f7; cursor: nesw-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: nesw-resize;</div>
		<div style="width: 25%; float: left; background: #ffffff; cursor: nwse-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: nwse-resize;</div>

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