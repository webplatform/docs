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
When the user enters information in a '''form''' and clicks the  '''submit''' button, there are two ways the information can be sent from the browser to the server: as part of the URL, or within the body of the HTTP request.
The '''GET''' method appends name/value pairs to the URL. The amount of data that can be sent is limited by the maximum length of a URL, which is 2048 bytes. The URL could be truncated if the form uses a large number of parameters, or if the parameters contain large amounts of data. Parameters passed on the URL are visible in the address field of the browser.
This '''POST''' method packages the name/value pairs inside the body of the HTTP request. When using the '''POST''' method, there is no theoretical limit to the amount of data that can be sent to the server. Because the parameters are not appended to the URL, this method is slightly more secure.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.3
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
*<code>form</code>
*<code>[[html/attributes/action|action]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}