{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Exposes the available methods on the connected ports.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=Two '''MessagePort''' objects are automatically created when a '''MessageChannel''' object is created,   and are returned by the '''port1''' and '''port2''' properties.  Messages are sent from one port are received by the other, and vice versa.
The '''MessagePort''' object provides the '''start''' method to begin dispatching  messages received on the port, and the '''close''' method to close and disconnect the port. The '''postMessage''' method sends  messages through the port.
In Internet Explorer 10, message ports are automatically enabled when a message event is registered with the '''onmessage''' property or  '''addEventListener''' method. This makes it unnecessary to explicitly call the '''start''' method under these conditions.
After posting a '''MessagePort''' object using '''postMessage''', the  '''MessagePort''' object is implicitly '''close'''d.

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