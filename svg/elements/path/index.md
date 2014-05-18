{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
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
|Description=In the following code example, the path element is used to create a red curved path.
|Code=<syntaxhighlight lang="xml">
<svg width="400" height="400">
  <path d="M 50,100 Q 150,50 250,100" stroke="red" stroke-width="10" fill="white"/>
</svg>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Path data can contain newline characters and thus can be broken up into multiple lines to improve readability. Because of line-length limitations with certain related tools, it is recommended to split long path data strings across multiple lines, with each line not exceeding 255 characters. Also note that newline characters are allowed only at certain places within path data.

The syntax of path data is concise in order to allow for minimal file size and efficient downloads, because many SVG files will be dominated by their path data. Some of the ways that SVG attempts to minimize the size of path data are as follows:

*All instructions are expressed as one character (for example, a ''moveto'' is expressed as an '''M''').

*Superfluous white space and separators such as commas can be eliminated (for example, "M 100 100 L 200 200" contains unnecessary spaces and could be expressed more compactly as "M100 100L200 200").

*The command letter can be eliminated on subsequent commands if the same command is used multiple times in a row (for example, you can drop the second '''L''' in "M 100 200 L 200 100 '''L''' -100 -200" and use "M 100 200 L 200 100 -100 -200" instead).

*Relative versions of all commands are available (uppercase means absolute coordinates, lowercase means relative coordinates).
*Alternate forms of ''lineto'' are available to optimize the special cases of horizontal and vertical lines (absolute and relative).

*Alternate forms of ''curve'' are available to optimize the special cases where some of the control points on the current segment can be determined automatically from the control points on the previous segment.

The path-data syntax is a prefix notation (that is, commands followed by parameters). The only allowable decimal point is a Unicode U+0046 FULL STOP (".") character (also referred to in Unicode as PERIOD, dot, and decimal point) and no other delimiter characters are allowed. (For example, the following is an invalid numeric value in a path data stream: "13,000.56". Instead, say: "13000.56".)

For the relative versions of the commands, all coordinate values are relative to the current point at the start of the command. For example, the absolute version of ''moveto'' is '''M''' whereas its relative form is indicated with a lowercase '''m'''. Absolute versus relative path commands are discussed in the following table.

'''Note:'''  In the Path Command Table below, the following notation is used.

{|
|'''()''' Indicates grouping of parameters.
|-
|'''+''' One or more of the given parameter(s) is required.
|}

{|
|-
!Path Command Table
|-
!''Command''
!''Name''
!''Parameters''
!''Description''
|-
|'''M''' (absolute)
'''m''' (relative)
|''moveto''
|(x y)+
|Starts a new path or subpath at the given (x,y) coordinates. '''M''' indicates that absolute coordinates will follow; '''m''' indicates that relative coordinates will follow. If a ''moveto'' is followed by multiple pairs of coordinates, the subsequent pairs are treated as implicit ''lineto'' commands. Hence, implicit ''lineto'' commands will be relative if the ''moveto'' is relative, and absolute if the ''moveto'' is absolute. If a relative ''moveto'' '''m''' appears as the first element of the path, then it is treated as a pair of absolute coordinates. In this case, subsequent pairs of coordinates are treated as relative even though the initial ''moveto'' is interpreted as an absolute ''moveto''.

The ''moveto'' commands ('''M''' or '''m''') establish a new current point. The effect is as if the "pen" were lifted and moved to a new location. A path data segment (if there is one) must begin with a ''moveto'' command. Subsequent ''moveto'' commands (that is, when the ''moveto'' is not the first command) represent the start of a new subpath.
|-
|'''Z''' or
'''z'''
|''closepath''
|(none)
|Closes the current subpath by drawing a straight line from the current point to current subpath's initial point. Because the '''Z''' and '''z''' commands take no parameters, they have an identical effect.

The ''closepath'' ('''Z''' or '''z''') ends the current subpath and causes an automatic straight line to be drawn from the current point to the initial point of the current subpath. If a ''closepath'' is followed immediately by a ''moveto'', then the ''moveto'' identifies the start point of the next subpath. If a ''closepath'' is followed immediately by any other command, then the next subpath starts at the same initial point as the current subpath.

When a subpath ends in a ''closepath'', it differs in behavior from what happens when "manually" closing a subpath via a ''lineto'' command in how 'stroke-linejoin' and 'stroke-linecap' are implemented. With ''closepath'', the end of the final segment of the subpath is "joined" with the start of the initial segment of the subpath using the current value of 'stroke-linejoin'. If you instead "manually" close the subpath via a ''lineto'' command, the start of the first segment and the end of the last segment are not joined but instead are each capped using the current value of 'stroke-linecap'. At the end of the command, the new current point is set to the initial point of the current subpath.
|-
|'''L''' (absolute)

'''l''' (relative)
|''lineto''
|(x y)+
|Draws a line from the current point to the given (x,y) coordinates, which becomes the new current point. '''L''' indicates that absolute coordinates will follow; '''l''' indicates that relative coordinates will follow. A number of coordinates pairs may be specified to draw a polyline. At the end of the command, the new current point is set to the final set of coordinates provided.
|-
|'''H''' (absolute)

'''h''' (relative)
|''horizontal lineto''
|x+
|Draws a horizontal line from the current point (cpx, cpy) to (x, cpy). '''H''' indicates that absolute coordinates will follow; '''h''' indicates that relative coordinates will follow. Multiple x values can be provided (although usually this doesn't make sense). At the end of the command, the new current point becomes (x, cpy) for the final value of x.
|-
|'''V''' (absolute)

'''v''' (relative)
|''vertical lineto''
|y+
|Draws a vertical line from the current point (cpx, cpy) to (cpx, y). '''V''' indicates that absolute coordinates will follow; '''v''' indicates that relative coordinates will follow. Multiple y values can be provided (although usually this doesn't make sense). At the end of the command, the new current point becomes (cpx, y) for the final value of y.
|-
|'''C''' (absolute)

'''c''' (relative)
|''curveto''
|(x1 y1 x2 y2 x y)+
|A cubic B&eacute;zier segment is defined by a start point, an end point, and two control points.

Draws a cubic B&eacute;zier curve from the current point to (x,y) using (x1,y1) as the control point at the beginning of the curve and (x2,y2) as the control point at the end of the curve. '''C''' indicates that absolute coordinates will follow; '''c''' indicates that relative coordinates will follow. Multiple sets of coordinates may be specified to draw a polyb&eacute;zier. At the end of the command, the new current point becomes the final (x,y) coordinate pair used in the polyb&eacute;zier.
|-
|'''S''' (absolute)

'''s''' (relative)
|Shorthand: ''smooth curveto''
|(x2 y2 x y)+
|Draws a cubic B&eacute;zier curve from the current point to (x,y). The first control point is assumed to be the reflection of the second control point on the previous command relative to the current point. (If there is no previous command or if the previous command was not a '''C''', '''c''', '''S''' or '''s''', assume the first control point is coincident with the current point.) (x2,y2) is the second control point (that is, the control point at the end of the curve). '''S''' indicates that absolute coordinates will follow; '''s''' indicates that relative coordinates will follow. Multiple sets of coordinates may be specified to draw a polyb&eacute;zier. At the end of the command, the new current point becomes the final (x,y) coordinate pair used in the polyb&eacute;zier.
|-
|'''Q''' (absolute)

'''q''' (relative)
|''quadratic B&eacute;zier curveto''
|(x1 y1 x y)+
|A quadratic B&eacute;zier segment is defined by a start point, an end point, and one control point.

Draws a quadratic B&eacute;zier curve from the current point to (x,y) using (x1,y1) as the control point. '''Q''' indicates that absolute coordinates will follow; '''q''' indicates that relative coordinates will follow. Multiple sets of coordinates may be specified to draw a polyb&eacute;zier. At the end of the command, the new current point becomes the final (x,y) coordinate pair used in the polyb&eacute;zier.
|-
|'''T''' (absolute)

'''t''' (relative)
|Shorthand: ''smooth quadratic B&eacute;zier curveto''
|(x y)+
|Draws a quadratic B&eacute;zier curve from the current point to (x,y). The control point is assumed to be the reflection of the control point on the previous command relative to the current point. (If there is no previous command or if the previous command was not a '''Q''', '''q''', '''T''' or '''t''', assume the control point is coincident with the current point.) '''T''' indicates that absolute coordinates will follow; '''t''' indicates that relative coordinates will follow. At the end of the command, the new current point becomes the final (x,y) coordinate pair used in the polyb&eacute;zier.
|-
|'''A''' (absolute)

'''a''' (relative)
|''elliptical arc''
|(rx ry x-axis-rotation large-arc-flag sweep-flag x y)+
|An elliptical arc segment draws a segment of an ellipse.
|}

Draws an elliptical arc from the current point to (x, y). The size and
orientation of the ellipse are defined by two radii (rx, ry) and an
x-axis rotation, which indicates how the ellipse as a whole is rotated
relative to the current coordinate system. The center (cx, cy) of the
ellipse is calculated automatically to satisfy the constraints imposed
by the other parameters. large-arc-flag and sweep-flag contribute to
the automatic calculations and help determine how the arc is
drawn. For more information, see the following discussion.

With respect to the last row of the above table, the elliptical arc
command draws a section of an ellipse that meets the following
constraints:

*The arc starts at the current point.
*The arc ends at point (x, y).
*The ellipse has the two radii (rx, ry).
*The x-axis of the ellipse is rotated by x-axis rotation relative to the x-axis of the current coordinate system.

For most situations, there are actually four different arcs (two different ellipses, each with two different arc sweeps) that satisfy these constraints. large-arc-flag and sweep-flag indicate which one of the four arcs is drawn, as follows:

*Of the four candidate arc sweeps, two will represent an arc sweep of greater than or equal to 180 degrees (the "large-arc"), and two will represent an arc sweep of less than or equal to 180 degrees (the "small-arc"). If large-arc-flag is '1', then one of the two larger arc sweeps will be chosen; otherwise, if large-arc-flag is '0', one of the smaller arc sweeps will be chosen.

*If sweep-flag is '1', then the arc will be drawn in a "positive-angle" direction (that is, the ellipse formula x{{=}}cx+rx*cos(?) and y{{=}}cy+ry*sin(?) is evaluated such that theta starts at an angle corresponding to the current point and increases positively until the arc reaches (x,y)). A value of 0 causes the arc to be drawn in a "negative-angle" direction (that is, theta starts at an angle value corresponding to the current point and decreases until the arc reaches (x,y)).

The following image illustrates the four combinations of
large-arc-flag and sweep-flag and the four different arcs that will be
drawn based on the values of these flags. For each case, the following
path data command was used:

 &lt;path d="M 125,75 a100,50 0 '''?''','''?''' 100,50" style="fill:none; stroke:red; stroke-width:6"/&gt;

where "'''?''','''?'''" is replaced by "0,0" "0,1" "1,0" and "1,1" to generate the four possible cases.
[[Image:arcsExplained.png]]
|Import_Notes====Standards information===

*[http://www.w3.org/TR/SVG11/paths.html Scalable Vector Graphics: Paths], Section 8.5.23

===Members===

The '''SVGPathElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGPathElement''' object has these methods:

*[[svg/methods/createSVGPathSegArcAbs|'''createSVGPathSegArcAbs''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegArcAbs|'''SVGPathSegArcAbs''']] object.
*[[svg/methods/createSVGPathSegArcRel|'''createSVGPathSegArcRel''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegArcRel|'''SVGPathSegArcRel''']] object.
*[[svg/methods/createSVGPathSegClosePath|'''createSVGPathSegClosePath''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegClosePath|'''SVGPathSegClosePath''']] object.
*[[svg/methods/createSVGPathSegCurvetoCubicAbs|'''createSVGPathSegCurvetoCubicAbs''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegCurvetoCubicAbs|'''SVGPathSegCurvetoCubicAbs''']] object.
*[[svg/methods/createSVGPathSegCurvetoCubicRel|'''createSVGPathSegCurvetoCubicRel''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegCurvetoCubicRel|'''SVGPathSegCurvetoCubicRel''']] object.
*[[svg/methods/createSVGPathSegCurvetoCubicSmoothAbs|'''createSVGPathSegCurvetoCubicSmoothAbs''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegCurvetoCubicSmoothAbs|'''SVGPathSegCurvetoCubicSmoothAbs''']] object.
*[[svg/methods/createSVGPathSegCurvetoCubicSmoothRel|'''createSVGPathSegCurvetoCubicSmoothRel''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegCurvetoCubicSmoothRel|'''SVGPathSegCurvetoCubicSmoothRel''']] object.
*[[svg/methods/createSVGPathSegCurvetoQuadraticAbs|'''createSVGPathSegCurvetoQuadraticAbs''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegCurvetoQuadraticAbs|'''SVGPathSegCurvetoQuadraticAbs''']] object.
*[[svg/methods/createSVGPathSegCurvetoQuadraticRel|'''createSVGPathSegCurvetoQuadraticRel''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegCurvetoQuadraticRel|'''SVGPathSegCurvetoQuadraticRel''']] object.
*[[svg/methods/createSVGPathSegCurvetoQuadraticSmoothAbs|'''createSVGPathSegCurvetoQuadraticSmoothAbs''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegCurvetoQuadraticSmoothAbs|'''SVGPathSegCurvetoQuadraticSmoothAbs''']] object.
*[[svg/methods/createSVGPathSegCurvetoQuadraticSmoothRel|'''createSVGPathSegCurvetoQuadraticSmoothRel''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegCurvetoQuadraticSmoothRel|'''SVGPathSegCurvetoQuadraticSmoothRel''']] object.
*[[svg/methods/createSVGPathSegLinetoAbs|'''createSVGPathSegLinetoAbs''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegLinetoAbs|'''SVGPathSegLinetoAbs''']] object.
*[[svg/methods/createSVGPathSegLinetoHorizontalAbs|'''createSVGPathSegLinetoHorizontalAbs''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegLinetoHorizontalAbs|'''SVGPathSegLinetoHorizontalAbs''']] object.
*[[svg/methods/createSVGPathSegLinetoHorizontalRel|'''createSVGPathSegLinetoHorizontalRel''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegLinetoHorizontalRel|'''SVGPathSegLinetoHorizontalRel''']] object.
*[[svg/methods/createSVGPathSegLinetoRel|'''createSVGPathSegLinetoRel''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegLinetoRel|'''SVGPathSegLinetoRel''']] object.
*[[svg/methods/createSVGPathSegLinetoVerticalAbs|'''createSVGPathSegLinetoVerticalAbs''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegLinetoVerticalAbs|'''SVGPathSegLinetoVerticalAbs''']] object.
*[[svg/methods/createSVGPathSegLinetoVerticalRel|'''createSVGPathSegLinetoVerticalRel''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegLinetoVerticalRel|'''SVGPathSegLinetoVerticalRel''']] object.
*[[svg/methods/createSVGPathSegMovetoAbs|'''createSVGPathSegMovetoAbs''']]: Returns a standalone parentless [[svg/objects/SVGPathSegMovetoAbs|'''SVGPathSegMovetoAbs''']] object.
*[[svg/methods/createSVGPathSegMovetoRel|'''createSVGPathSegMovetoRel''']]: Returns a stand-alone, parentless [[svg/objects/SVGPathSegMovetoRel|'''SVGPathSegMovetoRel''']] object.
*[[svg/methods/getBBox|'''getBBox''']]: Gets the bounding box, in current user space, of the geometry of all contained graphics elements.
*[[svg/methods/getCTM|'''getCTM''']]: Gets  the transformation matrix  that transforms from  the current user units to the viewport coordinate system for the [[svg/properties/nearestViewportElement|'''nearestViewportElement''']] object.
*[[svg/methods/getPathSegAtLength|'''getPathSegAtLength''']]: Gets the index of [[svg/properties/pathSegList|'''pathSegList''']] by using the specified distance along the path.
*[[svg/methods/getPointAtLength|'''getPointAtLength''']]: Gets the (x,y) coordinate in user space that is the specified distance along the path.
*[[svg/methods/getScreenCTM|'''getScreenCTM''']]: Gets  the transformation matrix from the current user units to the screen coordinate system.
*[[svg/methods/getTotalLength|'''getTotalLength''']]: Gets the total length of the path, as a distance in the current user coordinate system.
*[[svg/methods/getTransformToElement|'''getTransformToElement''']]: Gets  the transformation matrix  that transforms from the user coordinate system on the current element to the user coordinate system on the  specified  target element.
*[[svg/methods/hasExtension|'''hasExtension''']]: Determines if the specified extension  is supported.

