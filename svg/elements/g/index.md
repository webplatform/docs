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
|Description=In the following code example, the g element is used to group two elements together. They are then rotated together.
Copy this sample to a text file and save it with the ''.html'' file extension. Run it in Internet Explorer 9 to see the rotated firebrick rectangle and dodgerblue ellipse.

Before the rotation, the elements looked like this:

After the rotation, the elements look like this:
|LiveURL=
|Code=

<syntaxhighlight lang="xml">
<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <g transform="rotate(30 75 50)">
        <rect x="50" y="50" width="50" height="50" fill="firebrick"/>
        <ellipse cx="100" cy="50" rx="25" ry="50" fill="dodgerblue"/>
      </g>
    </svg>
  </body>
</html>
</syntaxhighlight>
}}}}
{{Notes_Section
|Notes=

===Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes=

===Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.3

===Members===

The '''SVGGElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGGElement''' object has these methods:

*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.

The '''SVGGElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]: Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/attributes/mask|'''mask''']]: Sets or retrieves a value that indicates a SVG mask.
*[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]: Gets  a value that indicates which element established the current viewport.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/properties/requiredExtensions|'''requiredExtensions''']]: Gets a white space-delimited list of required language extensions.
*[[svg/properties/requiredFeatures|'''requiredFeatures''']]: Gets or sets a white space-delimited list of feature strings.
*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
*[[svg/properties/systemLanguage|'''systemLanguage''']]: Gets or sets a comma-separated list of language names.
*[[svg/properties/transform|'''transform''']]: Gets the value of a [[svg/properties/transform|'''transform''']] attribute.
*[[svg/properties/viewportElement|'''viewportElement''']]: Gets the element that established the current viewport.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
*[[svg/properties/xmllang|'''xmllang''']]: Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
*[[svg/properties/xmlspace|'''xmlspace''']]: Gets or sets a value that indicates whether white space is preserved in character data.

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}