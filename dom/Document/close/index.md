{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters=
|Method_applies_to=dom/document
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Notes_Section
|Notes=
===Remarks===
When a function fired by an event on any object calls the 
[[dom/methods/close|'''close''']] method, the window.'''close''' method is implied.
 <code>&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
 function myClose() {
     close();}
 &lt;/SCRIPT&gt;
 &lt;BODY onclick{{=}}"myClose();"&gt;
 Click this page and window.close() is called.
 &lt;/BODY&gt;</code>
When an event on any 
object calls the [[dom/methods/close|'''close''']] method, the 
document.'''close''' method is implied.
'''Note'''  When [[dom/document|'''document''']].[[dom/methods/write|'''write''']] or '''document'''.[[dom/methods/writeln|'''writeln''']] is used in an event handler, '''document'''.'''close''' should also be used.
 <code>&lt;button onclick{{=}}"window.close();"&gt;
 Click this button to close the window.
 &lt;/button&gt;</code>
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}196991 Document Object Model (DOM) Level 2 HTML Specification], Section 1.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/document|document]]</code>
*<code>[[dom/methods/open (document)|open]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}