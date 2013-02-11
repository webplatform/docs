{{Page_Title}}
{{Flags
|Content=Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The color property sets the color of an element's foreground content (usually text), accepting any standard CSS color from keywords and hex values to RGB(a) and HSL(a).}}
{{CSS Property
|Initial value=black, except in a few cases (see notes)
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=For a non-translucent color, an hexadecimal equivalent is used. Otherwise it is the RGBa equivalent
|Animatable=Yes
|CSS object model property=color
|Values={{CSS Property Value
|Data Type=color
|Description=[[css/color|CSS color value]]
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=/* Setting a paragraph color to turquoise with a name value */
p {color:turquoise}

/* Setting the same propriety with an hexadecimal value*/
p {color:#40E0D0}

/* with a RGB decimal value */
p { color: rgb(64,224,208) }

/* with a RGB percentage value */
p { color: rgb(25.1%,87.8%,81.6%) }

/* with a HSL value */
p { color: hsl(174,72%,56%) }

/* We now want our color to be 20% translucent which means a 80% opacity */

/* We can set the color with a RGBa value */ 
p { color: rgb(64,224,208,0.8) }

/* Or a HSLa value */
p { color: hsl(174,72%,56%,0.8) }
}}
}}
{{Notes_Section
|Usage=Though CSS color values are precisely defined, they may appear differently on an output device. Most of them are not calibrated, and some browsers do not support output devices color profile. Without these, color rendering may vary a lot.
|Notes==== Default color ===
Some browsers change the default color from black to another color in their default css (user-agent stylesheet).

=== RGB, HSL, RGBa and HSLa support ===
RGB, HSL, RGBa and HSLa are not supported by older browsers, therefore if you do use such colours, you should also provide a fallback color property that uses something similar but more widely supported, like a hex value, either placed next to the modern color value but earlier in the cascade, or in a separate stylesheet hidden behind a conditional comment.

=== Separating foreground from background ===
In order to make it easier for users to see and hear content including separating foreground from background, [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/ WCAG]] indicates the following:
* color is not used as the only visual means of conveying information, indicating an action, prompting a response, or distinguishing a visual element. [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast-without-color Guideline 1.4.1]] (Level A)
* The visual presentation of text and images of text has a minimum contrast ratio of at least 4.5:1, with some exceptions. [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast-contrast Contrast Minimum Guideline 1.4.3]] (Level AA)
* The visual presentation of text and images of text has an enhanced contrast ratio of at least 7:1 [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast7 Guideline 1.4.6]] (Level AAA)
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS3 Color Module Level 3
|URL=http://www.w3.org/TR/css3-color/
|Status=W3C Recommendation
}}{{Related Specification
|Name=Color in CSS1
|URL=http://www.w3.org/TR/REC-CSS1/#color
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Keywords and hexadecimals colors
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=3.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=RGB
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=3.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=HSL
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=Translucent color value (RGBa, HSLa)
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.0
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=3.8
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=1.0
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
|Safari_mobile_prefixed_supported=No
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=Translucent color value (RGBa, HSLa)
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=No
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=18
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=9
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=<=7.0
|Note=no support for the "inherit" value
}}
}}
{{See_Also_Section
|Manual_sections=*[http://www.w3.org/Style/CSS/Test/CSS3/Color/current/ W3 css3-color Conformance Test Suite]
*[https://developer.mozilla.org/en-US/docs/CSS/color MDN color property]
*[http://msdn.microsoft.com/en-us/library/ie/ms530749(v=vs.85).aspx MSDN color property]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
===css color value===
See [[css/color/value|css color value]] for more information.
The color value may be given as:
*Basic color keyword
<pre><nowiki>aqua, black, blue, fuchsia, gray, green, lime, maroon, navy, olive, purple, red, silver, teal, white, yellow
</nowiki></pre>
*Extended color keyword
<pre><nowiki>aliceblue, antiquewhite, aqua, aquamarine, azure, beige, bisque, black, blanchedalmond, ...
</nowiki></pre>
:See [http://www.w3.org/TR/css3-color/#svg-color W3C CSS Color Module Recommendation 4.3. Extended color keywords] for a complete list of keywords.
*RGB
<pre><nowiki>#00f
#0000ff
rgb(0,0,255)
rgb(0%,0%,100%)
</nowiki></pre>
*RGBA
<pre><nowiki>rgba(0,0,255,0.5)
rgba(0%,0%,100%,0.5)
</nowiki></pre>
*HSL
<pre><nowiki>hsl(0, 100%, 50%)
</nowiki></pre>
*HSLA
<pre><nowiki>hsla(0, 100%, 50%, 0.5)
</nowiki></pre>
*"transparent" (since CSS3)
*"currentColor" (since CSS3) (same as "color: inherit")
*CSS2 system colors (Deprecated)

===More live examples===
*[http://www.w3schools.com/cssref/tryit.asp?filename=trycss_color w3schools Tryit]