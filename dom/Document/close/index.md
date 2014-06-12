{{Page_Title}}
{{Flags
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Closes an output stream and forces the sent data to display.}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/Document
|Example_object_name=document
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=//open a new window (or tab), open a new document in it,
//write to the document, and close the document (but not the window)
function newWinDoc() {
    var win=window.open();
    win.document.open();
    win.document.write("<h1>Hello, world</h1>");
    win.document.close();
}
}}
}}
{{Notes_Section
|Notes=When a function fired by an event on any object calls the 
[[dom/Window/close|'''close''']] method, the '''window.close''' method is implied.
When an event on any 
object calls the [[dom/Document/close|'''close''']] method, the 
'''document.close''' method is implied.

When [[dom/Document/write|'''document.write''']] or [[dom/Document/writeln|'''document.writeln''']] is used in an event handler, '''document.close''' should also be used.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 HTML
|URL=http://www.w3org/TR/DOM-Level-2-HTML/
|Status=Recommendation
|Relevant_changes=Section 1.5
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/Document/open|open]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}