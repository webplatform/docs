{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=apis/timing/objects/performanceTiming
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to calculate the time required to initialize the DOM content for the document.
|LiveURL=
|Code=
var oTiming {{=}} window.performance.timing;
var iLoadTimeMS {{=}} oTiming.domInteractive - oTiming.domLoading;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The value of the '''domInteractive''' property is controlled by the [[dom/document|'''document''']] object associated with the '''window''' object.  The value of the '''domInteractive''' property is updated when the '''readyState''' property is set to <code>interactive</code>.  If the document cannot be loaded, the value of the '''domInteractive''' property is available after the [[dom/events/load|'''onload''']] event has finished executing.
The value reported by the '''domInteractive''' property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).
Windows Internet Explorer 9.  This property is supported only for documents displayed in IE9 Standards mode.  For more information, see Defining Document Compatibility.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}210425 Navigation Timing], Section 4.2


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[apis/timing/objects/performanceTiming|performanceTiming]]</code>
*<code>[[apis/timing/properties/domLoading|domLoading]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}