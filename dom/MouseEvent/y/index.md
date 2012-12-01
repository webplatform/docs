{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name|y}}
{{Summary_Section|Gets the y-coordinate of the mouse pointer, relative to the last positioned ancestor element.}}
{{API_Object_Property
|Property_applies_to=dom/objects/MouseEvent
|Read_only=No
|Example_object_name=event
|Return_value_name=yCoordinate
|Javascript_data_type=Number
|Return_value_description=The Y coordinate of the mouse cursor.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example displays the current mouse position in the browser's status window.
|Code=document.body.onmousemove = function (e) { console.log('X = ' + e.x + ' Y = " + e.y); }
}}
}}
{{Notes_Section
|Notes=If the event firing element is relatively positioned, then the y-coordinate from the boundary of the element is returned. If the event firing element and all of its parent elements are not relatively positioned, then the '''y''' property returns a coordinate relative to the '''body''' element.
The '''y''' property returns a coordinate relative to the '''body''' element.
If the mouse or finger is outside the window at the time the event fires, this property returns -1.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSSOM View
|URL=http://www.w3.org/TR/cssom-view/
|Status=Working Draft
|Relevant_changes=Section 9
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=Earlier than 5
|Note=This property is read only. This property retrieves a coordinate relative to the client.
}}
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