{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/Element
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
A DOMTokenList object will stringify to the value of the DOMTokenList object's underlying string.
A set of space-separated tokens is a string containing zero or more words (known as tokens) separated by one or more space characters, where words consist of any string of one or more characters, none of which are space characters (the space characters are U+0020 SPACE, U+0009 CHARACTER TABULATION (tab), U+000A LINE FEED (LF), U+000C FORM FEED (FF), and U+000D CARRIAGE RETURN (CR)).
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_dom_general\ie]:%20DOMTokenList object%20 RELEASE:%20(7/27/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/27/2012
|Import_Notes=
===Syntax===
===Members===
The '''DOMTokenList''' object has these types of members:
*[#methods Methods]


====Methods====
The '''DOMTokenList''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/DOMTokenList/contains|'''contains''']]
|Returns <code>true</code> if the token is present; <code>false</code> otherwise.
|-
|[[dom/methods/toggle|'''toggle''']]
|Adds a token if it is not present, or removes it if it is. Returns <code>true</code> if the token is now present (it was added); returns <code>false</code> if it is not (it was removed).
|-
|[[dom/methods/toString|'''toString''']]
|Stringifies the token list.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}