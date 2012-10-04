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
The property can be changed programmatically, but doing so has no effect on the appearance of the check box or radio button or on how forms are submitted.
Windows Internet Explorer 8 and later. In IE8 Standards mode, the '''defaultChecked''' Document Object Model (DOM) attribute reflects the value of the [[html/attributes/checked|'''checked''']] content attribute. For more information, see Attribute Differences in Internet Explorer 8.
Internet Explorer 8 and later. In IE8 mode, parsing operations on the [[html/attributes/checked|'''checked''']] content attribute always affect both the '''checked''' content attribute and '''defaultChecked''' DOM attribute. For example, [[dom/methods/removeAttribute|'''removeAttribute('checked')''']] sets both '''checked''' and '''defaultChecked''' to false. Similarly, [[dom/methods/setAttribute|'''setAttribute('checked', 'checked')''']] sets both DOM attributes to true (as if the element was being re-parsed).
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}radio</code>
*<code>[[html/attributes/checked|checked]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}