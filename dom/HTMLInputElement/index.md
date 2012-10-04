{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{API_Object
|Subclass_of=dom/HTMLElement
}}
{{Topics|DOM}}
{{Notes_Section
|Import_Notes=
===Members===
The '''HTMLInputElement''' object has these types of members:
*[#methods Methods]
*[#properties Properties]


====Methods====
The '''HTMLInputElement''' object has these methods.
{| class="wikitable"
|-
!Method
!Description
|-
|[[dom/methods/checkValidity|'''checkValidity''']]
|Returns whether a form will validate when it is submitted, without having to submit it.
|-
|[[dom/methods/setCustomValidity|'''setCustomValidity''']]
|Sets a custom error message that is displayed when a form is submitted.
|-
|[[dom/methods/stepDown|'''stepDown''']]
|Decrements a range input control's value by the value given by the [[html/attributes/step|'''Step''']] attribute.
|-
|[[dom/methods/stepUp|'''stepUp''']]
|Increments a range input control's value by the value given by the [[html/attributes/step|'''Step''']] attribute.
|}
 

====Properties====
The '''HTMLInputElement''' object has these properties.
{| class="wikitable"
|-
!Property
!Description
|-
|[[html/attributes/autocomplete (input, form elements)|'''autocomplete''']]
|Specifies whether autocomplete is applied to an editable text field.
|-
|[[html/attributes/autofocus|'''autofocus''']]
|Provides a way to direct a user to a specific field when a document loads.
|-
|[[dom/properties/files|'''files''']]
|Returns a [[apis/file/FileList|'''FileList''']] object on a '''file type input''' object.
|-
|[[html/attributes/formAction|'''formAction''']]
|Overrides the action attribute (where  the data on a '''form''' is sent) on the parent '''form''' element.
|-
|[[html/attributes/formEnctype|'''formEnctype''']]
|Used to override the encoding ([[html/attributes/formEnctype|'''formEnctype''']] attribute) specified on the '''form''' element.
|-
|[[html/attributes/formMethod|'''formMethod''']]
|Overrides the submit '''method''' attribute previously specified on a '''form''' element.
|-
|[[html/attributes/formNoValidate|'''formNoValidate''']]
|Overrides any validation or [[html/attributes/required|'''required''']] attributes on a '''form''' or form elements to allow it to be submitted without validation.
|-
|[[dom/properties/formTarget|'''formTarget''']]
|Overrides the '''target''' attribute on a '''form''' element.
|-
|[[html/attributes/list|'''list''']]
|Specifies the ID of a pre-defined '''datalist''' of options for an input element.
|-
|[[html/attributes/max (HTMLInputElement)|'''max''']]
|Defines the maximum acceptable value for an input element with type{{=}}"number".
|-
|[[html/attributes/maxLength|'''maxLength''']]
|Sets or retrieves the maximum number of characters that the user can enter in a text control.
|-
|[[html/attributes/min|'''min''']]
|Defines the minimum acceptable value for an input element with type{{=}}"number".
|-
|[[dom/properties/multiple (type{{=}}"file")|'''multiple''']]
|When used with the '''type{{=}}"file"''' attribute, allows multiple files to be selected in the file selection dialog.
|-
|[[html/attributes/pattern|'''pattern''']]
|Gets or sets a string containing a regular expression that the user's input must match.
|-
|[[html/attributes/placeholder|'''placeholder''']]
|Gets or sets a text string that is displayed in an input field as a hint or prompt to users as the format or type of information they need to enter.
|-
|[[html/attributes/required|'''required''']]
|When present, marks an element that can't be submitted without a value.
|-
|[[dom/properties/selectionEnd|'''selectionEnd''']]
|Gets or sets  the end position or offset of a text selection.
|-
|[[dom/properties/selectionStart|'''selectionStart''']]
|Gets or sets  the starting position or offset of a text selection.
|-
|[[html/attributes/src (input, img)|'''src''']]
|Sets or retrieves a URL to be loaded by the object.
|-
|[[html/attributes/step|'''step''']]
|Defines an increment or jump between values that you want to allow the user to enter.
|-
|[[html/attributes/type|'''type''']]
|Retrieves or initially sets  the type of '''input''' control represented by the object.
|-
|[[dom/properties/validationMessage|'''validationMessage''']]
|Returns the error message that would be displayed if the user submits the form, or an empty string if no error message.
|-
|[[dom/properties/validity|'''validity''']]
|Returns a [[dom/ValidityState|''' ValidityState''']] object that represents the validity states of an element.
|-
|[[dom/properties/valueAsNumber|'''valueAsNumber''']]
|Returns the input field value as a number.
|-
|[[dom/properties/willValidate|'''willValidate''']]
|Returns whether an element will successfully validate based on forms validation rules and constraints.
|}
 
 
 
[mailto:wsddocfb@microsoft.com?subject{{=}}Documentation%20feedback [ie_htmlref\ie]:%20HTMLInputElement object%20 RELEASE:%20(7/24/2012)&amp;body{{=}}%0A%0APRIVACY STATEMENT%0A%0AThe doc team uses your feedback to improve the documentation. We don't use your email address for any other purpose. We'll remove your email address from our system after the issue that you are reporting is resolved. While we are working to resolve this issue, we may send you an email message to request more info about your feedback. After the issue is addressed, we may send you an email message to let you know that your feedback has been addressed.%0A%0AFor more info about Microsoft's privacy policy, see http://privacy.microsoft.com/en-us/default.aspx. Send comments about this topic to Microsoft]
Build date: 7/24/2012

}}
{{See_Also_Section
|Topic_clusters=input
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}