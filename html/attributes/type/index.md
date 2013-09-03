{{Page_Title|type}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|The type attribute is used to define what sort of type an input or ordered list element is.}}
{{Markup_Attribute
|Applies_to=html/elements/ol html/elements/input
|Property_applies_to=dom/HTMLElement
|Content=In general the type attribute is used for &lt;input&gt; and for &lt;ol&gt; elements.<br />
As with HTML5 the attribute is no longer deprecated for &lt;ol&gt; elements.

=== &lt;input&gt; ===
The type attribute specifies the type of an &lt;input&gt; element to display. There are several possible types like text, button or submit.

The default type for an &lt;input&gt; element is: text. The attribute is not required, but it is recommended to include the attribute to prevent misunderstandings.

An input element with a type attribute whose value is "button" represents a button with no default behavior.

An input element with a type attribute whose value is "checkbox" represents a state or option that can be toggled.

An input element with a type attribute whose value is "color" provides a widget for selecting a color value.

An input element with a type attribute whose value is "date" represents a widget for specifying a date value (year, month, day), with no time zone or time information.

An input element with a type attribute whose value is "datetime" represents a widget for setting a date-time value (year, month, day, hours, minutes, seconds, milliseconds) based on UTC time zone.

An input element with a type attribute whose value is "datetime-local" represents a widget for setting a date-time value (year, month, day, hours, minutes, seconds, milliseconds) with no time zone information.

An input element with a type attribute whose value is "email" represents a field for entering an e-mail address.

An input element with a type attribute whose value is "file" represents a widget for specifying a file.

An input element with a type attribute whose value is "hidden" represents a value that is hidden from the user, but which is sent with the form data; the value can be set programatically.

An input element with a type attribute whose value is "image" represents an image. The user can either use the image as a button to submit the form, or select a coordinate of the image to be submitted with the form data.

An input element with a type attribute whose value is "month" represents a widget for entering a month value.

An input element with a type attribute whose value is "number" represents a widget for entering a number.

An input element with a type attribute whose value is "password" represents a one-line plain-text edit control for entering a password, which renders input text in such a way as to hide the characters (e.g., a series of asterisks).

An input element with a type attribute whose value is "radio" represents a radio button control.

An input element with a type attribute whose value is "range" represents a field for setting a number value that falls in a given range.

An input element with a type attribute whose value is "reset" represents a form button that resets the form to default values.

An input element with a type attribute whose value is "search" represents an input text field that is used for search queries.

An input element with a type attribute whose value is "submit" represents a form button that submits the form data to the server.

An input element with a type attribute whose value is "tel" represents an input field intended for entering a telephone number; does not enforce any syntax.

An input element with a type attribute whose value is "text" represents a one-line plain text edit control for the input element’s value.

An input element with a type attribute whose value is "radio" represents an input field for entering a specific time value.

An input element with a type attribute whose value is "url" represents an input field for entering a single, absolute URL value.

An input element with a type attribute whose value is "week" represents an input field for entering a value that represents a specific week.


=== &lt;ol&gt; ===
For &lt;ol&gt; elements the type attribute is used to specify the kind of marker to use in the list.<br />
As default the list will be marked with decimal numbers (1, 2, 3, ...).

Possible attribute values are the following:<br />
"1" for decimal numbers (1, 2, 3, ...)<br />
"a" for lowercase, alphabetically ordered list (a, b, c, ...)<br />
"A" for uppercase, alphabetically ordered list (A, B, C, ...)<br />
"i" for lowercase, roman numbered list (i, ii, iii, iv, ...)<br />
"I" for uppercase, roman numbered list (I, II, III, IV, ...)
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Type attributes used in a form.
|Code=<form>
    Text: <input type="text" name="textInput"> <br/>
     <br/>	
    Color: <input type="color" value="#ff0000" name="colorInput"/> <br/>
    Date: <input type="date" value="2013-09-03" name="dateInput"> <br/>
    Datetime: <input type="datetime" name="datetimeInput"> <br/>
    Datetime-local: <input type="datetime-local" value="2013-09-03T20:00" name="datetime-local"> <br/>
    Email: <input type="email" name="emailInput"> <br/>
    File: <input type="file" name="fileInput"> <br/>
    Hidden: <input type="hidden" name="hiddenInput"> <br/>
    Month: <input type="month" value="2013-09" name="monthInput"> <br/>
    Number: <input type="number" name="numberInput"> <br/>
    Password: <input type="password" name="passwordInput"> <br/>
    Checkbox: <input type="checkbox" name="checkboxInput" id="checkboxId1" checked><label for="checkboxId1">label 1</label>
    <input type="checkbox" name="checkboxInput" id="checkboxId2"><label for="checkboxId2">label 2</label> <br/>
    Radio: <input type=radio name="radioInput" id="radioId1" checked><label for="radioId1">label 1</label>
    <input type=radio name="radioInput" id="radioId2"><label for="radioId2">label 2</label> <br/>
    Range: <input type="range" name="rangeInput"> <br/>
    Search: <input type="search" name="searchInput"> <br/>
    Tel: <input type="tel" name="telInput"> <br/>
    Time: <input type="time" name="timeInput"> <br/>
    Url: <input type="url" name="urlInput"> <br/>
    Week: <input type="week" name="weekInput"> <br/>
    <br/>
    Image: <input type="image" name="imageInput"> <br/>
    Button: <input type="button" value="Button" onclick="alert('This is a javascript alert')"> <br/>
    Reset: <input type="reset" value="Reset"> <br/>
    <br />
    Submit: <input type="submit" value="Submit"> <br/>
</form>
}}{{Single Example
|Language=HTML
|Description=Type attribute for lowercase, roman numbering used in an ordered list.
|Code=&lt;ol type{{=}}"i"&gt;
&lt;li&gt;First list item&lt;/li&gt;
&lt;li&gt;Second list item&lt;/li&gt;
&lt;li&gt;Third list item&lt;/li&gt;
&lt;li&gt;Forth list item&lt;/li&gt;
&lt;li&gt;Fifth list item&lt;/li&gt;
&lt;/li&gt;
}}
}}
{{Notes_Section
|Notes====Remarks===
Only the '''type''' property is writeable.
The '''type''' property is read/write-once, but only when an '''input''' element is created with the [[dom/methods/createElement|'''createElement''']] method and before it is added to the document.
|Import_Notes====Syntax===
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}221374 HTML5 A vocabulary and associated APIs for HTML and XHTML], Section 4.10.7
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}161725 Document Object Model (DOM) Level 1 Specification], Section 2.5.5
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}25320 HTML 4.01 Specification], Section 17.4
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
*<code>input type{{=}}button</code>
*<code>input type{{=}}checkbox</code>
*<code>[[html/elements/input/type/email|input type{{=}}email]]</code>
*<code>input type{{=}}file</code>
*<code>input type{{=}}hidden</code>
*<code>input type{{=}}image</code>
*<code>[[html/elements/input/type/number|input type{{=}}number]]</code>
*<code>input type{{=}}password</code>
*<code>[[html/elements/input/type/range|input type{{=}}range]]</code>
*<code>input type{{=}}radio</code>
*<code>input type{{=}}reset</code>
*<code>[[html/elements/input/type/search|input type{{=}}search]]</code>
*<code>input type{{=}}submit</code>
*<code>[[html/elements/input/type/tel|input type{{=}}tel]]</code>
*<code>input type{{=}}text</code>
*<code>[[html/elements/input/type/url|input type{{=}}url]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}