{{Page_Title}}
{{Flags
|State=In Progress
|Editorial notes=
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The <code>select</code> element is used to create a drop-down list. Used with <code>option</code> tags inside the <code>select</code> element to define the available options in the list.}}
{{Markup_Element
|DOM_interface=dom/HTMLSelectElement
|Tag_omissions=Closing tag required
|CSS_display=inline
|Content=== Attributes ==
*<code>autofocus</code> = boolean<br />Allows the author to indicate that a control is to be focused as soon as the page is loaded
*<code>disabled</code> = boolean<br />If present, make the control non-interactive and to prevent its value from being submitted.
*<code>form</code> = the ID of a form element in the element's owner<br />Associate the select element with its form owner.<br />By default, the select element is associated with its nearest ancestor form element.
*<code>multiple</code> = boolean<br />If the attribute is present, then the select element represents a control for selecting zero or more options from the list of options. [[#Example_B|[Example B]]]
*<code>name</code> = unique name<br />Represents the element's name.
*<code>required</code> = boolean<br />When specified, the user will be required to select a value before submitting the form.
*<code>size</code> = valid non-negative intege<br />Gives the number of options to show to the user.<br />If the multiple attribute is present, then the size attribute's default value is 4. If the multiple attribute is absent, then the size attribute's default value is 1.

== Internationalization ==

Internationalization topics related to the <code>select</code> element:
* [http://www.w3.org/International/techniques/authoring-html#linkloc Linking to localized content]
* [http://www.w3.org/International/techniques/authoring-html#formcontrols Working with form controls] (specifically sorting of select options)
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=This example uses the '''SELECT''' element to create a drop-down list box.
|Code=<nowiki><select name="Cats" size="1">
<option value="1">Calico</option>
<option value="2">Tortie</option>
<option value="3" selected>Siamese</option>
</select></nowiki>
|LiveURL=
}}{{Single Example
|Language=HTML
|Description=This example uses the '''select''' element to create a multi-select list box by setting the [[html/attributes/size (control)|'''SIZE''']] and [[html/attributes/multiple|'''MULTIPLE''']] attributes. To retrieve the selected options for a multi-select list box, iterate through the [[dom/HTMLElement/options|'''options''']] collection and check to see where [[html/attributes/selected|'''SELECTED''']] is set to '''true'''.
|Code=<nowiki><select id="select-element" name="cars" size="3" multiple="">
<option value="1" selected="">BMW</option>
<option value="2">Porsche</option>
<option value="3" selected>Mercedes</option>
</select></nowiki>
|LiveURL=
}}{{Single Example
|Language=JavaScript
|Description=This JavaScript example adds a new option to the end of the '''SELECT''' list created above. The [[dom/Option|Option]] constructor can also be used in JavaScript.
|Code=var option {{=}} document.createElement("OPTION");
option.text{{=}}"Ferrari";
option.value{{=}}"4";
document.getElementById("select-element").add(option);
|LiveURL=
}}
}}
{{Notes_Section
|Usage=
|Notes=In the Browser app for Android 4.1 (and possibly later versions), there is a bug where the menu indicator triangle on the side of a '''select''' will not be displayed if a <code>[[css/properties/background|background]]</code>, <code>[[css/properties/border|border]]</code>, or <code>[[css/properties/border-radius|border-radius]]</code> style is applied to the '''select'''.

Firefox for Android, by default, sets a <code>[[css/properties/background-image|background-image]]</code> gradient on all <code>&lt;select multiple&gt;</code> elements. This can be disabled using <code>background-image: none</code>.
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-select-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-select-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/interact/forms.html#edef-SELECT
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
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
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=5 - 6
|Note=The element is always on top, regardless of the value of its '''z-index''' CSS property.
}}
}}