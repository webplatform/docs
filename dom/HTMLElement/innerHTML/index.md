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
|Description=This example uses the '''innerHTML''' property to change the text of a paragraph when an [[dom/MouseEvent/mouseover|'''onmouseover''']] event occurs. The affected text and any tags within it are changed by the '''onmouseover''' and [[dom/MouseEvent/mouseout|'''onmouseout''']] events.
|Code=...
&lt;P onmouseover{{=}}"this.innerHTML{{=}}'&lt;B&gt;Mouse out to change back.&lt;/B&gt;'"
    onmouseout{{=}}"this.innerHTML{{=}}'&lt;I&gt;Mouse over again to change.&lt;/I&gt;'"&gt;
    &lt;I&gt;Mouse over this text to change it.&lt;/I&gt;
&lt;/P&gt;
...
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerHTML.htm
}}{{Single Example
|Description=This example uses the '''innerHTML''' property to insert script into the page.
|Code=&lt;HTML&gt;
&lt;SCRIPT&gt;
function insertScript(){
    var sHTML{{=}}"&lt;input type{{=}}button onclick{{=}}" + "go2()" + " value{{=}}'Click Me'&gt;&lt;BR&gt;";
    var sScript{{=}}"&lt;SCRIPT DEFER&gt;";
    sScript {{=}} sScript + "function go2(){ alert('Hello from inserted script.') }";
    sScript {{=}} sScript + "&lt;/SCRIPT" + "&gt;";
    ScriptDiv.innerHTML {{=}} sHTML + sScript;
}    
&lt;/SCRIPT&gt;
&lt;BODY onload{{=}}"insertScript();"&gt;
    &lt;DIV ID{{=}}"ScriptDiv"&gt;&lt;/DIV&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/insertScript_2.htm
}}{{Single Example
|Description=The following example demonstrates how to convert the HTML source to text using a temporary '''div''' element and [[dom/Document/createTextNode|'''createTextNode''']]. Once the HTML is sanitized, it can be safely inserted into the document using '''innerHTML'''.
|Code=&lt;body onload{{=}}"displaySource()"&gt;

&lt;script type{{=}}"text/javascript"&gt;
function sanitizeHTML(s) {
    var d {{=}} document.createElement('div');
    d.appendChild(document.createTextNode(s));
    return d.innerHTML;
}

function displaySource()
{
    var h {{=}} sanitizeHTML(document.documentElement.outerHTML);
    document.getElementById('asHTML').innerHTML {{=}} "&lt;pre&gt;" + h + "&lt;/pre&gt;";
    document.getElementById('asText').innerText {{=}} h;
}
&lt;/script&gt;

&lt;h2&gt;As HTML&lt;/h2&gt;
&lt;div id{{=}}"asHTML"&gt;&lt;/div&gt;
&lt;h2&gt;As Text&lt;/h2&gt;
&lt;div id{{=}}"asText"&gt;&lt;/div&gt;

&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/innerHTMLsafe.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The '''innerHTML''' property is valid for both block and inline elements. By definition, elements that do not have both an opening and closing tag cannot have an '''innerHTML''' property.
The '''innerHTML''' property takes a string that specifies a valid combination of text and elements. When the '''innerHTML''' property is set, the given string completely replaces the existing content of the object. If the string contains HTML tags, the string is parsed and formatted as it is placed into the document.
This property is accessible at run time as the document is being parsed; however, removing elements at run time, before the document is fully loaded, could prevent other areas of the document from rendering.
When using '''innerHTML''' to insert script, you must include the [[html/attributes/defer|'''DEFER''']] attribute in the '''script''' element.
The '''innerHTML''' property is read-only on the '''col''', '''colGroup''', '''frameSet''', '''html''', '''head''', '''style''', [[html/elements/table|'''table''']], '''tBody''', '''tFoot''', '''tHead''', '''title''', and '''tr''' objects.
You can change the value of the '''title''' element using the [[dom/Document|'''Document''']].title property.
To change the contents of the [[html/elements/table|'''table''']], '''tFoot''', '''tHead''', and '''tr''' elements, use the table object model described in Building Tables Dynamically. However, to change the content of a particular cell, you can use '''innerHTML'''.

'''Security Warning:  ''' Improper handling of the '''innerHTML''' property can enable script-injection attacks. When accepting text from an untrusted source (such as the query string of a URL), use [[dom/Document/createTextNode|'''createTextNode''']] to convert the HTML to text, and append the element to the document using [[dom/Node/appendChild|'''appendChild''']]. Refer to the Examples section below for more information.
To maintain compatibility with earlier versions of Windows Internet Explorer, this property applies to the '''textArea''' object.  However, the property works only with strings that do not contain tags. With a string that contains a tag, this property returns an error. It is better to use the [[dom/HTMLElement/innerText|'''innerText''']] property with this object.
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