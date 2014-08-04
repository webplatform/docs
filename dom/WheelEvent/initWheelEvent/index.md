{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Initializes a new WheelEvent that the createEvent method created.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=eventType
|Data type=String
|Description=The name of the event. Sets the value for the [[dom/Event/type|type]] property.
|Optional=No
}}{{Method Parameter
|Name=canBubble
|Data type=Boolean
|Description=Whether the event propagates upward. Sets the value for the [[dom/Event/bubbles|bubbles]] property.
|Optional=No
}}{{Method Parameter
|Name=cancelable
|Data type=Boolean
|Description=Whether the event is cancelable and so [[dom/Event/preventDefault|preventDefault]] can be called. Sets the value for the [[dom/Event/cancelable|cancelable]] property.
|Optional=No
}}{{Method Parameter
|Name=view
|Data type=Object
|Description=The window on which this event is occurring.  Sets the value for the [[dom/UIEvent/view|view]] property.
|Optional=No
}}{{Method Parameter
|Name=detail
|Data type=Number
|Description=Specifies additional information. This value is returned in the [[dom/UIEvent/detail|'''detail''']] property  of the event.
|Optional=No
}}{{Method Parameter
|Name=screenX
|Data type=Number
|Description=The x-coordinate of the mouse pointer, relative to the  upper-left corner of the screen. Sets the value for the [[dom/MouseEvent/screenX|'''screenX''']] property,
|Optional=No
}}{{Method Parameter
|Name=screenY
|Data type=Number
|Description=The y-coordinate of the mouse pointer, relative to the  upper-left corner of the screen. Sets the value for the [[dom/MouseEvent/screenY|'''screenY''']] property.
|Optional=No
}}{{Method Parameter
|Name=clientX
|Data type=Number
|Description=The x-coordinate of the mouse pointer, relative to the  upper-left corner of the browser's client area. Sets the value for the [[dom/MouseEvent/clientX|'''clientX''']] property.
|Optional=No
}}{{Method Parameter
|Name=clientY
|Data type=any
|Description=The y-coordinate of the mouse pointer, relative to the  upper-left corner of the browser's client area. Sets the value for the [[dom/MouseEvent/clientY|'''clientY''']] property.
|Optional=No
}}{{Method Parameter
|Name=button
|Data type=Number
|Description=The mouse button that caused the event. Sets the value for the [[dom/MouseEvent/button|'''button''']] property (see the property page for common values).
|Optional=No
}}{{Method Parameter
|Name=relatedTarget
|Data type=DOM Node
|Description=A secondary element that is involved in the event. Sets the value for the [[dom/MouseEvent/relatedTarget|'''relatedTarget''']] property.
|Optional=No
}}{{Method Parameter
|Name=modifiersListArg
|Data type=String
|Description=A space-separated list of any of the following values:
*'''Alt''' - The left or right Alt key. 
*'''AltGraph''' - The Ctrl and Alt keys.
*'''CapsLock''' - The Caps Lock toggle.
*'''Control''' - The left or right Ctrl key.
*'''Meta''' - The Meta/Control key.
*'''NumLock''' - The Num Lock toggle.
*'''ScrollLock''' - The Scroll Lock toggle.
*'''Shift''' - The left or right Shift key.
*'''Fn'''
*'''OS'''
*'''SymbolLock'''

Other implementation specific options may be supported.
For example -
*'''Win''' (on Microsoft Windows) - The left or right Windows logo key.
*'''Scroll''' - The Scroll Lock toggle.
|Optional=No
}}{{Method Parameter
|Name=deltaX
|Data type=Number
|Description=The distance that the mouse wheel has rotated around the x-axis. Sets the value for the [[dom/WheelEvent/deltaX|'''deltaX''']] property.
|Optional=No
}}{{Method Parameter
|Name=deltaY
|Data type=Number
|Description=The distance that the mouse wheel has rotated around the y-axis. Sets the value for the [[dom/WheelEvent/deltaY|'''deltaY''']] property.
|Optional=No
}}{{Method Parameter
|Name=deltaZ
|Data type=Number
|Description=The distance that the mouse wheel has rotated around the z-axis. Sets the value for the [[dom/WheelEvent/deltaZ|'''deltaZ''']] property.
|Optional=No
}}{{Method Parameter
|Name=deltaMode
|Data type=Number
|Description=The delta mode of the event. Sets the value for the [[dom/WheelEvent/deltaMode|'''deltaMode''']] property (see the property page for common values).
|Optional=No
}}
|Method_applies_to=dom/WheelEvent
|Example_object_name=event
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=function dispatchWheelEvent(){
   		var evt{{=}}document.createEvent('WheelEvent');
   		var theform{{=}}document.forms.dispatch;
   		//var retval {{=}} WheelEvent.initWheelEvent(eventType, canBubble, cancelable, view, detail, screenXArg, screenYArg, clientXArg, clientYArg, buttonArg, relatedTargetArg, modifiersListArg, deltaX, deltaY, deltaZ, deltaMode); 
   		evt.initWheelEvent('wheel', 
   							theform.chkcanbubble.checked,
   							theform.chkcancellable.checked,
   							eval(theform.view.value),
   							theform.detail.value,
   							theform.screenx.value,
   							theform.screeny.value,
   							theform.clientx.value,
   							theform.clienty.value,
   							theform.button.value,
   							null,
   							theform.modifierlist.value,
   							theform.deltax.value,
   							theform.deltay.value,
   							theform.deltaz.value,
   							theform.cbodeltamode.value);   

   							
   		window.dispatchEvent(evt);
   }
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 5.2.4
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff975254(v=vs.85).aspx initWheelEvent]
|HTML5Rocks_link=
}}