{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|This article outlines the HTML attribute "size", which allows the user to specify a width in characters of an <input> element.}}
{{Markup_Attribute
|Property_applies_to=dom/HTMLElement
|Content=The size attribute specifies the visible width, in characters, of an <input> element.

Note: The size attribute works with the following input types: text, search, tel, url, email, and password.

Tip: To specify the maximum number of characters allowed in the <input> element, use the maxlength attribute.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<form action="demo_form.asp">
  Email: <input type="text" name="email" size="35"><br>
  PIN: <input type="text" name="pin" maxlength="4" size="4"><br>
  <input type="submit" value="Submit">
</form>
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 15.2.2 (Deprecated)
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
|Topic_clusters=Fonts, HTML, Text
|Manual_sections====Related pages (MSDN)===
*<code>baseFont</code>
*<code>font</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}