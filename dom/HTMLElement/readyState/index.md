{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=
}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
An object's state is initially set to '''uninitialized''', and then to '''loading'''. When data loading is complete, the state of the link object passes through the '''loaded''' and '''interactive''' states to reach the '''complete''' state.
The states through which an object passes are determined by that object; an object can skip certain states (for example, '''interactive''') if the state does not apply to that object.
Data source objects and databound elements are normally populated asynchronously, and certain programmatic operations can only be performed reliably on databound objects when they are ready for use. Therefore, the appropriate code should be written to confirm the '''readyState''' of objects prior to performing certain operations on them. For example, walking the rows of a [[html/elements/table|'''table''']] should not be attempted until after the '''table''' has reached the '''complete''' state.
The '''readyState''' property enables the status of an object to be tested. The correct place to test the '''readyState''' property is in the event handler for [[dom/events/readystatechange|'''onreadystatechange''']]. Similarly, a data source object (DSO) fires the [[dom/events/datasetcomplete|'''ondatasetcomplete''']] event to notify the document that the dataset is ready for programmatic operation.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/Document|Document]]</code>
*<code>frame</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>link</code>
*<code>script</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>tr</code>
*<code>[[dom/events/readystatechange|onreadystatechange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}