---
title: type
tags:
  - Markup
  - Attributes
  - HTML
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
summary: 'The type attribute is used to define what sort of type an input or ordered list element is.'
uri: html/attributes/type
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/createElement

---
# type

## Summary

The type attribute is used to define what sort of type an input or ordered list element is.

Applies to
:   [HTMLInputElement](/html/elements/input) [OLElement](/html/elements/ol)

In general the type attribute is used for \<input\> and for \<ol\> elements.
 As with HTML5 the attribute is no longer deprecated for \<ol\> elements.

### \<input\>

The type attribute specifies the type of an \<input\> element to display. There are several possible types like text, button or submit.

The default type for an \<input\> element is: text. The attribute is not required, but it is recommended to include the attribute to prevent misunderstandings.

An input element with a type attribute whose value is:

-   **"button"**: represents a button with no default behavior
-   **"checkbox"**: represents a state or option that can be toggled
-   **"checkbox"**: represents a state or option that can be toggled
-   **"color"**: provides a widget for selecting a color value
-   **"date"**: represents a widget for specifying a date value (year, month, day), with no time zone or time information
-   **"datetime"**: represents a widget for setting a date-time value (year, month, day, hours, minutes, seconds, milliseconds) based on UTC time zone
-   **"datetime-local"**: represents a widget for setting a date-time value (year, month, day, hours, minutes, seconds, milliseconds) with no time zone information
-   **"email"**: represents a field for entering an e-mail address
-   **"file"**: represents a widget for specifying a file
-   **"hidden"**: represents a value that is hidden from the user, but which is sent with the form data; the value can be set programatically
-   **"image"**: represents an image. The user can either use the image as a button to submit the form, or select a coordinate of the image to be submitted with the form data
-   **"month"**: represents a widget for entering a month value
-   **"number"**: represents a widget for entering a number
-   **"password"**: represents a one-line plain-text edit control for entering a password, which renders input text in such a way as to hide the characters (e.g., a series of asterisks)
-   **"radio"**: represents a radio button control
-   **"range"**: represents a field for setting a number value that falls in a given range
-   **"reset"**: represents a form button that resets the form to default values
-   **"search"**: represents an input text field that is used for search queries
-   **"submit"**: represents a form button that submits the form data to the server
-   **"tel"**: represents an input field intended for entering a telephone number; does not enforce any syntax
-   **"text"**: represents a one-line plain text edit control for the input element’s value
-   **"radio"**: represents an input field for entering a specific time value
-   **"url"**: represents an input field for entering a single, absolute URL value
-   **"week"**: represents an input field for entering a value that represents a specific week

### \<ol\>

For \<ol\> elements the type attribute is used to specify the kind of marker to use in the list.
 As default the list will be marked with decimal numbers (1, 2, 3, ...).

Possible attribute values are the following:

-   "1": for decimal numbers (1, 2, 3, ...)
-   "a": for lowercase, alphabetically ordered list (a, b, c, ...)
-   "A": for uppercase, alphabetically ordered list (A, B, C, ...)
-   "i": for lowercase, roman numbered list (i, ii, iii, iv, ...)
-   "I": for uppercase, roman numbered list (I, II, III, IV, ...)

## Examples

Type attributes used in a form.

``` {.html}

<form>
    Text: <input type="text" name="textInput">
    Color: <input type="color" value="#ff0000" name="colorInput"/>
    Date: <input type="date" value="2013-09-03" name="dateInput">
    Datetime: <input type="datetime" name="datetimeInput">
    Datetime-local: <input type="datetime-local" value="2013-09-03T20:00" name="datetime-local">
    Email: <input type="email" name="emailInput">
    File: <input type="file" name="fileInput">
    Hidden: <input type="hidden" name="hiddenInput">
    Month: <input type="month" value="2013-09" name="monthInput">
    Number: <input type="number" name="numberInput">
    Password: <input type="password" name="passwordInput">
    Checkbox: <input type="checkbox" name="checkboxInput" id="checkboxId1" checked><label for="checkboxId1">label 1</label>
    <input type="checkbox" name="checkboxInput" id="checkboxId2"><label for="checkboxId2">label 2</label>
    Radio: <input type=radio name="radioInput" id="radioId1" checked><label for="radioId1">label 1</label>
    <input type=radio name="radioInput" id="radioId2"><label for="radioId2">label 2</label>
    Range: <input type="range" name="rangeInput">
    Search: <input type="search" name="searchInput">
    Tel: <input type="tel" name="telInput">
    Time: <input type="time" name="timeInput">
    Url: <input type="url" name="urlInput">
    Week: <input type="week" name="weekInput">
    Image: <input type="image" name="imageInput">
    Button: <input type="button" value="Button" onclick="alert('This is a javascript alert')">
    Reset: <input type="reset" value="Reset">
    Submit: <input type="submit" value="Submit">
</form>
```

Type attribute for lowercase, roman numbering used in an ordered list.

``` {.html}
<ol type="i">
<li>First list item</li>
<li>Second list item</li>
<li>Third list item</li>
<li>Forth list item</li>
<li>Fifth list item</li>
</li>
```

## Notes

### Remarks

Only the **type** property is writeable. The **type** property is read/write-once, but only when an **input** element is created with the [**createElement**](/w/index.php?title=dom/methods/createElement&action=edit&redlink=1) method and before it is added to the document.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7
-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5
-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 17.4

## See also

### Related pages (MSDN)

-   `HTMLInputElement`
-   `input type=button`
-   `input type=checkbox`
-   `input type=email`
-   `input type=file`
-   `input type=hidden`
-   `input type=image`
-   `input type=number`
-   `input type=password`
-   `input type=range`
-   `input type=radio`
-   `input type=reset`
-   `input type=search`
-   `input type=submit`
-   `input type=tel`
-   `input type=text`
-   `input type=url`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

