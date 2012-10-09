{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example shows the default and  '''_blank''' behaviors of the '''target'''  property.
|LiveURL=
|Code=
&lt;?xml version{{=}}"1.0" standalone{{=}}"no"?&gt;
&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
 "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;
  
&lt;svg width{{=}}"5cm" height{{=}}"7cm" viewBox{{=}}"0 0 5 7" version{{=}}"1.1"
     xmlns{{=}}"http://www.w3.org/2000/svg" 
	 xmlns:xlink{{=}}"http://www.w3.org/1999/xlink"&gt;
	 
  &lt;desc&gt;Two basic link types.&lt;/desc&gt;
	
  &lt;!-- Outline the SVG viewport. --&gt;
  &lt;rect x{{=}}"0" y{{=}}"0" width{{=}}"100%" height{{=}}"100%" 
        fill{{=}}"none" stroke{{=}}"blue"  stroke-width{{=}}".03"/&gt;
		
  &lt;a xlink:href{{=}}"http://www.w3.org"&gt;
    &lt;ellipse cx{{=}}"2.5" cy{{=}}"1.5" rx{{=}}"2" ry{{=}}"1" fill{{=}}"red" /&gt;
  &lt;/a&gt;
	
  &lt;a xlink:href{{=}}"http://dev.w3.org/SVG/profiles/1.1F2/publish/" target{{=}}"_blank"&gt;
    &lt;ellipse cx{{=}}"2.5" cy{{=}}"4.75" rx{{=}}"2" ry{{=}}"1" fill{{=}}"green" /&gt;
  &lt;/a&gt;
&lt;/svg&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The '''target'''  property specifies the name or portion of the target window, frame, pane, tab, or other relevant presentation context (that is, an HTML or XHTML frame, iframe, or object element)  where  a document is  opened when the link is activated.
Use '''target'''  when there are multiple possible targets for the ending resource, such as when the parent document is a multi-frame HTML or XHTML document.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199815 Scalable Vector Graphics: Linking], Section 17.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/a|SVGAElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}

[[Category:SVG]]