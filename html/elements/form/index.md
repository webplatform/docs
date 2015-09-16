---
title: form
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Add Category, Parent, Children and Compatibility information. Delete HTML information sub section.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLFormElement](/dom/HTMLFormElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The form element (&lt;form&gt;) defines an HTML form for user input, subsequently to be submitted to a website or service.'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/elements
    - dom/events/submit
uri: html/elements/form

---
## Summary

The form element (&lt;form&gt;) defines an HTML form for user input, subsequently to be submitted to a website or service.

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLFormElement](/dom/HTMLFormElement)

## Attributes

-   `accept-charset` = list of character-encoding names
    gives the character encodings that are to be used for the submission.

-   `action` = valid URL potentially surrounded by spaces
    Specify the form-submission action for the element.

-   `autocomplete` = on/ off
    Specifies whether the element represents a form for which by default a UA is meant to store the values entered into its input elements by the user (so that the UA can pre-fill the form later).
    -   on
        The on state indicates that the value is not particularly sensitive and the user can expect to be able to rely on his user agent to remember values he has entered for that control.
    -   off
        The off state indicates either that the control's input data is particularly sensitive (for example the activation code for a nuclear weapon); or that it is a value that will never be reused (for example a one-time-key for a bank login) and the user will therefore have to explicitly enter the data each time, instead of being able to rely on the UA to prefill the value for him; or that the document provides its own autocomplete mechanism and does not want the user agent to provide autocompletion values.

-   `enctype` = application/x-www-form-urlencoded / multipart/form-data / text/plain
    Specfy a MIME type with which a UA is meant to associate this element for form submission.
    The missing value default for these attributes is the application/x-www-form-urlencoded state.
    -   application/x-www-form-urlencoded
    -   multipart/form-data
    -   text/plain

-   `method` = get/ post
    Specify the HTTP method with which a UA is meant to associate this element for form submission.
    The missing value default for this attributes is the GET state.
    -   get
        Indicating the HTTP GET method.
    -   post
        Indicating the HTTP POST method.

-   `name` = string
    Gives the name of the input element.

-   `novalidate` = boolean
    If present, they indicate that the form is not to be validated during submission.

-   `target` = valid browsing context names or keywords
    Specfy a browsing context name or keyword that represents the target of the control.

## Examples

This example uses the **form** element to create a basic form containing a text entry box for the user's name and a select control for choosing a favorite ice cream flavor. When the user clicks the **Submit** button, the form sends the data to the URL listed in the [**action**](/html/attributes/action) attribute. The value of the [**method**](/html/attributes/method) attribute determines how to send the data to the server.

``` html
<form action="http://example.microsoft.com/sample.asp" method="post">
    Enter your name: <input name="FName"/><br/>
    Favorite Ice Cream Flavor:
    <select name="Flavor">
        <option value="Chocolate">Chocolate</option>
        <option value="Strawberry">Strawberry</option>
        <option value="Vanilla" selected="selected">Vanilla</option>
    </select>
    <p><input type="submit"/></p>
</form>
```

## Notes

### Remarks

**Security Warning:  **Using this object incorrectly can compromise the security of your application. Data submitted through a form using the HTTP protocol is not encrypted and can be read and possibly tampered with in transmission. The Secure Hypertext Transfer Protocol (HTTPS) can provide more secure data transmission. You should review the Security Considerations: Dynamic HTML before continuing. Forms enable client-side users to submit data to a server in a standardized format. The creator of a **form** designs it to collect the required data using a variety of controls, such as **input** or **select**. Users viewing the **form** fill in the data and then click the **Submit** button to send the data to the server. A script on the server then processes the data. Each control element's [**name**](/html/attributes/name_(frames)) attribute must be defined if the data is to be submitted with the form. An element in a form can be referenced by the **name** property or the [**id**](/html/attributes/id) property, or through the [**elements**](/w/index.php?title=dom/properties/elements&action=edit&redlink=1) collection. When the focus is on a control in a form and the user presses ESC, the value of the control reverts to the last value. The form resets if the user presses ESC again. If the form includes only one text box and the user presses ENTER, the [**onsubmit**](/w/index.php?title=dom/events/submit&action=edit&redlink=1) event fires. If the form has an **input type="submit"** element, it will appear as a button with a dark border, which indicates the user can press ENTER to submit the form. Windows Internet Explorer 8 and later. The value of the [**action**](/html/attributes/action) attribute depends on the current document compatibility mode. In addition, the **form object** now supports [**enctype**](/html/attributes/enctype) as a DOM attribute.

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-form-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-form-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-FORM)
:   W3C Recommendation

## See also

### Related pages

-   `1,001 Ways to Get Input from Web Users`

 }

}
