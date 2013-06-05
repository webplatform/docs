{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The <code>font-style</code> property allows italic or oblique faces to be selected within a font-family.}}
{{CSS Property
|Initial value=normal
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Computed value=as specified
|Animatable=No
|CSS object model property=fontStyle
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=normal
|Description=Selects a face that is classified as 'normal'.
}}{{CSS Property Value
|Data Type=italic
|Description=Selects a font that is labeled as 'italic' (cursive). If no font labeled 'italic' is available, a font that is labeled as 'oblique' is selected.
}}{{CSS Property Value
|Data Type=oblique
|Description=Selects a font that is labeled as 'oblique' (sloped version of the regular face). If no italic or oblique font is available, the browser slopes the normal version of the font to produce an oblique approximation.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A selection of examples showing uses of the font-style property.
|Code=&lt;p&gt;Regular ol' P&lt;/p&gt;
&lt;p class="normal"&gt;Normal P, no different from the regular ol' P&lt;/p&gt;
&lt;p class="italic"&gt;Italic P, the cursive version of the font&lt;/p&gt;
&lt;p class="oblique"&gt;Oblique P, the sloped version of the font&lt;/p&gt;
}}{{Single Example
|Language=CSS
|Code=p { font-family: "Trebuchet MS", "Gill sans", serif; }
p.normal { font-style: normal; }
p.italic { font-style: italic; }
p.oblique { font-style: oblique; }
|LiveURL=http://code.webplatform.org/gist/5628297
}}
}}
{{Notes_Section
|Usage=According to the specs, 'oblique' is a sloped version of the regular font. The example shows that the browsers actually use the 'italic' version for the 'oblique' variant as well. In the example, the bottom of the regular 'f' aligns with the bottom of the surrounding text. In the oblique line, this should be the case as well, but instead it shows the cursive 'f' that extends below the surrounding letters.
[[file:screenshot-font-style-example.png]]
|Notes====Remarks===
The '''oblique''' value is available as of Microsoft Internet Explorer 4.0. Internet Explorer 4.0 renders italic and oblique identically.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Fonts Module Level 3
|URL=http://www.w3.org/TR/css3-fonts/#font-style-prop
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSS Font, Fonts
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>[[css/properties/font|font]]</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/font-style
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}