{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=dom/Navigator
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
|Description=This example shows how to determine whether the '''userAgent''' of the browser contains "MSIE". If it does, the browser is Internet Explorer.
|Code=if (window.clientInformation.userAgent.indexOf( "MSIE " ) &gt; 0) {
    // The browser is Microsoft Internet Explorer.
}
}}
}}
{{Notes_Section}}
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