{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the time immediately before the user agent starts requesting the current document from the server, or from relevant application caches or from local resources. If the transport connection fails after a request is sent and the user agent reopens a connection and resends the request, returns the corresponding values of the new request.}}
{{API_Object_Property
|Property_applies_to=apis/navigation timing/PerformanceTiming
|Read_only=Yes
|Example_object_name=PerformanceTiming
|Javascript_data_type=unsigned long
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=The PerformanceTiming interface does not include an attribute to represent the completion of sending the request, e.g., requestEnd.
*Completion of sending the request from the user agent does not always indicate the corresponding completion time in the network transport, which brings most of the benefit of having such an attribute.
*Some user agents have high cost to determine the actual completion time of sending the request due to the HTTP layer encapsulation.
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