{{Page_Title}}
{{Flags
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
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

If an SVG document is likely to be referenced as a component of another document,  you might  want to include a [[svg/properties/viewBox|'''viewBox''']] attribute on the outermost '''svg''' element of the referenced document. This attribute provides a convenient way to design SVG documents to scale-to-fit into an arbitrary viewport.

'''svg''' elements can appear in the middle of SVG content. You can use these elements to embed SVG document fragments within other SVG document fragments. You can also use '''svg''' elements within the middle of SVG content  to establish a new viewport.

In all cases, you must declare an SVG namespace  so that all SVG elements are identified as belonging to the SVG namespace. Typically, you can declare an SVG namespace as follows:

 &lt;svg xmlns="http://www.w3.org/2000/svg" ... &gt;
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.2

===Members===

The '''SVGSVGElement''' object has these events:

*[[svg/events/onabort|'''onabort''']]: Occurs when page loading is stopped before an element is loaded completely.
*[[dom/events/click|'''onclick''']]: Fires when the user clicks the left mouse button on the object.
*[[dom/events/dblclick|'''ondblclick''']]: Fires when the user double-clicks the object.
*[[svg/events/error|'''onerror''']]: Occurs  when an element does not load properly or a script runs incorrectly.
*[[dom/events/focusin|'''onfocusin''']]: Fires for an element just prior to setting focus on that element.
*[[dom/events/focusout|'''onfocusout''']]: Fires for the current element with focus immediately after moving focus to another element.
*[[dom/events/load|'''onload''']]: Fires immediately after the client loads the object.
*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.
*[[dom/events/mousedown|'''onmousedown''']]: Fires when the user clicks the object with either mouse button.
*[[dom/events/mousemove|'''onmousemove''']]: Fires when the user moves the mouse over the object.
*[[dom/events/mouseout|'''onmouseout''']]: Fires when the user moves the mouse pointer outside the boundaries of the object.
*[[dom/events/mouseover|'''onmouseover''']]: Fires when the user moves the mouse pointer into the object.
*[[dom/events/mouseup|'''onmouseup''']]: Fires when the user releases a mouse button while the mouse is over the object.
*[[svg/events/resize|'''onresize''']]: Occurs  when the document view is being resized.
*[[svg/events/scroll|'''onscroll''']]: Occurs when a document view is being  moved  along the x-axis, y-axis, or both axes.
*[[svg/events/unload|'''onunload''']]: Occurs  when a document is removed from a window or frame.
*[[svg/events/onzoom|'''onzoom''']]: Occurs when the document zoom level or [[svg/properties/currentScale|'''currentScale''']] property changes.

The '''SVGSVGElement''' object has these methods:

*[[svg/methods/animationsPaused|'''animationsPaused''']]: Gets a value that indicates whether this SVG document fragment is in a paused state.
*[[svg/methods/checkEnclosure|'''checkEnclosure''']]: Determines if the rendered content of the specified element is entirely contained within the specified rectangle.
*[[svg/methods/checkIntersection|'''checkIntersection''']]: Determines if the rendered content of the specified element intersects the specified rectangle.
*[[svg/methods/createEvent|'''createEvent''']]: Creates an event object to be used in conjunction with the [[svg/methods/dispatchEvent|'''dispatchEvent''']]  method.
*[[svg/methods/createSVGAngle|'''createSVGAngle''']]: Creates a new [[svg/objects/SVGAngle|'''SVGAngle''']] object that does not have units, that is set to 0 degrees, and that is not attached to any document.
*[[svg/methods/createSVGLength|'''createSVGLength''']]: Creates a new [[svg/objects/SVGLength|'''SVGLength''']] object that has a length of 0 user units.
*[[svg/methods/createSVGMatrix|'''createSVGMatrix''']]: Creates a new [[svg/objects/SVGMatrix|'''SVGMatrix''']] object that is set to the identity matrix and that is not attached to any document.
*[[svg/methods/createSVGNumber|'''createSVGNumber''']]: Creates a new [[svg/objects/SVGNumber|'''SVGNumber''']] object that has a value of zero and that is not attached to any document.
*[[svg/methods/createSVGPoint|'''createSVGPoint''']]: Creates a new [[svg/objects/SVGPoint|'''SVGPoint''']] object that is initialized to the point (0,0) in the user coordinate system and that is not attached to any document.
*[[svg/methods/createSVGRect|'''createSVGRect''']]: Creates a new [[svg/objects/SVGRect|'''SVGRect''']] object that has all values set to 0 user units and that is not attached to any document.
*[[svg/methods/createSVGTransform|'''createSVGTransform''']]: Creates a new [[svg/objects/SVGTransform|'''SVGTransform''']] object that is set to the identity matrix and that is not attached to any document.
*[[svg/methods/createSVGTransformFromMatrix|'''createSVGTransformFromMatrix''']]: Creates a matrix transform object whose values are given by the specified matrix.
*[[svg/methods/deselectAll|'''deselectAll''']]: Cancels the selection of  any selected objects, including any selections of text strings and text boxes.
*[[svg/methods/forceRedraw|'''forceRedraw''']]: Redraws all regions of the viewport that require updating.
*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getComputedStyle|'''getComputedStyle''']]: Returns the current computed value of the combined CSS properties for an element.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getCurrentTime|'''getCurrentTime''']]: Gets the current time, in seconds, relative to the start time for the current SVG document fragment.
*[[svg/methods/getElementById|'''getElementById''']]: Gets the element that matches the specified ID from the SVG document or document fragment.
*[[svg/methods/getEnclosureList|'''getEnclosureList''']]: Gets the list of graphics elements whose rendered content is entirely contained within the  specified  rectangle.
*[[svg/methods/getIntersectionList|'''getIntersectionList''']]: Gets the list of graphics elements whose rendered content intersects the specified rectangle.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.
*[[svg/methods/pauseAnimations|'''pauseAnimations''']]: Pauses all currently running animations that are defined within the SVG document fragment that corresponds to this [[svg/objects/SVGElement|'''svg''']]  element.
*[[svg/methods/setCurrentTime|'''setCurrentTime''']]: Sets the new current time for this SVG document fragment.
*[[svg/methods/suspendRedraw|'''suspendRedraw''']]: Suspends redrawing a device for a specified duration.
*[[svg/methods/unpauseAnimations|'''unpauseAnimations''']]: Resumes currently running animations that are defined within the SVG document fragment.
*[[svg/methods/unsuspendRedraw|'''unsuspendRedraw''']]: Cancels the specified suspension of redrawing operations.
*[[svg/methods/unsuspendRedrawAll|'''unsuspendRedrawAll''']]: Cancels all currently active suspensions of redrawing operations.

The '''SVGSVGElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/contentScriptType|'''contentScriptType''']]: Gets the default scripting language of the current document fragment.
*[[svg/properties/contentStyleType|'''contentStyleType''']]: '''Note:'''
[[svg/properties/contentStyleType|'''contentStyleType''']] may be altered or unavailable in subsequent versions of the operating system or product.

Gets  the default style sheet language of the current document.
*[[svg/properties/currentScale|'''currentScale''']]: Gets or sets the current scale factor,  relative to the initial view (when this property is called from an outermost [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/properties/currentTranslate|'''currentTranslate''']]: Gets or sets  the current translation factor, relative to the initial view (when this property is called from an outermost [[svg/objects/SVGElement|'''svg''']] element).
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