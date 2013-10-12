{{Page_Title|font-variant}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>font-variant</code> property enables you to select the small-caps font within a font family.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=fontVariant
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=Selects a font that is not a 'small-caps' font, usually the available 'normal' font.
}}{{CSS Property Value
|Data Type=small-caps
|Description=Selects a 'small-caps' font. If not small caps variant is available, the browser generates a small caps approximation.
}}{{CSS Property Value
|Data Type=inherit
|Description=Inherits the font-variant setting from its parent.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example to show the effect achieved when small-caps are applied to a text paragraph.
|Code=<p>I think WebPlatform rocks.</p>
|LiveURL=http://code.webplatform.org/gist/5716625
}}{{Single Example
|Language=CSS
|Description=The CSS applied to the HTML above.
|Code=p {
  font-size: 300%;
  font-variant: small-caps;	
}
|LiveURL=http://code.webplatform.org/gist/5716625
}}
}}
{{Notes_Section
|Notes=In ([http://www.w3.org/TR/css3-fonts/#propdef-font-variant CSS Fonts Module Level 3, W3C Working Draft 11 December 2012]), this property is extended. However, no browser seems to support these changes yet.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://www.w3.org/TR/css3-fonts/#propdef-font-variant
|Status=W3C Working Draft
|Relevant_changes=Changes the property to an overall shorthand for font rendering. Extends the options that can be used as value. Not implemented in any browser as of yet.
}}{{Related Specification
|Name=Cascading Style Sheets Level 2 Revision 1 (CSS 2.1) Specification
|URL=http://www.w3.org/TR/CSS21/fonts.html#small-caps
|Status=W3C Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Basic support (CSS2.1 version)
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
|Opera_version=3.5
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
|Topic_clusters=CSS Font, Fonts
|External_links=* MDN: [https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}