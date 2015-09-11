---
title: TextEvent
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
  - API
  - Objects
  - DOM
uri: dom/TextEvent

---
## <span>Summary</span>

Represents a text event that usually occurs when text is actually inserted into the document.

Inherits from [UIEvent](/dom/UIEvent)[UIEvent](/dom/UIEvent)

## <span>Properties</span>

API Name
:   Summary

[inputMethod](/dom/TextEvent/inputMethod)
:   Gets a value that describes how text is entered.

## <span>Methods</span>

API Name
:   Summary

[initTextEvent](/dom/TextEvent/initTextEvent)
:   Initializes a new text event that the createEvent method created.

## <span>Events</span>

*No events.*

## <span>Inherited from UIEvent</span>

### <span>Properties</span>

API Name
:   Summary

[detail](/dom/UIEvent/detail)
:   Gets additional, developer defined, information about an event.

[view](/dom/UIEvent/view)
:   Gets the **window** object that an event is generated from.

    [object window]

### <span>Methods</span>

API Name
:   Summary

[initUIEvent](/dom/UIEvent/initUIEvent)
:   Initializes a new user interface event that the [createEvent](/dom/Document/createEvent) method created.

### <span>Events</span>

API Name
:   Summary

[abort](/dom/UIEvent/abort)
:   Fires when the user aborts the download.

[activate](/dom/UIEvent/activate)
:   Fires when the object is set as the active element.

## <span>Examples</span>

``` js
txtEl=document.getElementById('txtInput'); // textarea
if(window.addEventListener){
txtEl.addEventListener('textinput', handler, false);
}
```

## <span>Related specifications</span>

[DOM Level 3 Events (20110531)](http://www.w3.org/TR/2011/WD-DOM-Level-3-Events-20110531)
:   Outdated Working Draft
