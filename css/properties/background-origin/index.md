{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies what the background-position property is relative to.}}
{{CSS Property
|Initial value=padding-box
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=backgroundOrigin
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=padding-box
|Description=Default. The position is relative to the padding box.
}}{{CSS Property Value
|Data Type=border-box
|Description=The position is relative to the border box.
}}{{CSS Property Value
|Data Type=content-box
|Description=The position is relative to the content box. Useful for having background images automatically follow the padding.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;style&gt;
/**
&nbsp;* Background-origin Example
&nbsp;*/
.border-box {
&nbsp; background-origin: border-box;
}
.content-box {
&nbsp;&nbsp;background-origin: content-box;
}
.padding-box {
&nbsp;&nbsp;background-origin: padding-box;
}
div {
&nbsp;&nbsp;display: inline-block;
&nbsp;&nbsp;margin: 10px;
&nbsp;&nbsp;width: 100px;
&nbsp;&nbsp;height: 60px;
&nbsp;&nbsp;background-color: hsl(0,50%,90%);
&nbsp;&nbsp;padding: 20px;
&nbsp;&nbsp;border: 10px solid black;
&nbsp;&nbsp;background-origin: border-box;
&nbsp;&nbsp;background-image: url("http://docs.webplatform.org/w/skins/webplatform/images/logo.svg");
&nbsp;&nbsp;background-repeat: no-repeat;
}
&lt;/style&gt;

&lt;div class="border-box"&gt;Border box!&lt;/div&gt;
&lt;div class="padding-box"&gt;Padding box!&lt;/div&gt;
&lt;div class="content-box"&gt;Content box!&lt;/div&gt;
|LiveURL=[http://code.webplatform.org/gist/5842945 live example]
}}
}}
{{Notes_Section
|Usage=You should understand the CSS [[tutorials/box_model|Box Model]] before using this property.  Use this in conjunction with [[css/properties/background-image|background-image]] and optionally [[css/properties/background-position|background-position]].   See [[css/properties/background-position|background position]] for information about the coordinate system and positioning.
|Notes====Remarks===
For elements rendered as a single box, the '''background-origin''' property specifies the background positioning area. For elements rendered as multiple boxes (for instance, inline boxes on several lines or boxes on several pages), this property specifies which boxes determine the background positioning areas.
If the [[css/properties/background-attachment|'''background-attachment''']] value for this image is '''fixed''', then the '''background-origin''' property has no effect. In this case, the background positioning area is the initial containing block.
In Windows Internet Explorer 9, the background of a box can have multiple layers. The number of layers is determined by the number of comma-separated values in the [[css/properties/background-image|'''background-image''']] property. Each of the images is sized, positioned, and tiled according to the corresponding value in the other background properties ([[css/properties/background-attachment|'''background-attachment''']], [[css/properties/background-clip|'''background-clip''']], '''background-origin''', [[css/properties/background-position|'''background-position''']], [[css/properties/background-repeat|'''background-repeat''']], and [[css/properties/background-size|'''background-size''']]). The first image in the list is the layer closest to the user, the next one is painted behind the first, and so on.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Backgrounds & Borders Level 3
|URL=http://www.w3.org/TR/css3-background/#the-background-origin
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=4
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=1.0-3.6
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Background
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/background-origin
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}