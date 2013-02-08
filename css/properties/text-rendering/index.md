{{Page_Title}}
{{Flags
|Content=Grammar/Spelling
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The text-rendering CSS property provides information to the browser about what to optimize for when rendering text. Options are: optimize font rendering to legibility, speed or geometric precision.}}
{{CSS Property
|Initial value=auto
|Applies to=text elements
|Inherited=Yes
|Media=visual
|Computed value=auto
|Animatable=Yes
|CSS object model property=text-rendering
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=auto
|Description=Indicates that the browser shall choose the most appropriate method between speed, legibility and geometric precision but favors legibility over speed and geometric precision.
}}{{CSS Property Value
|Data Type=optimizeSpeed
|Description=Indicates that the browser shall favor rendering speed over legibility and geometric precision. The browser usually disables kerning and ligatures and sometimes will turn off anti-aliasing.
}}{{CSS Property Value
|Data Type=optimizeLegibility
|Description=Indicates that the browser shall favor legibility over rendering speed and geometric precision. The browser usually will apply anti-aliasing and / or font hinting to display the most legible text.
}}{{CSS Property Value
|Data Type=geometricPrecision
|Description=Indicates that the user agent shall favor the geometric precision over rendering speed and legibility. Usually, this option will cause the browser to not use hinting. Instead glyph outlines will be drawn with comparable geometric precision to the rendering of path data.
This setting can be helpful when using Kerning which does often not scale linearly and can make text using such fonts look good.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* Force the browser to display fonts with all its font-features to make them look good on big sized headlines but avoid using inadequate ligatures on copy text */

body {
	text-rendering: optimizeSpeed;
}

h1, h2, h3, h4, h5, h6 {
	text-rendering: optimizeSpeed;
}
}}
}}
{{Notes_Section
|Usage=Gecko note:
In Gecko browsers there is a way to set the threshold value for the auto keyword by changing the preference in browser.display.auto_quality_min_font_size. By default it is set to 20px.
On Gecko 2.0 (Firefox 4 / Thunderbird 3.3 / SeaMonkey 2.1) the optimizeSpeed option has no effect because there is no faster way of rendering text than the standard code already does. See bug [https://bugzilla.mozilla.org/show_bug.cgi?id=595688 bug 595688] for more details on that.
|Notes=The property is a SVG property not specified in any CSS standard yet. However, user agents including Gecko and WebKit browsers let you apply this property to HTML and XML content on Windows, Mac OS X and Linux via CSS.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table
|Page=https://developer.mozilla.org/en-US/docs/CSS/text-rendering
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Font, CSS Attributes
}}
{{Topics|CSS, Graphics, SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}