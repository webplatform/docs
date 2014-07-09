{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs an example....
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the secondary element that is involved in an event.
The relatedTarget property is used to find the other element, if any, involved in an event. Events like mouseover are oriented around a certain target, but also involve a secondary target, such as the target that is exited as the mouseover event fires for the primary target.
}}
{{API_Object_Property
|Property_applies_to=dom/MouseEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=relatedTargetElement
|Javascript_data_type=DOM Node
|Return_value_description=The secondary element that is involved in an event.
|Example_value_name=[object HTMLElement]
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Use this property to determine the secondary element that is involved in the event.
The secondary element depends on the type of event:
*In [[dom/MouseEvent/mouseover|'''mouseover''']] events, the secondary element is the element that the mouse pointer left.
*In [[dom/MouseEvent/mouseout|'''mouseout''']] events, the secondary element is the element that the mouse pointer entered.
*In [[dom/FocusEvent/focusin|'''focusin''']] events, the secondary element is the element that lost focus.
*In [[dom/FocusEvent/focusout|'''focusout''']] events, the secondary element is the element that gained focus.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 3 Events
|URL=http://www.w3.org/TR/DOM-Level-3-Events/
|Status=Working Draft
|Relevant_changes=Section 5.2.3
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
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN, HTML5Rocks
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/event.relatedTarget event.relatedTarget]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ff974881(v=vs.85).aspx event.relatedTarget]
|HTML5Rocks_link=[http://www.html5rocks.com/en/search?q=event.relatedTarget event.relatedTarget samples]
}}