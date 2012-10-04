{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/objects/MouseEvent
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example displays the current mouse position in the browser's status window.
|LiveURL=
|Code=
&lt;BODY onmousemove{{=}}"window.status {{=}} 'X{{=}}' + window.event.x + 
    ' Y{{=}}' + window.event.y"&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The property is read-only in Microsoft Internet Explorer 4.0, and read/write in Microsoft Internet Explorer 5 and later. In browser versions earlier than Internet Explorer 5, the '''y''' property retrieves a coordinate relative to the client.
If the event firing element is relatively positioned, then the y-coordinate from the boundary of the element is returned. If the event firing element and all of its parent elements are not relatively positioned, then the '''y''' property returns a coordinate relative to the '''body''' element.
The '''y''' property returns a coordinate relative to the '''body''' element.
If the mouse or finger is outside the window at the time the event fires, this property returns -1.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>event</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}