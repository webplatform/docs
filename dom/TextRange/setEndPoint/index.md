{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Sets the endpoint of one range based on the endpoint of another range.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=how
|Data type=BSTR
|Description='''String''' that specifies the endpoint to transfer using one of the following values.

StartToEnd

Move the start of the TextRange object to the end of the specified SourceRange parameter.

StartToStart

Move the start of the TextRange object to the start of the specified SourceRange parameter.

EndToStart

Move the end of the TextRange object to the start of the specified SourceRange parameter.

EndToEnd

Move the end of the TextRange object to the end of the specified SourceRange parameter.

|Optional=No
}}{{Method Parameter
|Name=SourceRange
|Data type=any
|Description=[[dom/TextRange|'''TextRange''']] object from which the source endpoint is to be taken.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=textRange
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=The following example shows how to use the '''setEndPoint''' method to set the start point of the current range (<code>r1</code>) to the endpoint of the second range (<code>r2</code>).
|Code=&lt;script type{{=}}"text/javascript"&gt;
r1.setEndPoint("StartToEnd", r2);
&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes====Syntax===
var retval = TextRange.setEndPoint(how, SourceRange);
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536745(v=vs.85).aspx setEndPoint Method]
|HTML5Rocks_link=
}}