{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, clean-up of MSDN import
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
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
An object's state is initially set to '''uninitialized''', and then to '''loading'''. When data loading is complete, the state of the link object passes through the '''loaded''' and '''interactive''' states to reach the '''complete''' state.
The states through which an object passes are determined by that object; an object can skip certain states (for example, '''interactive''') if the state does not apply to that object.
Data source objects and databound elements are normally populated asynchronously, and certain programmatic operations can only be performed reliably on databound objects when they are ready for use. Therefore, the appropriate code should be written to confirm the '''readyState''' of objects prior to performing certain operations on them. For example, walking the rows of a [[html/elements/table|'''table''']] should not be attempted until after the '''table''' has reached the '''complete''' state.
The '''readyState''' property enables the status of an object to be tested. The correct place to test the '''readyState''' property is in the event handler for [[dom/Element/readystatechange|'''onreadystatechange''']]. Similarly, a data source object (DSO) fires the [[dom/Event/datasetcomplete|'''ondatasetcomplete''']] event to notify the document that the dataset is ready for programmatic operation.
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}