{{Page_Title}}
{{Flags
|High-level issues=Data Not Semantic
|Content=Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|<code>writing-mode</code> specifies if lines of text are laid out horizontally or vertically, and the direction which lines of text and blocks progress.}}
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
|Data Type=horizontal-tb
|Description=Lines of text are laid out horizontally, and progress from the top to the bottom of the page. This is the writing mode used in many writing systems, such as Latin, Greek, Cyrillic, Arabic, Hebrew, etc.
}}{{CSS Property Value
|Data Type=vertical-rl
|Description=Lines of text are laid out vertically, and progress from the right to the left of the page. Asian languages, such as Chinese or Japanese traditionally used this writing mode.
}}{{CSS Property Value
|Data Type=vertical-lr
|Description=Lines of text are laid out vertically, and progress from the left to the right of the page. Mongolian-based writing systems typically use this writing mode.
}}{{CSS Property Value
|Data Type=lr-tb
|Description='''Deprecated''' value. Content flows horizontally from left to right, top to bottom. The next horizontal line is positioned underneath the previous line. All glyphs are positioned upright. This layout is used by most writing systems.
}}{{CSS Property Value
|Data Type=rl-tb
|Description='''Deprecated''' value. Content flows horizontally from right to left, top to bottom. The next horizontal line is positioned underneath the previous line. All glyphs are positioned upright. This layout is used with right-to-left scripts like Arabic, Hebrew, Thaana, and Syriac. Maps to the horizontal-tb value, and direction: rtl; in the current spec. Maps to the horizontal-tb value, and direction: ltr; in the current spec.
}}{{CSS Property Value
|Data Type=tb-rl
|Description='''Deprecated''' value. Content flows vertically from top to bottom, right to left. The next vertical line is positioned to the left of the previous line. Wide-cell glyphs are positioned upright; nonwide-cell glyphs (also known as narrow Latin or narrow Kana glyphs) are rotated 90° clockwise. This layout is used in East Asian typography. Maps to the vertical-rl value in the current spec.
}}{{CSS Property Value
|Data Type=bt-rl
|Description='''Deprecated''' value. Content flows vertically from bottom to top, right to left. The next vertical line is positioned to the left of the previous line. Wide-cell glyphs are positioned upright; nonwide-cell glyphs (also known as narrow Latin or narrow Kana glyphs) are rotated 90° clockwise. This layout is used for right-to-left script blocks used in vertical East Asian typography.
}}{{CSS Property Value
|Data Type=tb-lr
|Description='''Deprecated''' value. Content flows vertically from top to bottom, left to right. The next vertical line is positioned to the right of the previous line. Maps to the vertical-lr value in the current spec.
}}{{CSS Property Value
|Data Type=bt-lr
|Description='''Deprecated''' value. Content flows vertically from bottom to top, left to right.
}}{{CSS Property Value
|Data Type=lr-bt
|Description='''Deprecated''' value. Content flows horizontally from bottom to top, left to right. The next horizontal line is positioned above the previous line.
}}{{CSS Property Value
|Data Type=rl-bt
|Description='''Deprecated''' value. Content flows horizontally from bottom to top, right to left.
}}{{CSS Property Value
|Data Type=lr
|Description='''Deprecated''' value. For use on SVG and HTML elements. Equivalent to '''lr-tb'''.
}}{{CSS Property Value
|Data Type=rl
|Description='''Deprecated''' value. For use on SVG and HTML elements. Equivalent to '''rl-tb'''.
}}{{CSS Property Value
|Data Type=tb
|Description='''Deprecated''' value. For use on SVG and HTML elements. Equivalent to '''tb-rl'''.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Sets the writing mode to horizontal and top to bottom, including a fallback for the previous version of the spec, supported by IE. This is the default. Used by writing systems such as Latin, Greek and Cyrillic.
|Code=-ms-writing-mode: lr-tb; 
writing-mode: horizontal-tb;
}}{{Single Example
|Language=CSS
|Description=Sets the writing mode to horizontal and top to bottom, and the direction of text to right to left. Includes a fallback for the previous version of the spec, supported by IE. Used by writing systems such as Arabic and Hebrew. The horizontal-tb value is default, so not typically needed.
|Code=-ms-writing-mode: rl-tb; /* old spec includes the text direction in the writing-mode value */
writing-mode: horizontal-tb;

direction: rtl;
}}{{Single Example
|Language=CSS
|Description=Sets the writing mode to vertical and to progress from right to left. Includes fallback to old version of the spec, supported by IE. Sometimes used by East Asian languages such as Chinese and Japanese.
|Code=-ms-writing-mode: tb-rl;
writing-mode: vertical-rl;
}}{{Single Example
|Language=CSS
|Description=Sets the writing mode to vertical and to progress from left to right. Includes fallback to old version of the spec, supported by IE. Used by Mongolian scripts.
|Code=-ms-writing-mode: tb-lr;
writing-mode: vertical-lr;
}}{{Single Example
|Language=HTML
|Description=Complete example, including HTML.
|Code=&lt;style&gt;
    #horizontal-tb {
	-ms-writing-mode: lr-tb;  /* old syntax, supported by IE */		
	writing-mode: horizontal-tb;  /* modern syntax. WebKit currently requires prefix */
    }
   #horizontal-tb-direction-rtl {
	-ms-writing-mode: rl-tb;
        writing-mode: horizontal-tb;
	
        direction: rtl; /* sets the direction of text in a line to right to left */
   }
   #vertical-rl {
        -ms-writing-mode: tb-rl;
	writing-mode: vertical-rl; 
    }
    #vertical-lr {
	-ms-writing-mode: tb-lr;
        writing-mode: vertical-lr;
    }	
