{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/Element
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows how to determine whether the client can run Java applets.
|LiveURL=
|Code=
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
if (window.clientInformation.javaEnabled() {{=}}{{=}} true )
    // Java is enabled; applets can run.
&lt;/SCRIPT&gt;
}}
{{Single_Example
|Description=This example shows how to determine whether the [[dom/properties/userAgent|'''userAgent''']] of the browser contains "MSIE". If it does, the browser is Internet Explorer.
|LiveURL=
|Code=
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
if (window.clientInformation.userAgent.indexOf( "MSIE " ) &gt; 0)
    // The browser is Microsoft Internet Explorer.
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Standards information===
There are no standards that apply here.

===Members===
The '''clientInformation''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''clientInformation''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/javaEnabled|'''javaEnabled''']]
|Returns whether Java is enabled.
|-
|[[dom/methods/taintEnabled|'''taintEnabled''']]
|Returns whether data tainting is enabled.
|}
 

====Properties====
The '''clientInformation''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/appCodeName|'''appCodeName''']]
|Retrieves the code name.

This method is not supported for Metro style apps using JavaScript.
|-
|[[dom/properties/appMinorVersion|'''appMinorVersion''']]
|Retrieves the application's minor version value.
|-
|[[dom/properties/appName|'''appName''']]
|Retrieves the name of the client.
|-
|[[dom/properties/appVersion|'''appVersion''']]
|Retrieves the platform and version of the application.
|-
|[[dom/properties/browserLanguage|'''browserLanguage''']]
|Retrieves the current operating system language. 

'''Note'''  This property does not indicate the language or languages set by the user in Language Preferences, located in the '''Internet Options''' dialog box.
|-
|[[dom/properties/cookieEnabled|'''cookieEnabled''']]
|Retrieves whether client-side persistent cookies are enabled.  Persistent cookies are those that are stored on the client-side computer.
|-
|[[dom/properties/cpuClass|'''cpuClass''']]
|Retrieves a string denoting the CPU class.
|-
|[[dom/properties/onLine|'''onLine''']]
|Retrieves a value indicating whether the system is online.
|-
|[[dom/properties/platform|'''platform''']]
|Retrieves the name of the user's operating system.
|-
|[[dom/properties/systemLanguage|'''systemLanguage''']]
|Retrieves the default language used by the operating system. 



This property is not supported for Metro style apps using JavaScript.
Use '''Windows.System.UserProfile.GlobalizationPreferences.languages''' to get the user's language list and '''Windows.Globalization.ApplicationLanguages.languages''' to get the app's current language.
|-
|[[dom/properties/userAgent|'''userAgent''']]
|Retrieves a string equivalent to the HTTP user-agent request header.
|-
|[[dom/properties/userLanguage|'''userLanguage''']]
|Retrieves the operating system's natural language setting.


This property is not supported for Metro style apps using JavaScript.
Use '''Windows.System.UserProfile.GlobalizationPreferences.languages''' to get the user's language list and '''Windows.Globalization.ApplicationLanguages.languages''' to get the app's current language.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}