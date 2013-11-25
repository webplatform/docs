{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=html|Data type=BSTR|Description='''String''' that specifies the HTML text to paste. The string can contain text and any combination of the HTML tags described in HTML Elements.|Optional=}}
|Method_applies_to=dom/TextRange
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.


}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=This example uses the '''pasteHTML''' method to replace the current selection with a new paragraph.
|LiveURL=
|Code=
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
var sel {{=}} document.selection;
if (sel!{{=}}null) {
    var rng {{=}} sel.createRange();
    if (rng!{{=}}null)
        rng.pasteHTML("&lt;P&gt;&lt;B&gt;Selection has been replaced.&lt;/B&gt;&lt;/P&gt;");
}
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This method might alter the HTML text to make it fit the given text range. For example, pasting a table cell into a text range that does not contain a table might cause the method to insert a [[html/elements/table|'''table''']] element. For predictable results, paste only well-formed HTML text that fits within the given text range.
This method is accessible at run time. If elements are removed at run time, before the closing tag is parsed, areas of the document might not render.
This feature might not be available on non-Microsoft Win32 platforms.
This method fails only when used inappropriately to paste HTML into a '''TEXTAREA''' element in Microsoft Internet Explorer 5 and later.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/TextRange|TextRange]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}