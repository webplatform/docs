{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Returns the type of the last non-redirect navigation in the current browsing context. See Notes.}}
{{API_Object_Property
|Property_applies_to=apis/navigation timing/PerformanceTiming
|Read_only=Yes
|Javascript_data_type=unsigned short
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=This attribute must have one of the following navigation type values.
*TYPE_NAVIGATE (0): Navigation started by clicking on a link, or entering the URL in the user agent's address bar, or form submission, or initializing through a script operation other than the ones used by TYPE_RELOAD and TYPE_BACK_FORWARD as listed below.
*TYPE_RELOAD (1): Navigation through the reload operation or the location.reload() method.
*TYPE_BACK_FORWARD (2): Navigation through a history traversal operation.
*TYPE_RESERVED (255): Any navigation types not defined by values above.
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