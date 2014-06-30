{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Unreviewed MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===

'''Note:'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.

The following constants exist in group '''SVGException''' code:
*'''SVGWrongTypeError'''
is raised when an object of the wrong type is passed to an operation.

'''Note:'''  No operation is defined to raise an '''SVGException''' exception with this code in the SVG 1.1 Second Edition specification. The constant is  defined for consistency with the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203737  1.1 First Edition specification].

*'''SVGInvalidValueError'''
is raised when an invalid value is passed to an operation or assigned to an attribute.
*'''SVGMatrixNotInvertableError''' is raised when an application tries  to invert a matrix that is not invertible.
'''Note:'''  The unusual spelling of this constant is maintained for compatibility with existing content.
|Import_Notes====Standards information===

*[http://go.microsoft.com/fwlink/p/?linkid{{=}}190918 Scalable Vector Graphics (SVG) 1.1], Appendix B.4

===Members===

The '''SVGException''' object has these methods:

*[[svg/methods/toString|'''toString''']]: Returns a string that represents the current object.

The '''SVGException''' object has these properties:

*[[svg/properties/code|'''code''']]: Gets the exception code that is raised.
*[[svg/properties/message|'''message''']]: Gets a description of the exception that is raised.
*[[svg/properties/name|'''name''']]: Gets the exception name that is raised.
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

*DOM Exception Error Codes
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}