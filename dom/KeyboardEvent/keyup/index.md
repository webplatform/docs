---
title: keyup
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Summary, examples, compatibility, standards, clean-up of MSDN import'
readiness: 'Not Ready'
tags:
  - Events
uri: dom/KeyboardEvent/keyup

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
 ?

</td>
</tr>
</table>
**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

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

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML 4.01 Specification](http://go.microsoft.com/fwlink/p/?linkid=25320), Section 18.2.3

### <span>Event handler parameters</span>

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

