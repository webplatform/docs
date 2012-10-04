{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/location
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example function returns the '''port''' property of two [[html/elements/a|'''a''']] elements.
|LiveURL=
|Code=
&lt;SCRIPT&gt;
function getPort()
{
    alert ("FTP: " + oFtp.port + "\n" + "HTTP: " + oHttp.port);
}
&lt;/SCRIPT&gt;

&lt;A HREF{{=}}"ftp://www.microsoft.com" onclick{{=}}"getPort();" ID{{=}}oFtp&gt;ftp&lt;/A&gt;
&lt;A HREF{{=}}"http://www.microsoft.com" onclick{{=}}"getPort();" ID{{=}}oHttp&gt;http&lt;/A&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The port will resolve based on the default port for the protocol set in the HREF attribute:  <code>21</code> for FTP, <code>80</code> for HTTP, and so forth.
Proprietary protocols that do not require a port return <code>0</code> or an empty string.
[[dom/location|'''location''']].'''port''' returns an empty string when read in a page reached by the http protocol.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>area</code>
*<code>[[dom/location|location]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}