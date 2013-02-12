{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Begins dispatching messages received on the port.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=apis/web-messaging/MessagePort
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The '''start''' method is called implicitly by when an  event handler function is assigned to the '''onmessage''' property.
In Internet Explorer 10, the start method is also called implicitly when a message event is registered using the '''addEventListener''' method.

}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=W3C Web Messaging Specification
|URL=http://www.w3.org/TR/webmessaging/
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
{{Topics|Web Messaging}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}