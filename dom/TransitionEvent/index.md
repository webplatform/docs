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
The completion of a CSS transition generates a corresponding Document Object Model (DOM) event. An event is fired for each property that undergoes a transition. This allows a content developer to perform actions that synchronize with the completion of a transition. 

Each event provides the name of the property the transition is associated with as well as the duration of the transition.
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_dom_events\ie]:%20TransitionEvent object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Members===
The '''TransitionEvent''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''TransitionEvent''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/initTransitionEvent|'''initauthor{{=}}"jaymunro" time{{=}}"20120418T100943-0800" data{{=}}"MS"TransitionEvent''']]
|Used to initialize the value of a [[dom/methods/initTransitionEvent|'''TransitionEvent''']].
|}
 

====Properties====
The '''TransitionEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/elapsedTime (TransitionEvent)|'''elapsedTime''']]
|The amount of time the transition has been running, in seconds.
|-
|[[dom/properties/propertyName|'''propertyName''']]
|Name of the CSS property associated with the transition.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}