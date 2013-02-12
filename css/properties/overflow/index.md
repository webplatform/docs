{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The overflow property controls how extra text  exceeding the bounding box of an element is rendered. The overflow property can be used in conjunction with an element that has a fixed width and height, to eliminate text-induced page distortion.}}
{{CSS Property
|Initial value=visible
|Applies to=non-replaced block-level elements and non-replaced ‘inline-block’ elements
|Inherited=No
|Media=visual
|Computed value=as specified, but with URIs made absolute
|Animatable=No
|CSS object model property=overflow
|Values={{CSS Property Value
|Data Type=visible
|Description=Default. Content is not clipped and scroll bars are not added.
}}{{CSS Property Value
|Data Type=scroll
|Description=Content is clipped and scroll bars are added, even if the content does not exceed the dimensions of the object.
}}{{CSS Property Value
|Data Type=hidden
|Description=Content that exceeds the dimensions of the object is not shown.
}}{{CSS Property Value
|Data Type=auto
|Description=Content is clipped and scrolling is added only when necessary.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Four simple p elements
|Code=&lt;!DOCTYPE HTML&gt;
&lt;html lang="en-US"&gt;
&lt;head&gt;
  &lt;meta charset="UTF-8"&gt;
  &lt;title&gt;Overflow example&lt;/title&gt;
  &lt;link href="overflow.css" type="text/css" rel="stylesheet"&gt;
&lt;/head&gt;
&lt;body&gt;
  &lt;p class="one"&gt;visible(defult): Content is not clipped and scroll bars are not added.&lt;/p&gt;
  &lt;p class="two"&gt;scroll: Content is clipped and scroll bars are added, even if the content does not exceed the dimensions of the object.&lt;/p&gt;
  &lt;p class="three"&gt;hidden: Content that exceeds the dimensions of the object is not shown.&lt;/p&gt;
  &lt;p class="four"&gt;auto: Content is clipped and scrolling is added only when necessary.&lt;/p&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://jsbin.com/oqinud/1
}}{{Single Example
|Language=CSS
|Code=p{
  width: 100px;
  height: 50px;
  border: 1px solid #aaa;
  float: left;
  margin-right: 10px;
}

.one{
  overflow: visible;
}
.two{
  overflow: scroll;
}
.three{
  overflow: hidden;
}
.four{
  overflow: auto;
}
}}
}}
{{Notes_Section
|Usage=The default value for the '''body''' element is '''auto'''.
Setting the '''overflow''' property to '''hidden''' on a '''textArea''' object hides its scroll bars.
Setting the '''overflow''' property to '''visible''' causes the content to clip to the size of the window or frame that contains the object.
With Microsoft Internet Explorer 6 and later, when you use the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration to specify standards-compliant mode, this property applies to the '''html''' object.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS 2.1
|URL=http://www.w3.org/TR/CSS2/visufx.html#overflow
|Status=W3C Recommendation
}}{{Related Specification
|Name=CSS basic box model
|URL=http://www.w3.org/TR/css3-box/#overflow0
|Status=Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables={{Imported Compatibility Table}}
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Box Model
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}