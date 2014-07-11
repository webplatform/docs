{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference, remove topic cluster flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The text-rendering CSS property provides information to the browser about how to optimize when rendering text. Options are: legibility, speed or geometric precision.}}
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
|Description=Indicates that the browser should choose the most appropriate method between speed, legibility and geometric precision, but favors legibility over speed and geometric precision.
}}{{CSS Property Value
|Data Type=optimizeSpeed
|Description=Indicates that the browser should favor rendering speed over legibility and geometric precision. Browsers usually disable kerning and ligatures and sometimes turn off anti-aliasing.
}}{{CSS Property Value
|Data Type=optimizeLegibility
|Description=Indicates that the browser should favor legibility over rendering speed and geometric precision. Browsers usually apply anti-aliasing or font hinting to display the most legible text.
}}{{CSS Property Value
|Data Type=geometricPrecision
|Description=Indicates that the browser should favor geometric precision over rendering speed and legibility. Usually, this option causes the browser to not use hinting. Instead glyph outlines are drawn with comparable geometric precision to the rendering of path data.
This setting can be helpful when using kerning, which does often not scale linearly and can make text using such fonts look good.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* The user agent will decide how to optimize text for speed, legibility and geometric precision. */
body {
	text-rendering: auto;
}

/* The user agent will prioritize the rendering speed of text. */
body {
	text-rendering: optimizeSpeed;
}

/* The user agent will prioritize the legibility of text. */
body {
	text-rendering: optimizeLegibility;
}

/* The user agent will prioritize the geometric precision of text. */
body {
	text-rendering: optimizePrecision;
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
|Page=https://developer.mozilla.org/en-US/docs/CSS/text-rendering MDN Compatibility Table
}}
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Font, CSS Attributes, Text
}}
{{Topics|CSS, Graphics, SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}