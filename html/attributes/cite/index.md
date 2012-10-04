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
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The example shows the use of the '''cite''' property.
|LiveURL=
|Code=
&lt;HTML&gt;
&lt;BODY&gt;
&lt;Q id{{=}}"greatQuote" cite{{=}}"http://www.Shakespeare.the.great.com"&gt;
To Be or Not to Be, That is the Question.&lt;/Q&gt;
&lt;/BODY&gt;
&lt;/HTML&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
This property is designed to contain a Uniform Resource Identifier (URI) that points to information about why a document was changed,
or about the source of a quotation.
There is no functionality implemented for this property unless defined by the author.
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''cite''' attribute for the '''del''', '''ins''', and '''q''' elements depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute,  '''cite''' returns an absolute URL.  The value specified by the page author is returned when '''cite''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
'''cite''' was introduced in Microsoft Internet Explorer 6.
The value of the '''cite''' attribute for the '''del''', '''ins''', and '''q''' elements depends on the context of the reference to the attribute. When read as a DOM attribute,  '''cite''' returns an absolute URL.  The value specified by the document author is returned when '''cite''' is read as a content attribute, when the document is displayed in an earlier document compatibility mode.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>blockQuote</code>
*<code>q</code>
*<code>ins</code>
*<code>del</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}