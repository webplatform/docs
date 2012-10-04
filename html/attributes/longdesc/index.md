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
The long description supplements the shorter description specified by the [[html/attributes/alt|'''alt''']] attribute.
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''longDesc''' attribute for the '''frame''', '''iframe''', and '''img''' elements depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''longDesc''' returns an absolute URL.  The value specified by the page author is returned when '''longDesc''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
The [[html/attributes/alt|'''alt''']] attribute is no longer displayed as the image tooltip for pages displayed in IE8 mode. The target of the '''longDesc''' attribute is now displayed as the tooltip, if present; otherwise, the [[html/attributes/title|'''title''']] is displayed. However, the '''alt''' attribute is displayed as the Microsoft Active Accessibility (MSAA) tooltip. If this attribute is not present, the title attribute is displayed instead.  For more information, see Accessibility section in What's New in Internet Explorer 8.
'''longDesc''' was introduced in Microsoft Internet Explorer 6.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>frame</code>
*<code>iframe</code>
*<code>img</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}