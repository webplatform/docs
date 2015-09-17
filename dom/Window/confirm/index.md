---
title: 'confirm'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[confirm](https://developer.mozilla.org/en-US/docs/Web/API/window.confirm) Article]'
  - 'Microsoft Developer Network: [[confirm Method](http://msdn.microsoft.com/en-us/library/ie/ms536376(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/Window
summary: 'Displays a synchronized confirmation dialog box showing the given text and possibly localized OK and Cancel buttons.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Window/confirm

---
## Summary

Displays a synchronized confirmation dialog box showing the given text and possibly localized OK and Cancel buttons.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
var confirmed = window.confirm(/* see parameter list */);
```

## Parameters

### message

 Data-type
:   String

 The message to display in the confirmation dialog box. If no value is provided, the dialog box does not contain a message.

## Return Value

Returns an object of type BooleanBoolean

Whether the user confirmed (clicked on OK).

## Examples

``` js
if(window.confirm('Do you want to contine?')){
// Next action
}else{
// Return to previous
}
```

## Usage

     Not recommended for general use. See the notes for details.

Use this method to let the user confirm some action.

## Notes

-   The title bar of the confirmation dialog box cannot be changed.
-   Not recommended due to the following issues -
    -   This is a synchronized method call. Meaning, calling this method pauses scripting execution of the window from which this method is called, until the user closes the displayed dialog. Also, depending on your cross tab/window usage, this can sometimes pause scripting executions of other windows/tabs from the same domain.
    -   Calling this method in some browsers prevents the user from interacting with the entire browser, or browser window (along with all of its tabs), until the dialog is closed.
    -   Intrusive dialog boxes are generally annoying for the user.

Alternatively, create a dialog using other web platform means.
