{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>font-size-adjust</code> property adjusts the font-size of the fallback fonts defined with [[css/properties/font-family|font-family]], so that the [[x-height]] is the same no matter what font is used. This preserves the readability of the text when fallback happens.}}
{{CSS Property
|Initial value=none
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=Yes
|CSS object model property=fontSizeAdjust
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=none
|Description=Only use the font-size value to determine the size of the font.
}}{{CSS Property Value
|Data Type=number
|Description=The value used in calculating the size of the fallback fonts. For the adjusted font size calculation, see [[css/properties/font-size-adjust#Notes|Notes]].
}}{{CSS Property Value
|Data Type=auto
|Description=The aspect value is calculated by the browser for the first font in the font-family list, and used for every font in that list.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The popular font "Verdana" has an aspect value of 0.58. For comparison, Times New Roman has an aspect value of 0.45. Verdana will be more readable at smaller sizes than Times New Roman. Conversely, Verdana will often look 'too big' if substituted for Times New Roman.
|Code=&lt;table&gt;
  &lt;tr&gt;
    &lt;td class="demoblock"&gt;
      &lt;p class="verdana"&gt;Normal "Verdana" font text. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed tempus mattis lorem sed fringilla. Duis eu nulla dolor. Donec tempor risus sem, vitae sollicitudin nulla sagittis sit amet. Nulla laoreet augue in libero posuere lobortis. &lt;/p&gt;
	&lt;/td&gt;  
    &lt;td class="demoblock"&gt;
      &lt;p class="times"&gt;Normal "Times New Roman" font text. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed tempus mattis lorem sed fringilla. Duis eu nulla dolor. Donec tempor risus sem, vitae sollicitudin nulla sagittis sit amet. Nulla laoreet augue in libero posuere lobortis.&lt;/p&gt;
    &lt;td class="demoblock"&gt;
      &lt;p class="adjust"&gt;"Times New Roman" with font-size-adjust of 0.58. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed tempus mattis lorem sed fringilla. Duis eu nulla dolor. Donec tempor risus sem, vitae sollicitudin nulla sagittis sit amet. Nulla laoreet augue in libero posuere lobortis.&lt;/p&gt;
	&lt;/td&gt;  
  &lt;/tr&gt;
&lt;/table&gt;
}}{{Single Example
|Language=CSS
|Code=.demoblock {
	width: 33%;
}

p {
	font-size: 8px;
}

p.verdana { 
	font-family: Verdana,"Times New Roman", serif;
}

p.times {
	font-family: "Times New Roman";
}

p.adjust {
	font-family: hoge, "Times New Roman", serif;
	font-size-adjust: 0.58;
}
}}
}}
{{Notes_Section
|Notes=In script types that distinguish between uppercase and lowercase letters, such as the Latin script used for English, the height of the lowercase letters relative to the height of the uppercase letters impacts readability at smaller type sizes. This relation is called the '''aspect value''', which is calculated by dividing a font's '''[[x_height|x-height]]''' by the font's size.

The '''font-size-adjust''' property preserves the readability of text when the first specified font is not available and a fallback or replacement font is used. It adjusts the [[css/properties/font-size|font-size]] so the '''[[x_height|x-height]]''' of the fallback or replacement is similar to the '''[[x_height|x-height]]''' of the font it's replacing. 

Specify a value of '''auto''' to have the browser calculate the '''aspect value''' of the primary font and apply it to fallback or replacement fonts. When specifying a '''number''' value, use the preferred '''aspect value''' and the browser will apply it to fallback or replacement fonts using the following formula:

c = (p / a) * s

Where:
* c = adjusted font size
* p = preferred '''aspect value'''
* a = '''aspect value''' of the replacement or fallback
* s = the font size

As an abstract example, assume you specify a font-size-adjust value of 0.5, your fallback font's '''aspect value''' is .4, and the [[css/properties/font-size|font-size]] is 8px. The fallback font is rendered at 10px ((.5 /.4) * 8).

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://www.w3.org/TR/css3-fonts/#propdef-font-size-adjust
|Status=W3C Working Draft
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