{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|the <code>font</code> property is shorthand that allows you to do one of two things: you can either set up six of the most mature font properties in one line, or you can set one of a choice of keywords to adopt a system font setting.}}
{{CSS Property
|Initial value=<code>normal</code> for <code>font-style</code>, <code>font-variant</code> and <code>font-weight</code>. <code>medium</code> for <code>font-size</code>. <code>normal</code> for <code>line-height</code>. <code>font-family</code> initial value differs depending on the user agent.
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=For <code>font-style</code> as specified. For <code>font-variant</code> as specified. For <code>font-weight</code> the keyword or the numerical value as specified, with bolder and lighter transformed to the real value. For <code>font-size</code> as specified, but with relative lengths converted into absolute lengths. For percentage and length values of <code>line-height</code>, the absolute length, otherwise as specified; </code>font-family</code> as specified.
|Animatable=Yes
|CSS object model property=font
|Values={{CSS Property Value
|Data Type=font-weight font-style font-variant font-size/line-height font-family
|Description=Any of the range of font-style values available to the [[css/properties/font-style|'''font-style''']] property.
}}{{CSS Property Value
|Data Type=system font
|Description=caption: User-preference font used in objects that have captions—buttons, labels, and so on.
icon: User-preference font used in icon labels.
menu: User-preference font used in menus.
message-box: User-preference font used in dialog boxes.
small-caption: User-preference font used in small controls.
status-bar: User-preference font used in small controls.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=The following example demonstrates some of the uses of the <code>font</code> property.
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
|Code=&lt;p class="example-one"&gt;Example One: We &hearts; WebPlatform Docs!&lt;/p&gt;

&lt;p class="example-two"&gt;Example Two: Lorem ipsum dolor sit amet, consectetur adipisicing elit. Officiis, eos, dicta nihil aliquid quia dolores labore nesciunt unde consectetur blanditiis ex eius consequatur qui incidunt voluptatem inventore fugit quos amet!&lt;/p&gt;

&lt;p class="example-three"&gt;Example Three: Eius, earum unde eum distinctio ex accusamus rem eligendi optio mollitia deleniti? Iure, accusamus, fuga ipsa quas doloremque enim velit sed est earum pariatur ab optio quia molestiae repellendus non.&lt;/p&gt;
}}
}}
{{Notes_Section
|Notes=This is a composite property that specifies up to six font values. The '''font-style''', 
'''font-variant''', and '''font-weight''' values may appear in any order before '''font-size'''. However, the '''font-size''', '''line-height''', and '''font-family''' properties must appear in the order listed. Setting the '''font''' property also sets the component properties. In this case, the string must be a combination of valid values for the component properties; only '''font-family''' may have more than one value. 
If the string does not contain a value for a component property, that property is set to its default, regardless of prior settings for that component property.
|Import_Notes====Syntax===
<code>'''font: ''''''[''' '''[''' font-style '''{{!}}{{!}}''' font-variant '''{{!}}{{!}}''' font-weight ''']''''''?''' font-size '''[''' / line-height ''']''''''?''' font-family ''']''' '''{{!}}''' caption '''{{!}}''' icon '''{{!}}''' menu '''{{!}}''' message-box '''{{!}}''' small-caption '''{{!}}''' status-bar</code>
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}