&lt;/style&gt;
&lt;div id="horizontal-tb"&gt;
    &lt;h1&gt;Writing-mode: horizontal-tb/lr-tb&lt;/h1&gt;
    &lt;p&gt;This text should be horizontal, left to right, and &lt;em>under&lt;/em&gt; the heading.&lt;/p&gt;
    &lt;ol&gt;
        &lt;li>One&lt;/li&gt;
	&lt;li>Two&lt;/li&gt;
	&lt;li>Three&lt;/li&gt;
    &lt;/ol&gt;
&lt;/div&gt;
&lt;div id="horizontal-tb-direction-rtl"&gt;
    &lt;h1&gt;Writing-mode: horizontal-tb/rl-tb, direction: rtl&lt;/h1&gt;
    &lt;p&gt;This text should be horizontal, right to left, and &lt;em&gt;under&lt;/em&gt; the heading.&lt;/p&gt;
    &lt;ol>
	&lt;li&gt;One&lt;/li&gt;
	&lt;li&gt;Two&lt;/li&gt;
	&lt;li&gt;Three&lt;/li&gt;
    &lt;/ol&gt;
&lt;/div&gt;
&lt;div id="vertical-rl"&gt;
        &lt;h1&gt;Writing-mode: vertical-rl/tb-rl&lt;/h1&gt;
        &lt;p&gt;This text should be vertical, and to the &lt;em&gt;left&lt;/em&gt; of the heading.&lt;/p&gt;
	 &lt;ol&gt;
              &lt;li&gt;One&lt;/li&gt;
              &lt;li&gt;Two&lt;/li&gt;
	      &lt;li&gt;Three&lt;/li&gt;
	 &lt;/ol&gt;
&lt;/div&gt;	
&lt;div id="vertical-lr"&gt;
	&lt;h1&gt;Writing-mode: vertical-lr/tb-lr&lt;/h1&gt;
	&lt;p&gt;This text should be vertical, and to the &lt;em&gt;right&lt;/em&gt; of the heading.&lt;/p&gt;
	&lt;ol&gt;
		&lt;li&gt;One&lt;/li&gt;
		&lt;li&gt;Two&lt;/li&gt;
		&lt;li&gt;Three&lt;/li&gt;
	&lt;/ol&gt;
&lt;/div&gt;
}}
}}
{{Notes_Section}}
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5.5–current
|Note=Supports a previous version of the spec with alternative value names. Supported both with and without the -ms- prefix.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9
|Note=Added support for lr, rl and tb values
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8
|Note=Added support for tb-lr, bt-lr, lr-bt, and rl-bt values
}}{{Compatibility Notes Row
|Browser=WebKit
|Note=Currently requires the -webkit- prefix
}}
}}
{{See_Also_Section
|External_links=* [http://generatedcontent.org/post/45384206019/writing-modes Vertical text with CSS 3 Writing Modes]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}