{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Specifies the font for an element.}}
{{CSS Property
|Applies to=All elements
|Inherited=Yes
|Media=visual
|Animatable=No
|Values={{CSS Property Value
|Data Type=family-name
|Description=Any of the available font families supported by the browser. For example, <code>Times</code>, <code>Helvetica</code>, <code>Zapf-Chancery</code>, <code>Western</code>, or <code>Courier</code>.
}}{{CSS Property Value
|Data Type=generic-family
|Description=Any of the following font families: <code>serif</code>, <code>sans-serif</code>, <code>cursive</code>, <code>fantasy</code>, or <code>monospace</code>.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use a call to an embedded style sheet to set the '''font-family''' attribute .
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;STYLE&gt;
	P {font-family:"ARIAL"}
	.other {font-family:"COURIER"}
&lt;/STYLE&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;P tabindex{{=}}"1" onkeydown{{=}}"this.className{{=}}'other'" 
onmousedown{{=}}"this.className{{=}}'other'" onmouseup{{=}}"this.className{{=}}''" 
onkeyup{{=}}"this.className{{=}}''"&gt;Tab to select this paragraph and press down a 
key or just click it with the mouse to change the font-family style 
attribute to COURIER.&lt;/P&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/font-family.htm
}}{{Single Example
|Description=The following example shows how to use inline scripting to change the '''font-family''' property.
|Code=&lt;HTML&gt;
&lt;BODY&gt;
&lt;DIV tabindex {{=}}"1" onkeydown{{=}}"this.style.fontFamily{{=}}'Courier'"
onkeyup{{=}}"this.style.fontFamily{{=}}''" onmousedown{{=}}"this.style.fontFamily{{=}}'Courier'"
onmouseup{{=}}"this.style.fontFamily{{=}}''"&gt;Tab to select this DIV element and press 
down a key or just click it with the mouse to change the fontFamily style 
property to COURIER. 
&lt;/DIV&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/fontFamily.htm
}}{{Single Example
|Description=The following example shows how to define a hierarchy of fonts, in this case, an embedded font and a system font. The browser goes through the list until it finds a font it can apply. This is useful when the Web author wants to use fonts that might or might not be accessible or loaded onto a user's machine.
|Code=&lt;STYLE type{{=}}"text/css"&gt;
   @font-face {
      font-family: "My_font";
      src: url(http://www.adatum.com/some_font_file.eot);
   }
   BODY {font-family: "My_font", Arial}
&lt;/STYLE&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The value is a prioritized list of font family names and generic family names. List items are separated by commas to minimize confusion between multiple-word font family names. If the font family name contains white space, it should appear in single or double quotation marks; generic font family names are values and cannot appear in quotation marks.
Because you do not know which fonts users have installed, you should provide a list of alternatives with a generic font family at the end of the list. This list can include embedded fonts. For more information about embedding fonts, see the [[css/atrules/@font-face|'''@font-face''']] rule.
The default for this property can be set for Windows Internet Explorer on the '''General''' tab of the '''Internet Options''' menu by clicking the '''Fonts''' button.
|Import_Notes====Syntax===
<code>'''font-family: ''''''[''' '''[''' ''
&lt;family-name&gt;
'' '''{{!}}''' ''
&lt;generic-family&gt;
'' ''']''' '''[''' , '''{{!}}''' ''
&lt;family-name&gt;
'' '''{{!}}''' ''
&lt;generic-family&gt;
'' ''']''''''*''' ''']'''</code>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.2.2
}}
{{Related_Specifications_Section
|Specifications=
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
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}