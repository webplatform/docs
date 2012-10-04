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
|Description=The following example shows how to use the '''compact''' property in HTML. Note that the presence of the word '''COMPACT''' sets the '''compact''' property to '''true'''
|LiveURL=
|Code=

&lt;HTML&gt;
&lt;BODY&gt;
&lt;DL COMPACT&gt;
&lt;DT&gt;Cat
&lt;DD&gt;A small domesticated mammal.
&lt;DT&gt;Lizard
&lt;DD&gt;A reptile generally found in dry areas.
&lt;/DL&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;

}}
{{Single_Example
|Description=The following example shows how to set the '''compact''' property using JScript
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/compact.htm
|Code=

&lt;HTML&gt;
&lt;BODY&gt;
&lt;script&gt;
//Function that toggles the compact property for the DL element below
function compactDLToggle()
{
animals.compact {{=}} !animals.compact;
toggle.innerText {{=}} "Compact {{=}} "+animals.compact;
}
&lt;/script&gt;
&lt;P style{{=}}"color:blue; font-weight:bold"&gt;Effect of setting COMPACT property for a DL element&lt;/P&gt;
&lt;BUTTON id{{=}}"toggle" onclick{{=}}"compactDLToggle()"&gt;Toggle Compact Property&lt;/BUTTON&gt;
&lt;DL id{{=}}animals&gt;
&lt;DT&gt;Cat
&lt;DD&gt;A small domesticated mammal.
&lt;DT&gt;Lizard
&lt;DD&gt;A reptile generally found in dry areas.
&lt;/DL&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;

}}}}
{{Notes_Section
|Notes=
===Remarks===
There is no functionality implemented for the '''compact''' property  for the '''ul''', '''ol''', '''dir''' and  '''menu''' elements unless defined by the author.
In Microsoft Internet Explorer 6 and greater, this property applies to the '''menu'''  and '''dir''' objects.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 10.2 (Deprecated)


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>menu</code>
*<code>dir</code>
*<code>dl</code>
*<code>ul</code>
*<code>ol</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}