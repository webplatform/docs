{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
This topic describes the '''feFuncR''', '''feFuncG''', '''feFuncB''', and '''feFuncA''' elements. These four elements are typically children of [[svg/elements/feComponentTransfer|'''feComponentTransferelement''']] and specify the transfer functions for the four channels, as follows:
*'''feFuncR''' — transfer function for the red component of the input graphic
*'''feFuncG''' — transfer function for the green component of the input graphic
*'''feFuncB''' — transfer function for the blue component of the input graphic
*'''feFuncA''' — transfer function for the alpha component of the input graphic

The following rules apply to the processing of the [[svg/elements/feComponentTransfer|'''feComponentTransferelement''']] element:
*If more than one transfer function element of the same kind is specified, the last occurrence is used.
*If any of the transfer function elements are unspecified, the [[svg/elements/feComponentTransfer|'''feComponentTransferelement''']] must be processed as if those transfer function elements were specified with their '''type''' attributes set to '''identity''' (see below).

In addition to core attributes ('''id''', '''xml:base''', '''xml:lang''', and '''xml:space'''), the following seven attributes are applicable to the '''feFuncR''', '''feFuncG''', '''feFuncB''', and '''feFuncA''' elements:
*'''type'''

The '''type''' attribute can be one of five values: '''identity''', '''table''', '''discrete''', '''linear''', or '''gamma''' (see below). These five values indicate the type of component transfer function. The value of '''type''' determines the applicability of the other attributes (as discussed below).

In the following, C is the initial component (such as '''feFuncR'''), C' is the re-mapped component; both in the closed interval [0, 1]:
**For '''identity''':

C' {{=}} C
**For '''table''', the function is defined by linear interpolation between values given in the attribute '''tableValues''' (see below). The table has ''n''+1 values (that is, v<sub>0</sub> to v''<sub>n</sub>'') specifying the start and end values for ''n'' evenly sized interpolation regions. Interpolations use the following formula:

For a value C &lt; 1, find k such that k/n &lt;{{=}} C &lt; (k+1)/n

The result C' is given by C' {{=}} v<sub>k</sub> + (C - k/n)*''n'' * (v<sub>k+1</sub> - v<sub>k</sub>)

If C {{=}} 1 then C' {{=}} V''<sub>n</sub>''
**For '''discrete''', the function is defined by the step function given in the attribute '''tableValues''' (see below), which provides a list of ''n'' values (that is, v<sub>0</sub> to v<sub>n-1</sub>) in order to identify a step function consisting of n steps. The step function is defined by the following formula:

For a value C &lt; 1 find k such that k/''n'' &lt;{{=}} C &lt; (k+1)/''n''

The result C' is given by C' {{=}} v<sub>k</sub>

If C {{=}} 1 then C' {{=}} v<sub>n-1</sub>
**For '''linear''', the function is defined by the following linear equation:

C' {{=}} '''slope''' * C + '''intercept''' (see below for '''slope''' and '''intercept''')
**For '''gamma''', the function is defined by the following exponential function:

C' {{=}} '''amplitude''' * pow(C, '''exponent''') + '''offset''' (see below for '''amplitude''', '''exponent''', and '''offset''')
**'''tableValues'''

When '''type{{=}}"table"''', '''tableValue''' is a list of numbers v<sub>0</sub>, v<sub>1</sub>, ..., v''<sub>n</sub>'' separated by white space and/or a comma, which define the lookup table. An empty list results in an identity transfer function. If the attribute is not specified, then the effect is as if an empty list were provided.
**'''slope'''

When '''type{{=}}"linear"''', '''slope''' indicates the slope of the linear function.
If the attribute is not specified, then the effect is as if a value of 1 were specified.
**'''intercept'''

When '''type{{=}}"linear"''', '''intercept''' indicates the intercept of the linear function.
If the attribute is not specified, then the effect is as if a value of 0 were specified.
**'''amplitude'''

When '''type{{=}}"gamma"''', '''amplitude''' indicates the amplitude of the gamma function.
If the attribute is not specified, then the effect is as if a value of 1 were specified.
**'''exponent'''

When '''type{{=}}"gamma"''', '''exponent''' indicates the exponent of the gamma function.
If the attribute is not specified, then the effect is as if a value of 1 were specified.
**'''offset'''

When '''type{{=}}"gamma"''', '''offset''' indicates the offset of the gamma function.
If the attribute is not specified, then the effect is as if a value of 0 were specified
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.7

===Members===

====Properties====
The '''SVGFEFuncRElement''' object has these properties.

*[[svg/properties/amplitude|'''amplitude''']]: Indicates the amplitude of the gamma function.
*[[svg/properties/exponent|'''exponent''']]: Indicates the exponent of the gamma function.
*[[svg/properties/intercept|'''intercept''']]: Indicates the intercept of the linear function.
*[[svg/properties/slope|'''slope''']]: Indicates the slope of the linear function.
*[[svg/properties/tableValues|'''tableValues''']]: Define the lookup table.
*[[svg/properties/type (SVGComponentTransferFunctionElement)|'''type''']]: The type of component transfer function. The function type determines the applicability of the other attributes.
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
|Topic_clusters=Filters
|Manual_sections====Related pages (MSDN)===
*[[svg/elements/feComponentTransfer|'''SVGFEComponentTransferElement''']]
*[[svg/elements/feFuncGelement|'''SVGFEFuncGElement''']]
*[[svg/elements/feFuncB|'''SVGFEFuncBElement''']]
*[[svg/elements/feFuncA|'''SVGFEFuncAElement''']]
}}
{{Topics|SVG}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}