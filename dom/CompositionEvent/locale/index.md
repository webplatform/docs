{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs spec reference
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|Gets the locale name (language code, e.g., "en-US", "fr", "de", "ja", etc.) for the composition event, if available; otherwise, the empty string.}}
{{API_Object_Property
|Property_applies_to=dom/CompositionEvent
|Read_only=Yes
|Example_object_name=event
|Return_value_name=localeName
|Javascript_data_type=String
|Return_value_description=The locale of the event.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=function getLocale(e) {
//retrieve locale string for composition event
var localeString = e.locale;
return localeString;
}
}}
}}
{{Notes_Section
|Notes=For trusted events, the '''locale''' property is set for keyboard and Input Method Editor (IME) input only. The locale name is set from the default LCID of the thread, <code>en-US</code>, for example.
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
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/KeyboardEvent|KeyboardEvent]]</code>
*<code>[[dom/TextEvent|TextEvent]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}