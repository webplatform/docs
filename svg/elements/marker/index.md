{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following code example, square markers are added to each end of a path.
Copy this sample to a text file and save it with the ''.html'' file extension. Run it in Internet Explorer 9 to see the path with two markers on the screeen.

The path with markers will look like this:
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <!-- Inline SVG -->
    <svg width="400" height="400">
      <!-- Definition of marker -->
      <defs>
        <marker id="knob"
                  viewBox="0 0 10 10" refX="0" refY="5"
                  markerUnits="strokeWidth"
                  markerWidth="4" markerHeight="3" orient="auto">
                  <path d="M 0 0 L 10 5 L 0 10 z" />
        </marker>
      </defs>
      <!-- Path that will have knobs at both ends -->
      <path d="M 50,100 Q 150,50 250,100" stroke="hotpink"
                stroke-width="10" fill="white"
                marker-start="url(#knob)"
                marker-end="url(#knob)" />
    </svg>
  </body>
</html>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}199816 Scalable Vector Graphics: Painting, Filling, Stroking and Marker Symbols], Section 11.9.2

===Members===

The '''SVGMarkerElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGMarkerElement''' object has these methods:

*[[svg/methods/setOrientToAngle|'''setOrientToAngle''']]: Sets the value of the [[svg/properties/orientAngle|'''orientAngle''']] attribute to the specified angle.
*[[svg/methods/setOrientToAuto|'''setOrientToAuto''']]: Sets the value of the '''svgMarkerOrient''' attribute to '''auto'''.

The '''SVGMarkerElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/properties/markerHeight|'''markerHeight''']]: Gets the height attribute of the '''marker''' element.
*[[svg/properties/markerUnits|'''markerUnits''']]: Gets or sets the coordinate system for  the  [[svg/properties/markerWidth|'''markerWidth''']] and  [[svg/properties/markerHeight|'''markerHeight''']] attributes and  for the contents of the '''marker''' element.
*[[svg/properties/markerWidth|'''markerWidth''']]: Gets the width attribute of the '''marker''' element.
*[[svg/attributes/mask|'''mask''']]: Sets or retrieves a value that indicates a SVG mask.
*[[svg/properties/orientAngle|'''orientAngle''']]: Gets the angle of orientation of the '''marker''' element.
*[[svg/properties/orientType|'''orientType''']]: Gets the orientation type for a '''marker''' element.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/properties/preserveAspectRatio|'''preserveAspectRatio''']]: Gets  an XML value that indicates whether to force uniform graphic scaling.
*[[svg/properties/refX|'''refX''']]: Gets  the [[svg/properties/refX|'''refX''']] attribute on the '''marker''' element.
*[[svg/properties/refY|'''refY''']]: Gets  the [[svg/properties/refY|'''refY''']] attribute on the '''marker''' element.
*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
*[[svg/properties/viewBox|'''viewBox''']]: Gets  a value that indicates how a graphic scales to fit a container element.
*[[svg/properties/viewportElement|'''viewportElement''']]: Gets the element that established the current viewport.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
*[[svg/properties/xmllang|'''xmllang''']]: Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
*[[svg/properties/xmlspace|'''xmlspace''']]: Gets or sets a value that indicates whether white space is preserved in character data.
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
{{See_Also_Section}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}