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
While similar to [[dom/DOMException|'''DOMException''']] objects, '''DOMError''' objects represent errors that are generated through other means, such as return values.  ('''DOMException''' objects are thrown as exceptions.)  Both objects return similar values, so it is possible to create general handlers to respond to either type of error.
|Import_Notes=
===Members===
The '''DOMError''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''DOMError''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/name (DOMError, DOMException)|'''toString (DOMError)''']]
|Returns the [[dom/properties/toString (DOMError)|'''name''']] property of a '''DOMError''' and any associated message defined with the error.
|}
 

====Properties====
The '''DOMError''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/toString (DOMError)|'''name (DOMError, DOMException)''']]
|Returns a '''DOMString''' value an error that occurred during a DOM operation.
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/DOMException|DOMException]]</code>
*<code>[[dom/constants/DOM exception error codes|DOM Error Codes]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}