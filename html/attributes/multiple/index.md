{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|When present, it specifies that the user is allowed to enter more than one value in the <input> element.}}
{{Markup_Attribute
|Applies_to=http://docs.webplatform.org/wiki/html/elements/input
|Property_applies_to=dom/HTMLElement
|Content=The multiple attribute is a boolean attribute.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''MULTIPLE''' attribute and the '''multiple''' property to switch between allowing the user to select one item or multiple items from a list.
|Code=&lt;SELECT ID{{=}}oSelect MULTIPLE&gt;
&lt;OPTION&gt;Item 1&lt;/OPTION&gt;
&lt;OPTION&gt;Item 2&lt;/OPTION&gt;
&lt;OPTION&gt;Item 3&lt;/OPTION&gt;
&lt;/SELECT&gt;
:
&lt;BUTTON onclick{{=}}"oSelect.multiple{{=}}false"&gt;One&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oSelect.multiple{{=}}true"&gt;Many&lt;/BUTTON&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/multiple.htm
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.6
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
*<code>select</code>
*<code>[[html/attributes/type (select element)|type]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}