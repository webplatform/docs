{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=svg/objects/SVGElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
'''Note'''  In addition to the attributes, properties, events, methods, and styles listed above, SVG elements also inherent core HTML attributes, properties, events, methods, and styles.
The zoom event occurs when  a  user initiates an action  that  causes the current view of the SVG document (or SVGdocument fragment) to be rescaled (including any change to the [[svg/elements/svg|'''svg''']] element's [[svg/properties/currentScale|'''currentScale''']]  property).
'''Note'''  A zoom event  applies  only  to the outermost [[svg/elements/svg|'''svg''']] element.
 
 
Build date: 7/24/2012
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}204745 Scalable Vector Graphics: Scripting], Section 18.5.2


===Members===
The '''SVGZoomEvent''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''SVGZoomEvent''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
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
The '''SVGZoomEvent''' object has these properties.
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
|[[svg/properties/newScale|'''newScale''']]
|Gets the new scale value of a zoom event.
|-
|[[svg/properties/newTranslate|'''newTranslate''']]
|Gets the new translation values of a zoom event.
|-
|[[svg/properties/previousScale|'''previousScale''']]
|Gets the previous scale value of a zoom event.
|-
|[[svg/properties/previousTranslate|'''previousTranslate''']]
|Gets the previous translation values of a zoom event.
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