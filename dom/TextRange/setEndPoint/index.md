{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=how
|Data type=BSTR
|Description='''String''' that specifies the endpoint to transfer using one of the following values.
|Optional=No
}}{{Method Parameter
|Name=SourceRange
|Data type=any
|Description=[[dom/TextRange|'''TextRange''']] object from which the source endpoint is to be taken.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example shows how to use the '''setEndPoint''' method to set the start point of the current range (<code>r1</code>) to the endpoint of the second range (<code>r2</code>).
|Code=&lt;SCRIPT LANGUAGE{{=}}"JScript"&gt;
r1.setEndPoint("StartToEnd", r2);
&lt;/SCRIPT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
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