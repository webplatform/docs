{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Not recommended, synchronized, annoys users and causes user interface issues. Displays a dialog box showing the given text and a localized OK button.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=message
|Data type=String
|Description=The message to display in the dialog box.
|Optional=No
}}
|Method_applies_to=dom/window
|Example_object_name=window
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Not recommended for general use. See the notes for details.

Use this method to alert the user with some text.
|Notes=*You cannot change the title bar of the Alert dialog box.
*Not recommended due to the following issues -
**This is a synchronized method call. Meaning, calling this method pauses scripting execution of window that called the method, until the user closes the displayed dialog. Also, depending on your cross tab/window usage, this can sometimes pause scripting executions of other windows/tabs from the same domain.
**Calling this method in some browsers prevents the user from interacting with the entire browser, or browser window (along with all of its tabs), until the dialog is closed.
**Intrusive dialog boxes are generally annoying for the user.
Alternatively, create a dialog using other web platform means.
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