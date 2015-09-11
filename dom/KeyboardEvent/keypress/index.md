---
title: keypress
code_samples:
  - 'http://gist.github.com/8631904'
notes:
  - 'General cleanup, compatibility'
readiness: 'Almost Ready'
standardization_status: Deprecated
summary: 'Deprecated event for detecting when a key was pressed on the keyboard.'
tags:
  - Events
  - DOM
  - DOMEvents
uri: dom/KeyboardEvent/keypress

---
## <span>Summary</span>

Deprecated event for detecting when a key was pressed on the keyboard.

## <span>Overview Table</span>

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
[dom/Element](/dom/Element), [dom/Document](/dom/Document)

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
Yes

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
Varies: launch text composition system; blur and focus events; DOMActivate event; other event

</td>
</tr>
</table>
This event used to be used to detect when a key value was inserted into the DOM. Developers should use beforeInput, keyup, or keydown events depending on the task instead of this event.

### <span>Context information</span>

`Event.target`
:   focused element which triggered the key event. This will be the root element if no suitable input element is focused.
`KeyboardEvent.charCode`
:   legacy character code value for the event
`KeyboardEvent.keyCode`
:   legacy numerical code for the key pressed
`KeyboardEvent.which`
:   legacy numerical code for the key pressed
`KeyboardEvent.key`
:   The key value of the key pressed
 `KeybaordEvent.location`
:   The location of the key on the device
 `KeyboardEvent.altKey`
:   true if 'Alt' modifier was active, otherwise false
 `KeyboardEvent.shiftKey`
:   true if 'Shift' modifier was active, otherwise false
 `KeyboardEvent.ctrlKey`
:   true if 'Control' modifier was active, otherwise false
 `KeyboardEvent.metaKey`
:   true if 'Meta' modifier was active, otherwise false
 `KeyboardEvent.repeat`
:   true if a key has been depressed long enough to trigger key repetition, otherwise false.

## <span>Examples</span>

``` js
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <title>Keypress event demonstration</title>
    <style>
        // this styling only exists so things look better on code.webplatform.org
        form {
            padding-top: 30px;
        }
    </style>
</head>
<body>
    <form>
        <label for="keypress">Keypress</label>
        <input name="keypress"/>
    </form>
    <div id="target">
        <p>The last key code you entered for keypress is: <span id="keypressEcho"></span></p>
    </div>

    <script>
    // Getting the target elements from the DOM that we would like to mess with.
    var keypressInput = document.getElementsByName('keypress')[0];
    var keypressTarget = document.getElementById('keypressEcho');

    // This is going to run the function whenever a keypress event occurs on the Input element.
    keypressInput.addEventListener('keypress', function(e) {
        //Change the text of the target element to be the number of the key pressed. (number is based on the ASCII key standard.)
        keypressTarget.textContent = e.which;
        // Log the key event as well.
        console.log(e.which);
    });
    </script>
</body>
</html>
```

[View live example](http://code.webplatform.org/gist/8631904)

## <span>Usage</span>

     ===Related event order===

1.  keydown
2.  beforeInput
3.  keypress
4.  input
5.  keyup

## <span>See also</span>

### <span>Other articles</span>

-   `onkeydown`
-   `onkeyup`

### <span>External resources</span>

-   [DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/#event-type-keypress)
