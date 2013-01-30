{{Page_Title}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Removes all DOMHighResTimeStamp durations for the given measure name, or removes all measures and their associated DOMHighResTimeStamp durations.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=measureName
|Data type=any
|Description=Name of the measures(s) to be cleared.
|Optional=Yes
}}
|Method_applies_to=apis/user_timing/Performance
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section
|Notes=If a value for the  ''measureName'' parameter is specified, only measures with that name are removed.  If there are no measures with the specified name, this method does nothing.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C User Timing Specification
|URL=http://www.w3.org/TR/user-timing/
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[apis/timing/objects/performance|performance]]</code>
}}
{{Topics|User Timing}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}