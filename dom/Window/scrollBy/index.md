{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Causes the window to scroll relative to the current scrolled position by the specified x- and y-pixel offset. }}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description='''Integer''' that specifies the horizontal scroll offset, in pixels. Positive values scroll the window right, and negative values scroll it left.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description='''Integer''' that specifies the vertical scroll offset, in pixels. Positive values scroll the window down, and negative values scroll it up.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=// scroll one page 
window.scrollBy(0, window.innerHeight);
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
There are no standards that apply here.
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
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.scrollBy scrollBy]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536728(v=vs.85).aspx scrollBy Method]
|HTML5Rocks_link=
}}