{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example with getSelection feature testing.
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Pastes HTML text into the given text range, replacing any previous text and HTML elements in the range.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=html
|Data type=String
|Description='''String''' that specifies the HTML text to paste. The string can contain text and any combination of the HTML tags described in HTML Elements.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=range
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=This example uses the '''pasteHTML''' method to replace the current selection with a new paragraph.
|Code=&lt;script type{{=}}"text/javascript"&gt;
if(window.getSelection){
// use standards instead
}else{
var sel {{=}} document.selection;
if (sel!{{=}}null) {
    var rng {{=}} sel.createRange();
    if (rng!{{=}}null)
        rng.pasteHTML("&lt;P&gt;&lt;B&gt;Selection has been replaced.&lt;/B&gt;&lt;/P&gt;");
}
}
&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
This method might alter the HTML text to make it fit the given text range. For example, pasting a table cell into a text range that does not contain a table might cause the method to insert a [[html/elements/table|'''table''']] element. For predictable results, paste only well-formed HTML text that fits within the given text range.
This method is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render.
This feature might not be available on non-Microsoft Win32 platforms.
This method fails only when used inappropriately to paste HTML into a '''TEXTAREA''' element in Microsoft Internet Explorer 5 and later.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536656(v=vs.85).aspx pasteHTML Method]
|HTML5Rocks_link=
}}