{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The current history entry's state object (if any).}}
{{API_Object_Property
|Property_applies_to=dom/PopStateEvent
|Read_only=Yes
|Return_value_description=Represents the context information for the event, or null, if the state represented is the initial state of the document.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=window.onpopstate {{=}} function(event) {
  alert("location: " + document.location + ", state: " + JSON.stringify(event.state));
};
}}
}}
{{Notes_Section
|Notes====Remarks===
Represents the context information for the event, or '''null''', if the state represented is the initial state of the document.
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
*<code>[[dom/objects/PopStateEvent|PopStateEvent]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh772351(v=vs.85).aspx state Property]
|HTML5Rocks_link=
}}