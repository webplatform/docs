{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Links an image to a description of its content, for enhanced accessibility}}
{{Markup_Attribute
|Applies_to=dom/HTMLImageElement
|Property_applies_to=dom/HTMLElement
|Content=
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=The description is somewhere on the same page as the image
|Code=<nowiki>
<img src="http://example.com/graph1" alt="Drinks are getting sweeter"
    longdesc="#graph1Explained"/>
<p id="graph1Explained">A blue capital letter "W" with kerning so it touches a blue 3, followed by a black shadow of a white capital letter C all on a white background</p>
</nowiki>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=The description is one of several within an external page
|Code=<nowiki>
<img src="ExampleImage" alt="example" longdesc="http://example.com/descs#item3"/>
</nowiki>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=The description is included in a data: URI
|Code=<img src="logo" alt="W3C" longdesc="data:text/html;charset=utf-8;,%3C!DOCTYPE%20html%3E
%3Chtml%3E%3Chead%3E%3Ctitle%3EDescription%20of%20the%20W3C%20Logo%3C/title%3E%3C/head%3E
%3Cbody%3E%3Cp%3EA%20blue%20capital%20letter%20%22W%22%20with%20kerning%20so%20it%20
touches%20a%20blue%203%2C%20followed%20by%20a%20black%20shadow%20of%20a%20white%20
capital%20letter%20C%20all%20on%20a%20white%20background%3C/body%3E%3C/html%3E"/>
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
The long description supplements the shorter description specified by the [[html/attributes/alt|'''alt''']] attribute.
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''longDesc''' attribute for the '''frame''', '''iframe''', and '''img''' elements depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''longDesc''' returns an absolute URL.  The value specified by the page author is returned when '''longDesc''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
The [[html/attributes/alt|'''alt''']] attribute is no longer displayed as the image tooltip for pages displayed in IE8 mode. The target of the '''longDesc''' attribute is now displayed as the tooltip, if present; otherwise, the [[html/attributes/title|'''title''']] is displayed. However, the '''alt''' attribute is displayed as the Microsoft Active Accessibility (MSAA) tooltip. If this attribute is not present, the title attribute is displayed instead.  For more information, see Accessibility section in What's New in Internet Explorer 8.
'''longDesc''' was introduced in Microsoft Internet Explorer 6.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5 Image Description Extension
|URL=http://www.w3.org/TR/html-longdesc/
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=*[[html/elements/img|img]]
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}