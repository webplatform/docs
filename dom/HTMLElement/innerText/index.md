{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, compatibility, clean-up of MSDN section headers/rearrange content to use WPD sections
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
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
|Description=This example uses the '''innerText''' property to replace an object's contents. The object surrounding the text is not replaced.
|Code=&lt;P ID{{=}}oPara&gt;Here's the text that will change.&lt;/P&gt;
:
&lt;BUTTON onclick{{=}}"oPara.innerText{{=}}'WOW! It changed!'"&gt;Change text&lt;/BUTTON&gt;
&lt;BUTTON onclick{{=}}"oPara.innerText{{=}}'And back again'"&gt;Reset&lt;/BUTTON&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerText.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''innerText''' property is valid for block elements only. By definition, elements that do not have both an opening and closing tag cannot have an '''innerText''' property.
The '''innerText''' property is read-only on the '''html''', [[html/elements/table|'''table''']], '''tBody''', '''tFoot''', '''tHead''', and '''tr''' objects.
When the '''innerText''' property is set, the given string completely replaces the existing content of the object.
You can set this property only after the [[dom/Element/load|'''onload''']] event fires on the '''window'''. When dynamically creating a tag using [[dom/TextRange|'''TextRange''']], [[dom/HTMLElement/innerHTML|'''innerHTML''']], or [[dom/HTMLElement/outerHTML|'''outerHTML''']], use scripting to create new events to handle the newly formed tags. Microsoft Visual Basic Scripting Edition (VBScript) is not supported.
You can change the value of the '''title''' element using the [[html/elements/title|'''title''']] property.
To change the contents of the [[html/elements/table|'''table''']], '''tFoot''', '''tHead''', and '''tr''' elements, use the table object model. For example, use the [[dom/HTMLElement/rowIndex|'''rowIndex''']] property or the [[dom/HTMLElement/rows|'''rows''']] collection to retrieve a reference to a specific table row. You can add or delete rows using the [[dom/HTMLTableElement/insertRow|'''insertRow''']] and [[dom/HTMLTableElement/deleteRow|'''deleteRow''']] methods. To retrieve a reference to a specific cell, use the [[dom/HTMLElement/cellIndex|'''cellIndex''']] property or the [[html/attributes/cells|'''cells''']] collection. You can add or delete rows using the [[dom/HTMLTableElement/insertCell|'''insertCell''']] and [[dom/HTMLTableElement/deleteCell|'''deleteCell''']] methods. To change the content of a particular cell, use the [[dom/HTMLElement/innerHTML|'''innerHTML''']] property.
'''Security Warning:  ''' The '''innerText''' property can be used to safely add dynamic text to a webpage if the target element type is not a <code>script</code> element. With the exception of the <code>script</code> element, '''innerText''' does not execute script when inserting text into the Document Object Model (DOM) of a webpage.
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