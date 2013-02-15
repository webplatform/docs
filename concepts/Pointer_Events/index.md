{{Page_Title|Pointer Events Primer}}
{{Flags
|High-level issues=Stub
|Content=Incomplete
|Editorial notes=Created page as a placeholder; will be populating later this afternoon.
}}
{{API_Name}}
{{Summary_Section|This document is written for web developers who have basic familiarity with [http://docs.webplatform.org/wiki/html HTML] and [http://docs.webplatform.org/wiki/javascript JavaScript].  This document should help you:
# Understand the end-user and web developer problems that Pointer Events address
# Easily add Pointer Events to an existing web page
# Take advantage of additional methods and attributes available in Pointer Events
# Find additional resources to learn more about Pointer Events
}}
{{Concept_Page
|Content===1. WHY POINTER EVENTS==
===1.1 UNIFIED MODEL FOR MULTIPLE INPUT TYPES===
In the last few years, there has been an explosion of computing devices that use mechanisms other than a mouse for end user input.  These input mechanisms include touch as on a smartphone or pen/stylus as on a slate.  All of today’s web browsers support mouse events (mouseover, mousedown, mousemove, etc.) but many users aren’t using a mouse.  Today’s user may be interacting with a web page using their fingers on a smartphone while riding public transit or using a pen on a slate/tablet while in a meeting.  Pointer Events provides a unified model for all three of these input types without requiring web developers to write unique code for each.  And Pointer Events is intended to be forward compatible covering future interaction paradigms.
===1.2 ABILITY TO IDENTIFY DIFFERENT INPUT TYPES===
Most modern browsers such as the latest versions of Chrome, Firefox, Internet Explorer, Opera, and Safari all map touch or pen input to mouse events.  But this makes it hard to know if a mouse event is an actual mouse event or was synthetically generated from a touch or pen input event.  Pointer Events also includes attributes to identify which mouse or pen button(s) were pressed during the event.  
===1.3 ADDITIONAL METHODS AND ATTRIBUTES===
Finally, Pointer Events provides additional attributes such as touch contact geometry size, pressure, and pen tilt so that web developers can take advantage of these additional inputs in building experiences for end users.  And if web developers want, they can write unique code for each input type.

==2. BASIC POINTER EVENTS==
Pointer Events includes a number of basic events similar to mouse events:
=== 2.1 DOWN AND UP (WITH EXAMPLE)===
Pointer Events includes basic pointer down and pointer up events.  
* pointerdown is triggered when a user clicks a mouse button or touches the screen with a finger or pen.
* pointerup is triggered when a user releases a mouse button or releases their finger or pen from touching the screen. 
The below example shows how pointerdown and pointerup are similar to mousedown and mouseup:

}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section}}
{{Topics|DOM, DOMEvents, Touch}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}