The '''SVGPathElement''' object has these properties:

*[[svg/properties/animatedNormalizedPathSegList|'''animatedNormalizedPathSegList''']]: Gets or sets the normalized animated contents of
the [[svg/properties/d|'''d''']] attribute.
*[[svg/properties/animatedPathSegList|'''animatedPathSegList''']]: Gets or sets the animated contents of the [[svg/properties/d|'''d''']] attribute in a form that matches the SVG syntax.
*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/farthestViewportElement|'''farthestViewportElement''']]: Gets  a value that represents the farthest ancestor [[svg/elements/svg|'''svg''']] element.
*[[svg/attributes/fill|'''fill''']]: Sets or retrieves a value that indicates the color to paint the interior of the given graphical element.
*[[svg/attributes/fill-opacity|'''fillOpacity''']]: Sets or retrieves a value that specifies the opacity of the painting operation that is used to paint the interior of the current object.
*[[svg/attributes/fill-rule|'''fillRule''']]: Sets or retrieves a value that indicates the algorithm that is to be used to determine what parts of the canvas are included inside the shape.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/attributes/marker|'''marker''']]: Sets or retrieves a value that specifies the marker symbol that is used for all vertices on the given '''path''' element or basic shape.
*[[svg/attributes/marker-end|'''markerEnd''']]: Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the final vertex of a given '''path''' element or basic shape.
*[[svg/attributes/marker-mid|'''markerMid''']]: Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at every other vertex (that is, every vertex except the first and last) of a given '''path''' element or basic shape.
*[[svg/attributes/marker-start|'''markerStart''']]: Sets or retrieves a value that defines the arrowhead or polymarker that is drawn at the first vertex of a given '''path''' element or basic shape.
*[[svg/attributes/mask|'''mask''']]: Sets or retrieves a value that indicates a SVG mask.
*[[svg/properties/nearestViewportElement|'''nearestViewportElement''']]: Gets  a value that indicates which element established the current viewport.
*[[svg/properties/normalizedPathSegList|'''normalizedPathSegList''']]: Gets or sets  the  normalized  static contents of the [[svg/properties/d|'''d''']] attribute.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
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