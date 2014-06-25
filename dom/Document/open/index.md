{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Needs summary and compat, and better spec links
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=0
|Name=url
|Data type=any
|Optional=No
}}{{Method Parameter
|Index=1
|Name=name
|Data type=BSTR
|Description='''Note'''  The following applies only if this method is used instead of [[dom/Window/open|'''window.open''']].
|Optional=No
}}{{Method Parameter
|Index=2
|Name=features
|Data type=BSTR
|Description='''Note'''  The following applies only if this method is used instead of [[dom/Window/open|'''window.open''']].
|Optional=No
}}{{Method Parameter
|Index=3
|Name=replace
|Data type=any
|Optional=No
}}
|Method_applies_to=dom/Document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

'''document'''
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''open''' method to replace the current document with a new document and display the HTML markup contained in the variable ''sMarkup''.
|Code=&lt;html&gt;
&lt;head&gt;
&lt;title&gt;First Document&lt;/title&gt;
&lt;script&gt;
function replace(){
    var oNewDoc {{=}} document.open("text/html", "replace");
    var sMarkup {{=}} "&lt;html&gt;&lt;head&gt;&lt;title&gt;New Document&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Hello, world&lt;/body&gt;&lt;/html&gt;";
    oNewDoc.write(sMarkup);
    oNewDoc.close();
}
&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;h1&gt;I just want to say&lt;/h1&gt;&lt;br&gt;
&lt;!--Button will call the replace function and replace the current page with a new one--&gt;
&lt;input type {{=}}"button" value {{=}} "Finish Sentence" onclick{{=}}"replace();"&gt;
&lt;/body&gt;
&lt;/html&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
When a function fired by an event on any object calls the
'''open''' method,  the [[dom/Window/open|'''window.open''']] method is implied.
 <code>&lt;script language{{=}}"JScript"&gt;
 function myOpen() {
     open('about:blank');}
 &lt;/script&gt;
 &lt;body onclick{{=}}"myOpen();"&gt;
 Click this page and window.open() is called.
 &lt;/body&gt;</code>
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 3.4.1
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>Reference</code>
*<code>[[dom/Window/close|close]]</code>
*<code>[[dom/Window/open|open]]</code>
*<code>[[dom/Document/write|write]]</code>
*<code>[[dom/Document/writeln|writeln]]</code>
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}