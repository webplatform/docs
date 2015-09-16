---
title: initTextEvent
attributions:
  - 'Microsoft Developer Network: [[initTextEvent Method](http://msdn.microsoft.com/en-us/library/ie/ff975268(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/TextEvent
    href: /dom/TextEvent
summary: 'Initializes a new text event that the createEvent method created.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/TextEvent/initTextEvent

---
## Summary

Initializes a new text event that the createEvent method created.

Method of [dom/TextEvent](/dom/TextEvent)[dom/TextEvent](/dom/TextEvent)

## Syntax

``` js
 event.initTextEvent(/* see parameter list */);
```

## Parameters

### eventType

 Data-type
:   String

 The name of the event. Sets the value for the [**type**](/dom/Event/type) property. This parameter is case sensitive! Sets the type property of the event object.

For IE9 or higher use 'textinput' For Webkit use 'textInput'.

### canBubble

 Data-type
:   Boolean

 Whether the event propagates upward. Sets the value for the [bubbles](/dom/Event/bubbles) property.

### cancelable

 Data-type
:   Boolean

 Whether the event is cancelable and so [preventDefault](/dom/Event/preventDefault) can be called. Sets the value for the [cancelable](/dom/Event/cancelable) property.

### view

 Data-type
:   Object

 The window on which this event is occurring. Sets the value for the [view](/dom/UIEvent/view) property.

### data

 Data-type
:   String

 Character data. Sets the value for the [**data**](/dom/CompositionEvent/data) property.

### inputMethod

 Data-type
:   Number

 The input mode for the text. Sets the value for the [**inputMethod**](/dom/TextEvent/inputMethod) property.

Required in Internet Explorer, not supported and omitted in Safari and Google Chrome. Integer that specifies the input mode for the text.

### locale

 Data-type
:   String

 The locale name. Sets the value for the [**locale**](/dom/CompositionEvent/locale) property.

Required in Internet Explorer, not supported and omitted in Safari and Google Chrome. String that specifies the locale name of the text.

## Return Value

No return value

## Examples

The below sample shows a click event handler that creates and dispatches either a 'textinput' or 'textInput' event (depending on the selected options) to textarea element.

``` js
function InsertText () {
        try {
            var newtextEvent = document.createEvent('TextEvent');
            var textarea = document.getElementById ("textarea");
            var intputmethod=eval(document.getElementById('cboinputmethod').value);
            if(document.forms.frmTextEvent.chkontextinput.checked){
            //var retval = TextEvent.initTextEvent(eventType, canBubble, cancelable, viewArg, dataArg, inputMethod, locale);
                newtextEvent.initTextEvent ('textinput', true, true, null, "New text", intputmethod, "en-US");
            }
            else if(document.forms.frmTextEvent.chkontextInput.checked){
                newtextEvent.initTextEvent ('textInput', true, true, null, "New text", intputmethod, "en-US");
            }else{
                alert('First choose the textinput or textInput event handler.'); return;
            }
            //var selObj=window.getSelection();
            textarea.focus();
            textarea.selectionStart = 0;
            textarea.selectionEnd = 0;

            textarea.dispatchEvent(newtextEvent);
        }
        catch (e) {
            alert ('Your browser does not support this example!\nError :'+e);
        }
    }


// Outputs 'New text' at the beginning of the text area in Safari and Chromium
// Outputs nothing at the beginning of a the text area in MSIE browsers as DOM_INPUT_METHOD_SCRIPT is not a trusted (event.isTrusted) textinput input method.
```

The DOMInputMetod is present in the MSIE 'textinput' event handler only.

``` js
function getDOMInputMethod(iInputMethod){
        switch (iInputMethod){
            case TextEvent.DOM_INPUT_METHOD_UNKNOWN:// 0
                return 'Unknown';
            case TextEvent.DOM_INPUT_METHOD_KEYBOARD:// 1
                return 'Keyboard';
            case TextEvent.DOM_INPUT_METHOD_PASTE:// 2
                return 'Paste';
            case TextEvent.DOM_INPUT_METHOD_DROP:// 3
                return 'Drop';
            case TextEvent.DOM_INPUT_METHOD_IME:// 4
                return 'IME';
            case TextEvent.DOM_INPUT_METHOD_OPTION:// 5
                return 'Option';
            case TextEvent.DOM_INPUT_METHOD_HANDWRITING:// 6
                return 'Handwriting';
            case TextEvent.DOM_INPUT_METHOD_VOICE://7
                return 'Voice';
            case TextEvent.DOM_INPUT_METHOD_MULTIMODAL: // 8
                return 'MultiModal';
            case TextEvent.DOM_INPUT_METHOD_SCRIPT://9
                return 'Script';
            default:
                return 'Unknown';
        }
    }
```

## Usage

     Used to emulate keyboard events from other input devices like on screen keyboard clicks, voice input, handwriting, copy and paste operations and scripted input methods.

## Notes

The event type is case sensitive!

In Internet Explorer use 'textinput' for the eventType.

In Safari and Chromium use 'textInput' for the eventType parameter.

MSIE browsers further require that the event inputMethod isTrusted.

## Related specifications

[DOM Level 3 Events (20110531)](http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531)
:   Outdated Working Draft
