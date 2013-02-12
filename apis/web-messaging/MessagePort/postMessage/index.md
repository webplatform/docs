{{Page_Title}}
{{Flags}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Posts a message through the channel, from one port to the other.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=message
|Data type=any
|Description=JavaScript primitive, such as a '''string''', '''PixelArray''', '''ImageData''', '''Blob''', '''File''', or '''ArrayBuffer'''.
|Optional=No
}}{{Method Parameter
|Name=transfer
|Data type=any
|Description=Objects listed in ''transfer'' are transferred, not just cloned, meaning that they are no longer usable on the sending side. 
Throws a ''DataCloneError'' if ''transfer'' array contains duplicate objects or the source or target ports, or if ''message'' could not be cloned.
|Optional=Yes
}}
|Method_applies_to=apis/web-messaging/MessagePort
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=When you create a new '''MessageChannel''' object, it has two connected '''MessagePort''' objects that can only send and receive messages between them.  If the ''ports'' parameter is supplied but contains errors, an '''InvalidStateError''' exception is thrown. Sending a message containing an un-supported object (such as a function), a '''DataCloneError''' exception is thrown.
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