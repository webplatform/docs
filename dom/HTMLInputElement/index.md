---
title: HTMLInputElement
tags:
  - API
  - Objects
  - DOM
readiness: 'In Progress'
notes:
  - 'examples, compatibility'
summary: 'Represents an input element within the DOM.'
uri: dom/HTMLInputElement

---
# HTMLInputElement

## Summary

Represents an input element within the DOM.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[HTMLElement](/dom/HTMLElement)</span></span>

## Properties

API Name
:   Summary
[checked](/dom/HTMLInputElement/checked)
:   Gets or sets whether a check box or a radio button are checked.
[defaultChecked](/dom/HTMLInputElement/defaultChecked)
:   Gets whether the [checked](/html/attributes/checked) HTML attribute is present on the element.
[defaultValue](/dom/HTMLInputElement/defaultValue)
:   Gets or sets the value of the [**value**](/dom/HTMLElement/value) HTML attribute.
[files](/dom/HTMLInputElement/files)
:
[formTarget](/dom/HTMLInputElement/formTarget)
:
[multiple](/dom/HTMLInputElement/multiple)
:   Gets whether a file upload element can be populated with more than a single file.
[selectionEnd](/dom/HTMLInputElement/selectionEnd)
:
[selectionStart](/dom/HTMLInputElement/selectionStart)
:
[validationMessage](/dom/HTMLInputElement/validationMessage)
:   Returns the error message that would be displayed if the user submits the form, or an empty string if no error message.
[valueAsNumber](/dom/HTMLInputElement/valueAsNumber)
:

## Methods

API Name
:   Summary
[setSelectionRange](/dom/HTMLInputElement/setSelectionRange)
:
[stepDown](/dom/HTMLInputElement/stepDown)
:
[stepUp](/dom/HTMLInputElement/stepUp)
:

## Events

*No events.*

## Inherited from HTMLElement

### Properties

API Name
:   Summary
[aria-activedescendant](/aria/attributes/aria-activedescendant)
:
[aria-busy](/aria/attributes/aria-busy)
:
[aria-checked](/aria/attributes/aria-checked)
:
[aria-controls](/aria/attributes/aria-controls)
:
[aria-describedby](/aria/attributes/aria-describedby)
:   Sets or retrieves a list of elements that describe the current object.
[aria-disabled](/aria/attributes/aria-disabled)
:
[aria-expanded](/aria/attributes/aria-expanded)
:
[aria-flowto](/aria/attributes/aria-flowto)
:
[aria-haspopup](/aria/attributes/aria-haspopup)
:
[aria-hidden](/aria/attributes/aria-hidden)
:
[aria-invalid](/aria/attributes/aria-invalid)
:
[aria-labelledby](/aria/attributes/aria-labelledby)
:
[aria-level](/aria/attributes/aria-level)
:
[aria-live](/aria/attributes/aria-live)
:
[aria-multiselectable](/aria/attributes/aria-multiselectable)
:
[aria-owns](/aria/attributes/aria-owns)
:
[aria-posinset](/aria/attributes/aria-posinset)
:
[aria-pressed](/aria/attributes/aria-pressed)
:
[aria-readonly](/aria/attributes/aria-readonly)
:
[aria-relevant](/aria/attributes/aria-relevant)
:
[aria-required](/aria/attributes/aria-required)
:
[aria-secret](/aria/attributes/aria-secret)
:
[aria-selected](/aria/attributes/aria-selected)
:
[aria-setsize](/aria/attributes/aria-setsize)
:
[aria-valuemax](/aria/attributes/aria-valuemax)
:
[aria-valuemin](/aria/attributes/aria-valuemin)
:
[aria-valuenow](/aria/attributes/aria-valuenow)
:
[x-ms-aria-flowfrom](/aria/attributes/x-ms-aria-flowfrom)
:
[attribute](/dom/HTMLElement/attribute)
:
[canHaveHTML](/dom/HTMLElement/canHaveHTML)
:
[cellIndex](/dom/HTMLElement/cellIndex)
:
[className](/dom/HTMLElement/className)
:
[clientHeight](/dom/HTMLElement/clientHeight)
:
[clientLeft](/dom/HTMLElement/clientLeft)
:
[clientTop](/dom/HTMLElement/clientTop)
:
[clientWidth](/dom/HTMLElement/clientWidth)
:
[controlRange](/dom/HTMLElement/controlRange)
:
[dir](/dom/HTMLElement/dir)
:
[disabled](/dom/HTMLElement/disabled)
:
[document](/dom/HTMLElement/document)
:
[draggable](/dom/HTMLElement/draggable)
:   Gets or sets whether an element can be dragged and dropped.
[elements](/dom/HTMLElement/elements)
:
[embeds](/dom/HTMLElement/embeds)
:
[form](/dom/HTMLElement/form)
:
[frameElement](/dom/HTMLElement/frameElement)
:
[indeterminate](/dom/HTMLElement/indeterminate)
:
[index](/dom/HTMLElement/index)
:
[innerHTML](/dom/HTMLElement/innerHTML)
:
[innerText](/dom/HTMLElement/innerText)
:
[isContentEditable](/dom/HTMLElement/isContentEditable)
:

<!-- -->

    … further results

### Methods

API Name
:   Summary
[abort](/dom/HTMLElement/abort)
:
[blur](/dom/HTMLElement/blur)
:
[clearAttributes](/dom/HTMLElement/clearAttributes)
:
[click](/dom/HTMLElement/click)
:   Covers what the click action is and what happens when it is performed.
[componentFromPoint](/dom/HTMLElement/componentFromPoint)
:
[doScroll](/dom/HTMLElement/doScroll)
:
[focus](/dom/HTMLElement/focus)
:
[getBoundingClientRect](/dom/HTMLElement/getBoundingClientRect)
:   Returns a [ClientRect](/css/cssom/ClientRect) object that encloses a group of text rectangles.
[getClientRects](/dom/HTMLElement/getClientRects)
:   A collection of [ClientRect](/css/cssom/ClientRect) objects, one for each CSS border box associated with the element. Each ClientRect object contains read-only left, top, right, and bottom properties describing the border box, relative to the top-left of the viewport. For tables with captions, the caption is included even though it is outside the border box of the table.
[hide](/dom/HTMLElement/hide)
:
[item](/dom/HTMLElement/item)
:
[matches](/dom/HTMLElement/matches)
:   Returns `true` if an element matches a given selector. Otherwise, `false`.
[namedItem](/dom/HTMLElement/namedItem)
:
[remove](/dom/HTMLElement/remove)
:
[setActive](/dom/HTMLElement/setActive)
:
[setCustomValidity](/dom/HTMLElement/setCustomValidity)
:
[show](/dom/HTMLElement/show)
:
[toStaticHTML](/dom/HTMLElement/toStaticHTML)
:

### Events

*No events.*

**Needs Examples**: This section should include examples.

## Notes

### Compatibility Notes

Chrome 38 and below - [focusin](/dom/FocusEvent/focusin) is not fired when using the **tab** key to focus on the element.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

