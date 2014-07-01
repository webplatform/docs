{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=possible example
|Checked_Out=No
|High-level issues=Needs Review
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Returns the time immediately after the user agent finishes the domain name lookup for the resource.}}
{{API_Object_Property
|Property_applies_to=apis/resource_timing/PerformanceResourceTiming
|Read_only=Yes
|Return_value_description=DOMHighResTimeStamp
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=If a page is retrieved from an application cache, '''domainLookupEnd''' will have the same value as '''fetchStart'''.
The value reported by the '''domainLookupEnd''' property represents the number of milliseconds between the recorded time and midnight January 1, 1970 (UTC).
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Resource Timing Specification
|URL=http://www.w3.org/TR/resource-timing/#dom-performanceresourcetiming-domainlookupend
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
{{Topics|API, Resource Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}