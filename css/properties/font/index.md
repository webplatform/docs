{{Page_Title|font}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>font</code> property is shorthand that allows you to do one of two things: you can either set up six of the most mature font properties in one line, or you can set one of a choice of keywords to adopt a system font setting.}}
{{CSS Property
|Initial value=normal for font-style, font-variant and font-weight. medium for font-size. normal for line-height. font-family initial value differs depending on the user agent.
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=For <code>font-style</code> as specified. For <code>font-variant</code> as specified. For <code>font-weight</code> the keyword or the numerical value as specified, with bolder and lighter transformed to the real value. For <code>font-size</code> as specified, but with relative lengths converted into absolute lengths. For percentage and length values of <code>line-height</code>, the absolute length, otherwise as specified; </code>font-family</code> as specified.
|Animatable=Yes
|CSS object model property=font
|Values={{CSS Property Value
|Data Type=font-weight font-style font-variant font-size/line-height font-family
|Description=<code>font</code> can take up to six separate parts in its value, which set six different longhand property values. The options are as follows:

* <code>font-weight</code>: Sets boldness of font; can take values of <code>normal</code> (default), <code>bold</code> (standard bold weight), <code>lighter</code> or <code>bolder</code> (supposed to be a slightly lighter or bolder weight that standard <code>bold</code>), inherit, or various numerical values to indicate different degrees of boldness: <code>100</code>, <code>200</code>, <code>300</code>, <code>400</code>, <code>500</code>, <code>600</code>, <code>700</code>, <code>800</code>, or <code>900</code>.
* <code>font-style</code>: Allows an italic or oblique font face to be applied; values options are <code>normal</code> (default), italic, oblique, or inherit.
* <code>font-variant</code>: Allows a small caps font variant to be set. Value options are <code>normal</code> (default), <code>small-caps</code>, or <code>inherit</code>.
* <code>font-size/</code>: Sets a size for the font. Options are absolute size keywords (<code>xx-small</code>, <code>x-small</code>, <code>small</code>, <code>medium</code> (the default value), <code>large</code>, <code>x-large</code> or <code>xx-large</code>), relative size keywords (<code>smaller</code> or <code>larger</code>, which indicate a keyword size smaller or larger than the parent element's font size), length values (for example <code>12px</code>, or <code>5rem</code>), percentage values (for example <code>80%</code>), or <code>inherit</code>.
* <code>line-height</code>: Sets the height of the line the font is sat on. Value options include <code>normal</code> (the default), unitless values (for example <code>1.7</code>), length values (for example <code>20px</code> or <code>3.5rem</code>), percentage values (for example <code>120%</code>), or <code>inherit</code>.
* <code>font-family</code>: Allows one or more font family names and/or generic family names to be specified for usage on the selected element(s)' text. The browser then goes through the list; for each character in the selection it applies the first font family that has an available glyph for that character.
}}{{CSS Property Value
|Data Type=system font
|Description=Alternatively, you can set the value to be a single keyword that corresponds to a system font used to style a certain feature of the system the browser is running on (some browsers offer more, proprietary options. For more, see the links at the bottom of the document): 

* <code>caption</code>: User-preference font used in objects that have captions—buttons, labels, and so on.
* <code>icon</code>: User-preference font used in icon labels.
* <code>menu</code>: User-preference font used in menus.
* <code>message-box</code>: User-preference font used in dialog boxes.
* <code>small-caption</code>: User-preference font used in small controls.
* <code>status-bar</code>: User-preference font used in small controls.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A selection of examples showing some typical uses of the <code>font</code> property.
|Code=&lt;p class="example-one"&gt;Example One: We &hearts; WebPlatform Docs!&lt;/p&gt;

&lt;p class="example-two"&gt;Example Two: Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis, eos, dicta nihil aliquid quia dolores labore nesciunt unde consectetur blanditiis ex eius consequatur qui incidunt voluptatem inventore fugit quos amet!&lt;/p&gt;

&lt;p class="example-three"&gt;Example Three: Eius, earum unde eum distinctio ex accusamus rem eligendi optio mollitia deleniti? Iure, accusamus, fuga ipsa quas doloremque enim velit sed est earum pariatur ab optio quia molestiae repellendus non.&lt;/p&gt;
}}{{Single Example
|Language=CSS
|Code=.example-one {
  /*    size  family    */
  font: 1.5em sans-serif;
}

.example-two {
  /*    style  variant    weight size/line-height family    */
  font: italic small-caps bold   1em/1.5em        sans-serif; 
}

.example-three {
  /*    weight size/line-height family                         */
  font: bold   1em/2em          "Times New Roman", Times, serif;
}
|LiveURL=http://dabblet.com/gist/5521520
}}{{Single Example
|Language=HTML
|Description=A couple of theoretical font examples, showing first a <code>font</code> property value with all possible longhand values included, and second, a system default font being used.
|Code=.one {
  font: bold italic small-caps 18px/24px georgia;
}		

.two {
  font: status-bar;
}
|LiveURL=http://code.webplatform.org/gist/5586740
}}{{Single Example
|Language=CSS
|Code=<p class="one">First font example.<br>This shows all possible longhand values being used at once.</p>
<p class="two">Second font example.<br>This shows a system default being used.</p>
|LiveURL=http://code.webplatform.org/gist/5586740
}}
}}
{{Notes_Section
|Notes=*The '''font-style''', '''font-variant''', and '''font-weight''' values may appear in any order before '''font-size'''. However, the '''font-size''', '''line-height''', and '''font-family''' properties must appear in the order listed. Setting the '''font''' property also sets the component properties. In this case, the string must be a combination of valid values for the component properties; only '''font-family''' may have more than one value. 
If the string does not contain a value for a component property, that property is set to its default, regardless of prior settings for that component property.
* Read https://developer.mozilla.org/en-US/docs/Web/CSS/font for more information on Firefox's additional proprietary system font settings.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=6 and later
|Note=When the [[html/elements/!DOCTYPE|!DOCTYPE]] declaration is used to specify standards-compliant mode, the following conditions apply to this property -<br/>- The '''font-size''' and '''font-family''' values must be declared. If '''font-size''' and '''font-family''' are not declared, or are not in the correct order, the '''font''' property is ignored.<br/>- All specified values must appear in the correct order. Otherwise, the '''font''' property is ignored.<br/>- The default '''font-size''' is '''small''', not '''medium'''. If not explicitly set, '''font-size''' returns a point value.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=9 and later
|Note=Does not support the '''rem''' unit (it is supported for the separate properties).
}}
}}
{{See_Also_Section
|Topic_clusters=Fonts
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}