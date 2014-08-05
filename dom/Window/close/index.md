{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Closes the current browser window or tab, or HTML Application (HTA). }}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Window
|Example_object_name=window
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=&lt;script type="text/javascript"&gt;
function closeCurrentWindow()
{
  window.close();
}
&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
When a function fired by an event on any object calls the 
'''close''' method, the window.'''close''' method is implied.
 <code>&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
 function myClose() {
     close();}
 &lt;/SCRIPT&gt;
 &lt;BODY onclick{{=}}"myClose();"&gt;
 Click this page and window.close() is called.
 &lt;/BODY&gt;</code>
When an event on any 
object calls the '''close''' method, the 
[[dom/Document/close|'''Document.close''']] method is implied.
 <code>&lt;BUTTON onclick{{=}}"close();"&gt;
 Click this button and document.close() is called.
 &lt;/BUTTON&gt;</code>
How a window is closed programmatically determines whether the user is prompted with a confirmation dialog box:
*Invoking the window.'''close''' method on a window not opened with script displays a confirmation dialog box. Using script to close the last running instance of Windows Internet Explorer also opens the confirmation dialog box.
*Invoking the 
window.'''close''' method on an HTA closes the application without prompting the user because the HTA is trusted and follows a different security model.
For more information on the security model of HTAs, please refer to [_inet_HTML_Applications_Overview#Security#Security The Power of Trust: HTAs and Security].


====Using the close method in a Metro style app using JavaScript====
Invoking the '''window.close''' method on a Metro style app using JavaScript closes the app without prompting the user.
It is against Windows Store policy to programmatically close your app. The only time an app should programmatically close is when there is an unrecoverable error, in which case the app should throw an unhandled exception or  use the '''MSApp.terminateApp''' method.
In you use '''window.close''', it appears as a crash to the user is logged as a crash in the developer’s telemetry data on the Windows Store dashboard.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.close window.close]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536367(v=vs.85).aspx close Method]
|HTML5Rocks_link=
}}