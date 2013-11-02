{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Content=Examples Needed
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The '''multiple''' attribute indicates that the user is allowed to enter more than one value in an <input> element.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input|HTMLInputElement]]
|Property_applies_to=dom/HTMLElement
|Content=This attribute can be <code>true</code> or <code>false</code>.
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
{{See_Also_Section
|Topic_clusters=HTML
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}