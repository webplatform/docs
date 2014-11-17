{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>letter-spacing</code> CSS property specifies the spacing behavior between text characters.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=normal or absolute length
|Animatable=No
|CSS object model property=letterSpacing
|CSS percentages=
|Values={{CSS Property Value
|Data Type=normal
|Description=The spacing is the normal spacing for the current font.
}}{{CSS Property Value
|Data Type=length
|Description=Indicates inter-character space in addition to the default space between characters, followed by an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px). Values may be negative, but there may be implementation-specific limits.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A selection of examples showing some typical uses of the letter-spacing property.
|Code=&lt;p&gt;This is a simple paragraph with the default value for letter-spacing.&lt;/p&gt;

&lt;p class="pos"&gt;This is a simple paragraph with a altered letter-spacing value by 0.3em.&lt;/p&gt;

&lt;p class="neg"&gt;This is a simple paragraph withe a altered letter-spacing value by -0.1em&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/5671141
}}{{Single Example
|Language=CSS
|Description=
|Code=p {
    letter-spacing: normal;
}

p.pos {
    letter-spacing: .3em;
}

p.neg {
    letter-spacing: -.1em;
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=* Up to three different values can be specified, in the following order: optimum, minimum, maximum
* If one value is specified, it is used for all spacing. If two values are specified, the first is used for the optimum and minimum spacings, and the second is used for maximum.
|Notes=When specified as a positive '''length''' value, the '''letter-spacing''' attribute adds the specified value to the default spacing between characters within an element. A negative '''length''' value decreases the space between characters. Letter spacing can be influenced by justification.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/#letter-spacing
|Status=W3C Working Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Text
|Manual_links=*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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
|Opera_version=3.5
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=4.0.4
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
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
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.5
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}