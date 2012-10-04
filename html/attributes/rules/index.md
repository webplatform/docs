{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example initially sets the '''RULES''' attribute on the table, and then uses the '''rules''' property to dynamically change the table borders.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/rules.htm
|Code=
&lt;TABLE ID{{=}}"oID_1" RULES{{=}}"cols"&gt;
&lt;THEAD&gt;
&lt;TR&gt;
&lt;TD&gt;EST&lt;/TD&gt;&lt;TD&gt;1am&lt;/TD&gt;&lt;TD&gt;8pm&lt;/TD&gt;
&lt;/TR&gt;
&lt;/THEAD&gt;
&lt;TR&gt;
&lt;TD&gt;CST&lt;/TD&gt;&lt;TD&gt;2am&lt;/TD&gt;&lt;TD&gt;9pm&lt;/TD&gt;
&lt;/TR&gt;
&lt;TR&gt;
&lt;TD&gt;MST&lt;/TD&gt;&lt;TD&gt;3am&lt;/TD&gt;&lt;TD&gt;10pm&lt;/TD&gt;
&lt;/TR&gt;
&lt;TFOOT&gt;
&lt;TR&gt;
&lt;TD&gt;PST&lt;/TD&gt;&lt;TD&gt;4am&lt;/TD&gt;&lt;TD&gt;11pm&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TFOOT&gt;
&lt;/TABLE&gt;
&lt;P&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}''"&gt;No borders&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'none'"&gt;Exterior border&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'all'"&gt;All borders&lt;/BUTTON&gt;&lt;BR&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'cols'"&gt;Column borders&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'groups'"&gt;Groups borders&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'rows'"&gt;Table row borders&lt;/BUTTON&gt;
&lt;/P&gt;
}}
{{Single_Example
|Description=In this example, the table object contains the '''RULES'''  attribute set to <code>cols</code> and the [[css/properties/border|'''border''']] attribute set to an empty string (""). This example demonstrates that if the '''RULES''' attribute is set to an empty string (""), the '''border''' attribute will cause the table to show all borders, trumping the '''RULES''' attribute.
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/table_rules_border.htm
|Code=
&lt;TABLE ID{{=}}"oID_1" BORDER{{=}}"" RULES{{=}}"cols"&gt;
&lt;THEAD&gt;
&lt;TR&gt;
&lt;TD&gt;EST&lt;/TD&gt;&lt;TD&gt;1am&lt;/TD&gt;&lt;TD&gt;8pm&lt;/TD&gt;
&lt;/TR&gt;
&lt;/THEAD&gt;
&lt;TR&gt;
&lt;TD&gt;CST&lt;/TD&gt;&lt;TD&gt;2am&lt;/TD&gt;&lt;TD&gt;9pm&lt;/TD&gt;
&lt;/TR&gt;
&lt;TR&gt;
&lt;TD&gt;MST&lt;/TD&gt;&lt;TD&gt;3am&lt;/TD&gt;&lt;TD&gt;10pm&lt;/TD&gt;
&lt;/TR&gt;
&lt;TFOOT&gt;
&lt;TR&gt;
&lt;TD&gt;PST&lt;/TD&gt;&lt;TD&gt;4am&lt;/TD&gt;&lt;TD&gt;11pm&lt;/TD&gt;
&lt;/TR&gt;
&lt;/TFOOT&gt;
&lt;/TABLE&gt;
&lt;P&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}''"&gt;No borders&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'none'"&gt;Exterior border&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'all'"&gt;All borders&lt;/BUTTON&gt;&lt;BR&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'cols'"&gt;Column borders&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'groups'"&gt;Groups borders&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oID_1.rules{{=}}'rows'"&gt;Table row borders&lt;/BUTTON&gt;
&lt;/P&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The value '''none''' turns off only the interior borders. To turn off the table borders, set the '''rules''' property to <code>''</code>, or omit the '''RULES''' attribute from the [[html/elements/table|'''table''']] object.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[html/elements/table|table]]</code>
*<code>[[html/attributes/frame|frame]]</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}