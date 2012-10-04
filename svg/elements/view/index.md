{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Topics|SVG}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following code example shows how to zoom in and zoom out of rendered content.
|LiveURL=
|Code=
&lt;?xml version{{=}}"1.0" standalone{{=}}"no"?&gt;
&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
"http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;
&lt;!-- 400 pixels per 100 user units, or 4 pixels per 1 user unit. --&gt;
&lt;svg width{{=}}"400px" height{{=}}"400px" viewBox{{=}}"0 0 100 100" 
     version{{=}}"1.1" 
     xmlns{{=}}"http://www.w3.org/2000/svg"
     xmlns:xlink{{=}}"http://www.w3.org/1999/xlink"&gt;  &lt;!-- Required for 'xlink' usage. --&gt;
     
  &lt;title&gt;The SVG &amp;lt;view&amp;gt; Element&lt;/title&gt;
  &lt;desc&gt;
		The key concept is that the 'viewBox' attribute values of the 
		associated 'view' element are essentially applied to the 'viewBox' 
		attributes of its parent 'svg' element.
  &lt;/desc&gt;
	
  &lt;defs&gt;
    &lt;radialGradient id{{=}}"myRadialGradient"&gt;
      &lt;stop offset{{=}}"0%" stop-color{{=}}"yellow" /&gt;
      &lt;stop offset{{=}}"50%" stop-color{{=}}"white" /&gt;
      &lt;stop offset{{=}}"100%" stop-color{{=}}"blue" /&gt;
    &lt;/radialGradient&gt;    
  &lt;/defs&gt;
	
  &lt;view id{{=}}"normalView" viewBox{{=}}"0 0 100 100"/&gt;  &lt;!-- Same 'viewBox' values as on the 'svg' element (that is, 4 pixels per user unit). --&gt;
  &lt;view id{{=}}"halfView"   viewBox{{=}}"0 0 200 200"/&gt;  &lt;!-- 400 pixels per 200 user units, or 2 pixels per 1 user unit - shrinking things. --&gt;
  &lt;view id{{=}}"doubleView" viewBox{{=}}"0 0  50  50"/&gt;  &lt;!-- 400 pixels per 50 user units, or 8 pixels per 1 user unit - expanding things. --&gt;
	
  &lt;!-- Outline the initial viewport. --&gt;
  &lt;rect x{{=}}"0" y{{=}}"0" width{{=}}"100%" height{{=}}"100%" style{{=}}"stroke: green; fill: none;"/&gt;
	
  &lt;!-- Fill the viewport with something interesting. --&gt;
  &lt;circle fill{{=}}"url(#myRadialGradient)" stroke{{=}}"black" stroke-width{{=}}"1" cx{{=}}"50" cy{{=}}"50" r{{=}}"40"/&gt;
	
  &lt;!-- Provide the user with a way, by clicking the links, to essentially change the 'svg' element's 'viewBox' values. --&gt;
  &lt;a xlink:href{{=}}"#doubleView"&gt;
    &lt;text x{{=}}"2" y{{=}}"6" font-size{{=}}"5"&gt;[double size]&lt;/text&gt;
  &lt;/a&gt;
  &lt;a xlink:href{{=}}"#normalView"&gt;
    &lt;text x{{=}}"39" y{{=}}"6" font-size{{=}}"5"&gt;[normal size]&lt;/text&gt;
  &lt;/a&gt;
  &lt;a xlink:href{{=}}"#halfView"&gt;
    &lt;text x{{=}}"77" y{{=}}"6" font-size{{=}}"5"&gt;[half size]&lt;/text&gt;
  &lt;/a&gt;
				
&lt;/svg&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
The '''view''' element can  change the [[svg/properties/viewBox|'''viewBox''']] attributes of its parent [[svg/elements/svg|'''svg''']] element. For example, you can use this behavior to zoom in  or  zoom out  of rendered SVG content.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199815 Scalable Vector Graphics: Linking], Section 17.4.2


===Members===
The '''SVGViewElement''' object has these types of members:
*[#events Events]
*[#properties Properties]


====Events====
The '''SVGViewElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Properties====
The '''SVGViewElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]
|Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
|-
|[[svg/properties/focusable|'''focusable''']]
|Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
|-
|[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]
|Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
|-
|[[svg/properties/preserveAspectRatio|'''preserveAspectRatio''']]
|Gets  an XML value that indicates whether to force uniform graphic scaling.
|-
|[[svg/properties/viewBox|'''viewBox''']]
|Gets  a value that indicates how a graphic scales to fit a container element.
|-
|[[svg/properties/viewportElement|'''viewportElement''']]
|Gets the element that established the current viewport.
|-
|[[svg/properties/viewTarget|'''viewTarget''']]
|Gets  the  [[svg/properties/viewTarget|'''viewTarget''']]  attribute of a '''view''' element.
|-
|[[svg/properties/xmlbase|'''xmlbase''']]
|Gets or sets the <code>base</code> attribute on the element.
|-
|[[svg/properties/zoomAndPan|'''zoomAndPan''']]
|Gets the [[svg/properties/zoomAndPan|'''zoomAndPan''']] attribute of an element.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}