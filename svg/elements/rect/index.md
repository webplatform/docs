{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The rect element is a SVG basic shape to create a rectangle starting with a given with and height beginning at a x- and y-point.}}
{{Markup_Element
|DOM_interface=dom/SVGRectElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=In the following code example,  the rect element is used to draw a purple rectangle.
|Code=<syntaxhighlight lang="xml">
<svg width="200" height="200" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="5" width="100" height="80" fill="purple" />
</svg>

</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/44786e14924371effbe4
}}{{Single Example
|Description=In the following code example, the rect element is used to create a orange rectangle with rounded corners.
|Code=<syntaxhighlight lang="xml">
<svg width="200" height="200" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <rect x="10" y="5" width="100" height="80" fill="orange" rx="10" ry="10" />
</svg>

</syntaxhighlight>
|LiveURL=http://code.webplatform.org/gist/9697f0fe090f4ad2e6e9
}}
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
|Import_Notes====Standards information===

*[http://www.w3.org/TR/SVG11/shapes.html#RectElement Scalable Vector Graphics: The The ‘rect’ element], Section 9.2

===Attributes===

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

*[[svg/attributes/x|'''x''']]
*[[svg/attributes/y|'''y''']]
*[[svg/attributes/width|'''width''']]
*[[svg/attributes/height|'''height''']]
*[[svg/attributes/rx|'''rx''']]
*[[svg/attributes/ry|''r'y''']]

===DOM Interface===

This element implements the [[dom/SVGRectElement|'''SVGRectElement''']] interface.
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