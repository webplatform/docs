{{Page_Title}}
{{Flags
|Content=Cleanup, Examples Best Practices
}}
{{Summary_Section|The color property describes the foreground color of an element's text content.}}

{{Standardization_Status|[http://www.w3.org/TR/css3-color/ W3C Recommendation]}}
{{API_Name}}
{{CSS Property
|Initial value=depends on user agent
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=color
|Description=[[css/color/value|css color value]]
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following examples use the '''color''' attribute and the '''color''' property to change the text color of an object.
This example uses a call to an embedded (global) style sheet to change the text color to <code>red</code> when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|Code=&lt;STYLE&gt;
    .color1 { color:red }
    .color2 { color: }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;SPAN STYLE{{=}}"font-size:14" onmouseover{{=}}"this.className{{=}}'color1'"
    onmouseout{{=}}"this.className{{=}}'color2'"&gt; . . .
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/color_h.htm
}}<br /><hr /><br />{{Single Example
|Description=The following are all ways to make the element's text red:
|Code=element { color: pink }
element { color: #f00 }
element { color: #ff0000 }
element { color: rgb(255,0,0) }
element { color: rgb(100%, 0%, 0%) }
element { color: hsl(0, 100%, 50%) }
 
/* 50% translucent */
element { color: rgba(255, 0, 0, 0.5) } 
element { color: hsla(0, 100%, 50%, 0.5) }
}}<br /><hr /><br />
===More live examples===
*[http://www.w3schools.com/cssref/tryit.asp?filename=trycss_color w3schools Tryit]
}}
{{Notes_Section
|Notes==== Separating foreground from background ===
In order to make it easier for users to see and hear content including separating foreground from background, [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/ WCAG]] indicates the following:
* color is not used as the only visual means of conveying information, indicating an action, prompting a response, or distinguishing a visual element. [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast-without-color Guideline 1.4.1]] (Level A)
* The visual presentation of text and images of text has a minimum contrast ratio of at least 4.5:1, with some exceptions. [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast-contrast Contrast Minimum Guideline 1.4.3]] (Level AA)
* The visual presentation of text and images of text has an enhanced contrast ratio of at least 7:1 [[http://www.w3.org/TR/2008/REC-WCAG20-20081211/#visual-audio-contrast7 Guideline 1.4.6]] (Level AAA)
}}
===Standards information===
[http://www.w3.org/TR/css3-color W3C Recommendation] for
*[http://www.w3.org/TR/css3-color/#foreground the color property]
*[http://www.w3.org/TR/css3-color/#colorunits color units]
[http://dev.w3.org/csswg/css3-transitions W3C Working Draft] for
*[http://dev.w3.org/csswg/css3-transitions/#animatable-css animateable colors]
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Firefox_supported=Yes
|Firefox_version=1.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=3.0
|Opera_supported=Yes
|Opera_version=3.5
|Safari_supported=Yes
|Safari_version=1.0
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=1.0
|Blackberry_supported=Unknown
|Blackberry_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=1.0
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|IE_mobile_supported=Yes
|IE_mobile_version=6.0
|Opera_mobile_supported=Yes
|Opera_mobile_version=6.0
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=1.0
}}
|Notes_rows=
}}
==Notes==
*IE7 and earlier do not support "inherit" as value
{{See_Also_Section
|Manual_sections=*[http://www.w3.org/Style/CSS/Test/CSS3/Color/current/ W3 css3-color Conformance Test Suite]
*[http://www.w3schools.com/cssref/pr_text_color.asp w3schools color property]
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