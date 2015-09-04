---
title: keydown
tags:
  - Events
  - DOM
readiness: 'In Progress'
notes:
  - 'Summary, compatibility, standards, clean-up of MSDN import'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onkeydown.htm'
uri: dom/KeyboardEvent/keydown

---
# keydown

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

## Examples

This example uses the **onkeydown** event to cancel input from the keyboard.

    <script type="text/javascript">
    function fnTrapKD(){
       if(oTrap.checked){
          oOutput.innerText+="[trap = " + event.keyCode + "]";
          event.returnValue=false;
       }
       else{
          oOutput.innerText+=String.fromCharCode(event.keyCode);
       }
    }
    </script>
    <input type="checkbox" id="oTrap">
    <input id="oExample" type="text" onkeydown="fnTrapKD()">
    <textarea id="oOutput" rows="10" cols="50">
    </textarea>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onkeydown.htm)

## Notes

### Remarks

You can cancel all keys that fire the **onkeydown** event in HTML Applications, including most accelerator keys, such as ALT+F4. As of Microsoft Internet Explorer 5, the event also fires for the following keys:

-   Editing: BACKSPACE
-   Navigation: PAGE UP, PAGE DOWN
-   System: SHIFT+TAB

As of Internet Explorer 5, this event can be canceled for the following keys and key combinations by specifying **event.returnValue=false**:

-   Editing: BACKSPACE, DELETE
-   Letters: A - Z (uppercase and lowercase)
-   Navigation: PAGE UP, PAGE DOWN, END, HOME, LEFT ARROW, RIGHT ARROW, UP ARROW, DOWN ARROW
-   Numerals: 0 - 9
-   Symbols: ! @ \# \$ % \^ & \* ( ) \_ - + = \< [ ] { } , . / ? \\ | ' \` " \~
-   System: SPACEBAR, ESC, TAB, SHIFT+TAB

As of Microsoft Internet Explorer 4.0, the **onkeydown** event fires for the following keys:

-   Editing: DELETE, INSERT
-   Function: F1 - F12
-   Letters: A - Z (uppercase and lowercase)
-   Navigation: HOME, END, LEFT ARROW, RIGHT ARROW, UP ARROW, DOWN ARROW
-   Numerals: 0 - 9
-   Symbols: ! @ \# \$ % \^ & \* ( ) \_ - + = \< [ ] { } , . / ? \\ | ' \` " \~
-   System: ESC, SPACEBAR, SHIFT, TAB

In Internet Explorer 4.0, you cannot cancel the **onkeydown** event, but you can use the [**onkeypress**](/dom/KeyboardEvent/keypress) event to cancel keyboard events. Returns a number specifying the **keyCode** of the key that was pressed. To invoke this event, do one of the following:

-   Press any keyboard key.

### Syntax

### Standards information

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

