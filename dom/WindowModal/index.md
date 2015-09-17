---
title: 'WindowModal'
readiness: 'Ready to Use'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: Window
    href: /dom/Window
summary: 'Represents a modal or modeless child window of a window, with additional utility methods for arguments and return values.'
tags:
  - API_Objects
  - DOM
uri: dom/WindowModal

---
## Summary

Represents a modal or modeless child window of a window, with additional utility methods for arguments and return values.

Inherits from [Window](/dom/Window)[Window](/dom/Window)

## Properties

[dialogArguments](/dom/WindowModal/dialogArguments)
:   Gets the arguments that are specified when [showModalDialog](/dom/Window/showModalDialog) is called.

[dialogHeight](/dom/WindowModal/dialogHeight)
:   Gets or sets the height of the content area of a dialog window.

[dialogLeft](/dom/WindowModal/dialogLeft)
:   Gets or sets the X coordinate position of a dialog window.

[dialogTop](/dom/WindowModal/dialogTop)
:   Gets or sets the Y coordinate position of a dialog window.

[dialogWidth](/dom/WindowModal/dialogWidth)
:   Gets or sets the width of the content area of a dialog window.

## Methods

*No methods.*

## Events

*No events.*

## Inherited from Window

### Properties

[URL](/dom/Window/URL)
:   Sets or gets the URL for the current document.

[XMLHttpRequest](/dom/Window/XMLHttpRequest)
:   Represents an XML request using HTTP.

[animationStartTime](/dom/Window/animationStartTime)
:   Obsolete. Returns a timestamp of the start time of the current refresh interval, such that multiple animations can be synchronized with each other.

[closed](/dom/Window/closed)
:   This read-only property indicates whether the referenced window is closed or not.

[defaultStatus](/dom/Window/defaultStatus)
:   Sets or retrieves the default message displayed in the status bar at the bottom of the window.

[frames](/dom/Window/frames)
:   Returns the window itself, which is an array-like object, listing the direct sub-frames of the current window.

[indexedDB](/dom/Window/indexedDB)
:   Provides access to the IndexedDB features supported by the browser and/or device.

[innerHeight](/dom/Window/innerHeight)
:   Height (in pixels) of the browser window viewport including, if rendered, the horizontal scrollbar.

[onLine](/dom/Window/onLine)
:

[screenLeft](/dom/Window/screenLeft)
:   Retrieves the x-coordinate of the upper left-hand corner of the window frame, relative to the upper left-hand corner of the screen.

[screenTop](/dom/Window/screenTop)
:   Retrieves the y-coordinate of the top corner of the client area, relative to the top corner of the screen.

[status](/dom/Window/status)
:   Sets the text in the status bar at the bottom of the browser or returns the previously set text.

[styleMedia](/dom/Window/styleMedia)
:   Gets a StyleMedia object that contains methods and properties. These methods and properties determine the media types that are supported by the object that displays the document object.

[top](/dom/Window/top)
:   Retrieves the topmost ancestor window.

### Methods

[alert](/dom/Window/alert)
:   Displays a synchronized dialog box showing the given text and a localized OK button.

[cancelAnimationFrame](/dom/Window/cancelAnimationFrame)
:   Cancels a requestAnimationFrame request

[clearImmediate](/dom/Window/clearImmediate)
:   Cancels a function request created with setImmediate.

[clearInterval](/dom/Window/clearInterval)
:   Cancels the interval previously started using the setInterval method.

[clearTimeout](/dom/Window/clearTimeout)
:   Cancels a time-out that was set with the setTimeout method.

[close](/dom/Window/close)
:   Closes the current browser window or tab, or HTML Application (HTA).

[confirm](/dom/Window/confirm)
:   Displays a synchronized confirmation dialog box showing the given text and possibly localized OK and Cancel buttons.

[getComputedStyle](/dom/Window/getComputedStyle)
:   Gets the values of all the CSS properties of an element after applying the active stylesheets and resolving the basic computations they may contain.

    The returned object is of the same type that the object returned from the element's ["style"](/css/cssom/style) property, however the two objects have different purposes. The object returned from getComputedStyle is read-only and can be used to inspect the element's style (including those set by a \<style\> element or an external stylesheet). The elt.style object should be used to set styles on a specific element.

[getSelection](/dom/Window/getSelection)
:   Returns a [Selection](/dom/Selection) object that represents the current selection of the document.

[moveBy](/dom/Window/moveBy)
:   Moves the screen position of the window by the specified x and y offset values.

[moveRow](/dom/Window/moveRow)
:   Moves a table row to a new position.

[moveTo](/dom/Window/moveTo)
:   Moves the screen position of the upper-left corner of the window to the specified x and y position

[open](/dom/Window/open)
:   Opens a new window and loads the document specified by a given URL.

[postMessage](/dom/Window/postMessage)
:   Sends a cross-document message.

[requestAnimationFrame](/dom/Window/requestAnimationFrame)
:   A method to invoke at the optimal time a callback to update the frame of an animation.

[resizeBy](/dom/Window/resizeBy)
:   Changes the current size of the window by the specified x- and y-offset.

[resizeTo](/dom/Window/resizeTo)
:   Sets the size of the window to the specified width and height values.

[scroll](/dom/Window/scroll)
:   Causes the window to scroll to the specified x- and y-offset at the upper-left corner of the window.

[scrollBy](/dom/Window/scrollBy)
:   Causes the window to scroll relative to the current scrolled position by the specified x- and y-pixel offset.

[scrollTo](/dom/Window/scrollTo)
:   Scrolls the window to the specified x- and y-offset.

[setImmediate](/dom/Window/setImmediate)
:   Requests that a function be called when current or pending tasks are complete, such as events or screen updates.

[setInterval](/dom/Window/setInterval)
:   Evaluates an expression each time a specified number of milliseconds has elapsed.

[setTimeout](/dom/Window/setTimeout)
:   Evaluates an expression after a specified number of milliseconds has elapsed.

[showModalDialog](/dom/Window/showModalDialog)
:   Do not use. Use \<dialog\> or a popup window instead. Halts the script execution, creates a popup window, passes it parameters and returns a value when the new window is closed.

### Events

[message](/dom/Window/message)
:   Fires when a message is received from another context (frame, window, worker and similar).
