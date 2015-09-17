---
title: 'TextEvent'
attributions:
  - 'Microsoft Developer Network: [[TextEvent Object](http://msdn.microsoft.com/en-us/library/ie/ff974350(v=vs.85).aspx) Article]'
notes:
  - "Needs an example?\nhttp://help.dottoro.com/ljuecqgv.php\nonly works in webkit,\nFX has no TextEvent,\n\nIE11 has but above sample runs without errors or the expected result... appears IE prevent programmatic text input into input fields."
readiness: 'Almost Ready'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: UIEvent
    href: /dom/UIEvent
summary: 'Represents a text event that usually occurs when text is actually inserted into the document.'
tags:
  - API_Objects
  - DOM
uri: dom/TextEvent

---
## Summary

Represents a text event that usually occurs when text is actually inserted into the document.

Inherits from [UIEvent](/dom/UIEvent)[UIEvent](/dom/UIEvent)

## Properties

[inputMethod](/dom/TextEvent/inputMethod)
:   Gets a value that describes how text is entered.

## Methods

[initTextEvent](/dom/TextEvent/initTextEvent)
:   Initializes a new text event that the createEvent method created.

## Events

*No events.*

## Inherited from UIEvent

### Properties

[detail](/dom/UIEvent/detail)
:   Gets additional, developer defined, information about an event.

[view](/dom/UIEvent/view)
:   Gets the **window** object that an event is generated from.

    [object window]

### Methods

[initUIEvent](/dom/UIEvent/initUIEvent)
:   Initializes a new user interface event that the [createEvent](/dom/Document/createEvent) method created.

### Events

[abort](/dom/UIEvent/abort)
:   Fires when the user aborts the download.

[activate](/dom/UIEvent/activate)
:   Fires when the object is set as the active element.

## Examples

``` js
txtEl=document.getElementById('txtInput'); // textarea
if(window.addEventListener){
txtEl.addEventListener('textinput', handler, false);
}
```

## Related specifications

[DOM Level 3 Events (20110531)](http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531)
:   Outdated Working Draft
