{{Page Title}}
{{Flags
|State=In Progress
|Editorial notes=needs summary, clean-up of MSDN import
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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''selectedIndex''' property to retrieve individual values from a '''select''' object. When a site is selected from the list, the browser displays the associated page.
|LiveURL=
|Code=
&lt;SELECT onchange{{=}}"window.location.href{{=}}this.options
    [this.selectedIndex].value"&gt;
&lt;OPTION VALUE{{=}}"http://www.microsoft.com/ie"&gt;
    Internet Explorer&lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}"http://www.microsoft.com"&gt;
    Microsoft Home&lt;/OPTION&gt;
&lt;OPTION VALUE{{=}}"http://msdn.microsoft.com"&gt;
    Developer Network&lt;/OPTION&gt;
&lt;/SELECT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Options in a '''select''' object are indexed in the order in which they are defined, starting with an index of 0. When you set the '''selectedIndex''' property, the display of the '''select''' object updates immediately.
The '''selectedIndex''' property returns -1 if a '''select''' object does not contain any selected items. Setting the selectedIndex property clears any existing selected items.
The '''selectedIndex''' property is most useful when used with '''select''' objects that support selecting only one item at a time—that is, those in which the [[html/attributes/multiple|'''MULTIPLE''']] attribute is not specified. If the '''MULTIPLE''' attribute is specified for a '''select''' object, the '''selectedIndex''' property returns only the index of the first selected item, if any.
The [[html/attributes/selected|'''selected''']] property is most useful when used with '''select''' objects that support selecting more than one item at a time—that is, those in which the [[html/attributes/multiple|'''MULTIPLE''']] attribute is specified. You can use the '''selected''' property to determine whether an individual item in a '''select''' object is selected. In addition, selected items are not cleared when the '''selected''' property is set. This allows multiple items in the list to be selected at the same time.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>select</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}