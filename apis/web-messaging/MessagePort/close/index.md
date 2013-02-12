{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Disconnects the port, so that it is no longer active.}}
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
|Notes=This method releases the '''MessagePort''' from its corresponding '''MessagePort'''. After calling the '''close''' method, message events will no longer be received on this port and '''postMessage''' will no longer post any messages. To continue messaging, you need to create a new '''MessageChannel''' and resend one of the ports to the other window or document.
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