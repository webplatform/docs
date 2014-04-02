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
|Name=url
|Data type=BSTR
|Description='''String''' that specifies the URL of the document to display. If no URL is specified, a new window with '''about:blank''' is displayed.
|Optional=No
}}{{Method Parameter
|Name=name
|Data type=BSTR
|Description='''String''' that specifies the name of the window. This name is used as the value for the [[html/attributes/target|'''TARGET''']] attribute on a '''form''' or an [[html/elements/a|'''anchor''']] element.
|Optional=No
}}{{Method Parameter
|Name=features
|Data type=BSTR
|Description='''String''' that contains a list of items separated by commas. Each item consists of an option and a value, separated by an equals sign (for example, "fullscreen{{=}}yes, toolbar{{=}}yes"). The following values are supported.
|Optional=No
}}{{Method Parameter
|Name=replace
|Data type=any
|Description='''Boolean''' that specifies whether the ''url'' creates a new entry or replaces the current entry in the window's history list. This parameter only takes effect if the ''url'' is loaded into the same window.
|Optional=No
}}
|Method_applies_to=dom/Window
|Example_object_name=object
|Return_value_name=object
|Javascript_data_type=DOM Node
|Return_value_description='''IHTMLWindow2'''

Returns a reference to the new
'''window''' object. Use this
reference to access properties and methods on the new window.

'''Internet Explorer 7 on Windows Vista:''' Opening a new window from an application (other than the Internet Explorer process) may result in a null return value. This restriction occurs because Internet Explorer runs in protected mode, by default. One facet of protected mode prevents applications from having privileged access to Internet Explorer when that access spans process boundaries. Opening a new window by using this method generates a new process. For more information about protected mode, see Understanding and Working in Protected Mode Internet Explorer. This commonly occurs for applications that host the WebBrowser control.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the '''open''' method to create a new window that contains Sample.htm. The new window is 200 pixels by 400 pixels and has a status bar, but it does not have a toolbar, menu bar, or address field.
|Code=window.open("Sample.htm",null,
    "height{{=}}200,width{{=}}400,status{{=}}yes,toolbar{{=}}no,menubar{{=}}no,location{{=}}no");
}}
}}
{{Notes_Section
|Notes====Remarks===
By default, the '''open''' method creates a window that has a default width and height and the standard menu, toolbar, and other features of Internet Explorer. You can alter this set of features by using the ''features'' parameter. This parameter is a string consisting of one or more feature settings.
When the ''features'' parameter is specified, the features that are not defined in the parameter are disabled. Therefore, when using the ''features'' parameter, it is necessary to enable all the features that are to be included in the new window. If the ''features'' parameter is not specified, the window features maintain their default values. In addition to enabling a feature by setting it to a specific value, simply listing the feature name also enables that feature for the new window. Most of the ''features'' specified in the window.open method are ignored if user has selected, "Always open pop-ups in a new tab" setting in the Internet options control panel.
When a function fired by an event on any object calls the
'''open''' method, the window.'''open''' method is implied.
 <code>&lt;script language{{=}}"JScript"&gt;
 function myOpen() {
     open('about:blank');}
 &lt;/script&gt;
 &lt;body onclick{{=}}"myOpen();"&gt;
 Click this page and window.open() is called.
 &lt;/body&gt;</code>
When an event on any
object calls the '''open''' method, the
document.'''open''' method is implied.
 <code>&lt;button onclick{{=}}"open('Sample.htm');"&gt;
 Click this button and document.open() is called.
 &lt;/button&gt;</code>
Windows Internet Explorer 8. New windows and pop-ups always inherit the zoom level of the parent window.
Internet Explorer 7. The '''Back''', '''Forward''', and '''Stop''' commands are now located in the Navigation bar of the user interface.  Prior to Internet Explorer 7 navigation commands were located in the toolbar.
Internet Explorer 7 on Windows Vista. Opening a new window from an application other than the Internet Explorer process may result in a NULL return value.  This occurs because Internet Explorer runs in protected mode by default. Protected mode prevents applications from privileged access to Internet Explorer when that access spans process boundaries. Because this method opens windows in a new process, protected mode restricts access to the new window. For more information, please see Understanding and Working in Protected Mode Internet Explorer.
Internet Explorer 6 for Windows XP SP2 places several restrictions on windows created with this method. For several of the parameter values listed in the Parameters table, these restrictions are indicated by the minimum value. For more information, see About Window Restrictions.
This method must use a user-initiated action, such as clicking on a link or tabbing to a link and pressing enter, to open a pop-up window. The Pop-up Blocker feature in Internet Explorer 6 blocks windows that are opened without being initiated by the user. The Pop-up Blocker also prevents windows from appearing if you call this method from an [[dom/Element/unload|'''onunload''']] event.
In Internet Explorer 6, the '''_media''' value of the ''name'' parameter specifies that this method loads a URL into the HTML content area of the Media Bar.
Internet Explorer 5 allows further control over windows through the implementation of <code>title</code> in the ''features'' parameter of the '''open''' method. Turn off the title bar by opening the window from a trusted application, such as Microsoft Visual Basic or an HTML Application (HTA). These applications are considered trusted, because each uses Internet Explorer interfaces instead of the browser.
In Windows CE, the [[dom/Document|Document]] object is not available through scripting for a '''window''' opened using the '''open''' method.
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