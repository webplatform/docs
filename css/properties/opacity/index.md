{{Page_Title}}
{{Flags
|High-level issues=Merge Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Editorial notes=This page should be kept, and the data at http://docs.webplatform.org/wiki/css/Properties/opacity merged into it as appropriate.
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The opacity property controls transparency and opacity of an element. Assuming defaults at parent level, an element with an opacity of 1 is completely opaque, whereas and element with an opacity of 0 is completely transparent. The opacity used when rendering an element is the product of its opacity and the opacity of its ancestors.}}
{{CSS Property
|Initial value=1
|Applies to=All elements
|Inherited=No
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=&lt;alphavalue&gt;
|Description=A '''Floating-point''' value between 0.0 (fully transparent) and 1.0 (fully opaque), inclusive.
}}{{CSS Property Value
|Data Type=inherit
|Description=Indicates that the property takes the same computed value as the property for the element's parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=.example1 {
  opacity: 0.5;
}
}}{{Single Example
|Language=CSS
|Description=Internet Explorer 5-7
|Code=.example2 {	
  filter: alpha(opacity=50);
}
}}{{Single Example
|Description=Internet Explorer 8
|Code=.example3 {
  -ms-filter:"progid:DXImageTransform.Microsoft.Alpha(Opacity=50)";
}
}}{{Single Example
|Description=Internet Explorer 5-8
|Code=.opaque {
  -ms-filter:"progid:DXImageTransform.Microsoft.Alpha(Opacity=50)"; // first!
	filter: alpha(opacity=50);					// second!
}
}}
}}
{{Notes_Section
|Notes====Remarks===
The opacity setting is applied uniformly across the entire object. Any values outside the range 0.0 to 1.0 will be clamped to this range.
Object or group opacity can be thought of conceptually as a postprocessing operation. Conceptually, after the object or group is rendered into an RGBA offscreen image, the object or group opacity setting specifies how to blend the offscreen image into the current background.
|Import_Notes====Syntax===
<code>'''opacity: '''&lt;alphavalue&gt; '''{{!}}''' inherit</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203761 CSS Color Module Level 3], Section 3.2
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0+
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=2.0+
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0+
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.0+
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.1+
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1+
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0+
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18+
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15+
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=15+
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0+7.0
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.1+
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5-7
|Note=You can use filter: alpha(opacity=50); to obtain the same effect
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8
|Note=You can use -ms-filter:"progid:DXImageTransform.Microsoft.Alpha(Opacity=50)"; to obtain the same effect
}}
}}
{{See_Also_Section
|Topic_clusters=Visual Effects
|Manual_links=[[filter]]
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[svg/properties/a|a]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}