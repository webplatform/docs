{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Represents text in an HTML element.}}
{{API_Object}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example changes the text of a '''button''' element to "Clicked" through the '''TextRange''' object.
|Code=&lt;script type{{=}}"text/javascript"&gt;
var b {{=}} document.all.tags("button");
if (b!{{=}}null) {
    var r {{=}} b[0].createTextRange();
    if (r !{{=}} null) {
        r.text {{=}} "Clicked";
    }
}
&lt;/script&gt;
}}
}}
{{Notes_Section
|Usage=Use this object to retrieve and modify text in an element, to locate specific strings in the text, and to carry out commands that affect the appearance of the text. 
|Notes====Remarks===
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms535872(v=vs.85).aspx TextRange Object]
|HTML5Rocks_link=
}}