{{Page_Title}}
{{Flags
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
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Sets the writing mode to vertical and to progress from right to left. Sometimes used by East Asian, especially Japanese and Chinese. This example is Japanese use case.
|Code=&lt;p&gt;日本では、新聞や書籍などで縦書きを使用することがあります。これは、縦書きのシンプルな例です。&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/5833192
}}{{Single Example
|Language=CSS
|Code=p {
	width: 100%;
	-webkit-writing-mode: vertical-rl;
}
}}{{Single Example
|Language=CSS
|Description=Sets the writing mode, including a fallback for the previous version of the spec, supported by IE.
|Code=/* horizontal and top to bottom */
writing-mode: horizontal-tb;
-ms-writing-mode: lr-tb; 

/* horizontal and top to bottom, and the direction of text to right to left */
writing-mode: horizontal-tb;
-ms-writing-mode: rl-tb;
direction: rtl;

/* vertical and to progress from right to left */
writing-mode: vertical-rl;
-ms-writing-mode: tb-rl;

/* vertical and to progress from left to right */
writing-mode: vertical-lr;
-ms-writing-mode: tb-lr;
}}{{Single Example
|Language=CSS
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
    &lt;p&gt;This text should be horizontal, left to right, and &lt;em&gt;under&lt;/em&gt; the heading.&lt;/p&gt;
    &lt;ol&gt;
        &lt;li&gt;One&lt;/li&gt;
	&lt;li&gt;Two&lt;/li&gt;
	&lt;li&gt;Three&lt;/li&gt;
    &lt;/ol&gt;
&lt;/div&gt;
&lt;div id="horizontal-tb-direction-rtl"&gt;
    &lt;h1&gt;Writing-mode: horizontal-tb/rl-tb, direction: rtl&lt;/h1&gt;
    &lt;p&gt;This text should be horizontal, right to left, and &lt;em&gt;under&lt;/em&gt; the heading.&lt;/p&gt;
    &lt;ol&gt;
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