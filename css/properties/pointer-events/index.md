{{Page_Title|pointer-events}}
{{Flags
|Content=Incomplete, Compatibility Incomplete, Examples Needed
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The pointer-events property  allows you to control whether an element can be the target for the pointing device (e.g, mouse, pen) events.}}
{{CSS Property
|Initial value=auto
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=the specified value
|Animatable=No
|CSS object model property=pointerEvents
|Values={{CSS Property Value
|Data Type=auto
}}{{CSS Property Value
|Data Type=none
}}{{CSS Property Value
|Data Type=visiblePainted
}}{{CSS Property Value
|Data Type=visibleFill
}}{{CSS Property Value
|Data Type=visibleStroke
}}{{CSS Property Value
|Data Type=visible
}}{{CSS Property Value
|Data Type=painted
}}{{CSS Property Value
|Data Type=fill
}}{{CSS Property Value
|Data Type=stroke
}}{{CSS Property Value
|Data Type=inherit
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!DOCTYPE HTML&gt;
&lt;html lang="en-US"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;title&gt;Pointer-events example&lt;/title&gt;
  &lt;link href="pointer-events.css" type="text/css" rel="stylesheet"&gt;
&lt;/head&gt;
&lt;body&gt;

  &lt;p&gt;&lt;a href="http://docs.webplatform.org" id="one"&gt;webplatform.org(none)&lt;/a&gt;&lt;/p&gt;
  &lt;p&gt;&lt;a href="http://docs.webplatform.org" id="two"&gt;webplatform.org(all)&lt;/a&gt;&lt;/p&gt;

&lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Language=CSS
|Code=#one{
  pointer-events: none;
}
#two{
  pointer-events: all;
}
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Scalable Vector Graphics (SVG) 1.1 (Second Edition)
|URL=http://www.w3.org/TR/SVG11/interact.html#PointerEventsProperty
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=For HTML
|Chrome_supported=Yes
|Chrome_version=2.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.6
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=For SVG
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=For HTML
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
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
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=For SVG
|Android_supported=Yes
|Android_version=3.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}