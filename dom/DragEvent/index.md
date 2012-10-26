{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/objects/MouseEvent
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 7.9.2


===Members===
The '''DragEvent''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''DragEvent''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/getModifierState|'''getModifierState''']]
|Queries the state of the specified modifier key.
|-
|[[dom/methods/initDragEvent|'''initDragEvent''']]
|Initializes a new drag event.
|-
|[[dom/methods/initEvent|'''initEvent''']]
|Initializes a new generic event that the  [[dom/methods/createEvent|'''createEvent''']] method created.
|-
|[[dom/methods/initMouseEvent|'''initMouseEvent''']]
|Initializes a new mouse event that the  [[dom/methods/createEvent|'''createEvent''']] method created.
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
The '''DragEvent''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/altKey|'''altKey''']]
|Gets a value that indicates whether the Alt key is pressed.
|-
|[[dom/properties/bubbles|'''bubbles''']]
|Gets a value that  indicates whether an event propagates up from the event target.
|-
|[[dom/properties/button|'''button''']]
|Gets the mouse button that caused an event.
|-
|[[dom/properties/buttons|'''buttons''']]
|Gets a value that indicates which mouse buttons  a user pressed.
|-
|[[dom/properties/cancelable|'''cancelable''']]
|Gets a value that indicates whether you can cancel an event's default action.
|-
|[[dom/methods/cancelBubble|'''cancelBubble''']]
|Gets or sets a value that indicates whether an event should be stopped from propagating up from the current target.
|-
|[[dom/properties/clientX|'''clientX''']]
|Gets the x-coordinate of the mouse pointer, relative to the upper-left corner of the viewport (that is, the application's client area).
|-
|[[dom/properties/clientY|'''clientY''']]
|Gets the y-coordinate of the mouse pointer, relative to the upper-left corner of the viewport (that is, the application's client area).
|-
|[[dom/properties/ctrlKey|'''ctrlKey''']]
|Gets a value that indicates whether the Ctrl key is pressed.
|-
|[[dom/properties/currentTarget|'''currentTarget''']]
|Gets the event target that is currently being processed.
|-
|[[dom/properties/dataTransfer|'''dataTransfer''']]
|Retrieves the [[dom/objects/dataTransfer|'''dataTransfer''']] object associated with the event.
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
|[[dom/properties/fromElement|'''fromElement''']]
|Gets the object that the mouse pointer exited.
|-
|[[dom/properties/isTrusted|'''isTrusted''']]
|Gets a value that indicates whether a trusted event source created an event.
|-
|[[dom/properties/layerX|'''layerX''']]
|Gets the x-coordinate of the mouse pointer, relative to the last positioned ancestor element.
|-
|[[dom/properties/layerY|'''layerY''']]
|Gets the y-coordinate of the mouse pointer, relative to the last positioned ancestor element.
|-
|[[dom/properties/metaKey|'''metaKey''']]
|Gets a value that indicates whether the Meta/Control key is pressed.
|-
|[[css/cssom/properties/offsetX|'''offsetX''']]
|Gets the x-coordinate of the mouse pointer, relative to the target node.
|-
|[[css/cssom/properties/offsetY|'''offsetY''']]
|Gets the y-coordinate of the mouse pointer, relative to the target node.
|-
|[[css/cssom/properties/pageX|'''pageX''']]
|Gets the y-coordinate of the mouse pointer, relative to the upper-left corner of the page.
|-
|[[css/cssom/properties/pageY|'''pageY''']]
|Gets the y-coordinate of the mouse pointer, relative to the upper-left corner of the page.
|-
|[[dom/properties/relatedTarget|'''relatedTarget''']]
|Gets   the secondary element that is involved in an event.
|-
|[[dom/properties/screenX|'''screenX''']]
|Gets the x-coordinate of the mouse pointer, relative to the  upper-left corner of the screen.
|-
|[[dom/properties/screenY|'''screenY''']]
|Gets the y-coordinate of the mouse pointer, relative to the  upper-left corner of the screen.
|-
|[[dom/properties/shiftKey|'''shiftKey''']]
|Gets a value that indicates whether the Shift key is pressed.
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
|[[dom/properties/toElement|'''toElement''']]
|Gets the object that the mouse pointer entered.
|-
|[[dom/properties/type (event)|'''type''']]
|Gets the name of an event.
|-
|[[dom/properties/view|'''view''']]
|Gets  the '''window''' object  that an  event is generated from.
|-
|[[dom/properties/which|'''which''']]
|Gets which mouse button is pressed.
|-
|'''x'''
|Gets the x-coordinate of the mouse pointer, relative to the last positioned ancestor element.
|-
|[[css/cssom/properties/y|'''y''']]
|Gets the y-coordinate of the mouse pointer, relative to the last positioned ancestor element.
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[dom/methods/initDragEvent|initDragEvent]]</code>
*<code>[[dom/events/drag|ondrag]]</code>
*<code>[[dom/events/dragend|ondragend]]</code>
*<code>[[dom/events/dragenter|ondragenter]]</code>
*<code>[[dom/events/dragleave|ondragleave]]</code>
*<code>[[dom/events/dragover|ondragover]]</code>
*<code>[[dom/events/dragstart|ondragstart]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}