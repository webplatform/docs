{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Causes the window to scroll to the specified x- and y-offset at the upper-left corner of the window.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=Number
|Description='''Integer''' that specifies the horizontal scroll offset, in pixels.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=Number
|Description='''Integer''' that specifies the vertical scroll offset, in pixels.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Javascript_data_type=void
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!-- put the 100th vertical pixel at the top of the window --&gt;

&lt;button onClick{{=}}"scroll(0, 100);"&gt;click to scroll down 100 pixels&lt;/button&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
This method is provided for backward compatibility only. The recommended way to scroll a window is to use the [[dom/Window/scrollTo|'''scrollTo''']] method.
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.scroll scroll]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536726(v=vs.85).aspx scroll Method]
|HTML5Rocks_link=
}}