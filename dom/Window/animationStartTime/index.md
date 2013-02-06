{{Page_Title}}
{{Flags
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces.
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/window
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Obsolete.  Originally supported in pre-release versions of Internet Explorer 10, the '''animationStartTime''' property is superceded in favor of the [[apis/timing/methods/now|'''performance.now''']] property.  Applications using '''animationStartTime''' should be updated accordingly.
Use the ''animationStartTime'' property instead  of recording animation start time using the '''Date.now''' function in order to ensure that the clock you are using has millisecond resolution and is monotonically increasing (where later values are always larger than earlier values).
The value reported by the ''animationStartTime''  property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}229562 Timing control for script-based animations]
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
*<code>Window</code>
*<code>[[apis/timing/methods/requestAnimationFrame|requestAnimationFrame]]</code>
*<code>[[apis/timing/methods/cancelAnimationFrame|cancelAnimationFrame]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}