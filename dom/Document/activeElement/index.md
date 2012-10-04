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
You can set the active element with the [[dom/methods/setActive|'''setActive''']] method or
the [[dom/methods/focus|'''focus''']] method; however, using the '''setActive''' method has no effect on document focus. Use the '''focus''' method to cause an individual element to gain focus and become the active element.
The active element retains focus in the parent [[dom/document|'''document''']] even when focus is shifted from the parent to another application. If the focus returns to the parent '''document''', focus also returns to the same active element.

'''Note'''  For versions of Microsoft Internet Explorer 5 and later, the '''activeElement''' property is not defined until a document is loaded. A value of null is given for this property, if it is accessed inline during the loading of a document. This property can be accessed in the [[dom/events/load|'''onload''']] event handler function.

'''Note'''  Microsoft Internet Explorer 4.0 returns  '''body''' as the '''activeElement''' when it is accessed inline during the loading of a document.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}