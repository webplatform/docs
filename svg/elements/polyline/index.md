{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The poyline element is a SVG basic shape to create a series of lines connecting several points. Usually, a polyline is used to create open shapes.}}
{{Markup_Element
|DOM_interface=dom/SVGPolylineElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following code example, the polyline element is used to draw a gold polyline inside an inline SVG element.
|Code=<syntaxhighlight lang="xml">
<svg width="400" height="400"  version="1.1" xmlns="http://www.w3.org/2000/svg">
  <polyline points="50,50 150,120 100,220 200,150" stroke="gold" stroke-width="1" fill="none" />
</svg>
</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/37caee51f773695efdd4
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

Typically, '''polyline''' elements define open shapes.
'''Note:'''  You cannot provide an odd number of coordinates.
|Import_Notes====Attributes===

====Global attributes====
*[[svg/attributes#Conditional_Processing_Attributes|'''Conditional processing attributes''']]
*[[svg/attributes#Core_Attributes|'''Core attributes''']]
*[[svg/attributes#Graphical_Event_Attributes|'''Graphical events attributes''']]
*[[svg/attributes#Presentation_Attributes|'''Presentation attributes''']]

*[[svg/attributes/style|'''style''']]
*[[svg/attributes/class|'''class''']]
*[[svg/attributes/externalResourcesRequired|'''externalResourcesRequired''']]
*[[svg/attributes/transform|'''transform''']]

====Specific attributes====

*[[svg/attributes/points|'''points''']]

===DOM Interface===

This element implements the [[dom/SVGPolylineElement|'''SVGPolylineElement''']] interface.
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