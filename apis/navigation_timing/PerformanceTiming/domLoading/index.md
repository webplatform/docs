{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the time immediately before the user agent sets the current document readiness to "loading".}}
{{API_Object_Property
|Property_applies_to=apis/navigation_timing/PerformanceTiming
|Read_only=Yes
|Example_object_name=PerformanceTiming
|Javascript_data_type=unsigned long
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The value of the '''domLoading''' property is controlled by the '''document''' object associated with the '''window''' object.  The value of the '''domLoading''' property is updated when the '''readyState''' property is set to <code>loading</code>.  If the document cannot be loaded, the value of the '''domLoading''' property is available after the '''onload''' event has finished executing.
The value reported by the '''domLoading''' property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Navigation Timing Specification
|URL=http://w3c-test.org/webperf/specs/NavigationTiming/
|Status=W3C Editor's Draft
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Navigation Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}