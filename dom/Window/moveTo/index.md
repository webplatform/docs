{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object_Method
|Parameters={{Method Parameter|Name=x|Data type=Integer|Description='''Integer''' that specifies the horizontal scroll offset in pixels. The value can be either positive or negative.|Optional=}}
{{Method Parameter|Name=y|Data type=Integer|Description='''Integer''' that specifies the vertical scroll offset in pixels. The value can be either positive or negative.|Optional=}}
|Method_applies_to=dom/window
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
This method is not valid with windows created using the [[dom/methods/showModalDialog|'''showModalDialog''']] or [[dom/methods/showModelessDialog|'''showModelessDialog''']] methods. In order to move or resize a dialog window created with these methods, change the [[dom/properties/dialogHeight|'''dialogHeight''']], [[dom/properties/dialogWidth|'''dialogWidth''']], [[dom/properties/dialogTop|'''dialogTop''']], and [[dom/properties/dialogLeft|'''dialogLeft''']] properties.
If the page (that contains this script) is hosted within an IFRAME, the IFRAME will move relative to the upper-left corner of the content area.
Windows XP Service Pack 2 (SP2) or later. Windows that are located in the Internet Zone are subject to Window_Restrictions and will be forced to stay on screen. This applies to '''moveTo''', [[dom/methods/moveBy|'''moveBy''']], [[dom/methods/resizeTo|'''resizeTo''']], and [[dom/methods/resizeBy|'''resizeBy''']] methods.
'''Note'''  When operating in high-dpi mode, pixel values are scaled up accordingly. See Adjusting Scale for Higher DPI Screens for additional information.
Windows Internet Explorer 7. This method is only effective when a single tab is open or when tabbed browsing is disabled.  If multiple tabs are open, this method is blocked.  For information regarding tab interaction from a script, see Tabbed Browsing for Developers.
Internet Explorer 7. This method is blocked if called by a foreign domain within a sub-frame (FRAME/IFRAME).
|Import_Notes=
===Syntax===
===Standards information===
There are no standards that apply here.

}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>window</code>
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}