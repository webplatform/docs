{{Page_Title}}
{{Flags
|Content=Not Neutral, Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Sets the maximum number of PerformanceResourceTiming resources that may be stored in the buffer to the value of the maxSize parameter.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=maxSize
|Data type=unsigned long
|Description=The maximum number of PerformanceResourceTiming resources that will be stored in the buffer.
|Optional=No
}}
|Method_applies_to=apis/resource_timing/Performance
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The '''setResourceTimingBufferSize''' does not take effect until the '''clearResourceTimings''' method is called.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Resource Timing Specification
|URL=http://www.w3.org/TR/resource-timing
|Status=W3C Candidate Recommendation
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
{{Topics|Resource Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}