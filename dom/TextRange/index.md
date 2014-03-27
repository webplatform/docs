{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example changes the text of a '''button''' element to "Clicked" through the '''TextRange''' object.
|Code=&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
var b {{=}} document.all.tags("BUTTON");
if (b!{{=}}null) {
    var r {{=}} b[0].createTextRange();
    if (r !{{=}} null) {
        r.text {{=}} "Clicked";
    }
}
&lt;/SCRIPT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Use this object to retrieve and modify text in an element, to locate specific strings in the text, and to carry out commands that affect the appearance of the text.
To retrieve a text range object, apply the [[dom/Document/createRange|'''createRange''']] method to a '''body''', '''button''', or '''textArea''' element or an '''input''' element that has [[html/attributes/type|'''TYPE''']] text.
Modify the extent of the text range by moving its start and end positions with methods such as [[dom/TextRange/move|'''move''']] and [[dom/TextRange/moveToElementText|'''moveToElementText''']]. Within the text range, you can retrieve and modify plain text or HTML text. These forms of text are identical except that HTML text includes HTML tags, and plain text does not.
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