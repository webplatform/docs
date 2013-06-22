{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The CSS text-shadow property adds one or more shadows to a specified text or [[html|HTML]] element. The text-shadow property accepts a comma-separated list of values that can be applied to the text and [[css/properties/text-decoration|text-decorations]].}}
{{CSS Property
|Initial value=none
|Applies to=All elements and generated content
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=textShadow
|Values={{CSS Property Value
|Data Type=none
|Description=Default. Indicates there is no shadow.
}}{{CSS Property Value
|Data Type=<color>
|Description=Optional. See [[css/color|CSS color values]] for possible keywords and notations. If not specified, the color used depends on the browser. The color value can be specified either before or after the offset values.
}}{{CSS Property Value
|Data Type=<offset-x> <offset-y>
|Description=Required. Two [[css/data_types/length|<length>]] values that specify the shadow's distance from the text. 
The first is the horizontal distance, with positive values moving it to the right, and negative values moving it to the left.
The secont is the vertical distance, with positive values moving the shadow down, and negative values moving it up.
}}{{CSS Property Value
|Data Type=<blur-radius>
|Description=Optional. The blur radius is a [[css/data_types/length|<length>]] value that indicates the boundaries of the blur effect. Defaults to 0.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The following examples use the HTML as described below:
|Code=&lt;!DOCTYPE html&gt;
&lt;html&gt;
  &lt;head&gt;
    &lt;title&gt;Text-shadow example&lt;/title&gt;
  &lt;/head&gt;
  &lt;body&gt;
    &lt;div id=&quot;foo&quot;&gt;bar&lt;/div&gt;
  &lt;/body&gt;
&lt;/html&gt;
}}{{Single Example
|Language=CSS
|Description=The following example creates a duplicate text, a solid text-shadow, 10px to the bottom right. The color shows the default color based on the UA.
|Code=#foo {
  text-shadow: 10px 10px;
}
|LiveURL=http://codepen.io/pverbeek/pen/BkcLe
}}{{Single Example
|Language=CSS
|Description=The following example creates a duplicate text, a solid text-shadow, 10px to the top right. With a greenish color.
|Code=#foo {
  text-shadow: 10px -10px OliveDrab;
}
|LiveURL=http://codepen.io/pverbeek/pen/GKIgi
}}{{Single Example
|Language=CSS
|Description=The following example creates a greenish blurred text-shadow without an offset.
|Code=#foo {
  text-shadow: #bada55 -10px -10px 2px;
}
|LiveURL=http://codepen.io/pverbeek/pen/cJLlz
}}{{Single Example
|Language=CSS
|Description=The following example shows that text-decorations will also be shown in the shadow.
|Code=#foo {
  text-decoration: line-through;
  text-shadow: rgb(0,0,0) 15px 15px 2px;
}
|LiveURL=http://codepen.io/pverbeek/pen/kaeKD
}}{{Single Example
|Language=CSS
|Description=The following example demonstrates the multiple text-shadows.
|Code=#foo {
  text-shadow: hsl(0,0,0) 15px 15px 2px,
               rgba(255,0,0,.5) -15px -15px,
               navy -15px 15px 8px,
               #00FF00 15px -15px;
}
|LiveURL=http://codepen.io/pverbeek/pen/HyrfE
}}
}}
{{Notes_Section
|Notes=Multiple shadows are applied front-to-back, with the first-specified shadow on top.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Decoration Module Level 3
|URL=http://www.w3.org/TR/css-text-decor-3/#text-shadow-property
|Status=Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=2.0.158.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=9.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Text
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}