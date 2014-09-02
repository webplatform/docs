{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|A collection of the document's stylesheets.}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example shows how to display the titles of the style sheets in the document.
|Code=for ( i {{=}} 0; i &lt; document.styleSheets.length; i++ )
{
    alert("Style sheet " + i + " is titled " + document.styleSheets(i).title);
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Style sheets that are imported using the [[css/atrules/@import|'''@import''']] rule and are contained within the '''style''' object are available through the [[css/cssom/imports|'''imports''']] collection.
|Import_Notes=
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
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}