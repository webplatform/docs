{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs example with modern syntax... not for method.
not jScript.
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|Non-Standard}}
{{API_Name}}
{{Summary_Section|Moves the start and end positions of the text range to the given point.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=any
|Description='''Integer''' that specifies the horizontal offset relative to the upper-left corner of the window, in pixels.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=any
|Description='''Integer''' that specifies the vertical offset relative to the upper-left corner of the window, in pixels.
|Optional=No
}}
|Method_applies_to=dom/TextRange
|Example_object_name=textRange
|Return_value_name=result
|Javascript_data_type=Number
|Return_value_description=Type: '''HRESULT'''

If this method succeeds, it returns '''S_OK'''. Otherwise, it returns an '''HRESULT''' error code.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''moveToPoint''' method to move the text range to the point where the user clicked the mouse, expands the range, and selects the text within the new range.
|Code=&lt;SCRIPT FOR{{=}}document EVENT{{=}}onclick LANGUAGE{{=}}"JScript"&gt;
    var rng {{=}} document.body.createTextRange();
    rng.moveToPoint(window.event.x, window.event.y);
    rng.expand("word");
    rng.select();
&lt;/SCRIPT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
The coordinates of the point must be in pixels and be relative to the upper-left corner of the window. The resulting text range is empty, but you can expand and move the range using methods such as '''expand''' and [[dom/TextRange/moveEnd|'''moveEnd''']].
This feature might not be available on non-Microsoft Win32 platforms.
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
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536632(v=vs.85).aspx moveToPoint Method]
|HTML5Rocks_link=
}}