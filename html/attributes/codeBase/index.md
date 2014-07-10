{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Sets or retrieves the URL of the component.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=The following example uses the '''CODEBASE''' attribute to specify the download location of the Common Dialog control.
|Code=&lt;OBJECT ID{{=}}"CommonDialog1" WIDTH{{=}}32 HEIGHT{{=}}32
    CLASSID{{=}}"CLSID:F9043C85-F6F2-101A-A3C9-08002B2F49FB"
    CODEBASE{{=}}"http://activex.microsoft.com/controls/vb5/comdlg32.cab
    #Version{{=}}1,0,0,0"&gt;
&lt;/OBJECT&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Applets do not support version information supplied as part of the URL.
If ''a'', ''b'', ''c'', and ''d'' are all set to <code>-1</code> (#Version{{=}}-1,-1,-1,-1), the component is downloaded from the server if the release date is later than the installation date on the client computer. If the component is installed on the client computer and the release date is the same or earlier than the installation date, only an HTTP header transaction occurs.
The URL of the component cannot be a local path.
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''codeBase''' attribute depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''codeBase''' returns an absolute URL.  The value specified by the page author is returned when '''codeBase''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
|Import_Notes====Syntax===
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
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>applet</code>
*<code>object</code>
*<code>Managing Versions of a Component</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}