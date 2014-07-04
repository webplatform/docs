{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=summary and examples needed.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the y-coordinate of the mouse cursor, relative to the upper-left corner of the page.}}
{{API_Object_Property
|Property_applies_to=dom/objects/MouseEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=yCoordinate
|Javascript_data_type=Number
|Return_value_description=The Y coordinate of the mouse cursor.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes=The '''pageY'''  property  is equivalent to the [[dom/properties/clientY|'''clientY''']] value plus the [[dom/properties/scrollTop|'''scrollTop''']]  value of the document, as the following code example shows.
 <code>var pageY {{=}} event.clientY + document.documentElement.scrollTop; </code>
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
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/objects/DragEvent|DragEvent]]</code>
*<code>[[dom/objects/MouseWheelEvent|MouseWheelEvent]]</code>
*<code>[[dom/objects/WheelEvent|WheelEvent]]</code>
*<code>Reference</code>
*<code>[[dom/properties/clientY|clientY]]</code>
*<code>[[css/cssom/properties/offsetY|offsetY]]</code>
*<code>[[dom/properties/screenY|screenY]]</code>
*<code>[[css/cssom/properties/y|y]]</code>
}}
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}