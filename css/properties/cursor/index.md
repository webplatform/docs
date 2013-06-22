{{Page_Title}}
{{Flags
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The cursor CSS property specifies the mouse cursor displayed when the mouse pointer is over an element.}}
{{CSS Property
|Initial value=auto
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=as specified (if a keyword), URLs are converted to absolute
|Animatable=No
|CSS object model property=cursor
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=standard values
|Description=There are many standard cursors available:
 
* <code>auto</code>
* <code>default</code>
* <code>none</code>
* <code>context-menu</code>
* <code>help</code>
* <code>pointer</code>
* <code>progress</code>
* <code>wait</code>
* <code>cell</code>
* <code>crosshair</code>
* <code>text</code>
* <code>vertical-text</code>
* <code>alias</code>
* <code>copy</code>
* <code>move</code>
* <code>no-drop</code>
* <code>not-allowed</code>
* <code>e-resize</code>
* <code>n-resize</code>
* <code>ne-resize</code>
* <code>nw-resize</code>
* <code>s-resize</code>
* <code>se-resize</code>
* <code>sw-resize</code>
* <code>w-resize</code>
* <code>ew-resize</code>
* <code>ns-resize</code>
* <code>nesw-resize</code>
* <code>nwse-resize</code>
* <code>col-resize</code>
* <code>row-resize</code>
* <code>all-scroll</code>
* <code>zoom-in</code>
* <code>zoom-out</code>

These have varying support across different browsers — see the support section. The examples below feature different boxes with different cursor values set on them, so you can get an idea of what the different ones look like.
}}{{CSS Property Value
|Data Type=url(), keyword
|Description=Instead of specifying a standard pointer type, you can specify a <code>url()</code> function pointing to a custom graphic to use as a cursor, which must be followed by a fallback keyword to use as a pointer if the image is not available (this can be <code>auto</code> or a standard keyword value). For example, <code>cursor: url(), auto;</code>

You can supply multiple <code>url()</code> functions separated by commas (<code>url(), url(), auto</code> for example), and the browser will use the earliest appropriate image it can find. Limitations include:

* Cursor size: if the cursor image is over a certain size it will be ignored (in Gecko for example the limit is 128×128px). You should limit yourself about 32×32px anyway, for maximum compatibility with operating systems and platforms.
* Browser: In Opera, the custom cursors are just ignored, and the keywords are used instead.
* Transparency: Translucent cursors are not supported on Windows releases earlier than XP. This is a limitation of the operating system. Transparency works on all platforms.
* Image format: Most browsers support a wide variety of image formats, but you should stick to something common and web-optimizable for the most part, such as JPG or PNG. You'll also need to include a CUR format image, as they are required by IE. Animateds PNGs and GIFs will only produce static cursors.
}}{{CSS Property Value
|Data Type=url() hotspot-x hotspot-y, keyword;
|Description=CSS3 allows you to specify a custom cusor image along with an X and Y number values for the pointer hotspot, for example <code>cursor:  url(cursor2.png) 2 2, auto;</code>. If not specified, the hotspot position defaults to the top left corner of the cursor image, or may be read from the meta data inside the image file, in the case of CUR and XBM format files.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following Example shows the standard cursors. Just hover the boxes and you see the cursors.

		<div style="overflow: hidden;">
		<h3>General</h3>
		<div style="overflow: hidden;">
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: auto; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: auto;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: default; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: default;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: none; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: none;</div></div>
		<h3>Links & status</h3>
		<div style="overflow: hidden;">
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: context-menu; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: context-menu;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: help; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: help;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: pointer; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: pointer;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: progress; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: progress;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: wait; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: wait;</div></div>
		<h3>Selection</h3>
		<div style="overflow: hidden;"><div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: cell; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: cell;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: crosshair; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: crosshair;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: text; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: text;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: vertical-text; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: vertical-text;</div></div>
		<h3>Drag & drop</h3>
		<div style="overflow: hidden;"><div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: alias; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: alias;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: copy; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: copy;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: move; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: move;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: no-drop; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: no-drop;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: not-allowed; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: not-allowed;</div>
		</div>
		<h3>Resize & scrolling</h3>
		<div style="overflow: hidden;">
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: all-scroll; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: all-scroll;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: col-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: col-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: row-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: row-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: n-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: n-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: e-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: e-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: s-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: s-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: w-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: w-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: ne-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: ne-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: nw-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: nw-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: se-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: se-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: sw-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: sw-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: ew-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: ew-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: ew-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: ew-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: ns-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: ns-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: nesw-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: nesw-resize;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: nwse-resize; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: nwse-resize;</div>
		</div>
		<h3>Zoom</h3>
		<div style="overflow:hidden;">
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: zoom-in; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: zoom-in;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: zoom-out; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: zoom-out;</div>
		</div>
		<h3>Mozilla extensions</h3>
		<div style="overflow: hidden;">
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #ffffff; cursor: -moz-grab; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: -moz-grab;</div>
		<div style="width: 25%; text-align: center; margin-right: 2%; float: left; background: #f4f5f7; cursor: -moz-grabbing; padding: 1em; border-radius: 4px; color: #58595B; border: 1px solid #cdced0; margin-bottom: 1em;">cursor: -moz-grabbing;</div>
		</div>
	</div>
<h3>Code examples</h3>
|Code=.foo { cursor: crosshair; }
 
/* use prefixed-value if "zoom-in" isn't supported */
.bar { cursor: -webkit-zoom-in;  cursor: -moz-zoom-in;  cursor: zoom-in; } 
 
/* standard cursor value as fallback for url() must be provided (doesn't work without) */
.baz { cursor: url(hyper.cur), auto }

/* multiple url() functions for fallback in browsers */
p { cursor: url(hyper.svg), url(hyper.cur), auto }

/* url() function with custom cursor and X and Y hotspot coordinates */
div { cursor: url(hyper.svg) 5 10, auto
}}{{Single Example
|Language=CSS
|Description=This example shows a custom cursor image being used.
|Code=html {
  cursor: url(http://www.webplatform.org/logo/wplogo_transparent.png), auto;
}
|LiveURL=http://code.webplatform.org/gist/5503046
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS2 UI section (18.1)
|URL=http://www.w3.org/TR/CSS2/ui.html
|Status=W3C recommendation
}}{{Related Specification
|Name=CSS Basic User Interface module level 3
|URL=http://www.w3.org/TR/css3-ui/
|Status=Working Draft
|Relevant_changes=New cursor types added, and the ability to set the hotspot position.
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=auto, crosshair, default, move, text, wait, help, n-resize, e-resize, s-resize, w-resize, ne-resize, nw-resize, se-resize, sw-resize
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
}}{{Compatibility Table Desktop Row
|Feature=hand (just use pointer for this purpose)
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=pointer, progress
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=6.0
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
}}{{Compatibility Table Desktop Row
|Feature=url()
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.5 (1.8) On MacOs 4.0 (2.0)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=6.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Positioning syntax for url() values (Experimental)
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=(Yes)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
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
}}{{Compatibility Table Desktop Row
|Feature=not-allowed, no-drop, vertical-text, all-scroll, col-resize, row-resize
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.5 (1.8)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=6.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.6
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=alias, cell, copy, ew-resize, ns-resize, nesw-resize, nwse-resize, context-menu
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.5 (1.8)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.6
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=none
|Chrome_supported=Yes
|Chrome_version=5.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.0 (1.9)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=inherit
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.2
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=zoom-in, zoom-out (Experimental)
|Chrome_supported=Yes
|Chrome_version=1.0 (-webkit)
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 (1.4) (-moz)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=11.6
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.0 (-webkit)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Visual Effects
|External_links=* [http://www.sitepoint.com/css3-cursor-styles/ Introducing the New Cursor Styles in CSS3]
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