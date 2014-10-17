{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Needs a clean up - compatibility notes should be in their own appropriate section.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Changes the current size of the window by the specified x- and y-offset.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Index=
|Name=x
|Data type=Number
|Description='''Integer''' that specifies the horizontal offset in pixels. The value can be either positive or negative.
|Optional=No
}}{{Method Parameter
|Index=
|Name=y
|Data type=Number
|Description='''Integer''' that specifies the vertical offset in pixels. The value can be either positive or negative.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=window
|Return_value_name=
|Javascript_data_type=void
|Return_value_description=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=
|Code=// shrink the window 
window.resizeBy(-200, -200);
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=This method is not valid with windows created using the [[dom/Window/showModalDialog|'''showModalDialog''']] method. In order to move or resize a dialog window created with these methods, change the [[dom/WindowModal/dialogHeight|'''dialogHeight''']], [[dom/WindowModal/dialogWidth|'''dialogWidth''']], [[dom/WindowModal/dialogTop|'''dialogTop''']], and [[dom/WindowModal/dialogLeft|'''dialogLeft''']] properties.
If the page (that contains this script) is hosted within an IFRAME, the IFRAME will move relative to the upper-left corner of the content area.
Windows XP Service Pack 2 (SP2) or later. Windows that are located in the Internet Zone are subject to Window_Restrictions and will be forced to stay on screen. This applies to [[dom/Window/moveTo|'''moveTo''']], [[dom/Window/moveBy|'''moveBy''']], [[dom/Window/resizeTo|'''resizeTo''']], and '''resizeBy''' methods.
'''Note:''' When operating in high-dpi mode, pixel values are scaled up accordingly. See Adjusting Scale for Higher DPI Screens for additional information.
Windows Internet Explorer 7. This method is only effective when a single tab is open or when tabbed browsing is disabled.  If multiple tabs are open, this method is blocked.  For information regarding tab interaction from a script, see Tabbed Browsing for Developers.
Internet Explorer 7. This method is blocked if called by a foreign domain within a sub-frame (FRAME/IFRAME).
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.resizeBy resizeBy]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536722(v=vs.85).aspx resizeBy Method]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}