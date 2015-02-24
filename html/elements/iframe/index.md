{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
Notes section is from MSDN and very IE-specific.
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The '''iframe''' element (&lt;iframe&gt;) introduces a new nested browsing context.}}
{{Markup_Element
|DOM_interface=dom/HTMLIFrameElement
|Tag_omissions=Closing tag required
|CSS_display=inline-block
|Content=Iframes are one the best ways to build up a complex, detailed webpage from smaller, more manageable chunks. By using iframe tags, a developer can include webpages as part of a larger, enompassing parent page. Unlike frames, iframes can be styled through CSS and easily molded to fit seamlessly within the parent page. One neat use of an iframe is to display a custom Google map within the page. This can be done by setting the 'src' attribute of the iframe tag to Google Map URL.


== HTML Attributes ==

*<code>src</code> = URL potentially surrounded by spaces<br />Gives the address of a page that the nested browsing context is to contain. 
*<code>srcdoc</code> = HTML contents<br />Gives the content of the page that the nested browsing context is to contain.
*<code>name</code> = browsing-context name<br />Represents the browsing-context name. When the browsing context is created, if the attribute is present, the browsing context name must be set to the value of this attribute; otherwise, the browsing context name must be set to the empty string.
*<code>sandbox</code> = allow-same-origin/ allow-top-navigation/ allow-forms/ allow-scripts<br />Enables a set of extra restrictions on any content hosted by the iframe.
**If presents, given in the following list set.
***prevents content from navigating browsing contexts other than the sandboxed browsing context itself.
***prevents content from navigating their top-level browsing context.
***prevents content from instantiating plugins, whether using the embed element, the object element, the applet element, or through navigation of a nested browsing context.
***prevents content from using the seamless attribute on descendant iframe elements.
***forces content into a unique origin, thus preventing it from accessing other content from the same origin.
***blocks form submission, blocks script execution.
***blocks features that trigger automatically, such as automatically playing a video or automatically focusing a form control.
**<code>allow-same-origin</code><br />allows the content to be treated as being from the same origin instead of forcing it into a unique origin.
**<code>allow-top-navigation</code><br />allows the content to navigate its top-level browsing context
**<code>allow-forms</code> and <code>allow-scripts</code><br />re-enable forms and scripts respectively (though scripts are still prevented from creating popups).
*<code>seamless</code> = boolean<br />Indicates that the iframe element's browsing context is to be rendered in a manner that makes it appear to be part of the containing document (seamlessly included in the parent document).
*<code>width</code> = non-negative integer<br />Give the width of the visual content of the element, in CSS pixels.
*<code>height</code> = non-negative integer<br />Give the height of the visual content of the element, in CSS pixels.

}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example embeds <code>http://example.com/</code> via an IFrame element.
|Code=&lt;iframe id{{=}}"theFrame" src{{=}}"http://example.com/"&gt;&lt;/iframe&gt;
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=This example shows how to grab the Document contained within an IFrame element (note that you may only reach down into an IFrame if the page it has loaded is same-origin).
|Code=var frameDoc {{=}} document.getElementById("theFrame").contentDocument;
|LiveURL=
}}
}}
{{Notes_Section
|Usage=The developer should be careful not to overuse iframes, because they dramatically slow down the rendering of a page. For each extra iframe, the browser has to make an extra request to the server.
|Notes====Remarks===
The '''iframe''' element functions as a document within a document, or like a floating '''frame'''. The [[dom/properties/frames|'''frames''']] collection provides access to the contents of an '''iframe'''. Use the '''frames''' collection to read or write to elements contained in an '''iframe'''. For example, the syntax for accessing the [[css/properties/background-color|'''backgroundColor''']] style of the '''body''' object in an '''iframe''' is:
 <code>sColor {{=}} document.frames("sFrameName").document.body.style.backgroundColor;</code>
You can access the '''iframe''' object's properties, but not its contents, through the object model of the page where the '''iframe''' object resides. For example, the syntax for accessing the [[css/properties/border|'''border''']] style of the '''iframe''' object is:
 <code>sBorderValue {{=}} document.all.oFrame.style.border;</code>
'''Note'''  Properties of the '''iframe''' must be accessed using the prefix, <code>document.all</code>, for example, <code>document.all.iframeId.marginWidth</code>.

'''Security Warning:  '''
To protect user privacy and safeguard your applications, Windows Internet Explorer restricts some interactions between frames that host Web pages from different domains. To treat the content of the '''iframe''' as if it were in the Restricted Sites zone, set the '''SECURITY''' attribute to "restricted." For more information about using the Dynamic HTML (DHTML) object model with the '''frame''' and '''iframe''' objects, see About Cross-Frame Scripting and Security and Security Considerations: Dynamic HTML.
Windows Internet Explorer 8 and later. The values of the [[html/attributes/longDesc|'''longDesc''']] and [[html/attributes/src (iframe, embed, xml)|'''src''']] attributes depend on the current document compatibility mode.
Windows Internet Explorer 7 and later. For security reasons, resizing is disabled for '''iframe''' objects that display content hosted on a domain different from the domain hosting the parent document. If you trust the content you are loading into an '''iframe''' object, you can enable resizing by specifying values for the [[css/properties/min-width|'''minWidth''']] and [[css/properties/max-width|'''maxWidth''']] attributes of the '''iframe''' element in the source of the parent document. You must specify values for both attributes to enable resizing.
Microsoft Internet Explorer 5.5 supports transparent content with inline floating frames. The following conditions must be met to define transparent content for inline floating frames.
#The [[html/attributes/allowTransparency|'''allowTransparency''']] attribute, used with the '''iframe''' element, must be set to <code>true</code>.
#In the '''iframe''' content source document, the  [[css/properties/background-color|'''backgroundColor''']] attribute of the '''body''' element must be set to <code>transparent</code>.

Using Transparency with Inline Floating Frames
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/embedded-content.html#the-iframe-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-iframe-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/present/frames.html#edef-IFRAME
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=http://www.w3.org/TR/html-markup/iframe.html#iframe
|Manual_sections====Related pages (MSDN)===
*<code>Using IFRAME Elements</code>
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