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
The '''indeterminate''' property can be used to indicate whether the user has acted on a control. For example, setting the '''indeterminate''' to '''true''' causes the check box to appear checked and dimmed, indicating an indeterminate state.
The value of the '''indeterminate''' property acts independently of the values of the [[html/attributes/checked|'''checked''']] and [[dom/properties/status|'''status''']] properties. Creating an indeterminate state is different from disabling the control. Consequently, a check box in the indeterminate state can still receive the focus. When the user clicks an indeterminate control, the indeterminate state turns off and the checked state of the check box toggles.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>input type{{=}}checkbox</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}