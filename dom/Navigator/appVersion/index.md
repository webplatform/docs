{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Returns the version of the browser as a string. It may be either a plain version number, like "5.0", or a version number followed by more detailed information. The HTML5 specification also allows any browser to return "4.0" here, for compatibility reasons.}}
{{API_Object_Property
|Property_applies_to=dom/Navigator
|Read_only=Yes
|Example_object_name=navigator
|Return_value_name=result
|Javascript_data_type=String
|Return_value_description=The '''appVersion''' property returns a value based on the application name, application version, and platform. This syntax shows the format of the returned value.
 <code>clientVersion (platform; information; extra Information)
 or
 5.0 (compatible; MSIE 5.5; Windows 98; Win 9x 4.90)</code>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example enumerates the properties of the navigator object for the current web browser and displays them on the screen.
|LiveURL=http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788
}}
}}
{{Notes_Section
|Usage=Do not rely on this property to return the correct browser version. In Gecko-based browsers (like Firefox) and WebKit-based browsers (like Chrome and Safari) the returned value starts with "5.0" followed by platform information. In Opera 10 and newer the returned version does not match the actual browser version, either.
|Notes====Remarks===
|Import_Notes====Syntax===
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID.appVersion navigator.appVersion]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms533080(v=vs.85).aspx navigator.appVersion]
|HTML5Rocks_link=
}}