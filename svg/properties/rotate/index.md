{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code  example  shows  how  to rotate individual characters. Because the number of rotate values is less than the number of characters in the string, all characters after the fourth character are rendered at 30°.
|LiveURL=
|Code=
&lt;?xml version{{=}}"1.0" standalone{{=}}"no"?&gt;
&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;
&lt;svg width{{=}}"100%" height{{=}}"100%" version{{=}}"1.1" 
     xmlns{{=}}"http://www.w3.org/2000/svg"
     xmlns:xlink{{=}}"http://www.w3.org/1999/xlink"&gt; 
  &lt;text font-family{{=}}"Verdana" font-size{{=}}"55" fill{{=}}"blue" &gt;
    &lt;!--  --&gt;
    &lt;tspan x{{=}}"250" y{{=}}"150" rotate{{=}}"-30, -15, 0, 15, 30"&gt;
      Hello World!
    &lt;/tspan&gt;
  &lt;/text&gt;
  
&lt;/svg&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''rotate''' property gets or sets the supplemental rotation about the current text position that  is  applied to all of the glyphs  that correspond  to each character within this element.
If  you provide a comma-separated or space-separated list of numbers,  the first number represents the supplemental rotation for the glyphs that correspond to the first character within this element or any of its descendants, the second number represents the supplemental rotation for the glyphs that correspond to the second character, and so on.
If you provide  more numbers  than there are characters,  the extra numbers  are  ignored.
If more characters are provided than numbers, for each of these extra characters, the rotation value  that is specified by the last number is used for these remaining characters.
If  you do not specify the  '''rotate''' attribute  and if an ancestor [[svg/elements/text|'''text''']] or [[svg/elements/tspan|'''tSpan''']] element specifies a supplemental rotation for a given character  through a '''rotate''' attribute,  the  specified supplemental rotation is applied to the given character (the nearest ancestor has precedence). If there are more characters than numbers that are specified in the ancestor's '''rotate''' attribute,  for each of these extra characters, the rotation value that is specified by the last number is used.
This supplemental rotation does not impact  how the current text position is modified as glyphs get rendered and is supplemental to any rotation  because of text on a path and to <code>glyph-orientation-horizontal</code> or <code>glyph-orientation-vertical</code>.
'''Note'''  If you do not specify the  '''rotate''' attribute  on an element or any of its descendants, no supplemental rotations occur.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}190918 Scalable Vector Graphics (SVG) 1.1], Appendix M


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/text|SVGTextElement]]</code>
*<code>[[svg/elements/textPositioning|SVGTextPositioningElement]]</code>
*<code>[[svg/elements/tspan|SVGTSpanElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}