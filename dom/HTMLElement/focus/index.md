{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=summary, examples, compatibility, standards, clean-up of MSDN sections
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/HTMLElement
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
This method raises the [[dom/HTMLElement/focus|'''onfocus''']] event. The effect depends on the object calling the method. When called for child windows (such as those created with the [[dom/Window/open|'''open''']] method of a '''window''' object), '''focus''' brings the target window to the foreground.
Elements cannot receive focus until the document finishes loading.
Windows Internet Explorer 8 and later. The '''focus''' method no longer brings child windows (such as those created with the '''open''' method) to the foreground. Child windows now request focus from the user, usually by flashing the title bar. To directly bring the window to the foreground, add script to the child window that calls the '''focus''' method of its '''window''' object.

Windows Internet Explorer 7 and later. For security reasons, child windows will only respond to the focus method when the following conditions are true:
*The child window does not have multiple tabs open.
*The focus method was not triggered by a double-click action.

If any of these conditions are true, the child window ignores the focus event.
As of Microsoft Internet Explorer 5, elements that expose the '''focus''' method must have the [[html/attributes/tabIndex|'''TABINDEX''']] attribute set.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.6.5
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