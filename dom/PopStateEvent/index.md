{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/Event
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
A pop state event is dispatched to the window object every time the active history entry changes.
To read the current history entry immediately, invoke <code>history.state</code>.
|Import_Notes=
===Syntax===
===Members===
The '''PopStateEvent''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''PopStateEvent''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/initPopStateEvent|'''initPopStateEvent''']]
|Initializes the properties of a '''PopStateEvent'''.
|}
 

====Properties====
The '''PopStateEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/state|'''state''']]
|Returns the information that was provided to [[dom/methods/pushState|'''pushState''']] or [[dom/methods/replaceState|'''replaceState''']].
|}
 

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/properties/state|state]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}