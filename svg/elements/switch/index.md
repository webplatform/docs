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
|Description=The following code  example uses the '''switch''' element to provide a  graphical representation of a paragraph if XMHTML is not supported.
|LiveURL=
|Code=
&lt;?xml version{{=}}"1.0" standalone{{=}}"yes"?&gt;
&lt;svg width{{=}}"4in" height{{=}}"3in" version{{=}}"1.1"
 xmlns {{=}} 'http://www.w3.org/2000/svg'&gt;
  &lt;!-- The &lt;switch&gt; element will process the first child element
       whose testing attributes evaluate to TRUE.--&gt;
  &lt;switch&gt;
    &lt;!-- Process the embedded XHTML if the requiredExtensions attribute
         evaluates to TRUE (that is, the browser supports XHTML
         embedded within SVG). --&gt;
    &lt;foreignObject width{{=}}"100" height{{=}}"50"
                   requiredExtensions{{=}}"http://example.com/SVGExtensions/EmbeddedXHTML"&gt;
      &lt;!-- XHTML content goes here --&gt;
      &lt;body xmlns{{=}}"http://www.w3.org/1999/xhtml"&gt;
        &lt;p&gt;Here is a paragraph that requires word wrap.&lt;/p&gt;
      &lt;/body&gt;
    &lt;/foreignObject&gt;
    &lt;!-- ELSE, process the following alternate SVG.
         Note that there are no testing attributes on the &lt;text&gt; element.
         If no testing attributes are provided, it is as if there
         were testing attributes and they evaluated to TRUE.--&gt;
    &lt;text font-size{{=}}"10" font-family{{=}}"Verdana"&gt;
      &lt;tspan x{{=}}"10" y{{=}}"10"&gt;Here is a paragraph that&lt;/tspan&gt;
      &lt;tspan x{{=}}"10" y{{=}}"20"&gt;requires word wrap.&lt;/tspan&gt;
    &lt;/text&gt;
  &lt;/switch&gt;
&lt;/svg&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
The '''switch''' element evaluates the [[svg/properties/requiredFeatures|'''requiredFeatures''']], [[svg/properties/requiredExtensions|'''requiredExtensions''']], and [[svg/properties/systemLanguage|'''systemLanguage''']] attributes on its direct child elements in order, and then processes and renders the first child element  that these attributes evaluate to TRUE for. All other child elements are  skipped and  not rendered. If the child element is a container element (such as an  [[svg/elements/g|'''g''']] element), the entire subtree is  processed  and rendered or skipped and not rendered.
The values of the  [[css/properties/display|'''display''']] and [[css/properties/visibility|'''visibility''']]  properties does not affect the  '''switch''' element processing. In particular, if you set  '''display''' to [[css/properties/text-decoration-none|'''none''']] on a child element of a '''switch''' element, it does not affect TRUE and FALSE testing that is associated with processing  '''switch''' elements.
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.13


===Members===
The '''SVGSwitchElement''' object has these types of members:
*[#events Events]
*[#methods Methods]
*[#properties Properties]


====Events====
The '''SVGSwitchElement''' object has these events.
{| class="wikitable"
|-
!Event
!Description
|-
|[[svg/events/load|'''onload''']]
|Occurs  when the browser has fully parsed the element and all of its descendants.
|}
 

====Methods====
The '''SVGSwitchElement''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[svg/methods/getBBox|'''getBBox''']]
|Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
|-
|[[svg/methods/getCTM|'''getCTM''']]
|Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
|-
|[[svg/methods/getScreenCTM|'''getScreenCTM''']]
|Gets  the transformation matrix from the current user units to the screen coordinate system.
|-
|[[svg/methods/getTransformToElement|'''getTransformToElement''']]
|Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
|-
|[[svg/methods/hasExtension|'''hasExtension''']]
|Determines if the specified extension  is supported.
|}
 

====Properties====
The '''SVGSwitchElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/className|'''className''']]
|Gets  the names of the classes  that are assigned to this object.
|-
|[[svg/properties/clipPath|'''clipPath''']]
|Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
|-
|[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]
|Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
|-
|[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]
|Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
|-
|[[svg/properties/focusable|'''focusable''']]
|Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
|-
|[[svg/attributes/mask|'''mask''']]
|Sets or retrieves a value that indicates a SVG mask.
|-
|[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]
|Gets  a value that indicates which element established the current viewport.
|-
|[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]
|Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
|-
|[[svg/properties/requiredExtensions|'''requiredExtensions''']]
|Gets a white space-delimited list of required language extensions.
|-
|[[svg/properties/requiredFeatures|'''requiredFeatures''']]
|Gets or sets a white space-delimited list of feature strings.
|-
|[[svg/properties/style|'''style''']]
|Gets a [[css/cssom/style|'''style''']] object.
|-
|[[svg/properties/systemLanguage|'''systemLanguage''']]
|Gets or sets a comma-separated list of language names.
|-
|[[svg/properties/transform|'''transform''']]
|Gets the value of a [[svg/properties/transform|'''transform''']] attribute.
|-
|[[svg/properties/viewportElement|'''viewportElement''']]
|Gets the element that established the current viewport.
|-
|[[svg/properties/xmlbase|'''xmlbase''']]
|Gets or sets the <code>base</code> attribute on the element.
|-
|[[svg/properties/xmllang|'''xmllang''']]
|Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
|-
|[[svg/properties/xmlspace|'''xmlspace''']]
|Gets or sets a value that indicates whether white space is preserved in character data.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}