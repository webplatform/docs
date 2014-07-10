{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info

|Checked_Out=No
|High-level issues=Unreviewed Import
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The formmethod attribute defines the HTTP method for sending form-data to the action URL.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input|HTMLInputElement]]
|Property_applies_to=dom/HTMLElement
|Content=The formmethod attribute overrides the method attribute of the <form> element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<form action="submit_post.php" method="post">
  Input field: <input type="text" name="inputfield">
  <input type="submit" value="Submit">
  <input type="submit" formmethod="get" formaction="submit_get.asp" value="Submit using GET">
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
|Manual_sections====Related pages (MSDN)===
*<code>[[dom/HTMLInputElement|HTMLInputElement]]</code>
*<code>[[dom/HTMLBGSoundElement|HTMLButtonElement]]</code>
*<code>input type{{=}}submit</code>
*<code>[[html/attributes/formEnctype|formEnctype]]</code>
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