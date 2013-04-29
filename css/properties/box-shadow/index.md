{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The ‘box-shadow’ property attaches one or more shadows inside or outside of a box-model element. The property is a comma-separated list of shadows, each specified by 2-4 length values, an optional color, and an optional ‘inset’ keyword. box-shadow is a simple style that can be manipulated to generate complex effects.|The ‘box-shadow’ property attaches one or more shadows inside or outside of a box-model element_ The property is a comma-separated list of shadows, each specified by 2-4 length values, an optional color, and an optional ‘inset’ keyword_ box-shadow is a simple style that can be manipulated to generate complex effects_

Given a box, the shadow style is represented as follows:

<pre><shadow>=inset? && [ <length>{2,4} && <color>? ]</pre>

Links to descriptions of length and color are in the [[#Remarks]] section, below.
}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=any length made absolute; any specified color computed; otherwise as specified
|Animatable=No
|CSS object model property=boxShadow
|CSS percentages=???
|Values={{CSS Property Value
|Data Type=inset
|Description=If not specified (default), the shadow is assumed to be a drop shadow (as if the box were raised above the content). The presence of the inset keyword changes the shadow to one inside the frame (as if the content was depressed inside the box). Inset shadows are drawn inside the border (even transparent ones), above the background, but below content.
}}{{CSS Property Value
|Data Type=<offset-x>
|Description=The first length is the horizontal offset of the shadow. <offset-x> specifies the horizontal distance. Negative values place the shadow to the left of the element. If both <offset-x> and <offset-y> values are 0, the shadow is placed behind the element (and may generate a blur effect if <blur-radius> and/or <spread-radius> is set).
}}{{CSS Property Value
|Data Type=<offset-y>
|Description=The second length is the vertical offset of the shadow. <offset-y> specifies the vertical distance. Negative values place the shadow above the element. If both <offset-x> and <offset-y> values are 0, the shadow is placed behind the element (and may generate a blur effect if <blur-radius> and/or <spread-radius> is set).
}}{{CSS Property Value
|Data Type=<blur-radius>
|Description=The third length is a blur radius. The larger this value, the bigger the blur, so the shadow becomes bigger and lighter. Negative values are not allowed. If not specified, it is 0 (the shadow's edge is sharp).
}}{{CSS Property Value
|Data Type=<spread-distance>
|Description=The fourth length is a spread distance. Positive values cause the shadow to expand and grow bigger, negative values cause the shadow to shrink. If not specified, it is 0 (the shadow is the same size as the element). (A zero-sized shadow shape causes the outer shadow to disappear, and the inner shadow to cover the entire padding-box.) For inner shadows, expanding the shadow (creating more shadow area) means contracting the shadow's perimeter shape.
}}{{CSS Property Value
|Data Type=<color>
|Description=See color values for possible keywords and notations. If not specified, the color used depends on the browser - it is usually the value of the color property, but note that Safari currently paints a transparent shadow in this case.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=An example of a multiple box-shadows. The inner shadow appears on all four sides by creating two box-shadows.
|Code=&lt;style&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;.shadow-style {<br>
&nbsp;&nbsp;&nbsp;&nbsp;width: 100px;<br>
&nbsp;&nbsp;&nbsp;&nbsp;height: 100px;<br>
&nbsp;&nbsp;&nbsp;&nbsp;box-shadow: inset 30px 30px 5px green, inset -30px -30px 5px blue;<br>
&nbsp;&nbsp;&nbsp;&nbsp;border: 10px solid yellow;<br>
&nbsp;&nbsp;&nbsp;&nbsp;background-color: red;<br>
}<br>
&lt;/style&gt;<br>
&lt;body&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;div class=&quot;shadow-style&quot;&gt;<br>
&nbsp;&nbsp;&nbsp;&nbsp;&lt;/div&gt;<br>
&lt;/body&gt;
|LiveURL=http://code.webplatform.org/gist/5259531
}}{{Single Example
|Language=CSS
|Description=An example of a basic Drop Shadow. An outer box-shadow casts a shadow as if the border-box of the element were opaque. The shadow is drawn outside the border edge only: it is clipped inside the border-box of the element.
|Code=article {
/* box-shadow: left-offset top-offset blur color; */
   box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}
|LiveURL=http://code.webplatform.org/gist/5259244
}}{{Single Example
|Language=CSS
|Description=An example of inner drop shadows. An inner box-shadow casts a shadow as if everything outside the padding edge were opaque. The inner shadow is drawn inside the padding edge only: it is clipped outside the padding box of the element.
|Code=article {
/* box-shadow: left-offset top-offset blur color; */
   box-shadow: 0 0 10px rgba(0, 0, 0, 0.5) inset;
}
|LiveURL=http://code.webplatform.org/gist/5259299
}}{{Single Example
|Language=CSS
|Description=An example of how a positive spread distance length value affects the drop shadow. If a spread distance is defined, the shadow is expanded outward or contracted inward.
|Code=article {
/* box-shadow: left-offset top-offset blur spread color; */
   box-shadow: 0 0 5px 10px rgba(0, 0, 0, 0.5);
}
|LiveURL=http://code.webplatform.org/gist/5259449
}}{{Single Example
|Language=CSS
|Description=Negative values cause the shadow shape to contract.
|Code=article {
/* box-shadow: left-offset top-offset blur spread color; */
   box-shadow: 0 20px 5px -10px rgba(0, 0, 0, 0.5);
}
|LiveURL=http://code.webplatform.org/gist/5259463
}}{{Single Example
|Language=CSS
|Description=If the blur value is zero, the shadow's edge is sharp. (A non-zero blur value indicates that the resulting shadow should be blurred, such as by a Gaussian filter.)
|Code=article {
/* box-shadow: left-offset top-offset blur spread color; */
   box-shadow: 0 0 0 5px rgba(0, 0, 0, 0.5);
}
|LiveURL=http://code.webplatform.org/gist/5259501
}}{{Single Example
|Language=CSS
|Description=If the box has a nonzero ‘border-radius’, the shadow shape is rounded in the same way. (The ‘border-image’ does not affect the shape of the box-shadow.)
|Code=article {
/* box-shadow: left-offset top-offset blur color; */
   box-shadow: 0 0 10px rgba(0, 0, 0, 1);
	
   border-radius: 10px;
}
|LiveURL=http://code.webplatform.org/gist/5259470
}}
}}
{{Notes_Section
|Usage====Remarks===
See also:
* [[css/data_types/length]]
* [[css/color]]
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds and Borders Module Level 3
|URL=http://dev.w3.org/csswg/css3-background/#box-shadow
|Status=Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=10.0
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=1.0
|Firefox_supported=Yes
|Firefox_version=13.0
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=4.0
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=3.0
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=4.0
|Android_prefixed_supported=Yes
|Android_prefixed_version=2.1
|Blackberry_supported=Yes
|Blackberry_version=10.0
|Blackberry_prefixed_supported=Yes
|Blackberry_prefixed_version=7.0
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0-5.1
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=3.2
}}
|Notes_rows={{Compatibility Notes Row
|Browser=IE
|Version=9.0
|Note=In order to get box-shadow in IE9 or later, you need to set border-collapse to separate. Since version 5.5, Internet Explorer supports Microsoft's DropShadow and Shadow Filter. You can use this proprietary extension to cast a drop shadow (though the syntax and the effect are different from CSS3).
}}{{Compatibility Notes Row
|Browser=Chrome
|Version=10.0
|Note=Basic support in 1.0 with -webkit prefix, inset and spread radius in 4.0  with -webkit prefix.
}}{{Compatibility Notes Row
|Browser=Firefox (Gecko)
|Version=4.0 (2.0)
|Note=Since Firefox 13 (Gecko 13), -moz-box-shadow prefix was dropped and only the unprefixed version is supported.
}}
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}