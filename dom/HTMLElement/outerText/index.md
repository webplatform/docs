{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Property
|Property_applies_to=dom/HTMLElement
|Read_only=No
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''outerText''' property to replace an object's content; the object itself also is replaced.
|Code=&lt;DIV ID{{=}}oDiv&gt;
&lt;P ID{{=}}oPara&gt;Here's the text that will change.&lt;/P&gt;
&lt;/DIV&gt;
:
&lt;BUTTON onclick{{=}}"oPara.outerText{{=}}'WOW! 
    It changed!'"&gt;Change text&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oDiv.innerHTML{{=}}'&lt;P ID{{=}}oPara&gt;
    And back again&lt;/P&gt;'"&gt;Reset&lt;/BUTTON&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/outerText.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''outerText''' property is read-only on the '''html''', '''tBody''', '''td''', '''tFoot''', '''th''', '''tHead''', and '''tr''' objects.
When this property is set, the given string completely replaces the original text in the object.
You can set this property only after the [[dom/Element/load|'''onload''']] event fires on the '''window'''. When dynamically creating a tag using [[dom/TextRange|'''TextRange''']], [[dom/HTMLElement/innerHTML|'''innerHTML''']], or [[dom/HTMLElement/outerHTML|'''outerHTML''']], use script to create new events to handle the newly formed tags. Microsoft Visual Basic Scripting Edition (VBScript) is not supported.
You can change the value of the '''title''' element using the [[html/elements/title|'''title''']] property.
To change the contents of the [[html/elements/table|'''table''']], '''tFoot''', '''tHead''', and '''tr''' elements, use the table object model. For example, use the [[dom/HTMLElement/rowIndex|'''rowIndex''']] property or the [[dom/HTMLElement/rows|'''rows''']] collection to retrieve a reference to a specific table row. You can add or delete rows using the [[dom/HTMLTableElement/insertRow|'''insertRow''']] and [[dom/HTMLTableElement/deleteRow|'''deleteRow''']] methods. To retrieve a reference to a specific cell, use the [[dom/HTMLElement/cellIndex|'''cellIndex''']] property or the [[dom/HTMLTableElement/cellSpacing|'''cells''']] collection. You can add or delete rows using the [[dom/HTMLTableElement/insertCell|'''insertCell''']] and [[dom/HTMLTableElement/deleteCell|'''deleteCell''']] methods. To change the content of a particular cell, use the [[dom/HTMLElement/innerHTML|'''innerHTML''']] property.
|Import_Notes====Syntax===
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}