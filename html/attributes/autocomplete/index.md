{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The autocomplete attribute specifies whether a browser should automatically provide values for a form element.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input|HTMLInputElement]]
|Property_applies_to=dom/HTMLElement
|Content=When autocomplete is on, the browser may automatically fill previously entered values, or match input [[html/attributes/name|names]] with values the user has provided.

For sensitive information or form content that is not repeated, autocomplete should be turned off so the user is forced to fill the field every time. 

Autocomplete should also be turned off if the website provides its own mechanism for filling a field; for example, an autocomplete like shown in this site's search.

Valid values for autocomplete are <code>on</code> or <code>off</code>. The attribute is not required.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''AUTOCOMPLETE''' attribute to disable the AutoComplete feature.
|Code=<input type="password" autocomplete="off">
}}{{Single Example
|Language=HTML
|Description=The following example shows an HTML form with autocomplete on. One of the inputs ha autocomplete off.
|Code=<form action="submit.php" autocomplete="on">
  First name:<input type="text" name="name"><br />
  Last name: <input type="text" name="surname"><br />
  E-mail: <input type="email" name="email" autocomplete="off"><br />
  <input type="submit">
</form>
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#attr-form-autocomplete
|Status=W3C Candidate Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=HTML, Security
|Manual_sections====Related pages (MSDN)===
*<code>input type{{=}}password</code>
*<code>input type{{=}}text</code>
*<code>form</code>

[[html/elements/input/password]]
[[html/elements/input/text]]
[[html/elements/form]]
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}