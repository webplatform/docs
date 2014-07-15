{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=needs example
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Defines a line by using beginning and ending (x,y) coordinate values with stroke and stroke-width styles .}}
{{API_Object
|Subclass_of=dom/SVGElement,dom/SVGTests,dom/SVGLangSpace,dom/SVGExternalResourcesRequired,dom/SVGStylable,dom/SVGTransformable
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;?xml version="1.0"?&gt;
&lt;svg width="120" height="120" 
     viewPort="0 0 120 120" version="1.1"
     xmlns="http://www.w3.org/2000/svg"&gt;

    &lt;line x1="20" y1="100" 
          x2="100" y2="20" 
          stroke="black" 
          stroke-width="2"/&gt;

&lt;/svg&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;?xml version="1.0"?&gt;
&lt;svg xmlns="http://www.w3.org/2000/svg"&gt;
    &lt;line x1="20" y1="100" x2="100" y2="100" stroke-width="2" 
	stroke="black" transform="rotate(-45 20 100)"/&gt;
&lt;/svg&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204732 Scalable Vector Graphics: Basic Data Types and Interfaces], Section 4.5.1

===Members===

The '''SVGElement''' object has these properties:

*[[svg/properties/focusable|'''focusable''']]: Determines if an element can acquire keyboard focus (that is, receive keyboard events) and be a target for field-to-field navigation actions (such as when  a user presses  the Tab key).
*[[svg/properties/id|'''id''']]: Standard XML attribute for assigning a unique name to an element.
*[[svg/properties/ownerSVGElement|'''ownerSVGElement''']]: Gets the nearest ancestor '''svg''' element.
*[[svg/properties/viewportElement|'''viewportElement''']]: Gets the element that established the current viewport.
*[[svg/properties/xmlbase|'''xmlbase''']]: Gets or sets the '''base''' attribute on the element.
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/SVG/Element/line SVGLineElement]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff972079(v=vs.85).aspx SVGLineElement]
|HTML5Rocks_link=
}}