{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Property
|Applies to=All elements
|Media=visual
|Inherited=Yes
|Initial value=
|Values={{CSS_Property_Value|Data Type=color |Description=A '''String''' that specifies or receives one of the color names or RGB values in the Color Table.}}
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples use the '''color''' attribute and the '''color''' property to change the text color of an object.

This example uses a call to an embedded (global) style sheet to change the text color to <code>red</code> when an [[dom/events/mouseover|'''onmouseover''']] event occurs.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/color_h.htm
|Code=
&lt;STYLE&gt;
    .color1 { color:red }
    .color2 { color: }
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;SPAN STYLE{{=}}"font-size:14" onmouseover{{=}}"this.className{{=}}'color1'"
    onmouseout{{=}}"this.className{{=}}'color2'"&gt; . . .
}}
{{Single_Example
|Description=
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/color_s.htm
|Code=
&lt;SPAN STYLE{{=}}"font-size:14" onmouseover{{=}}"this.style.color{{=}}'red'"&gt;
:
&lt;/SPAN&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
These are different ways to specify a color—in this example, red.
 <code>EM { color: red }              /* natural language / CNS */
 EM { color: #F00 }             /* #RGB */
 EM { color: #FF0000 }          /* #RRGGBB */
 EM { color: rgb(1.0,0.0,0.0) } /* float range: 0.0 - 1.0 */
 EM { color: rgb(100%,0%,0%) ]  /* float range: 0.0 - 100.0 */</code>
Some browsers do not recognize color names, but all browsers should recognize RGB color values and display them correctly.
In Windows CE, specifying a value for the '''color''' property of the '''OPTION''' element when applied through the [[css/cssom/style|'''style''']] object has no effect.
Windows Internet Explorer 9 introduces support for the RGBA, HSL, and HSLA color models.
In Internet Explorer 9, the RGB color model has been extended to include an alpha channel, or transparency. The format of an RGBA value is <code>rgba(red,green,blue,alpha)</code>. The red, green, and blue components are identical to those of the RGB color model, and are expressed as integers or percentages. The alpha component is expressed as a value between 0.0 (completely transparent) and 1.0 (completely opaque).
Internet Explorer 9 supports hue-saturation-lightness (HSL) color values. The format of an HSL value is <code>hsl(hue,saturation,lightness)</code>. In the HSL color model, "hue" is defined as the indicated color's angle on the color wheel (for instance, red is 0 or 360, green is 120, blue is 240, and so on). "Saturation" and "lightness" are expressed as percentages.
Internet Explorer 9 also extends the HSL color model with an alpha channel. As with the RGBA model, the alpha channel is expressed as a value between 0.0 and 1.0. The format of an HSLA value is <code>hsla(hue,saturation,lightness,alpha)</code>.
|Import_Notes=
===Syntax===
<code>'''color: '''''
&lt;color&gt;
''</code>
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/runtimeStyle|runtimeStyle]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>Color Table</code>
|Topic_clusters=Visual Effects
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}