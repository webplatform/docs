{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Compatibility table; fix see also
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Prevents users from changing, clicking on, or submitting an element.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input]]
|Property_applies_to=dom/HTMLElement
|Content=When an element has the disabled attribute set, it appears dimmed and does not respond to user input. Disabled elements do not respond to mouse events or the [[html/attributes/contentEditable|contentEditable]] property.

If an element is contained within a disabled ([[html/elements/fieldset|fieldset]], the fieldset will override its disabled attribute.

The disabled attribute will prevent javascript click events on the element.

If the disabled element is present without a value (<code><input disabled></code>) it will default to true. Other valid values are <code>true</code> and <code>false</code>.

=== Affects ===

When this is present a user cannot make the element active. Further, when the form is submitted, the input's name and value will not be present. If you wish to submit the value, but make it so the user cannot manipulate the value see the [[html/attributes/readonly|readonly attribute]].
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This shows a basic form, with an email input and a submit button disabled.
|Code=<!doctype html>
<title>Disabled attribute demo</title>
<form role="form">
	<label for="name">Name</label>
	<input name="name">
	<br>
	<label for="email">Email</label>
	<input type="email" name="email" disabled>
	<br>
	<input type="submit" disabled>
	<input type="button" value="cancel">
</form>
|LiveURL=http://code.webplatform.org/gist/7282815
}}
}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=HTML
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML, JavaScript, Security}}
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