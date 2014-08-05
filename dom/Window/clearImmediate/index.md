{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=Not part of user_timing, resource_timing, or navigation_timing interfaces.
|Checked_Out=No
|High-level issues=Deletion Candidate, Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Cancels a function request created with setImmediate.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=handle
|Data type=Number
|Description=A handle to an immediate callback request, which is the value returned by [[dom/Window/setImmediate|'''setImmediate''']].
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var immediateID {{=}} setImmediate(function () {
  // Run some code
}

document.getElementById("button").addEventListener(function () {
  clearImmediate(immediateID);
}, false);
}}
}}
{{Notes_Section
|Notes====Remarks===
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}247522 Efficient Script Yielding]
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.clearImmediate clearImmediate]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/windows/apps/hh965354.aspx clearImmediate Method]
|HTML5Rocks_link=
}}