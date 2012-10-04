{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=how|Data type=BSTR|Description='''String''' that specifies the endpoint to transfer using one of the following values.|Optional=}}
{{Method Parameter|Name=SourceRange|Data type=IHTMLTxtRange|Description=[[dom/traversal/TextRange|'''TextRange''']] object from which the source endpoint is to be taken.|Optional=}}
|Method_applies_to=dom/traversal/TextRange
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
|Description=The following example shows how to use the '''setEndPoint''' method to set the start point of the current range (<code>r1</code>) to the endpoint of the second range (<code>r2</code>).
|LiveURL=
|Code=
&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
r1.setEndPoint("StartToEnd", r2);
&lt;/SCRIPT&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
A text range has two endpoints: one at the beginning of the text range and one at the end. An endpoint can also be the position between two characters in an HTML document.
There are four possible endpoint locations in the following HTML.
 <code>&lt;BODY&gt;&lt;P&gt;&lt;B&gt;abc</code>
The possible endpoint locations are:
*Before the letter a.
*Between the letters a and b.
*Between the letters b and c.
*After the letter c.

This feature might not be available on platforms other than Microsoft Win32.
In Microsoft Internet Explorer 4.0, an endpoint is relative to text only, not HTML tags.
In Internet Explorer 4.0, an endpoint cannot be established between '''body''' and '''p'''. Specifying an endpoint between '''body''' and '''p'''  is interpreted as if it occurs before the letter a.
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[dom/traversal/TextRange|TextRange]]</code>
*<code>TextRange Constructor</code>
*<code>[[dom/traversal/methods/compareEndPoints|compareEndPoints]]</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}