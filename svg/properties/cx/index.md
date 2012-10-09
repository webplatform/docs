{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code  example demonstrates how the starting point and direction of an arc for an ellipse are affected by a user space transform.
|LiveURL=
|Code=
&lt;?xml version{{=}}"1.0" standalone{{=}}"no"?&gt;
&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;
&lt;svg width{{=}}"400px" height{{=}}"300px" viewBox{{=}}"0 0 400 300"
     xmlns{{=}}"http://www.w3.org/2000/svg" version{{=}}"1.1"
     xmlns:xlink{{=}}"http://www.w3.org/1999/xlink"&gt;
  &lt;desc&gt;Arc Transform&lt;/desc&gt;
  &lt;!-- Show the outline of the canvas by using a rect element. --&gt;
  &lt;rect x{{=}}"1" y{{=}}"1" width{{=}}"399" height{{=}}"299"
        fill{{=}}"none" stroke{{=}}"black" stroke-width{{=}}"1" /&gt;
  &lt;defs&gt;
    &lt;ellipse id{{=}}"theEllipse" x{{=}}"0" y{{=}}"0" rx{{=}}"50" ry{{=}}"100" 
             style{{=}}"fill: blue; stroke: black; stroke-width: 5px;"/&gt;
  &lt;/defs&gt;
  
  &lt;use xlink:href{{=}}"#theEllipse" x{{=}}"90" y{{=}}"150"/&gt;
  
  &lt;!-- transform{{=}}"rotate(30, 280, 150)" rotates the ellipse 30 degrees about the 
       point (280, 150) as opposed to the origin of the viewport. --&gt;
  &lt;use xlink:href{{=}}"#theEllipse" x{{=}}"280" y{{=}}"150" transform{{=}}"rotate(30, 280, 150)"/&gt;
  
 &lt;/svg&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The arc of a [[svg/elements/circle|'''circle''']] element and the arc of an [[svg/elements/ellipse|'''ellipse''']] element begin at the 3 o'clock point on the associated radius and progress towards the 9 o'clock point. The starting point and direction of the arc are affected by the user space transform in the same manner as the geometry of the element.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}190918 Scalable Vector Graphics (SVG) 1.1], Appendix M


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/circle|SVGCircleElement]]</code>
*<code>[[svg/elements/ellipse|SVGEllipseElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}

[[Category:SVG]]