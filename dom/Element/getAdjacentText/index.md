{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Non standard. Gets a text from a given location around the edges of the element.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=where
|Data type=String
|Description=Where the text is located by using one of the following values.


'''beforeBegin'''

Text is returned immediately before the element.


'''afterBegin'''

Text is returned after the start of the element but before all other content in the element.


'''beforeEnd'''

Text is returned immediately before the end of the element but after all other content in the element.

'''afterEnd'''

Text is returned immediately after the end of the element.
|Optional=No
}}
|Method_applies_to=dom/Element
|Example_object_name=element
|Return_value_name=text
|Javascript_data_type=String
|Return_value_description=The first adjacent text.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''getAdjacentText''' method to find specific text.
|Code=&lt;script&gt;
function findText(){
        var select = document.getElementById("sel");
	var whereToFind {{=}} select.options[select.selectedIndex].textContent;
	console.log(document.getElementById("para").getAdjacentText(whereToFind));
}
&lt;/script&gt;
This is the text before (beforeBegin).
&lt;p id{{=}}"para"&gt;
This is the text after (afterBegin).
&lt;b&gt;A few extra words.&lt;/b&gt;
This is the text before (beforeEnd).
&lt;/p&gt;
This is the text after (afterEnd).
&lt;select id{{=}}"sel"&gt;
&lt;option selected="selected"&gt;beforeBegin&lt;/option&gtl
&lt;option&gt;afterBegin&lt;/option&gtl
&lt;option&gt;beforeEnd&lt;/option&gtl
&lt;option&gt;afterEnd&lt;/option&gtl
&lt;/select&gt;
&lt;input type{{=}}"button" value{{=}}"Find text" onclick{{=}}"findText()"&gt;
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[html/elements/a|a]]</code>
*<code>abbr</code>
*<code>[[html/elements/acronym|acronym]]</code>
*<code>address</code>
*<code>applet</code>
*<code>area</code>
*<code>b</code>
*<code>base</code>
*<code>baseFont</code>
*<code>bdo</code>
*<code>big</code>
*<code>blockQuote</code>
*<code>body</code>
*<code>br</code>
*<code>button</code>
*<code>caption</code>
*<code>center</code>
*<code>cite</code>
*<code>code</code>
*<code>col</code>
*<code>colGroup</code>
*<code>comment</code>
*<code>custom</code>
*<code>dd</code>
*<code>del</code>
*<code>dfn</code>
*<code>dir</code>
*<code>div</code>
*<code>dl</code>
*<code>dt</code>
*<code>em</code>
*<code>embed</code>
*<code>fieldSet</code>
*<code>font</code>
*<code>form</code>
*<code>frame</code>
*<code>frameSet</code>
*<code>head</code>
*<code>hn</code>
*<code>hr</code>
*<code>html</code>
*<code>i</code>
*<code>iframe</code>
*<code>img</code>
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>input type{{=}}password</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>input type{{=}}submit</code>
*<code>input type{{=}}text</code>
*<code>ins</code>
*<code>kbd</code>
*<code>label</code>
*<code>legend</code>
*<code>li</code>
*<code>link</code>
*<code>listing</code>
*<code>map</code>
*<code>marquee</code>
*<code>menu</code>
*<code>[[html/elements/nextID|nextID]]</code>
*<code>object</code>
*<code>ol</code>
*<code>option</code>
*<code>p</code>
*<code>plainText</code>
*<code>pre</code>
*<code>q</code>
*<code>s</code>
*<code>samp</code>
*<code>script</code>
*<code>select</code>
*<code>small</code>
*<code>span</code>
*<code>strike</code>
*<code>strong</code>
*<code>sub</code>
*<code>sup</code>
*<code>[[html/elements/table|table]]</code>
*<code>tBody</code>
*<code>td</code>
*<code>textArea</code>
*<code>tFoot</code>
*<code>th</code>
*<code>tHead</code>
*<code>title</code>
*<code>tr</code>
*<code>tt</code>
*<code>u</code>
*<code>ul</code>
*<code>var</code>
*<code>xmp</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}