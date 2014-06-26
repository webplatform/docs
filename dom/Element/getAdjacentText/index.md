{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs spec and compat table
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Non standard. Gets a text from a given location around the edges of the element.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
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