{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/Window
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
In Windows Internet Explorer 8 and later, the '''onLine''' property returns <code>true</code> if both of the following conditions are true:
*the system is able to communicate with the network
*the system is not in global offline mode (Users can modify the global offline state by choosing '''Work Offline''' on the '''File''' menu.)

onLine
false
In Microsoft Internet Explorer 4.0 through Windows Internet Explorer 7, the '''onLine''' property indicates whether the system is in global offline mode. It does not indicate whether the system  can communicate with the network.
'''onLine''' returns <code>true</code> if the WWAHost.exe can contact the network, otherwise, it returns <code>false</code>.
A Metro style app using JavaScript uses event listeners ([[dom/EventTarget/addEventListener|'''addEventListener''']]) to monitor online and offline events that fire when the state of the window object changes. The offline event fires when the '''onLine''' property changes from <code>true</code> to <code>false</code>. The online event fires when the '''onLine''' property changes from <code>false</code> to <code>true</code>.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 5.6.10
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