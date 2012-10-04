{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Property
|Property_applies_to=dom/location
|Read_only=
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example shows a URL list. The user is taken to the URL selected from the options, if the selection is different from the list's default value.
|LiveURL=
|Code=
&lt;SELECT onchange{{=}}"window.location.href{{=}}this.options[this.selectedIndex].value"&gt;
&lt;OPTION VALUE{{=}}"http://www.microsoft.com/ie"&gt;Internet Explorer&lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}"http://www.microsoft.com"&gt;Microsoft Home&lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}"http://msdn.microsoft.com"&gt;Developer Network&lt;/OPTION&gt;
&lt;/SELECT&gt;
}}}}
{{Notes_Section
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/location|location]]</code>
*<code>[[dom/methods/navigate|navigate]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}