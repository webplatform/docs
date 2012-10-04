{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=code|Data type=unsigned short|Description=|Optional=}}
{{Method Parameter|Name=reason|Data type=DOMString|Description=|Optional=}}
|Method_applies_to=apis/websocket/objects/WebSocket
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=This method does not return a value.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
The '''onclose''' event will return three attributes:
*'''wasClean''' - '''binary''' - was the connection closed cleanly or not?
*'''code''' - '''unsigned long''' - code from the server.
*'''reason''' - '''text''' - reason provided by the server.

If the ''code'' parameter is present but is not an integer equal to 1000 or in the range 3000 to 4999, this method throws an '''InvalidAccessError''' exception and aborts.
If the ''reason'' parameter is longer than 123 bytes the event will throw a '''SyntaxError''' exception, and aborts.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_websockets\ie]:%20close method%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Syntax===
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}