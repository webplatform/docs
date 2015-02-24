{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, example, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <svg> element represents the root of a Scalable Vector Graphics (SVG) fragment.}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
|Tag_omissions=
|CSS_display=
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=
|Code=<nowiki>
<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100">
  <circle cx="50" cy="50" r="40"
      fill="red" stroke="blue" stroke-width="5" />
</svg>
</nowiki>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=Scalable Vector Graphics (SVG) is a modularized language for describing two-dimensional vector and mixed vector/raster graphics in XML. Only a correct HTML5 parser, using the syntax defined in [http://www.w3.org/TR/2010/WD-html5-20100624/syntax.html#syntax 8 The HTML syntax], will be able to properly interpret SVG elements when using '''text/html'''. When using '''application/xhtml+xml''', one must use proper [http://www.w3.org/TR/html-polyglot/#namespaces namespaces] to ensure that SVG elements are interpreted correctly.
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

If an SVG document is likely to be referenced as a component of another document,  you might  want to include a [[svg/properties/viewBox|'''viewBox''']] attribute on the outermost '''svg''' element of the referenced document. This attribute provides a convenient way to design SVG documents to scale-to-fit into an arbitrary viewport.

'''svg''' elements can appear in the middle of SVG content. You can use these elements to embed SVG document fragments within other SVG document fragments. You can also use '''svg''' elements within the middle of SVG content  to establish a new viewport.

In all cases, you must declare an SVG namespace  so that all SVG elements are identified as belonging to the SVG namespace. Typically, you can declare an SVG namespace as follows:

 &lt;svg xmlns="http://www.w3.org/2000/svg" ... &gt;
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=* [[svg/elements|List of SVG Elements]]
* [[HTML/Canvas_and_SVG|A comparison of canvas and SVG]]
|External_links=* [http://www.w3.org/TR/SVG11/ Scalable Vector Graphics (SVG) 1.1]
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