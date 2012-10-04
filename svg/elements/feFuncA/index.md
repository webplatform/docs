{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Element
|DOM_interface=svg/objects/SVGElement
}}
{{Topics|SVG}}
{{Notes_Section
|Notes=
===Remarks===
This topic describes the <code>feFuncR</code>, <code>feFuncG</code>, <code>feFuncB</code>, and <code>feFuncA</code> elements. These four elements are typically children of [[svg/elements/feComponentTransfer|'''feComponentTransferelement''']] and specify the transfer functions for the four channels, as follows:
*<code>feFuncR</code> — transfer function for the red component of the input graphic
*<code>feFuncG</code> — transfer function for the green component of the input graphic
*<code>feFuncB</code> — transfer function for the blue component of the input graphic
*<code>feFuncA</code> — transfer function for the alpha component of the input graphic

The following rules apply to the processing of the [[svg/elements/feComponentTransfer|'''feComponentTransferelement''']] element:
*If more than one transfer function element of the same kind is specified, the last occurrence is used.
*If any of the transfer function elements are unspecified, the [[svg/elements/feComponentTransfer|'''feComponentTransferelement''']] must be processed as if those transfer function elements were specified with their <code>type</code> attributes set to <code>identity</code> (see below).

In addition to core attributes (<code>id</code>, <code>xml:base</code>, <code>xml:lang</code>, and <code>xml:space</code>), the following seven attributes are applicable to the <code>feFuncR</code>, <code>feFuncG</code>, <code>feFuncB</code> and <code>feFuncA</code> elements:
*<code>type</code>

The <code>type</code> attribute can be one of five values: <code>identity</code>, <code>table</code>, <code>discrete</code>, <code>linear</code>, or <code>gamma</code> (see below). These five values indicate the type of component transfer function. The value of <code>type</code> determines the applicability of the other attributes (as discussed below).

In the following, C is the initial component (such as <code>feFuncR</code>), C' is the re-mapped component; both in the closed interval [0, 1]:
**For <code>identity</code>:

C' {{=}} C
**For <code>table</code>, the function is defined by linear interpolation between values given in the attribute <code>tableValues</code> (see below). The table has ''n''+1 values (that is, v<sub>0</sub> to v''<sub>n</sub>'') specifying the start and end values for ''n'' evenly sized interpolation regions. Interpolations use the following formula:

For a value C &lt; 1, find k such that k/''n'' &lt;{{=}} C &lt; (k+1)/''n''

The result C' is given by C' {{=}} v<sub>k</sub> + (C - k/''n'')*''n'' * (v<sub>k+1</sub> - v<sub>k</sub>)

If C {{=}} 1 then C' {{=}} V''<sub>n</sub>''
**For <code>discrete</code>, the function is defined by the step function given in the attribute <code>tableValues</code> (see below), which provides a list of ''n'' values (that is, v<sub>0</sub> to v<sub>n-1</sub>) in order to identify a step function consisting of ''n'' steps. The step function is defined by the following formula:

For a value C &lt; 1 find k such that k/''n'' &lt;{{=}} C &lt; (k+1)/''n''

The result C' is given by C' {{=}} v<sub>k</sub>

If C {{=}} 1 then C' {{=}} v<sub>n-1</sub>
**For <code>linear</code>, the function is defined by the following linear equation:

C' {{=}} <code>slope</code> * C + <code>intercept</code> (see below for <code>slope</code> and <code>intercept</code>)
**For <code>gamma</code>, the function is defined by the following exponential function:

C' {{=}} <code>amplitude</code> * pow(C, <code>exponent</code>) + <code>offset</code> (see below for <code>amplitude</code>, <code>exponent</code>, and <code>offset</code>)
**<code>tableValues</code>

When <code>type{{=}}"table"</code>, <code>tableValue</code> is a list of numbers v<sub>0</sub>, v<sub>1</sub>, ..., v''<sub>n</sub>'' separated by white space and/or a comma, which define the lookup table. An empty list results in an identity transfer function. If the attribute is not specified, then the effect is as if an empty list were provided.
**<code>slope</code>

When <code>type{{=}}"linear"</code>, <code>slope</code> indicates the slope of the linear function.
If the attribute is not specified, then the effect is as if a value of 1 were specified.
**<code>intercept</code>

When <code>type{{=}}"linear"</code>, <code>intercept</code> indicates the intercept of the linear function.
If the attribute is not specified, then the effect is as if a value of 0 were specified.
**<code>amplitude</code>

When <code>type{{=}}"gamma"</code>, <code>amplitude</code> indicates the amplitude of the gamma function.
If the attribute is not specified, then the effect is as if a value of 1 were specified.
**<code>exponent</code>

When <code>type{{=}}"gamma"</code>, <code>exponent</code> indicates the exponent of the gamma function.
If the attribute is not specified, then the effect is as if a value of 1 were specified.
**<code>offset</code>

When <code>type{{=}}"gamma"</code>, <code>offset</code> indicates the offset of the gamma function.
If the attribute is not specified, then the effect is as if a value of 0 were specified

|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}226062 Scalable Vector Graphics: Filter Effects], Section 15.25.10


===Members===
The '''SVGFEFuncAElement''' object has these types of members:
*[#properties Properties]


====Properties====
The '''SVGFEFuncAElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[svg/properties/amplitude|'''amplitude''']]
|Indicates the amplitude of the gamma function.
|-
|[[svg/properties/exponent|'''exponent''']]
|Indicates the exponent of the gamma function.
|-
|[[svg/properties/intercept|'''intercept''']]
|Indicates the intercept of the linear function.
|-
|[[svg/properties/slope|'''slope''']]
|Indicates the slope of the linear function.
|-
|[[svg/properties/tableValues|'''tableValues''']]
|Define the lookup table.
|-
|[[svg/properties/type (SVGComponentTransferFunctionElement)|'''type''']]
|The type of component transfer function. The function type determines the applicability of the other attributes.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/feComponentTransfer|SVGFEComponentTransferElement]]</code>
*<code>[[svg/elements/feFuncR|SVGFEFuncRElement]]</code>
*<code>[[svg/elements/feFuncGelement|SVGFEFuncGElement]]</code>
*<code>[[svg/elements/feFuncB|SVGFEFuncBElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}