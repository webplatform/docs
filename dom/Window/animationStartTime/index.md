{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces.
see http://www.w3.org/TR/animation-timing/
|Checked_Out=No
|High-level issues=Deletion Candidate, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section|Obsolete. Returns a timestamp of the start time of the current refresh interval, such that multiple animations can be synchronized with each other.}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=No
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
Obsolete.  Originally supported in pre-release versions of Internet Explorer 10, the '''animationStartTime''' property is superceded in favor of the '''performance.now''' property.  Applications using '''animationStartTime''' should be updated accordingly.
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.mozAnimationStartTime mozAnimationStartTime]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh972901(v=vs.85).aspx animationStartTime Property]
|HTML5Rocks_link=
}}