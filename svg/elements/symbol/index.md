{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, usage, spec reference, standardization status
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
|Description=In the following code example, a symbol is created and displayed in two different sizes.
Copy this sample to a text file and save it with the ''.html'' file extension. Run it in Internet Explorer 9 to see the symbols.

The symbols will look like this:
|Code=<syntaxhighlight lang="xml">
<!DOCTYPE HTML>
<html>
  <head></head>
  <body>
    <!-- Create SVG container. -->
    <svg width="400" height="400">
      <!-- Definitions -->
      <defs>
        <!-- Define symbol for fill. -->
        <symbol id="mySymbol" viewBox="0 0 50 50" x="0" y="0" width="10" height="10" >
          <!-- Create path for individual symbol. -->
          <path d="M 0 10 L 25 30 L 50 30 Z" stroke="darkorchid" stroke-width="3" fill="cornflowerblue" />
        </symbol>
      </defs>
      <!-- Insert symbol twice. -->
      <use x="50" y="50" width="50" height="50" xlink:href="#mySymbol" />
      <use x="50" y="100" width="100" height="100" xlink:href="#mySymbol" />
      </svg>
  </body>
</html>
</syntaxhighlight>
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Use  '''symbol''' elements for graphics that are used multiple times in the same document to add  structure and semantics. Documents that are rich in structure  can  be rendered graphically, as speech or  braille, and  promote accessibility.

Compared to a [[svg/elements/g|'''g''']] element, the '''symbol''' element itself is not rendered. Only instances of a '''symbol''' element (that is, a reference to a '''symbol''' by a [[svg/elements/use|'''use''']] element) are rendered.

The '''symbol''' element has   [[svg/properties/viewBox|'''viewBox''']] and [[svg/properties/preserveAspectRatio|'''preserveAspectRatio''']]  attributes that  enable  a '''symbol''' to scale-to-fit within a rectangular viewport  that the referencing [[svg/elements/use|'''use''']] element defines.

The [[css/properties/display|'''display''']] property does not apply to the '''symbol''' element. Thus, '''symbol''' elements are not directly rendered even if  you set the '''display''' property  to a value other than [[css/properties/text-decoration-none|'''none''']].  '''symbol''' elements are available for referencing even when  you set the '''display''' property on the '''symbol''' element or any of its ancestors  to '''none'''.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.7

===Members===

The '''SVGSymbolElement''' object has these events:

*[[svg/events/load|'''onload''']]: Occurs  when the browser has fully parsed the element and all of its descendants.

The '''SVGSymbolElement''' object has these properties:

*[[svg/properties/className|'''className''']]: Gets  the names of the classes  that are assigned to this object.
*[[svg/properties/clipPath|'''clipPath''']]: Sets or retrieves a reference to the SVG graphical object that will be used as the clipping path.
*[[svg/properties/externalResourcesRequired|'''externalResourcesRequired''']]: Gets a value that indicates whether referenced resources that are not in the current document are required to correctly render a given element.
*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/attributes/mask|'''mask''']]: Sets or retrieves a value that indicates a SVG mask.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor [[svg/objects/SVGElement|'''svg''']] element.
*[[svg/properties/preserveAspectRatio|'''preserveAspectRatio''']]: Gets  an XML value that indicates whether to force uniform graphic scaling.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===

===Reference===

*[[svg/elements/marker|'''SVGMarkerElement''']]
*[[svg/elements/patterrn|'''SVGPatternElement''']]
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}