{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|Indicates the initial state of a checkbox or radio button.}}
{{Markup_Attribute
|Applies_to=[[html/elements/input]]
|Property_applies_to=dom/HTMLElement
|Content=The checked attribute can be used to specify what the visual or initial state of an input element is. It's often used to toggle an element through JavaScript.

Valid values are "<code>checked</code>" and nothing. The attribute is never required.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example shows a set of radio buttons with one checked.
|Code=<code>
<form role="form">
	<p>Radio buttons</p>
	<label for="rad1">Option 1</label>
	<input type="radio" name="rad1">
	<label for="rad2">Option 2</label>
	<input type="radio" name="rad2" checked>
	<label for="rad3">Option 3</label>
	<input type="radio" name="rad3">
	<label for="rad4">Option 4</label>
	<input type="radio" name="rad4">
</form>
</code>
|LiveURL=http://code.webplatform.org/gist/7282321
}}
}}
{{Notes_Section
|Notes====Remarks===
Check boxes that are not selected do not return their values when the '''form''' is submitted.
A user can select a radio button only if the button has a [[html/attributes/name|'''name''']]. To clear a selected radio button, a user must select another button in the set.
Windows Internet Explorer 8 and later. In IE8 Standards mode, parsing operations on the '''checked''' content attribute always affect both the '''checked''' content attribute and [[dom/properties/defaultChecked|'''defaultChecked''']] Document Object Model (DOM) attribute. For example, [[dom/methods/removeAttribute|'''removeAttribute('checked')''']] sets both '''checked''' and '''defaultChecked''' to false. Similarly, [[dom/methods/setAttribute|'''setAttribute('checked', 'checked')''']] sets both DOM attributes to true (as if the element was being re-parsed)  For more information on IE8 mode, see Defining Document Compatibility.
Internet Explorer 8 and later. In IE8 mode, the [[dom/properties/defaultChecked|'''defaultChecked''']] DOM attribute reflects the value of the '''checked''' content attribute.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5
|URL=http://www.w3.org/TR/html5/forms.html#attr-input-checked
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
|Topic_clusters=HTML
|External_links=* http://www.w3.org/TR/html-markup/input.radio.html
* http://www.w3.org/TR/html-markup/input.checkbox.html
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}