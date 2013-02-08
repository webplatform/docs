{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This property adjusts the font-size of the fallback fonts defined with font-family, so that the x-height is the same no matter what font is used. This preserves the readability of the text when fallback occurs.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=fontSizeAdjust
|Values={{CSS Property Value
|Data Type=none
|Description=Only use the font-size value to determine the size of the font.
}}{{CSS Property Value
|Data Type=number
|Description=The aspect value used in calculating the size of the fallback fonts.. For the adjusted font size calculation, see Remarks.
}}{{CSS Property Value
|Data Type=auto
|Description=The aspect value is calculated by the user agent for the first font in the font-family list, and used for every font in that list.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=p { font-family: Courier, serif; font-size: 10pt; font-size-adjust: 0.4; }
|LiveURL=http://dabblet.com/gist/4740493
}}{{Single Example
|Description=Transitioning a paragraph to a smaller font-size using font-size-adjust.
|LiveURL=http://codepen.io/anon/pen/Gtuwa
}}
}}
{{Notes_Section
|Usage=This property is only supported by Firefox, as of version 3.
|Notes====Remarks===
For any given font size, the apparent size and legibility of text varies across fonts. For scripts such as Latin or Cyrillic that distinguish between uppercase and lowercase letters, the relative height of lowercase letters compared to their uppercase counterparts is a determining factor of legibility. This is commonly referred to as the '''aspect value'''. Precisely defined, it is equal to the x-height of a font (the height of a font's lowercase 'x' character) divided by the font size.
In situations where font fallback occurs, fallback fonts cannot share the same aspect ratio as the desired font family and  thus appear less legible. Font fallback occurs when the specified font is not available and the client uses a fallback font, or a replacement font. The '''font-size-adjust''' property is a way to preserve the legibility of text when font fallback occurs. It does this by adjusting the font size so that the x-height is the same regardless of the font that is used.
The following calculation uses the '''number''' value to calculate the adjusted font size: <code>c  {{=}}  ( a / a' ) s</code>
In this equation, <code>s</code> is the font-size value, <code>a</code> is the '''number''' value of the '''font-size-adjust''' property, <code>a'</code> is the aspect value of the actual font, and <code>c</code> is the adjusted font size to use.
This property applies to any font that is selected, but in typical usage it should be based on the aspect value of the first font in the font-family list. If this is specified accurately, the (<code>a/a'</code>) term in the formula listed previously is 1 for the first font and no adjustment occurs. If the value is specified inaccurately, text that is rendered by using the first font in the family list displays differently in earlier versions of Windows Internet Explorer, which do not support the '''font-size-adjust''' property.
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199818 Scalable Vector Graphics: Text], Section 10.10
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://dev.w3.org/csswg/css3-fonts/#propdef-font-size-adjust
|Status=Editor's draft 6 February 2013
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=No
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3+
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Font, Fonts
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/properties/font-stretch|font-stretch]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}