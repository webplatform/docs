---
title: 'alert'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[window.alert](https://developer.mozilla.org/en-US/docs/Web/API/Window.alert) Article]'
  - 'Microsoft Developer Network: [[alert Method](http://msdn.microsoft.com/en-us/library/ie/ms535933(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
standardization_status: Non-Standard
summary: 'Displays a synchronized dialog box showing the given text and a localized OK button.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Window/alert

---
## Summary

Displays a synchronized dialog box showing the given text and a localized OK button.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
 window.alert(/* see parameter list */);
```

## Parameters

### message

 Data-type
:   String

 The message to display in the dialog box.

## Return Value

No return value

## Examples

``` js
window.alert('A message from the web page');
```

## Usage

     Not recommended for general use. See the notes for details.

Use this method to alert the user with some text.

## Notes

-   You cannot change the title bar of the Alert dialog box.
-   Not recommended due to the following issues -
    -   This is a synchronized method call. Meaning, calling this method pauses scripting execution of the window from which this method is called, until the user closes the displayed dialog. Also, depending on your cross tab/window usage, this can sometimes pause scripting executions of other windows/tabs from the same domain.
    -   Calling this method in some browsers prevents the user from interacting with the entire browser, or browser window (along with all of its tabs), until the dialog is closed.
    -   Intrusive dialog boxes are generally annoying for the user.

Alternatively, create a dialog using other web platform means.
