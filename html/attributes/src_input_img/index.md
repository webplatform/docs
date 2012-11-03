{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
|Content=The required src attribute specifies the URL of the image.

Note: When a web page loads; it is the browser, at that moment, that gets the image from a web server and inserts it into the page. Therefore, make sure that the image actually stay in the same spot in relation to the web page, otherwise your visitors will get a broken link icon. The broken link icon is shown if the browser cannot find the image.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Description=This example uses the [[html/attributes/src (iframe, embed, xml)|'''src''']] property to change the image's '''src''' attribute.
|Code=&lt;body onmousedown{{=}}"oImage.src{{=}}'sphere.png'" onmouseup{{=}}"oImage.src{{=}}'cone.png'"&gt;
... 
	&lt;img id{{=}}"oImage" src{{=}}"cone.jpeg"&gt;

&lt;/body&gt;
|LiveURL=http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/src.htm
}}
}}
{{Notes_Section
|Notes====Remarks===
The value of the [[html/attributes/src (iframe, embed, xml)|'''src''']] attribute of the '''img''' and '''input type{{=}}image''' elements depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''src''' returns a URL relative to the hosting domain.  The value specified by the page author is returned when '''src''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode.
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the [[html/attributes/src (iframe, embed, xml)|'''src''']] attribute of the '''img''' and '''input type{{=}}image''' elements depends on the context of the reference to the attribute.  When read as a DOM attribute,  '''src''' returns a URL relative to the domain hosting the Web page.  The value specified by the page author is returned when '''src''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
|Import_Notes====Syntax===
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Related pages (MSDN)===
*<code>img</code>
*<code>input type{{=}}image</code>
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}