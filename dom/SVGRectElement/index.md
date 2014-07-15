{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs some inline SVG examples...
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The SVGRectElement interface provides access to the properties of the rect element.}}
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
	
	&lt;rect x="10" y="10" width="100" height="100"/&gt;
	
&lt;/svg&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;?xml version="1.0"?&gt;
&lt;svg width="120" height="120" 
     viewPort="0 0 120 120" version="1.1"
     xmlns="http://www.w3.org/2000/svg"&gt;
	
	&lt;rect x="10" y="10" 
	      width="100" height="100"
	      rx="15" ry="15"/&gt;
	
&lt;/svg&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204732 Scalable Vector Graphics: Basic Data Types and Interfaces], Section 4.5.1

===Members===

The '''SVGRectElement''' object has these properties:

*[[svg/properties/height|'''height''']]: Gets or sets  the height of an element.
*[[svg/properties/width|'''width''']]: Defines the width of an element.
*[[svg/properties/x|'''x''']]: Gets or sets the x-coordinate value.
*[[svg/properties/y|'''y''']]: Gets or sets the y-coordinate value.
*[[svg/properties/rx|'''rx''']]: Gets or sets  the x-axis radius of a rounded corner rectangle.
*[[svg/properties/ry|'''ry''']]: Gets or sets  the y-axis radius of a rounded corner rectangle.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/SVG/Element/rect SVGRectElement]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff972117(v=vs.85).aspx SVGRectElement]
|HTML5Rocks_link=
}}