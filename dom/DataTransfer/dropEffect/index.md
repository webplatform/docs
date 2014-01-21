{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Sets or gets the type of drag-and-drop operation and the type of cursor to display.}}
{{API_Object_Property
|Property_applies_to=dom/DataTransfer
|Read_only=No
|Example_object_name=event.dataTransfer
|Return_value_name=dropEffect
|Javascript_data_type=String
|Return_value_description=One of the following values -
*'''none'''
*'''copy'''
*'''link'''
*'''move'''
|Example_value_name=newDropEffect
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''dropEffect''' and [[dom/DataTransfer/effectAllowed|effectAllowed]] properties of the [[dom/DataTransfer|DataTransfer]] object to display the move cursor.
{{TODO|Make sure this examples works and remove this comment (also in the effectAllowed page).}}
|Code=<!doctype html>
<html>
 <body>
<p><br/><p>
<div id="oTarget">
(drop text here)
  </div>
 </body>
</html>
}}
}}
{{Notes_Section
|Usage=Use this property to get or set the current operation, using one of the following values -
*'''none'''
*'''copy'''
*'''link'''
*'''move'''
|Notes=The '''dropEffect''' property must be used with the [[dom/properties/effectAllowed|'''effectAllowed''']] property. These properties are set on the source object of a drag-and-drop operation. The '''effectAllowed''' property determines which drag-and-drop operations are available from the source object. The '''dropEffect''' property determines which drag-and-drop operations are allowed on the target object. For example, the source object might set the '''effectAllowed''' property to '''all''' drag-and-drop operations, while the target object specifies that the '''dropEffect''' allows only '''copy''' operations.
The recommended technique for dropping text is to set the '''dropEffect''' in the target object's event handler function for the following events: [[dom/events/dragenter|'''ondragenter''']], [[dom/events/dragover|'''ondragover''']], and [[dom/events/drop|'''ondrop''']]. The [[dom/properties/effectAllowed|'''effectAllowed''']] property must be set in one of the source object's drag-and-drop event handlers, such as the [[dom/events/dragstart|'''ondragstart''']] event.
The target object of a drag-and-drop operation can set the '''dropEffect''' during the following events: [[dom/events/dragenter|'''ondragenter''']], [[dom/events/dragover|'''ondragover''']], and [[dom/events/drop|'''ondrop''']]. To display the cursor until the final drop, the default action of the following events must be canceled: '''ondragenter''', '''ondragover''', and '''ondrop''': and the '''dropEffect''' must be set. Otherwise, the copy cursor, move cursor, or link cursor set by this property displays only until the first valid drop target is intersected, at which point the cursor is replaced by the drop/no-drop cursor for the rest of the drag operation.
There is a default drag-and-drop functionality for the following elements: [[html/elements/a|'''a''']], [[html/elements/img|'''img''']], [[html/elements/textarea|'''textarea''']], and [[html/elements/input|'''input type{{=}}text''']]. When one of these objects is the source element, the default drop effect cannot be overridden by setting the '''dropEffect''' property of the target element. Instead, the default behavior of the source object must be canceled.
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
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}