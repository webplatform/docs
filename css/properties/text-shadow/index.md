{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The CSS <code>text-shadow</code> property applies one or more drop shadows, outlines, or bevels, and numerous other effects to the text of an element. Each <code>text-shadow</code> property must contain both an x-offset and y-offset shadow value and, optionally, a blur radius and color value. The <code>text-shadow property</code> can include multiple comma-delimited shadow effects. Multiple shadow effects are applied in a first-to-last order, whereas the first shadow effect will appear at the top, and the last shadow effect at the bottom.}}
{{CSS Property
|Initial value=none
|Applies to=All elements and generated content
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=textShadow
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=None is a default value if unspecified. No shadow is displayed.
}}{{CSS Property Value
|Data Type=<color>
|Description=Optional. See [[css/color|CSS color values]] for possible keywords and notations. If not specified, a default color is chosen by a user agent. The color value can be specified either before or after the offset values.
}}{{CSS Property Value
|Data Type=<offset-x> <offset-y>
|Description=Offset values can be . Two [[css/data_types/length|<length>]] values that specify the shadow's distance from the text. 
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
|Language=CSS
|Description=This example uses all four values of the text-shadow property in the following order: <offset-x>, <offset-y>, <blur-radius>, and <color>.
|Code=p {
  text-shadow: 2px 2px 2px grey;
}
|LiveURL=http://code.webplatform.org/gist/5842702
}}{{Single Example
|Language=CSS
|Description=This example places a text shadow to the left and above the element's text. Since no color is specified the shadow will inherit the same color as the element, and since no blur radius is specified, the text shadow will not be blurred:
|Code=p {
  text-shadow: -0.1em -0.1em;
}
|LiveURL=http://code.webplatform.org/gist/5842702
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