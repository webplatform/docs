{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/HTMLInputElement
}}
{{Topics|DOM}}
{{Examples_Section
|Not_required=No
|Examples=}}
{{Notes_Section
|Notes=
===Remarks===
The following example displays all validation states for a validated field.
|Import_Notes=
===Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.21.3


===Members===
The '''ValidityState''' object has these types of members:
*[#properties Properties]


====Properties====
The '''ValidityState''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[dom/properties/customError|'''customError''']]
|Returns whether the input field has raised a custom error.
|-
|[[dom/properties/patternMismatch|'''patternMismatch''']]
|Returns whether the input field value does not match the rules defined by the pattern attribute.
|-
|[[dom/properties/rangeOverflow|'''rangeOverflow''']]
|Returns whether a value is greater than the '''max''' attribute on an input control.
|-
|[[dom/properties/rangeUnderflow|'''rangeUnderflow''']]
|A value is less than the '''min''' attribute on an input control.
|-
|[[dom/properties/stepMismatch|'''stepMismatch''']]
|Returns whether the input field value does not fit the rules given by the '''step''' attribute.
|-
|[[dom/properties/tooLong|'''tooLong''']]
|Returns whether an input field's value is longer than is allowed by the '''maxlength''' attribute.
|-
|[[dom/properties/typeMismatch|'''typeMismatch''']]
|Returns whether the input field value is not the correct syntax.
|-
|[[dom/properties/valid|'''valid''']]
|Returns whether the input field value has any validity errors.
|-
|[[dom/properties/valueMissing|'''valueMissing''']]
|Returns whether a value has not been entered in an input field that is required.
|}
 

}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}