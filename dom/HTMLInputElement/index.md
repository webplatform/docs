{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Represents an [[html/elements/input|input]] element within the DOM.}}
{{API_Object
|Subclass_of=dom/HTMLElement
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section
|Import_Notes====Additional Members (MSDN)===
The '''HTMLInputElement''' object has these types of members:
[[#Additional_Methods|Additional Methods]]
[[#Additional_Properties|Additional Properties]]


====Additional Methods====
The '''HTMLInputElement''' object has these methods.
{{{!}} class="wikitable"
{{!}}-
!Method
!Description
{{!}}-
{{!}}[[dom/methods/checkValidity|'''checkValidity''']]
{{!}}Returns whether a form will validate when it is submitted, without having to submit it.
{{!}}-
{{!}}[[dom/methods/setCustomValidity|'''setCustomValidity''']]
{{!}}Sets a custom error message that is displayed when a form is submitted.
{{!}}-
{{!}}[[dom/methods/stepDown|'''stepDown''']]
{{!}}Decrements a range input control's value by the value given by the [[html/attributes/step|'''Step''']] attribute.
{{!}}-
{{!}}[[dom/methods/stepUp|'''stepUp''']]
{{!}}Increments a range input control's value by the value given by the [[html/attributes/step|'''Step''']] attribute.
{{!}}}
 

====Additional Properties====
The '''HTMLInputElement''' object has these properties.
{{{!}} class="wikitable"
{{!}}-
!Property
!Description
{{!}}-
{{!}}[[html/attributes/autocomplete (input, form elements)|'''autocomplete''']]
{{!}}Specifies whether autocomplete is applied to an editable text field.
{{!}}-
{{!}}[[html/attributes/autofocus|'''autofocus''']]
{{!}}Provides a way to direct a user to a specific field when a document loads.
{{!}}-
{{!}}[[dom/properties/files|'''files''']]
{{!}}Returns a [[apis/file/FileList|'''FileList''']] object on a '''file type input''' object.
{{!}}-
{{!}}[[html/attributes/formAction|'''formAction''']]
{{!}}Overrides the action attribute (where  the data on a '''form''' is sent) on the parent '''form''' element.
{{!}}-
{{!}}[[html/attributes/formEnctype|'''formEnctype''']]
{{!}}Used to override the encoding ([[html/attributes/formEnctype|'''formEnctype''']] attribute) specified on the '''form''' element.
{{!}}-
{{!}}[[html/attributes/formMethod|'''formMethod''']]
{{!}}Overrides the submit '''method''' attribute previously specified on a '''form''' element.
{{!}}-
{{!}}[[html/attributes/formNoValidate|'''formNoValidate''']]
{{!}}Overrides any validation or [[html/attributes/required|'''required''']] attributes on a '''form''' or form elements to allow it to be submitted without validation.
{{!}}-
{{!}}[[dom/properties/formTarget|'''formTarget''']]
{{!}}Overrides the '''target''' attribute on a '''form''' element.
{{!}}-
{{!}}[[html/attributes/list|'''list''']]
{{!}}Specifies the ID of a pre-defined '''datalist''' of options for an input element.
{{!}}-
{{!}}[[html/attributes/max (HTMLInputElement)|'''max''']]
{{!}}Defines the maximum acceptable value for an input element with type{{=}}"number".
{{!}}-
{{!}}[[html/attributes/maxLength|'''maxLength''']]
{{!}}Sets or retrieves the maximum number of characters that the user can enter in a text control.
{{!}}-
{{!}}[[html/attributes/min|'''min''']]
{{!}}Defines the minimum acceptable value for an input element with type{{=}}"number".
{{!}}-
{{!}}[[dom/properties/multiple (type{{=}}"file")|'''multiple''']]
{{!}}When used with the '''type{{=}}"file"''' attribute, allows multiple files to be selected in the file selection dialog.
{{!}}-
{{!}}[[html/attributes/pattern|'''pattern''']]
{{!}}Gets or sets a string containing a regular expression that the user's input must match.
{{!}}-
{{!}}[[html/attributes/placeholder|'''placeholder''']]
{{!}}Gets or sets a text string that is displayed in an input field as a hint or prompt to users as the format or type of information they need to enter.
{{!}}-
{{!}}[[html/attributes/required|'''required''']]
{{!}}When present, marks an element that can't be submitted without a value.
{{!}}-
{{!}}[[dom/properties/selectionEnd|'''selectionEnd''']]
{{!}}Gets or sets  the end position or offset of a text selection.
{{!}}-
{{!}}[[dom/properties/selectionStart|'''selectionStart''']]
{{!}}Gets or sets  the starting position or offset of a text selection.
{{!}}-
{{!}}[[html/attributes/src (input, img)|'''src''']]
{{!}}Sets or retrieves a URL to be loaded by the object.
{{!}}-
{{!}}[[html/attributes/step|'''step''']]
{{!}}Defines an increment or jump between values that you want to allow the user to enter.
{{!}}-
{{!}}[[html/attributes/type|'''type''']]
{{!}}Retrieves or initially sets  the type of '''input''' control represented by the object.
{{!}}-
{{!}}[[dom/properties/validity|'''validity''']]
{{!}}Returns a [[dom/ValidityState|''' ValidityState''']] object that represents the validity states of an element.
{{!}}-
{{!}}[[dom/properties/valueAsNumber|'''valueAsNumber''']]
{{!}}Returns the input field value as a number.
{{!}}-
{{!}}[[dom/properties/willValidate|'''willValidate''']]
{{!}}Returns whether an element will successfully validate based on forms validation rules and constraints.
{{!}}}
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
{{See_Also_Section}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}