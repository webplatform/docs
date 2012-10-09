{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections, Needs Topics, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''action''' attribute to post a form to a specified URL.
|Code=<form action="/sendmail.asp" method="get">
  <input name="subject" type="hidden" value="Widget Product Information Request" />
  <label for="body">Please enter your email body</label>
  <textarea name="body" cols="40"></textarea>
  <input type="submit" value="Send Request" />
</form>
}}
}}
{{Notes_Section
|Notes====Remarks===
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''action''' attribute depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''action''' returns an absolute URL.  The value specified by the page author is returned when '''action''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
The value of the '''action''' attribute depends on the context of the reference to the attribute.  When read as a DOM attribute,  '''action''' returns an absolute URL.  The value specified by the page author is returned when '''action''' is read as a content attribute.
|Import_Notes====Mailto actions===
It is possible to make an email form by placing an mailto address in the action attribute. Although it is technically possible, we recommend strongly to 'not' use them, as it doesn't work in every browser as it was once supposed to. Please use an email script instead, and make the form post to that certain email script.

===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.3
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
*<code>form</code>
*<code>isIndex</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}