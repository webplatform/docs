{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=url|Data type=Note|Description=|Optional=}}
{{Method Parameter|Name=name|Data type=BSTR|Description='''Note'''  The following applies only if this method is used instead of window.[[dom/methods/open|'''open''']].|Optional=}}
{{Method Parameter|Name=features|Data type=BSTR|Description='''Note'''  The following applies only if this method is used instead of window.[[dom/methods/open|'''open''']].|Optional=}}
{{Method Parameter|Name=replace|Data type=Note|Description=|Optional=}}
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Object

'''document'''


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following example shows how to use the '''open''' method to replace the current document with a new document and display the HTML markup contained in the variable ''sMarkup''.
|LiveURL=
|Code=
&lt;html&gt;
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

}}}}
{{Notes_Section
|Notes=
===Remarks===
When a function fired by an event on any object calls the
'''open''' method,  the window.[[dom/methods/open|'''open''']] method is implied.
 <code>&lt;script language{{=}}"JScript"&gt;
 function myOpen() {
     open('about:blank');}
 &lt;/script&gt;
 &lt;body onclick{{=}}"myOpen();"&gt;
 Click this page and window.open() is called.
 &lt;/body&gt;</code>
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 3.4.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>Reference</code>
*<code>[[dom/methods/close (document)|close]]</code>
*<code>[[dom/methods/open|open (window)]]</code>
*<code>[[dom/methods/write|write]]</code>
*<code>[[dom/methods/writeln|writeln]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}