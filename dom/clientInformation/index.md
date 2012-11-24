{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/navigator
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example shows how to determine whether the client can run Java applets.
|Code=if (window.clientInformation.javaEnabled()) {
    // Java is enabled; applets can run.
}
}}{{Single Example
|Language=JavaScript
|Description=This example shows how to determine whether the [[dom/properties/userAgent|'''userAgent''']] of the browser contains "MSIE". If it does, the browser is Internet Explorer.
|Code=if (window.clientInformation.userAgent.indexOf( "MSIE " ) &gt; 0) {
    // The browser is Microsoft Internet Explorer.
}
}}
}}
{{Notes_Section
|Import_Notes====Standards information===
There are no standards that apply here.

===Additional Members (MSDN)===
The '''clientInformation''' object has these types of members:
[[#Additional_Methods|Additional Methods]]
[[#Additional_Properties|Additional Properties]]


====Additional Methods====
The '''clientInformation''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[dom/methods/javaEnabled|'''javaEnabled''']]
{{!}}Returns whether Java is enabled.
{{!}}-
{{!}}[[dom/methods/taintEnabled|'''taintEnabled''']]
{{!}}Returns whether data tainting is enabled.
{{!}}}
 

====Additional Properties====
The '''clientInformation''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[dom/properties/appCodeName|'''appCodeName''']]
{{!}}Retrieves the code name.

This method is not supported for Metro style apps using JavaScript.
{{!}}-
{{!}}[[dom/properties/appMinorVersion|'''appMinorVersion''']]
{{!}}Retrieves the application's minor version value.
{{!}}-
{{!}}[[dom/properties/appName|'''appName''']]
{{!}}Retrieves the name of the client.
{{!}}-
{{!}}[[dom/properties/appVersion|'''appVersion''']]
{{!}}Retrieves the platform and version of the application.
{{!}}-
{{!}}[[dom/properties/browserLanguage|'''browserLanguage''']]
{{!}}Retrieves the current operating system language. 

'''Note'''  This property does not indicate the language or languages set by the user in Language Preferences, located in the '''Internet Options''' dialog box.
{{!}}-
{{!}}[[dom/properties/cookieEnabled|'''cookieEnabled''']]
{{!}}Retrieves whether client-side persistent cookies are enabled.  Persistent cookies are those that are stored on the client-side computer.
{{!}}-
{{!}}[[dom/properties/cpuClass|'''cpuClass''']]
{{!}}Retrieves a string denoting the CPU class.
{{!}}-
{{!}}[[dom/properties/onLine|'''onLine''']]
{{!}}Retrieves a value indicating whether the system is online.
{{!}}-
{{!}}[[dom/properties/platform|'''platform''']]
{{!}}Retrieves the name of the user's operating system.
{{!}}-
{{!}}[[dom/properties/systemLanguage|'''systemLanguage''']]
{{!}}Retrieves the default language used by the operating system. 



This property is not supported for Metro style apps using JavaScript.
Use '''Windows.System.UserProfile.GlobalizationPreferences.languages''' to get the user's language list and '''Windows.Globalization.ApplicationLanguages.languages''' to get the app's current language.
{{!}}-
{{!}}[[dom/properties/userAgent|'''userAgent''']]
{{!}}Retrieves a string equivalent to the HTTP user-agent request header.
{{!}}-
{{!}}[[dom/properties/userLanguage|'''userLanguage''']]
{{!}}Retrieves the operating system's natural language setting.


This property is not supported for Metro style apps using JavaScript.
Use '''Windows.System.UserProfile.GlobalizationPreferences.languages''' to get the user's language list and '''Windows.Globalization.ApplicationLanguages.languages''' to get the app's current language.
{{!}}}
 
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