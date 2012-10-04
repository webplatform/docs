{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/objects/Event
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
Mutation events occur when DOM nodes are inserted and removed, or when character data or attributes are modified. For more information, see [[dom/methods/initMutationEvent|'''initMutationEvent''']].
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_dom_events\ie]:%20MutationEvent object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012
|Import_Notes=
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203756 Document Object Model (DOM) Level 3 Events Specification], Section 5.2.8


===Members===
The '''MutationEvent''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''MutationEvent''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/initEvent|'''initEvent''']]
|Initializes a new generic event that the  [[canvas/methods/createEvent|'''createEvent''']] method created.
|-
|[[dom/methods/initMutationEvent|'''initMutationEvent''']]
|Initializes a new  DOM  mutation (modification) event that the  [[canvas/methods/createEvent|'''createEvent''']] method created.
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
The '''MutationEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/attrChange|'''attrChange''']]
|Gets a value that indicates what type of change occurred.
|-
|[[dom/properties/attrName|'''attrName''']]
|Gets the name of the attribute that changed.
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
|[[dom/properties/defaultPrevented|'''defaultPrevented''']]
|Gets a value that indicates whether the default action should be canceled.
|-
|[[dom/properties/eventPhase|'''eventPhase''']]
|Gets the event phase that is being evaluated.
|-
|[[dom/properties/isTrusted|'''isTrusted''']]
|Gets a value that indicates whether a trusted event source created an event.
|-
|[[dom/properties/newValue|'''newValue''']]
|Gets the new value of the attribute or text node.
|-
|[[dom/properties/prevValue|'''prevValue''']]
|Gets the previous value of the attribute or text node.
|-
|[[dom/properties/relatedNode|'''relatedNode''']]
|Gets a second node related to a mutation event.
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
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}