{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=The live example link uses "/path/to" which is great to demonstrate the syntax, but should we use a working example like Google Fonts for the sandbox?
|Checked_Out=No
|High-level issues=Data Not Semantic
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>@font-face</code> CSS at-rule allows authors to specify online fonts to display text on their web pages. By allowing authors to provide their own fonts, <code>@font-face</code> eliminates the need to depend on the limited number of fonts users have installed on their computers.}}
{{CSS_At_Rule
|Content=The <code>@font-face</code> at-rule may be used not only at the top level of a CSS, but also inside any CSS conditional-group at-rule.

==Syntax==
<syntaxhighlight lang="css">
@font-face {
  [font-family: <family-name>;]?
  [src: [ <uri> [format(<string>#)]? | <font-face-name> ]#;]?
  [unicode-range: <urange>#;]?
  [font-variant: <font-variant>;]?
  [font-feature-settings: normal|<feature-tag-value>#;]?
  [font-stretch: <font-stretch>;]?
  [font-weight: <weight>];
  [font-style: <style>];
}
</syntaxhighlight>

===Values===
;'''&lt;family-name&gt;'''
:''Specifies a [[css/properties/font-family|'''font-family''']] name that will be used as font face value for font properties.''
;'''&lt;uri&gt;'''
:''The location of a font file to use (either an external reference with an optional hint or a local reference). To specify an external reference, use '''url(sURL)''', where '''sURL''' is an absolute or relative URL. To specify specific font formats (only for externally referenced font files), use a '''format''' hint ('''format(fontFormat)''') where '''fontFormat''' is a comma-separated list of format strings that denote supported font formats. Possible '''fontFormat''' values are '''woff''', '''truetype''', '''opentype''', and '''embedded-opentype'''. The '''format''' hint is optional.

:''To specify a local reference, use '''local(sFontName)''', where '''sFontName''' is the name of the locally-installed font to use.  If that font is not found, other sources will be tried until one is found.''
;'''&lt;urange&gt;'''
:''A list of Unicode character ranges, where ''urange'' is a comma-separated list of Unicode range values.''
;'''&lt;font-variant&gt;'''
:''A [[css/properties/font-variant|'''font-variant''']] value.''
;'''&lt;font-stretch&gt;'''
:''A valid [[css/properties/font-stretch|'''font-stretch''']] property value.''
;'''&lt;weight&gt;'''
:''A valid [[css/properties/font-weight|'''font-weight''']] property value (except for the relative values, <code>bolder</code> and <code>lighter</code>).''
;'''&lt;style&gt;'''
:''A valid [[css/properties/font-style|'''font-style''']] property value.''
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
|Usage=Use this at-rule in order to use specific fonts that might not be available on your local system.
|Notes=The rule has no default value.
The <code>unicode-range</code> descriptor defines the range of Unicode characters that are supported by a given font. The values of ''urange'' are expressed by hexadecimal numbers prefixed by "<code>U+</code>", that correspond&gt; to Unicode character code points. The <code>unicode-range</code> descriptor serves as a hint for the browser when it decides whether to download a font resource. Unicode range values are written by using hexadecimal values and are case insensitive. Each is prefixed by "<code>U+</code>" and multiple, discontinuous ranges are separated by commas. Whitespace before or after commas is ignored. Valid character code values vary between <code>0</code> and <code>10FFFF</code> inclusive. A single range has three basic forms:
*A single code point (for instance, <code>U+416</code>)
*An interval value range (for instance, <code>U+400-4ff</code>)
*A range where trailing ‘<code>?</code>’ characters imply ‘any digit value’ (for instance, <code>U+4??</code>)
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://www.w3.org/TR/css3-fonts/
|Status=Working Draft
|Relevant_changes=
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=
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
|Feature=
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
|Version=5.5 - 8
|Note=Only Embedded OpenType (EOT) file (.eot or .ote format) is supported.
}}{{Compatibility Notes Row
|Browser=Android
|Version=2.2 - 3.0
|Note=Partial support
}}{{Compatibility Notes Row
|Browser=Safari Mobile
|Version=3.2 - 4.1
|Note=Only SVG font is supported.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and earlier
|Note=Only one URL value is supported as the ```src``` value.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and earlier
|Note='''format(fontFormat)''' is not supported.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9 and later
|Note=Installable (no embedding permission bits set) raw TrueType are also supported.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5.5 - 7
|Note=Expressions can be used instead of '''format(fontFormat)'''.
}}{{Compatibility Notes Row
|Browser=WebKit based browsers
|Version=Any
|Note=The same origin policy is not implemented.
}}{{Compatibility Notes Row
|Browser=Chrome
|Version=37 and later
|Note=The same origin policy is implemented.
}}{{Compatibility Notes Row
|Browser=Opera
|Version=24 and later
|Note=The same origin policy is implemented.
}}
}}
{{See_Also_Section
|Topic_clusters=Fonts, Syntax
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/@font-face
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/ms530757(v=vs.85).aspx
|HTML5Rocks_link=
}}