{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Return values for Android, iOS and blackberry operating systems from browsers hosted on non-wintel OS.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name|DOM Navigator Platform}}
{{Summary_Section|Retrieves the name of the user's operating system.

In IE10 and higher and WaterFox browsers this will return the bitness of the current tab. eg

Win32 or Win64.
}}
{{API_Object_Property
|Property_applies_to=dom/Navigator
|Read_only=Yes
|Example_object_name=navigator
|Return_value_name=returnValue
|Javascript_data_type=String
|Return_value_description=
HP-UX

HP UNIX-based computers.

MacPPC

Macintosh PowerPC-based computers.

Mac68K

Macintosh 68K-based computers.

SunOS

Solaris-based computers.

Win64

Windows 64-bit platform.

Win32

Windows 32-bit platform.

Win16

Windows 16-bit platform.

WinCE

Windows CE platform.

}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Usage=Could be used to feature test for support for x86 plugins or ActiveX controls.

To determine what bitness a web page is being rendered with, and subsequently the required bitness of any ActiveX controls it may be hosting type
javascript:alert(navigator.platform);
in the browser's Address bar.
|Import_Notes====Syntax===
var platform = navigator.platform 
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Navigator Platform
|URL=http://www.w3.org/TR/html5/webappapis.html#dom-navigator-platform
|Status=Draft
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
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/NavigatorID.platform navigator.platform]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms534340(v=vs.85).aspx navigator.platform]
|HTML5Rocks_link=
}}