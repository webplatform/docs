{{Page_Title}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|N/A}}
{{API_Name}}
{{Summary_Section|Moves the screen position of the window by the specified x and y offset values.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=x
|Data type=any
|Description='''Integer''' that specifies the horizontal scroll offset in pixels. The value can be either positive or negative.
|Optional=No
}}{{Method Parameter
|Name=y
|Data type=any
|Description='''Integer''' that specifies the vertical scroll offset in pixels. The value can be either positive or negative.
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
|Code=function budge() {
  moveBy(10, -10);
}
}}
}}
{{Notes_Section
|Notes====Remarks===
This method is not valid with windows created using the [[dom/HTMLElement/showModalDialog|'''showModalDialog''']] or [[dom/HTMLElement/showModelessDialog|'''showModelessDialog''']] methods. In order to move or resize a dialog window created with these methods, change the [[dom/WindowModal/dialogHeight|'''dialogHeight''']], [[dom/WindowModal/dialogWidth|'''dialogWidth''']], [[dom/WindowModal/dialogTop|'''dialogTop''']], and [[dom/WindowModal/dialogLeft|'''dialogLeft''']] properties.
If the page (that contains this script) is hosted within an IFRAME, the IFRAME will move relative to the upper-left corner of the content area.
Windows XP Service Pack 2 (SP2) or later. Windows that are located in the Internet Zone are subject to Window_Restrictions and will be forced to stay on screen. This applies to [[dom/Window/moveTo|'''moveTo''']], '''moveBy''', [[dom/Window/resizeTo|'''resizeTo''']], and [[dom/Window/resizeBy|'''resizeBy''']] methods.
'''Note:'''  When operating in high-dpi mode, pixel values are scaled up accordingly. See Adjusting Scale for Higher DPI Screens for additional information.
Windows Internet Explorer 7. This method is only effective when a single tab is open or when tabbed browsing is disabled.  If multiple tabs are open, this method is blocked.  For information regarding tab interaction from a script, see Tabbed Browsing for Developers.
Internet Explorer 7. This method is blocked if called by a foreign domain within a sub-frame (FRAME/IFRAME).
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
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/API/Window.moveBy moveBy]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/ms536618(v=vs.85).aspx moveBy Method]
|HTML5Rocks_link=
}}