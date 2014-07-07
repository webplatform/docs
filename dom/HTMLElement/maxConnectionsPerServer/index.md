{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=summary, examples, general clean-up of MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
The maximum number of connections per server returned by the '''maxConnectionsPerServer''' property is determined by the HTTP version (1.0 or 1.1) used by the server. This number applies to any Web server connection, not just to downloads.
The '''maxConnectionsPerServer''' attribute will return <code>6</code> on a broadband connection unless a user or an administrator has overridden the default settings. If the  client computer is connected through dial-up, '''maxConnectionsPerServer''' will return <code>2</code> if connected to an HTTP 1.1 server or <code>4</code> if connected to an HTTP 1.0 server.
To learn how to change the connection limits from their default values, see Connectivity Enhancements in Internet Explorer 8.
|Import_Notes====Syntax===
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
*<code>window</code>
*<code>Connectivity Enhancements in Internet Explorer 8</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}