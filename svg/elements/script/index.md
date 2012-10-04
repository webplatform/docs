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
|Description=In the following code example,  the [[dom/events/click|'''onclick''']] event attribute on the [[svg/elements/circle|'''circle''']] element calls the <code>circle_click</code> function.
|LiveURL=
|Code=
&lt;?xml version{{=}}"1.0" standalone{{=}}"no"?&gt;
&lt;!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" 
  "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd"&gt;
&lt;svg width{{=}}"6cm" height{{=}}"5cm" viewBox{{=}}"0 0 600 500"
     xmlns{{=}}"http://www.w3.org/2000/svg" version{{=}}"1.1"&gt;
  &lt;desc&gt;Invoke an ECMAScript function from an onclick event&lt;/desc&gt;
  &lt;!-- ECMAScript to change the radius with each click. --&gt;
  &lt;script type{{=}}"application/ecmascript"&gt; 
    function circle_click(evt) {
      var circle {{=}} evt.target;
      var currentRadius {{=}} circle.getAttribute("r");
      if (currentRadius {{=}}{{=}} 100)
        circle.setAttribute("r", currentRadius*2);
      else
        circle.setAttribute("r", currentRadius*0.5);
    }
  &lt;/script&gt;
  &lt;!-- Outline the drawing area with a blue line. --&gt;
  &lt;rect x{{=}}"1" y{{=}}"1" width{{=}}"598" height{{=}}"498" fill{{=}}"none" stroke{{=}}"blue"/&gt;
  &lt;!-- Act on each click event. --&gt;
  &lt;circle onclick{{=}}"circle_click(evt)" cx{{=}}"300" cy{{=}}"225" r{{=}}"100"
          fill{{=}}"blue"/&gt;
  &lt;text x{{=}}"300" y{{=}}"480" 
        font-family{{=}}"Verdana" font-size{{=}}"35" text-anchor{{=}}"middle"&gt;
    Click on circle to change its size
  &lt;/text&gt;
&lt;/svg&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
A   '''script''' element is equivalent to the <code>script</code> element in HTML and  is the place for scripts (for example, ECMAScript). Any functions that you  define  within any '''script''' element have a global scope across the entire current document.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204745 Scalable Vector Graphics: Scripting], Section 18.5.1


===Members===
The '''SVGScriptElement''' object has these types of members:
*[#events Events]
*[#properties Properties]


====Events====
The '''SVGScriptElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Properties====
The '''SVGScriptElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]
|Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
|-
|[[svg/properties/href|'''href''']]
|Gets an <code>xlink:href</code> attribute of an element.
|-
|[[svg/properties/type (SVGScriptElement)|'''type''']]
|Gets the scripting language for the given '''script''' element.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}