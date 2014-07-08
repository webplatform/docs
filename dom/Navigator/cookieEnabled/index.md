{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Retrieves whether client-side persistent cookies are enabled. Persistent cookies are those that are stored on the client-side computer.}}
{{API_Object_Property
|Property_applies_to=dom/Navigator
|Read_only=Yes
|Example_object_name=navigator
|Javascript_data_type=Boolean
|Return_value_description=
false (false)

Client does not support cookies or cookies are disabled.

true (true)

Client does support cookies.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=if (!navigator.cookieEnabled) { 
  // let the user know that enabling cookies makes the web page much more useful
}
}}
}}
{{Notes_Section
|Usage=Some websites may require cookies to be enabled on the client in order to work as intended. 
eg. a cookie may be used to store a user token that is used to automatically log a user back in when they return visit.

Use navigator.cookieEnabled to determine if the client web browser has cookies enabled. Display a message if they are not and your site requires it.
|Notes====Remarks===
'''Note'''  CookieEnabled does not check the status of session cookies.
This property does not check whether third-party persistent cookies are enabled.
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
{{See_Also_Section
|External_links=[http://www.wikihow.com/Enable-Cookies-in-Your-Internet-Web-Browser How to enable cookies in your Web Browser]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Navigator.cookieEnabled navigator.cookieEnabled]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms533694(v=vs.85).aspx navigator.cookieEnabled]
|HTML5Rocks_link=
}}