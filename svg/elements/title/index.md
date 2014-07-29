{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs usage, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics
|Content=Compatibility Incomplete
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The '''title''' element (<title>) provides a human readable name for container elements and graphics elements.}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following code example, a title element is provided for an ellipse. When you hover over the ellipse, a tooltip may be displayed.
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <ellipse cx="150" cy="100" rx="100" ry="75" fill="greenyellow">
        <title>This is the title of an ellipse.</title>
      </ellipse>
    </svg>
  </body>
</html>
</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/3fe2120a26327b9b9b8e
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Each container element or graphics element in a Scalable Vector Graphics (SVG) drawing can provide  a [[svg/elements/desc|'''desc''']]  or a '''title''' textual description. The '''title''' elements are not rendered as part of the graphics. Instead, they appear as a tooltip as the the pointer  moves over particular elements in the drawing.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.6

===Members===

The '''SVGTitleElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/properties/style|'''style''']]: Gets a [[css/cssom/style|'''style''']] object.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===

*[[svg/elements/desc|'''SVGDescElement''']]
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}