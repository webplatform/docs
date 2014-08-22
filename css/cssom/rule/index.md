{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Summary needed, double check correct printing of tokens, needs spec reference, standardization status
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses a '''rule''' object consisting of the selector '''H1''' to define a single rule that changes the H1 headings in a document to red.
|Code=&lt;STYLE&gt;
    H1 { color: red }
&lt;/STYLE&gt;
}}{{Single Example
|Language=JavaScript
|Description=If the style sheet containing the preceding rule is the first style sheet in the document, the following code returns the '''rule''' object associated with the rule.
|Code=oRule{{=}}document.styleSheets(0).rules(0)
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''rule''' object defines a set of Cascading Style Sheets (CSS) attributes applied to a set of HTML elements. For example, a rule consisting of the selector '''H1''' and the declaration [[css/properties/font-family|'''font-family''']]:Arial defines all '''H1''' elements to render in the Arial font.
This object is available in script as of Microsoft Internet Explorer 5.
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
|Topic_clusters=CSSOM
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/rules|rules]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}