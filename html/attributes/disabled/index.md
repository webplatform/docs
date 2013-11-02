{{Page_Title}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|The disabled attribute prevents users from changing, clicking on, or submitting an element.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input]]
|Property_applies_to=dom/HTMLElement
|Content=When an element has the disabled attribute set, it appears dimmed and does not respond to user input. Disabled elements do not respond to mouse events or the [[html/attributes/contentEditable|contentEditable]] property.

If an element is contained within a disabled ([[html/elements/fieldset|fieldset]], the fieldset will override its disabled attribute.

The disabled attribute will prevent javascript click events on the element.

If the disabled element is present without a value (<code><input disabled></code>) it will default to true. Other valid values are <code>true</code> and <code>false</code>.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This shows a basic form, with an email input and a submit button disabled.
|Code=<form role="form">
	<label for="name">Name</label>
	<input type="text" name="name">
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
{{Notes_Section}}
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
}}
{{Topics|HTML, JavaScript, Security}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}