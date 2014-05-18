{{Page_Title|text-shadow}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The CSS <code>text-shadow</code> property applies one or more drop shadows to the text and <code>[[css/properties/text-decoration|<text-decorations>]]</code> of an element. Each shadow is specified as an offset from the text, along with optional color and blur radius values.}}
{{CSS Property
|Initial value=none
|Applies to=all elements
|Inherited=Yes
|Media=visual
|Computed value=a color plus three absolute lengths
|Animatable=Yes, as shadow list
|CSS object model property=textShadow
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Default value.
}}{{CSS Property Value
|Data Type=<offset-x>
|Description=Required. Specifies the horizontal <code>[[css/data_types/length|<length>]]</code> term to the right of the text. A negative horizontal <code>[[css/data_types/length|<length>]]</code> term will place the shadow to the left of the text.
}}{{CSS Property Value
|Data Type=<offset-y>
|Description=Required. Specifies the vertical <code>[[css/data_types/length|<length>]]</code> value below the text. A negative vertical <code>[[css/data_types/length|<length>]]</code> term will place the shadow above the text.
}}{{CSS Property Value
|Data Type=<blur-radius>
|Description=Optional. The blur radius is a <code>[[css/data_types/length|<length>]]</code> term that indicates the boundaries of the blur effect.
}}{{CSS Property Value
|Data Type=<color>
|Description=Optional. A color value may be applied before or after the <code>[[css/data_types/length|<length>]]</code> terms of both shadow effects. The color value will be inherited as the basis for the shadow. If a color is not specified by the user, the value of the color property will be used instead.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=*/ This example uses all four values of the text-shadow property in the following order: <offset-x>, <offset-y>, <blur-radius>, and <color>. /*

p {
  text-shadow: 2px 2px 2px grey;
}
|LiveURL=http://code.webplatform.org/gist/5842702
}}{{Single Example
|Language=CSS
|Code=*/ This example uses both required offset values, <offset-x> and <offset-y>. The optional <blur-radius> and <color> values have been omitted. /*

p {
  text-shadow: -0.1em -0.1em;
}
|LiveURL=http://code.webplatform.org/gist/5864800
}}{{Single Example
|Language=CSS
|Code=*/ This example shows multiple shadow effects separated by a comma. Note the use of various units and color models applied to the values. /*

p {
  text-shadow: -0.1em -0.1em 1em purple, 3px 3px 0.1em rgba(0, 0, 0, 0.5);
}
|LiveURL=http://code.webplatform.org/gist/5864841
}}
}}
{{Notes_Section
|Usage=The <code>text-shadow</code> propertie can also be used to draw outlines, bevels, and other effects.
|Notes=Multiple shadows are applied front-to-back, with the first-specified shadow on top.

The <code>text-shadow</code> property applies to both the ::first-line and ::first-letter pseudo-elements.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Decoration Module Level 3
|URL=http://www.w3.org/TR/css-text-decor-3/#text-shadow-property
|Status=Working Draft
|Relevant_changes=Lists text-shadow as animatable.
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
|Notes_rows={{Compatibility Notes Row
|Browser=Firefox
|Version=4.0 and later
|Note=cap the blur radius at 300 for performance reasons
}}{{Compatibility Notes Row
|Browser=Firefox
|Version=N/A
|Note=if the <color> value is undefined, Firefox use the elements <code>[[css/properties/color|<color>]]</code> value
}}{{Compatibility Notes Row
|Browser=Opera
|Version=N/A
|Note=max. 6-9 text-shadows for performance reason
}}{{Compatibility Notes Row
|Browser=Opera
|Version=N/A
|Note=blur radius is limited to 100px
}}
}}
{{See_Also_Section
|Topic_clusters=Text
}}
{{Topics|CSS, Design}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow
|MSDN_link=
|HTML5Rocks_link=
}}