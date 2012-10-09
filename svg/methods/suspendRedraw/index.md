{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Notes_Section
|Notes=
===Remarks===
The redrawing operation is suspended until one of the following actions occur:
*The  [[svg/methods/unsuspendRedraw|'''unsuspendRedraw''']] method is called.
*The  [[svg/methods/unsuspendRedrawAll|'''unsuspendRedrawAll''']]  method is called.
*The ''maxWaitMilliseconds'' time-out interval elapses.

|Import_Notes=
===Syntax===
<div class{{=}}"code">var retval {{=}} SVGSVGElement.suspendRedraw(maxWaitMilliseconds);
</div>
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204733 Scalable Vector Graphics: Document Structure], Section 5.11.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[svg/elements/svg|SVGSVGElement]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}

[[Category:SVG]]