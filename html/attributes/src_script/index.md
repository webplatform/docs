{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Notes====Remarks===
A '''script''' element can use the '''SRC''' attribute to refer to code stored in an external script library.  If a '''script''' element refers to an external library and also contains code local to the block defined by the element, the code in the external library is executed before the local code.
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''SRC''' attribute depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''SRC''' returns an absolute URL.  The value specified by the page author is returned when '''SRC''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
In Microsoft Internet Explorer 5 and later, the '''SRC''' attribute of the '''script''' element can refer to an XML data set if the [[html/attributes/language|'''LANGUAGE''']] attribute is set to '''XML'''.
The '''SRC''' attribute was first available in Microsoft Internet Explorer 3.022. The '''src''' property is exposed through the object model as of Microsoft Internet Explorer 4.0.
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
*<code>script</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}