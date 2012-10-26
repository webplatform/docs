{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/objects/UIEvent
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 5.2.7


===Members===
The '''CompositionEvent''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''CompositionEvent''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/initCompositionEvent|'''initCompositionEvent''']]
|Initializes a new text composition event that the [[dom/methods/createEvent|'''createEvent''']] method created.
|-
|[[dom/methods/initEvent|'''initEvent''']]
|Initializes a new generic event that the  [[dom/methods/createEvent|'''createEvent''']] method created.
|-
|[[dom/methods/initUIEvent|'''initUIEvent''']]
|Initializes a new user interface event that the  [[dom/methods/createEvent|'''createEvent''']] method created.
|-
|[[dom/methods/preventDefault|'''preventDefault''']]
|Cancels the default action of an event.
|-
|[[dom/methods/stopImmediatePropagation|'''stopImmediatePropagation''']]
|Prevents any further propagation of an event.
|-
|[[dom/methods/stopPropagation|'''stopPropagation''']]
|Prevents propagation of an event beyond the current target.
|}
 

====Properties====
The '''CompositionEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/bubbles|'''bubbles''']]
|Gets a value that  indicates whether an event propagates up from the event target.
|-
|[[dom/properties/cancelable|'''cancelable''']]
|Gets a value that indicates whether you can cancel an event's default action.
|-
|[[dom/methods/cancelBubble|'''cancelBubble''']]
|Gets or sets a value that indicates whether an event should be stopped from propagating up from the current target.
|-
|[[dom/properties/currentTarget|'''currentTarget''']]
|Gets the event target that is currently being processed.
|-
|[[dom/properties/data|'''data''']]
|Gets the data of the event.
|-
|[[dom/properties/defaultPrevented|'''defaultPrevented''']]
|Gets a value that indicates whether the default action should be canceled.
|-
|[[dom/properties/detail|'''detail''']]
|Gets additional  information about  an event.
|-
|[[dom/properties/eventPhase|'''eventPhase''']]
|Gets the event phase that is being evaluated.
|-
|[[dom/properties/isTrusted|'''isTrusted''']]
|Gets a value that indicates whether a trusted event source created an event.
|-
|[[dom/properties/locale|'''locale''']]
|Gets the locale name for the event.
|-
|[[dom/properties/srcElement|'''srcElement''']]
|Gets the element that the event was originally dispatched to. Compare to [[dom/properties/target|'''target''']].
|-
|[[dom/properties/target|'''target''']]
|Gets the element that is the target of the event.
|-
|[[dom/properties/timeStamp|'''timeStamp''']]
|Gets the time, in milliseconds, when an event occurred.
|-
|[[dom/properties/type (event)|'''type''']]
|Gets the name of an event.
|-
|[[dom/properties/view|'''view''']]
|Gets  the '''window''' object  that an  event is generated from.
|}
 
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_dom_events\ie]:%20CompositionEvent object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}