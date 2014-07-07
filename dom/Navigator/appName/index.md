{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|appName Returns a string with the name of the browser/user agent.
The HTML5 specification also allows any browser to return "Netscape" here, for compatibility reasons.
}}
{{API_Object_Property
|Property_applies_to=dom/Navigator
|Read_only=Yes
|Example_object_name=navigator
|Javascript_data_type=String
|Return_value_description=
Microsoft Internet Explorer

Returned by Internet Explorer 10 and earlier.

Netscape

Default. Returned by Netscape Navigator, Google Chrome, Mozilla Firefox, and IE11.

MSAppHost/1.0 

Returned by WWAHost.exe.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var browserName = navigator.appName;
//broswerName returns "Netscape"
|LiveURL=http://result.dabblet.com/gist/b1e7c611e97594b60956/56337717d0b88e99b8944707d60bb7072b359788
}}
}}
{{Notes_Section
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
{{Topics|DOM, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID.appName navigator.appName]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms533079(v=vs.85).aspx navigator.appName]
|HTML5Rocks_link=
}}