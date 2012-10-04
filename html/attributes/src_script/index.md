{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Topics|HTML}}
{{Notes_Section
|Notes=
===Remarks===
A '''script''' element can use the '''SRC''' attribute to refer to code stored in an external script library.  If a '''script''' element refers to an external library and also contains code local to the block defined by the element, the code in the external library is executed before the local code.
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''SRC''' attribute depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''SRC''' returns an absolute URL.  The value specified by the page author is returned when '''SRC''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
In Microsoft Internet Explorer 5 and later, the '''SRC''' attribute of the '''script''' element can refer to an XML data set if the [[html/attributes/language|'''LANGUAGE''']] attribute is set to '''XML'''.
The '''SRC''' attribute was first available in Microsoft Internet Explorer 3.022. The '''src''' property is exposed through the object model as of Microsoft Internet Explorer 4.0.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>script</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}