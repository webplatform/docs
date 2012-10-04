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
{{Notes_Section
|Notes=
===Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
The closepath command (<code>Z</code> or <code>z</code>) ends the current subpath and causes an automatic straight line to be drawn from the current point to the initial point of the current subpath. If you follow a "closepath" command immediately by a "moveto" command, the "moveto" command identifies the start point of the next subpath. If you follow a "closepath" command  immediately by any other command,  the next subpath starts at the same initial point as the current subpath.
When a subpath ends in a "closepath" command, the implementation of 'stroke-linejoin' and 'stroke-linecap'  differs from when you manually close a subpath through a "lineto" command. With a "closepath" command, the end of the final segment of the subpath is joined with the start of the initial segment of the subpath by using the current value of 'stroke-linejoin'. If you manually close the subpath through a "lineto" command, the start of the first segment and the end of the last segment are each capped by using the current value of 'stroke-linecap' instead of being joined. At the end of the command, the new current point is set to the initial point of the current subpath.
 
 
Build date: 7/24/2012
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204736 Scalable Vector Graphics: Paths], Section 8.5.2


===Members===
The '''SVGPathSegClosePath''' object has these types of members:
*[#properties Properties]


====Properties====
The '''SVGPathSegClosePath''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/pathSegType|'''pathSegType''']]
|Gets the type of the path segment.
|-
|[[svg/properties/pathSegTypeAsLetter|'''pathSegTypeAsLetter''']]
|Gets the type of the path segment, specified by the corresponding one-character command name.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}