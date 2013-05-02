{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The <code>@font-face</code> CSS at-rule allows authors to specify online fonts to display text on their web pages. By allowing authors to provide their own fonts, <code>@font-face</code> eliminates the need to depend on the limited number of fonts users have installed on their computers.}}
{{CSS_At_Rule
|Content=The <code>@font-face</code> at-rule may be used not only at the top level of a CSS, but also inside any CSS conditional-group at-rule.

<blockquote>'''Note:''' ''This is an experimental technology'' Because this technology's specification has not stabilized, check the compatibility table below for the proper prefixes to use in various browsers. Also note that the syntax and behavior of an experimental technology is subject to change in future versions of browsers as the spec changes.</blockquote>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example uses the Open Sans font to style the paragraph element.
|Code=/* Declare the font using @font-face. */
@font-face {
  font-family: "Open Sans";
  src: local("Open Sans"), /* Prefer a locally installed version of the font. */
       local("OpenSans"),
       /* URL requires a valid path to the respective font file.
          Same origin policy is applicable here.
       */
       url("/path/to/OpenSans.eot?#iefix") format("embedded-opentype"),
       url("/path/to/OpenSans.woff") format("woff"),
       url("/path/to/OpenSans.ttf") format("truetype"),
       url("/path/to/OpenSans.svg#OpenSans") format("svg");
  src: url("/path/to/OpenSans.eot");

  font-weight: normal;
  font-style: normal;
}

/* Use the font in your CSS as follows. */
p {
  font-family: "Open Sans", sans-serif;
}
|LiveURL=http://code.webplatform.org/gist/5481068
}}
}}
{{Notes_Section
|Notes====Remarks===
The rule has no default value.
This feature enables you to use specific fonts that might not be available on your local system. In Internet Explorer 8 and earlier, the URL must point to an Embedded OpenType (EOT) file (.eot or .ote format). No other font formats are supported. (For more information about the font embedding feature and pointers to a tool for creating .eot files, see About Font Embedding.)
In addition to legacy EOT format files, Internet Explorer 9 also supports the Web Open Font Format (WOFF) and installable (no embedding permission bits set) raw TrueType.
The <code>unicode-range</code> descriptor defines the range of Unicode characters that are supported by a given font. The values of ''urange'' are expressed by hexadecimal numbers prefixed by "<code>U+</code>", that correspond&gt; to Unicode character code points. The <code>unicode-range</code> descriptor serves as a hint for Windows Internet Explorer when it decides whether to download a font resource. Unicode range values are written by using hexadecimal values and are case insensitive. Each is prefixed by "<code>U+</code>" and multiple, discontinuous ranges are separated by commas. Whitespace before or after commas is ignored. Valid character code values vary between <code>0</code> and <code>10FFFF</code> inclusive. A single range has three basic forms:
*A single code point (for instance, <code>U+416</code>)
*An interval value range (for instance, <code>U+400-4ff</code>)
*A range where trailing ‘<code>?</code>’ characters imply ‘any digit value’ (for instance, <code>U+4??</code>)

The '''@font-face''' rule acts differently from the behavior that is specified in the World Wide Web Consortium (W3C) Cascading Style Sheets, Level 3 (CSS3) Working Draft in Internet Explorer 8. In particular, Internet Explorer 8 does not support format hint strings. Internet Explorer 9 supports format hint strings.
Dynamic HTML (DHTML) expressions can be used instead of the preceding value(s). As of Internet Explorer 8, expressions are not supported in IE8 Standards mode. For more information, see About Dynamic Properties.
|Import_Notes====Syntax===
<code>'''@font-face '''{ ''Font-Description'' }</code>
===Parameters===
;''Font-Description'':'''String''' that specifies one or more of the following descriptors:<table><tr><th>Value</th><th>Meaning</th></tr><tr><td width{{=}}"40%"><a id{{=}}"font-family_fontFamilyName"/><a id{{=}}"font-family_fontfamilyname"/><a id{{=}}"FONT-FAMILY_FONTFAMILYNAME"/><dl><dt>'''font-family:fontFamilyName'''</dt></dl></td><td width{{=}}"60%">A valid [[css/properties/font-family|'''font-family''']] property value.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"font-weight_fontWeight"/><a id{{=}}"font-weight_fontweight"/><a id{{=}}"FONT-WEIGHT_FONTWEIGHT"/><dl><dt>'''font-weight:fontWeight'''</dt></dl></td><td width{{=}}"60%">Internet Explorer 9. A valid [[css/properties/font-weight|'''font-weight''']] property value (except for the relative values, <code>bolder</code> and <code>lighter</code>).</td></tr><tr><td width{{=}}"40%"><a id{{=}}"font-style_fontStyleName"/><a id{{=}}"font-style_fontstylename"/><a id{{=}}"FONT-STYLE_FONTSTYLENAME"/><dl><dt>'''font-style:fontStyleName'''</dt></dl></td><td width{{=}}"60%">Internet Explorer 9. A valid [[css/properties/font-style|'''font-style''']] property value.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"font-stretch_fontStretchValue"/><a id{{=}}"font-stretch_fontstretchvalue"/><a id{{=}}"FONT-STRETCH_FONTSTRETCHVALUE"/><dl><dt>'''font-stretch:fontStretchValue'''</dt></dl></td><td width{{=}}"60%">Internet Explorer 9. A valid [[css/properties/font-stretch|'''font-stretch''']] property value.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"src_url_sURL__format_fontFormat__local_fontName_"/><a id{{=}}"src_url_surl__format_fontformat__local_fontname_"/><a id{{=}}"SRC_URL_SURL__FORMAT_FONTFORMAT__LOCAL_FONTNAME_"/><dl><dt>'''src:url(sURL) format(fontFormat) local(fontName)'''</dt></dl></td><td width{{=}}"60%">The location of a font file to use (either an external reference with an optional hint or a local reference). To specify an external reference, use ''url(sURL)'', where ''sURL'' is an absolute or relative URL. In Internet Explorer 8 and earlier versions, only one URL value is supported.To specify specific font formats (only for externally referenced font files), use a ''format'' hint (''format(fontFormat)'') where ''fontFormat'' is a comma-separated list of format strings that denote supported font formats. Possible ''fontFormat'' values are <code>"woff"</code>, <code>"truetype"</code>, <code>"opentype"</code>, and <code>"embedded-opentype"</code>. The ''format'' hint is optional starting in Internet Explorer 9. (''format'' hints are not supported in Internet Explorer 8 and earlier versions and are ignored.)To specify a local reference, use ''local(sFontName)'', where ''sFontName'' is the name of the locally-installed font to use.</td></tr><tr><td width{{=}}"40%"><a id{{=}}"unicode-range_urange"/><a id{{=}}"UNICODE-RANGE_URANGE"/><dl><dt>'''unicode-range:urange'''</dt></dl></td><td width{{=}}"60%">Internet Explorer 9. A list of Unicode character ranges, where ''urange'' is a comma-separated list of Unicode range values.</td></tr></table> 
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.5
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3.2
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.2
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=10
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10
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
|Feature=TTF/OTF - TrueType and OpenType Font
|Android_supported=Yes
|Android_version=2.3
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=10.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=WOFF - Web Open Font Format
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=18.0
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=15.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=10.0
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=11.5
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=5.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}{{Compatibility Table Mobile Row
|Feature=EOT - Embedded OpenType font
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=No
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Yes
|IE_mobile_version=10.0
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
|Safari_mobile_supported=No
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5.5 - 9.0
|Note=Supports EOT fonts only
}}{{Compatibility Notes Row
|Browser=Android
|Version=2.2 - 3.0
|Note=Partial support
}}{{Compatibility Notes Row
|Browser=Safari Mobile
|Version=3.2 - 4.1
|Note=Supports SVG fonts only
}}
}}
{{See_Also_Section
|Topic_clusters=Syntax
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/@font-face
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ms530757(v=vs.85).aspx
|HTML5Rocks_link=
}}