{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|An interface that provides Web applications with timing-related information.}}
{{API_Object}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=When a webpage is displayed in Windows Internet Explorer 9 mode, Windows Internet Explorer records timestamps that correspond to the time when various steps occurred during the process used to load a document. Each property of the '''performanceTiming''' object corresponds to one of these timestamps.
This object is not supported for Metro style apps using JavaScript.
The built-in performance marks occur in the following order:
*'''navigationStart'''
*'''redirectStart'''
*'''unloadEventStart'''
*'''unloadEventEnd'''
*'''redirectEnd'''
*'''fetchStart'''
*'''domainLookupStart'''
*'''domainLookupEnd'''
*'''connectStart'''
*'''connectEnd'''
*'''requestStart'''
*'''responseStart'''
*'''responseEnd'''
*'''domLoading'''
*'''domInteractive'''
*'''domContentLoadedEventStart'''
*'''domContentLoadedEventEnd'''
*'''domComplete'''
*'''loadEventStart'''
*'''loadEventEnd'''
*'''msFirstPaint'''

The properties of the '''performanceTiming''' object represent the number of milliseconds that have elapsed between midnight January 1, 1970 and the time the measurement was recorded.

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
{{Topics|DOM, Navigation Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}