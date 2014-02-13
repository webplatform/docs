{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=any
|Description= Specifies the client window coordinate of x.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=any
|Description= Specifies the client window coordinate of y.
|Optional=No
}}
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=String

String

{| class="wikitable"
|-
!Return value
!Description
|-
|empty string
|Component is inside the client area of the object.
|-
|outside
|Component is outside the bounds of the object.
|-
|scrollbarDown
|Down scroll arrow is at the specified location.
|-
|scrollbarHThumb
|Horizontal scroll thumb or box is at the specified location.
|-
|scrollbarLeft
|Left scroll arrow is at the specified location.
|-
|scrollbarPageDown
|Page-down scroll bar shaft is at the specified location.
|-
|scrollbarPageLeft
|Page-left scroll bar shaft is at the specified location.
|-
|scrollbarPageRight
|Page-right scroll bar shaft is at the specified location.
|-
|scrollbarPageUp
|Page-up scroll bar shaft is at the specified location.
|-
|scrollbarRight
|Right scroll arrow is at the specified location.
|-
|scrollbarUp
|Up scroll arrow is at the specified location.
|-
|scrollbarVThumb
|Vertical scroll thumb or box is at the specified location.
|-
|handleBottom
|Bottom sizing handle is at the specified location.
|-
|handleBottomLeft
|Lower-left sizing handle is at the specified location.
|-
|handleBottomRight
|Lower-right sizing handle is at the specified location.
|-
|handleLeft
|Left sizing handle is at the specified location.
|-
|handleRight
|Right sizing handle is at the specified location.
|-
|handleTop
|Top sizing handle is at the specified location.
|-
|handleTopLeft
|Upper-left sizing handle is at the specified location.
|-
|handleTopRight
|Upper-right sizing handle is at the specified location.
|}
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''componentFromPoint''' method to determine which object the mouse pointer is hovering over.
|Code=&lt;HTML&gt;
&lt;HEAD&gt;
&lt;SCRIPT&gt;
/*When this function is activated, an alert pops up displays the component at the position of the pointer. */
function ComponentSnapShot(){
   var sElem {{=}} "";
   sElem {{=}} document.body.componentFromPoint(
      event.clientX,
      event.clientY
   );
   if (sElem{{=}}{{=}}"")
    alert("No component there!");
   else
    alert("Component: " + sElem);    
}
function trackElement(){
   var sElem {{=}} "";
   sElem {{=}} document.body.componentFromPoint(
      event.clientX,
      event.clientY
   );
   window.status {{=}} "mousemove " + event.clientX + ", "
      + event.clientY +
      " The mouse pointer is hovering over: " + sElem;
   
}
&lt;/SCRIPT&gt;
&lt;/HEAD&gt;
&lt;!-- There are several different events that can be used with componentFromPoint. Below are a few of them. 
Be carefull! Not all mouse events can be used with componentFromPoint.  --&gt;
&lt;BODY onmousemove{{=}}"trackElement()" onmousedown{{=}}"ComponentSnapShot()" onkeydown{{=}}"ComponentSnapShot()" oncontextmenu{{=}}"ComponentSnapShot()"&gt;
&lt;TEXTAREA COLS{{=}}500 ROWS{{=}}500&gt;
This text forces scroll bars to appear in the window.
&lt;/TEXTAREA&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/componentFromPointEX1.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''componentFromPoint''' method, available as of Microsoft Internet Explorer 5, is applicable to any object that can be given scroll bars through Cascading Style Sheets (CSS).
The '''componentFromPoint''' method might not  return the same object consistently when it is used with the [[dom/MouseEvent/mouseover|'''onmouseover''']] event. Because a user's mouse speed and 
entry point can vary, different components of an element can fire the 
'''onmouseover''' event. For example, when a 
user moves the cursor over a '''textArea''' object with 
scroll bars, the event might fire when the mouse enters the component 
border, the scroll bars, or the client region. After the event fires, 
the expected element might not be returned, unless the scroll bars were 
the point of entry for the mouse. In this case, the [[dom/MouseEvent/mousemove|'''onmousemove''']] 
event can be used to provide more consistent results.
For the object's sizing handles to appear, [[dom/Document/designMode|'''designMode''']] must be '''On''', and the object must be selected.
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
}}
{{Related_Specifications_Section
|Specifications=
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}