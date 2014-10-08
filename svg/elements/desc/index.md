{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''desc''' element (<desc>) provides a human readable description for container elements and graphics elements.}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=
|Description=In the following code example, the '''desc''' element is used to define a description of an element. This element can be read programatically to analyze SVG structure.

Copy this sample to a text file and save it with the ''.html'' file extension. Run it in Internet Explorer 9 to see a greenyellow ellipse.

The element will look like this:
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <svg width="400" height="400">
      <ellipse cx="150" cy="100" rx="100" ry="75" fill="greenyellow">
        <desc>This is the description of an ellipse.</desc>
      </ellipse>
    </svg>
  </body>
</html>
</syntaxhighlight>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.5

===Members===

The '''SVGDescElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGDescElement''' object has these properties:

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
|Specifications={{Related Specification
|Name=SVG 1.1
|URL=http://www.w3.org/TR/SVG/struct.html#DescriptionAndTitleElements
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=SVG Tiny 1.2
|URL=http://www.w3.org/TR/SVGTiny12/struct.html#TitleAndDescriptionElements
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}