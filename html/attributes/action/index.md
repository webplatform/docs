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
|Description=This example uses the '''ACTION''' attribute to post a form to a specified URL.
|LiveURL=
|Code=
&lt;HTML&gt;
   &lt;FORM ACTION{{=}}"http://example.microsoft.com/sample.asp" 
      METHOD{{=}}"POST"&gt;
      Enter your name: &lt;INPUT NAME{{=}}"FName"&gt;&lt;BR&gt;
      Favorite Ice Cream Flavor:
      &lt;SELECT NAME{{=}}"Flavor"&gt;
         &lt;OPTION VALUE{{=}}"Chocolate"&gt;Chocolate
         &lt;OPTION VALUE{{=}}"Strawberry"&gt;Strawberry
         &lt;OPTION VALUE{{=}}"Vanilla" SELECTED&gt;Vanilla
      &lt;/SELECT&gt;
      &lt;P&gt;&lt;INPUT TYPE{{=}}SUBMIT&gt;
   &lt;/FORM&gt;
&lt;/HTML&gt;
}}
{{Single_Example
|Description=This example uses the '''ACTION''' attribute to specify a URL for the mailto protocol.
|LiveURL=
|Code=
&lt;form ACTION{{=}}"mailto:sales@widgets.com" method{{=}}GET&gt;
  &lt;input name{{=}}subject type{{=}}hidden 
     value{{=}}"Widget%20Product%20Information%20Request"&gt;
  Enter your full mailing address&lt;BR&gt;
  &lt;TextArea name{{=}}body cols{{=}}40&gt;&lt;/textarea&gt;
  &lt;input type{{=}}submit value{{=}}"Send Request"
&lt;/form&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the '''action''' attribute depends on the context of the reference to the attribute.  When read as a Document Object Model (DOM) attribute,  '''action''' returns an absolute URL.  The value specified by the page author is returned when '''action''' is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser.  For more information, see Attribute Differences in Internet Explorer 8.
The value of the '''action''' attribute depends on the context of the reference to the attribute.  When read as a DOM attribute,  '''action''' returns an absolute URL.  The value specified by the page author is returned when '''action''' is read as a content attribute.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.3


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>form</code>
*<code>isIndex</code>
|Topic_clusters=html
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}