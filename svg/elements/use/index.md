{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, usage, spec reference
|Checked_Out=No
|High-level issues=Stub, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=Here, the '''use''' element is used to create three instances of a rectangle defined in a [[svg/elements/defs|'''defs''']] tag.
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE html>
<html>
    <head></head>
    <body>
        <svg>
            <defs>
                <rect id="myRect" width="50" height="50" />
            </defs>
            <use x="50" y="50" fill="red" xlink:href="#myRect" />
            <use x="75" y="75" fill="green" xlink:href="#myRect" />
            <use x="100" y="100" fill="blue" xlink:href="#myRect" />
        </svg>
    </body>
</html>
</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/9492902
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

For more information, see the [http://go.microsoft.com/fwlink/p/?LinkID{{=}}190918 SVG specification].
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.8

===Members===

The '''SVGUseElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGUseElement''' object has these methods:

*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.

The '''SVGUseElement''' object has these properties:

*[[svg/properties/animatedInstanceRoot|'''animatedInstanceRoot''']]: Gets the animated root of the instance tree of a '''use''' element.
*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]: Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
*[[svg/properties/href|'''href''']]: Gets an '''xlink:href''' attribute of an element.
*[[svg/properties/instanceRoot|'''instanceRoot''']]: Gets  the root of the instance tree of a  '''use'''  element.
*[[svg/attributes/mask|'''mask''']]: Sets or retrieves a value that indicates a SVG mask.
*[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]: Gets  a value that indicates which element established the current viewport.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/attributes/pointers|'''pointerEvents''']]: Sets or retrieves a value that specifies under what circumstances a given graphics element can be the target element for a pointer event in SVG.
*[[svg/properties/requiredExtensions|'''requiredExtensions''']]: Gets a white space-delimited list of required language extensions.
*[[svg/properties/requiredFeatures|'''requiredFeatures''']]: Gets or sets a white space-delimited list of feature strings.
*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
*[[svg/properties/systemLanguage|'''systemLanguage''']]: Gets or sets a comma-separated list of language names.
*[[svg/properties/transform|'''transform''']]: Gets the value of a [[svg/properties/transform|'''transform''']] attribute.
*[[svg/properties/viewportElement|'''viewportElement''']]: Gets the element that established the current viewport.
*[[svg/properties/width|'''width''']]: Defines the width of an element.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
*[[svg/properties/xmllang|'''xmllang''']]: Gets or sets a value that specifies the language that is used in the contents and attribute values of an element.
*[[svg/properties/xmlspace|'''xmlspace''']]: Gets or sets a value that indicates whether white space is preserved in character data.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
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