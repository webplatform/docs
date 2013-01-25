{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The error code of the current PositionError.}}
{{API_Object_Property
|Property_applies_to=apis/geolocation/PositionError
|Read_only=Yes
|Example_object_name=PositionError
|Javascript_data_type=Number
|Return_value_description=Must be one of the following constant values:
*PERMISSION_DENIED (numeric value 1): The location acquisition process failed because the document does not have permission to use the Geolocation API.
*POSITION_UNAVAILABLE (numeric value 2): The position of the device could not be determined. For instance, one or more of the location providers used in the location acquisition process reported an internal error that caused the process to fail entirely.
*TIMEOUT (numeric value 3): The length of time specified by the ''timeout'' property has elapsed before the implementation could successfully acquire a new '''Position''' object.
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Geolocation Specification
|URL=http://dev.w3.org/geo/api/spec-source.html
|Status=W3C Proposed Recommendation
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
{{Topics|Geolocation}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}