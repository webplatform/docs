---
title: keyup
tags:
  - Events
readiness: 'Not Ready'
notes:
  - 'Summary, examples, compatibility, standards, clean-up of MSDN import'
uri: dom/KeyboardEvent/keyup

---
# keyup

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:    ?

**Needs Examples**: This section should include examples.

## Notes

### Remarks

As of Microsoft Internet Explorer 5, the event also fires for the following keys:

-   Editing: BACKSPACE
-   Navigation: PAGE UP, PAGE DOWN
-   System: SHIFT+TAB

As of Microsoft Internet Explorer 4.0, the **onkeyup** event fires for the following keys:

-   Editing: DELETE, INSERT
-   Function: F1 - F12
-   Letters: A - Z (uppercase and lowercase)
-   Navigation: HOME, END, LEFT ARROW, RIGHT ARROW, UP ARROW, DOWN ARROW
-   Numerals: 0 - 9
-   Symbols: ! @ \# \$ % \^ & \* ( ) \_ - + = \< [ ] { } , . / ? \\ | ' \` " \~
-   System: ESC, SPACEBAR, SHIFT, TAB

Returns a number specifying the **keyCode** of the key that was released. To invoke this event, do one of the following:

-   Release any keyboard key.

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

