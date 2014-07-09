{{Page_Title}}
{{Flags
|State=Unreviewed
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|This method indicates whether the current browser is Java Run Time Environment-enabled or not.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Navigator
|Example_object_name=navigator
|Return_value_name=result
|Javascript_data_type=Boolean
|Return_value_description=Boolean

'''Boolean'''. Returns one of the following possible values:

{{{!}} class="wikitable"
{{!}}-
!Return value
!Description
{{!}}-
{{!}}true
{{!}}Java JRE is enabled.
{{!}}-
{{!}}false
{{!}}Java JRE is not enabled.
{{!}}}
 
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Feature test for Java JRE. Negative results do not mean that Java JRE is not installed on the client. It can also indicate that the Java JRE has been disabled by the client Addons Manager or the Java JRE control panel.
|Code=if (window.navigator.javaEnabled()) {
   // browser has java JRE and it is enabled.
}
}}
}}
{{Notes_Section
|Notes=This method does NOT determine if javascript or active scripting is enabled in the web browser or not.
To detect if active scripting is enabled in a web browser add &lt;noscript&gt; tags to your web page.

The return value for this method indicates whether the preference that controls Java Run Time Environment is on or off - not whether the browser offers Java support in general.

Java JRE can also be disabled from the web browser's Addons manager or the Java JRE control panel.
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
{{See_Also_Section
|Manual_links=[http://java.com Download Java JRE from java.com]
[http://javatester.org JavaTester.org ]
[http://javatester.org/version.html Test the version of Java JRE your browser is using]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NavigatorPlugins.javaEnabled javaEnabled Method]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536610(v=vs.85).aspx javaEnabled Method]
|HTML5Rocks_link=
}}