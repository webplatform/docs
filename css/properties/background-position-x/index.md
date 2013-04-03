{{Page_Title}}
{{Flags
|Content=Broken Links, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Sets the horizontal position of a background image.}}
{{CSS Property
|Initial value=0%
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=as specified
|Animatable=No
|Values={{CSS Property Value
|Data Type=length
|Description=Floating-point number, followed by an absolute units designator (<code>cm</code>, <code>mm</code>, <code>in</code>, <code>pt</code>, or <code>pc</code>) or a relative units designator (<code>em</code>, <code>ex</code>, or <code>px</code>). For more information about the supported length units, see CSS Values and Units Reference.
}}{{CSS Property Value
|Data Type=percentage
|Description=Integer, followed by a percent sign (%). The value is a percentage of the width or height of the object.
}}{{CSS Property Value
|Data Type=hAlignment
|Description=Horizontal alignment value (e.g. "left", "right", or "center").
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Moving the background image to the right by 50px.
|Code=background-position-x: 50px;
}}{{Single Example
|Language=CSS
|Description=Moving the background image to the left by 50px.
|Code=background-position-x: -50px;
}}{{Single Example
|Language=CSS
|Description=Moving the background image to the right by half the width of its element.
|Code=background-position-x: 50%;
}}{{Single Example
|Language=CSS
|Description=Moving the background image to the left by half the width of its element.
|Code=background-position-x: -50%;
}}{{Single Example
|Language=CSS
|Description=Centering a background image inside its element.
|Code=background-position-x: center;
}}
}}
{{Notes_Section
|Usage====Usage===
* Often used to manipulate sprites (i.e. using CSS to expose small portions of a single background image, which is composed of multiple smaller images, such that HTTP requests are reduced).
* If browser support is of utmost importance, use [[background-position]] instead.
|Notes====Remarks===
* Windows Internet Explorer 8. The '''-ms-background-position-x''' attribute is an extension to CSS, and can be used as a synonym for '''background-position-x''' in IE8 Standards mode.

* Although background-position-x is currently non-standard, Jonathan Snook provides a case for its inclusion regarding right-to-left languages, such as Arabic or Hebrew. When using sprites, developers would be able to accomodate LTR and RTL environments with a single line of code by including the background-position-x property, rather than redeclaring every single sprite's position in their stylesheet.  [http://snook.ca/archives/html_and_css/background-position-x-y Read his blog entry on this and the background-position-y property.]
|Import_Notes====Syntax===
<code>'''background-position-x: '''length '''{{!}}''' percentage '''{{!}}''' hAlignment</code>
===Standards information===
There are no standards that apply here.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=7
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=3
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Background
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/background-position-y|-ms-background-position-y]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ff521123(v=vs.85).aspx]
|HTML5Rocks_link=
}}