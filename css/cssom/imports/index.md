{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary, spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object
|Subclass_of=
|Overview=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example shows how to display the URL paths of the imported style sheets in the document.
|Code=for ( i {{=}} 0; i &lt; document.styleSheets.length; i++ )
{
    if ( document.styleSheets(i).owningElement.tagName {{=}}{{=}} "STYLE" )
    {
        for ( j {{=}} 0; j &lt; document.styleSheets(i).imports.length; j++ )
            alert("Imported style sheet " + j + " is at " +
                   document.styleSheets(i).imports(j).href);
    }
}
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
An imported style sheet is one that is brought into the document using the cascading style sheets (CSS) [[css/atrules/@import|'''@import''']] rule.
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