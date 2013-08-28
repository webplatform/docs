{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The formaction attribute specifies the URL of a file that will process the input control when the form is submitted.}}
{{Markup_Attribute
|Applies_to=http://docs.webplatform.org/wiki/html/elements/input
|Property_applies_to=dom/HTMLElement
|Content=The formaction attribute overrides the action attribute of the <form> element.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=<form action="login.php">
  First name: <input type="text" name="name"><br>
  Last name: <input type="text" name="surname"><br>
  <input type="submit" value="Login"><br>
  <input type="submit" formaction="admin_login.php"
  value="Login as admin">
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
*<code>input type{{=}}image</code>
*<code>[[html/attributes/formMethod|formMethod]]</code>
*<code>[[html/attributes/formEnctype|formEnctype]]</code>
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