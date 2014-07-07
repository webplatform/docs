{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=summary, clean-up of MSDN import
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
|Description=This example uses the '''outerHTML''' property to copy an object, accompanying attributes, and children to a list when a user clicks one of the objects.
|Code=&lt;SCRIPT&gt;
function fnCopyHTML(){
   var oWorkItem {{=}} event.srcElement;
   if((oWorkItem.tagName !{{=}} "UL") &amp;&amp; (oWorkItem.tagName !{{=}} "LI")){
      alert("Adding " + oWorkItem.outerHTML + " to the list.");
      oScratch.innerHTML +{{=}} oWorkItem.outerHTML + "&lt;BR&gt;";
   }
}	
&lt;/SCRIPT&gt;

&lt;UL onclick {{=}} "fnCopyHTML()"&gt;
&lt;LI&gt;&lt;B&gt;Bold text&lt;/B&gt;
&lt;LI&gt;&lt;I&gt;Italic text&lt;/I&gt;
&lt;LI&gt;&lt;U&gt;Underlined text&lt;/U&gt;
&lt;LI&gt;&lt;STRIKE&gt;Strikeout text&lt;/STRIKE&gt;
&lt;/UL&gt;
&lt;P&gt;
&lt;DIV ID {{=}} "oScratch" &gt;
&lt;/DIV&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''outerHTML''' property is read-only on the '''caption''', '''col''', '''colGroup''', '''html''', '''head''', '''body''', '''frameSet''', '''tBody''', '''td''', '''tFoot''', '''th''', '''tHead''', and '''tr''' objects.
The property can be any valid string containing a combination of text and tags.
When the property is set, the given string completely replaces the object, including its start and end tags. If the string contains HTML tags, the string is parsed and formatted as it is placed into the document.
You can set this property only after the [[dom/Element/load|'''onload''']] event fires on the '''window'''. When dynamically creating a tag using [[dom/TextRange|'''TextRange''']], [[dom/HTMLElement/innerHTML|'''innerHTML''']], or '''outerHTML''', use script to create new events to handle the newly formed tags. Microsoft Visual Basic Scripting Edition (VBScript) is not supported.
You can change the value of the '''title''' element using the [[html/elements/title|'''title''']] property.
To change the contents of the [[html/elements/table|'''table''']], '''tFoot''', '''tHead''', and '''tr''' elements, use the table object model. For example, use the [[dom/HTMLElement/rowIndex|'''rowIndex''']] property or the [[dom/HTMLElement/rows|'''rows''']] collection to retrieve a reference to a specific table row. You can add or delete rows using the [[dom/HTMLTableElement/insertRow|'''insertRow''']] and [[dom/HTMLTableElement/deleteRow|'''deleteRow''']] methods. To retrieve a reference to a specific cell, use the [[dom/HTMLElement/cellIndex|'''cellIndex''']] property or the [[dom/HTMLTableElement/cellSpacing|'''cells''']] collection. You can add or delete rows using the [[dom/HTMLTableElement/insertCell|'''insertCell''']] and [[dom/HTMLTableElement/deleteCell|'''deleteCell''']] methods. To change the content of a particular cell, use the [[dom/HTMLElement/innerHTML|'''innerHTML''']] property.
This property is accessible at run time as of Microsoft Internet Explorer 5. Removing elements at run time, before the closing tag has been parsed, can prevent other areas of the document from rendering.
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