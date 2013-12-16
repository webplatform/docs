{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the port number associated with a URL.}}
{{API_Object_Property
|Property_applies_to=dom/Location
|Read_only=No
|Example_object_name=location
|Return_value_name=port
|Javascript_data_type=String
|Return_value_description=The port of the URL.
|Example_value_name=port
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example function returns the '''port''' property of two [[html/elements/a|'''a''']] elements.
|Code=&lt;script&gt;
function getPort()
{
    console.log("FTP: " + document.getElementById("ftp").port + "\n" + "HTTP: " + document.getElementById("http").port);
}
&lt;/script&gt;

&lt;a href{{=}}"ftp://www.microsoft.com" onclick{{=}}"getPort();" id{{=}}"ftp"&gt;ftp&lt;/a&gt;
&lt;a href{{=}}"http://www.microsoft.com" onclick{{=}}"getPort();" id{{=}}"http"&gt;http&lt;/a&gt;
}}
}}
{{Notes_Section
|Notes=The port will resolve based on the default port for the protocol set in the HREF attribute:  <code>21</code> for FTP, <code>80</code> for HTTP, and so forth.
Proprietary protocols that do not require a port return <code>0</code> or an empty string.
[[dom/location|'''location''']].'''port''' returns an empty string when read in a page reached by the http protocol.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>[[html/elements/area|area]]</code>
*<code>[[dom/location|location]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}