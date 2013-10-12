{{Page_Title}}
{{Flags
|High-level issues=Unreviewed Import
|Content=Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The formenctype attribute specifies how the form-data should be encoded when submitting it to the server.}}
{{Markup_Attribute
|Applies_to=http://docs.webplatform.org/wiki/html/elements/input
|Property_applies_to=dom/HTMLElement
|Content=The formenctype attribute overrides the enctype attribute of the <form> element with method="post".
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<form action="submit.php" method="post">
  Input field: <input type="text" name="inputfield">
  <input type="submit" value="Submit">
  <input type="submit" formenctype="multipart/form-data" value="Submit as Multipart/form-data">
</form>
}}
}}
{{Notes_Section
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.19.6
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
|Topic_clusters=HTML
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
*<code>[[dom/HTMLBGSoundElement|HTMLButtonElement]]</code>
*<code>input type{{=}}submit</code>
*<code>[[html/attributes/formMethod|formMethod]]</code>
*<code>[[html/attributes/formAction|formAction]]</code>
*<code>[[html/attributes/formNoValidate|formNoValidate]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}