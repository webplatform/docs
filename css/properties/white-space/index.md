{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The white-space property controls whether and how white space inside the element is collapsed, and whether lines may wrap at unforced "soft wrap" opportunities.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=whiteSpace
|Values={{CSS Property Value
|Data Type=normal
|Description=This value prevents user agents from collapsing sequences of white space. Segment breaks such as line feeds and carriage returns are preserved as forced line breaks. Lines only break at forced line breaks; content that does not fit within the block container overflows it.
}}{{CSS Property Value
|Data Type=nowrap
|Description=Like <code>normal</code>, but content does not wrap to the next line.
}}{{CSS Property Value
|Data Type=pre
|Description=Line breaks and other whitespace are preserved.
}}{{CSS Property Value
|Data Type=pre-line
|Description=Like <code>normal</code>, this value collapses consecutive spaces and allows wrapping, but preserves segment breaks in the source as forced line breaks.
}}{{CSS Property Value
|Data Type=pre-wrap
|Description=Like <code>pre</code>, but allows wrapping (like <code>normal</code>'s wrapping).
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=See the live example that has all the properties implemented side by side for comparison.
|Code=/**
 * white-space
 * CSS3 property
 * http://docs.webplatform.org/wiki/css/properties/white-space
 */

.white-space--nowrap {
  white-space:nowrap;
}

.white-space--normal {
  white-space:normal;
}

.white-space--pre {
  white-space:pre;
}

.white-space--pre-wrap {
  white-space:pre-wrap;
}

.white-space--pre-line {
  white-space:pre-wrap;
}

body {
  font-size: large;
  width: 500px;
}

p {
  background-color: #ddd;
}
|LiveURL=http://code.webplatform.org/gist/7284477
}}
}}
{{Notes_Section
|Notes=Whitespace, such as line breaks, spaces, and tabs, is collapsed by default in HTML documents. You can use the nonbreaking space entity <code>(&amp;nbsp;)</code> to add extra spaces to an object when the '''white-space''' property is set to '''normal''' or '''nowrap'''.  You can add extra line breaks using the '''br''' element.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Text Module Level 3
|URL=http://www.w3.org/TR/css3-text/#white-space-property
|Status=Working Draft
}}
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
|Internet_explorer_version=5.5
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=4.0
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
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Reference</code>
*<code>pre</code>
*<code>[[css/properties/word-wrap|-ms-word-wrap]]</code>
*<code>Other Resources</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/Web/CSS/white-space
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}