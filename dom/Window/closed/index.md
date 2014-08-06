{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|This read-only property indicates whether the referenced window is closed or not.}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=Yes
|Example_object_name=window
|Javascript_data_type=Boolean
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var popupWindow {{=}} null;

function refreshPopupWindow() {
  if (popupWindow && !popupWindow.closed) {
    // popupWindow is open, refresh it
    popupWindow.location.reload(true);
  } else {
    // Open a new popup window
    popupWindow {{=}} window.open("popup.html","dataWindow");
  }
}
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.closed window.closed]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms533574(v=vs.85).aspx closed Property]
|HTML5Rocks_link=
}}