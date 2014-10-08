{{Page_Title}}
{{Flags
|State=Almost Ready
|Editorial notes=Compatibility table;
|Checked_Out=No
|High-level issues=Needs Review
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Indicates the initial state of a checkbox or radio button.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input]]
|Property_applies_to=dom/HTMLElement
|Content=The checked attribute can be used to specify what the visual or initial state of an input element is. It's often used to toggle an element through JavaScript.

As a boolean attribute, valid values are "<code>checked</code>" and nothing. The attribute is never required.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example shows a set of radio buttons with one checked by default.
|Code=<form>
	<fieldset>
		<legend>Radio buttons</legend>
		<input type="radio" name="rad" id="rad1" value="Option 1">
		<label for="rad1">Option 1</label><br>		
		<input type="radio" name="rad" id="rad2" value="Option 2" checked>
		<label for="rad2">Option 2</label><br>
		<input type="radio" name="rad" id="rad3" value="Option 3">
		<label for="rad3">Option 3</label><br>	
		<input type="radio" name="rad" id="rad4" value="Option 4">		
		<label for="rad4">Option 4</label>		
	</fieldset>
</form>
|LiveURL=http://code.webplatform.org/gist/7282321
}}{{Single Example
|Language=HTML
|Description=This example shows a set of check boxes with multiple checked by default.
|Code=<form>
	<fieldset>
		<legend>Check boxes</legend>
		<input type="checkbox" name="check1" id="check1" value="Option 1">
		<label for="check1">Option 1</label><br>		
		<input type="checkbox" name="check2" id="check2" value="Option 2" checked>
		<label for="check2">Option 2</label><br>
		<input type="checkbox" name="check3" id="check3" value="Option 3">
		<label for="check3">Option 3</label><br>	
		<input type="checkbox" name="check4" id="check4" value="Option 4"  checked>		
		<label for="check4">Option 4</label>		
	</fieldset>
</form>
|LiveURL=http://code.webplatform.org/gist/33aa4c8bece121ba6e9e
}}
}}
{{Notes_Section
|Usage=
|Notes====Remarks===
Check boxes that are not selected do not return their values when the '''form''' is submitted.

A user can select a radio button only if the button has a [[html/attributes/name|'''name''']]. A set of radio buttons is defined by the same value for the '''name''' attribute. To clear a selected radio button, a user must select another button in the set. One radio button in a set should always be checked, else the form is invalid by default. Only the value of the selected radio button is returned when the '''form''' is submitted.

Windows Internet Explorer 8 and later. In IE8 Standards mode, parsing operations on the '''checked''' content attribute always affect both the '''checked''' content attribute and [[dom/properties/defaultChecked|'''defaultChecked''']] Document Object Model (DOM) attribute. For example, [[dom/methods/removeAttribute|'''removeAttribute('checked')''']] sets both '''checked''' and '''defaultChecked''' to false. Similarly, [[dom/methods/setAttribute|'''setAttribute('checked', 'checked')''']] sets both DOM attributes to true (as if the element was being re-parsed)  For more information on IE8 mode, see Defining Document Compatibility.
Internet Explorer 8 and later. In IE8 mode, the [[dom/properties/defaultChecked|'''defaultChecked''']] DOM attribute reflects the value of the '''checked''' content attribute.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#attr-input-checked
|Status=W3C Candidate Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=HTML
|Manual_links=* [[html/elements/input/type/checkbox|'''checkbox''']] element
* [[html/elements/input/type/radio|'''radio''']] element
|External_links=* http://www.w3.org/TR/html-markup/input.radio.html
* http://www.w3.org/TR/html-markup/input.checkbox.html
|Manual_sections=
}}
{{Topics|HTML}}
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