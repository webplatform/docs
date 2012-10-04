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
|Description=This example uses the '''src'''
property to change the '''src'''
attribute of an '''iframe'''.
|LiveURL=
|Code=

function changeFrame(){
  alert (document.all.iframe1.src);
  document.all.iframe1.src{{=}}"http://www.microsoft.com/";
  alert (document.all.iframe1.src);
}
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''SRC''' attribute of the '''frame''' and '''iframe''' elements depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''SRC''' returns an absolute URL.  The value specified by the page author is returned when '''SRC''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
|Import_Notes=
===Syntax===
}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>applet</code>
*<code>embed</code>
*<code>frame</code>
*<code>iframe</code>
*<code>xml</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}