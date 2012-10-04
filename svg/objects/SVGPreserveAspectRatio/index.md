{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=svg/objects/SVGElement
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=
|LiveURL=Scalable Vector Graphics (SVG) 1.0 Specification
|Code=
&lt;?xml version{{=}}"1.0" encoding{{=}}"UTF-8"?&gt;
&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"
[ &lt;!ENTITY Smile "
&lt;rect x{{=}}'.5' y{{=}}'.5' width{{=}}'29' height{{=}}'39' fill{{=}}'black' stroke{{=}}'red'/&gt;
&lt;g transform{{=}}'translate(0, 5)'&gt;
&lt;circle cx{{=}}'15' cy{{=}}'15' r{{=}}'10' fill{{=}}'yellow'/&gt;
&lt;circle cx{{=}}'12' cy{{=}}'12' r{{=}}'1.5' fill{{=}}'black'/&gt;
&lt;circle cx{{=}}'17' cy{{=}}'12' r{{=}}'1.5' fill{{=}}'black'/&gt;
&lt;path d{{=}}'M 10 19 A 8 8 0 0 0 20 19' stroke{{=}}'black' stroke-width{{=}}'2'/&gt;
&lt;/g&gt;
"&gt;
&lt;!ENTITY Viewport1 "&lt;rect x{{=}}'.5' y{{=}}'.5' width{{=}}'49' height{{=}}'29'
fill{{=}}'none' stroke{{=}}'blue'/&gt;"&gt;
&lt;!ENTITY Viewport2 "&lt;rect x{{=}}'.5' y{{=}}'.5' width{{=}}'29' height{{=}}'59'
fill{{=}}'none' stroke{{=}}'blue'/&gt;"&gt;
]&gt;
&lt;svg width{{=}}"450px" height{{=}}"300px" version{{=}}"1.1"
     xmlns{{=}}"http://www.w3.org/2000/svg"&gt;
  &lt;desc&gt;Example PreserveAspectRatio - illustrates preserveAspectRatio attribute&lt;/desc&gt;
  &lt;rect x{{=}}"1" y{{=}}"1" width{{=}}"448" height{{=}}"298"
        fill{{=}}"none" stroke{{=}}"blue"/&gt;
  &lt;g font-size{{=}}"9"&gt;
    &lt;text x{{=}}"10" y{{=}}"30"&gt;SVG to fit&lt;/text&gt;
    &lt;g transform{{=}}"translate(20,40)"&gt;&amp;Smile;&lt;/g&gt;
    &lt;text x{{=}}"10" y{{=}}"110"&gt;Viewport 1&lt;/text&gt;
    &lt;g transform{{=}}"translate(10,120)"&gt;&amp;Viewport1;&lt;/g&gt;
    &lt;text x{{=}}"10" y{{=}}"180"&gt;Viewport 2&lt;/text&gt;
    &lt;g transform{{=}}"translate(20,190)"&gt;&amp;Viewport2;&lt;/g&gt;
    &lt;g id{{=}}"meet-group-1" transform{{=}}"translate(100, 60)"&gt;
      &lt;text x{{=}}"0" y{{=}}"-30"&gt;--------------- meet ---------------&lt;/text&gt;
      &lt;g&gt;&lt;text y{{=}}"-10"&gt;xMin*&lt;/text&gt;&amp;Viewport1;
        &lt;svg preserveAspectRatio{{=}}"xMinYMin meet" viewBox{{=}}"0 0 30 40"
             width{{=}}"50" height{{=}}"30"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
      &lt;g transform{{=}}"translate(70,0)"&gt;&lt;text y{{=}}"-10"&gt;xMid*&lt;/text&gt;&amp;Viewport1;
        &lt;svg preserveAspectRatio{{=}}"xMidYMid meet" viewBox{{=}}"0 0 30 40"
             width{{=}}"50" height{{=}}"30"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
      &lt;g transform{{=}}"translate(0,70)"&gt;&lt;text y{{=}}"-10"&gt;xMax*&lt;/text&gt;&amp;Viewport1;
        &lt;svg preserveAspectRatio{{=}}"xMaxYMax meet" viewBox{{=}}"0 0 30 40"
             width{{=}}"50" height{{=}}"30"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
    &lt;/g&gt;
    &lt;g id{{=}}"meet-group-2" transform{{=}}"translate(250, 60)"&gt;
      &lt;text x{{=}}"0" y{{=}}"-30"&gt;---------- meet ----------&lt;/text&gt;
      &lt;g&gt;&lt;text y{{=}}"-10"&gt;*YMin&lt;/text&gt;&amp;Viewport2;
        &lt;svg preserveAspectRatio{{=}}"xMinYMin meet" viewBox{{=}}"0 0 30 40"
             width{{=}}"30" height{{=}}"60"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
      &lt;g transform{{=}}"translate(50, 0)"&gt;&lt;text y{{=}}"-10"&gt;*YMid&lt;/text&gt;&amp;Viewport2;
        &lt;svg preserveAspectRatio{{=}}"xMidYMid meet" viewBox{{=}}"0 0 30 40"
             width{{=}}"30" height{{=}}"60"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
      &lt;g transform{{=}}"translate(100, 0)"&gt;&lt;text y{{=}}"-10"&gt;*YMax&lt;/text&gt;&amp;Viewport2;
        &lt;svg preserveAspectRatio{{=}}"xMaxYMax meet" viewBox{{=}}"0 0 30 40"
             width{{=}}"30" height{{=}}"60"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
    &lt;/g&gt;
    &lt;g id{{=}}"slice-group-1" transform{{=}}"translate(100, 220)"&gt;
      &lt;text x{{=}}"0" y{{=}}"-30"&gt;---------- slice ----------&lt;/text&gt;
      &lt;g&gt;&lt;text y{{=}}"-10"&gt;xMin*&lt;/text&gt;&amp;Viewport2;
        &lt;svg preserveAspectRatio{{=}}"xMinYMin slice" viewBox{{=}}"0 0 30 40"
             width{{=}}"30" height{{=}}"60"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
      &lt;g transform{{=}}"translate(50,0)"&gt;&lt;text y{{=}}"-10"&gt;xMid*&lt;/text&gt;&amp;Viewport2;
        &lt;svg preserveAspectRatio{{=}}"xMidYMid slice" viewBox{{=}}"0 0 30 40"
             width{{=}}"30" height{{=}}"60"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
      &lt;g transform{{=}}"translate(100,0)"&gt;&lt;text y{{=}}"-10"&gt;xMax*&lt;/text&gt;&amp;Viewport2;
        &lt;svg preserveAspectRatio{{=}}"xMaxYMax slice" viewBox{{=}}"0 0 30 40"
             width{{=}}"30" height{{=}}"60"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
    &lt;/g&gt;
    &lt;g id{{=}}"slice-group-2" transform{{=}}"translate(250, 220)"&gt;
      &lt;text x{{=}}"0" y{{=}}"-30"&gt;--------------- slice ---------------&lt;/text&gt;
      &lt;g&gt;&lt;text y{{=}}"-10"&gt;*YMin&lt;/text&gt;&amp;Viewport1;
        &lt;svg preserveAspectRatio{{=}}"xMinYMin slice" viewBox{{=}}"0 0 30 40"
             width{{=}}"50" height{{=}}"30"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
      &lt;g transform{{=}}"translate(70,0)"&gt;&lt;text y{{=}}"-10"&gt;*YMid&lt;/text&gt;&amp;Viewport1;
        &lt;svg preserveAspectRatio{{=}}"xMidYMid slice" viewBox{{=}}"0 0 30 40"
             width{{=}}"50" height{{=}}"30"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
      &lt;g transform{{=}}"translate(140,0)"&gt;&lt;text y{{=}}"-10"&gt;*YMax&lt;/text&gt;&amp;Viewport1;
        &lt;svg preserveAspectRatio{{=}}"xMaxYMax slice" viewBox{{=}}"0 0 30 40"
             width{{=}}"50" height{{=}}"30"&gt;&amp;Smile;&lt;/svg&gt;&lt;/g&gt;
    &lt;/g&gt;   
  &lt;/g&gt;
&lt;/svg&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
In some cases, typically when you are using the [[svg/properties/viewBox|'''viewBox''']] attribute,  you want the graphics to stretch to  non-uniformly  fill the entire viewport. In other cases,  you want to use uniform scaling  to preserve  the aspect ratio of the graphics. The [[svg/properties/preserveAspectRatio|'''preserveAspectRatio''']] attribute indicates whether  to force uniform scaling.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204735 Scalable Vector Graphics: Coordinate Systems, Transformations and Units], Section 7.14.7


===Members===
The '''SVGPreserveAspectRatio''' object has these types of members:
*[#properties Properties]


====Properties====
The '''SVGPreserveAspectRatio''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/align|'''align''']]
|Gets or sets  the type of alignment value.
|-
|[[svg/properties/meetOrSlice|'''meetOrSlice''']]
|Gets or sets the type of meet-or-slice value.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}