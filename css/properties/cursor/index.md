{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add example, description, specifications, compatibility.
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
|Examples=
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=Visual Effects
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}