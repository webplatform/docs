---
title: Window
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[window Object](https://developer.mozilla.org/en-US/docs/Web/API/Window) Article]'
  - 'Microsoft Developer Network: [[window Object](http://msdn.microsoft.com/en-us/library/ie/ms535873(v=vs.85).aspx) Article]'
notes:
  - 'New listing page with proper object capitalization; replaces window.'
readiness: 'Ready to Use'
relationships:
  subclass_of:
    predicate: 'Inherits from '
    value: EventTarget
    href: /dom/EventTarget
summary: "The window object is the top level Javascript object in a page, and is the global scope for a browser tab.\nGlobal Javascript variables appear in the window object, as well as several important objects such as Document.\n"
tags:
  - API
  - Objects
  - DOM
uri: dom/Window

---
## Summary

The window object is the top level Javascript object in a page, and is the global scope for a browser tab. Global Javascript variables appear in the window object, as well as several important objects such as Document.

Inherits from [EventTarget](/dom/EventTarget)[EventTarget](/dom/EventTarget)

## Properties

API Name
:   Summary

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

## Methods

API Name
:   Summary

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

## Events

API Name
:   Summary

[message](/dom/Window/message)
:   Fires when a message is received from another context (frame, window, worker and similar).

## Inherited from EventTarget

### Properties

*No properties.*

### Methods

API Name
:   Summary

[addEventListener](/dom/EventTarget/addEventListener)
:   Registers an event handler for the specified event type.

[dispatchEvent](/dom/EventTarget/dispatchEvent)
:   Sends an event to the current element.

[removeEventListener](/dom/EventTarget/removeEventListener)
:   Removes an event handler that the [addEventListener](/dom/EventTarget/addEventListener) method registered.

### Events

*No events.*

## Examples

This example displays an alert for the current window.

``` js
alert("A simple message.")
```

``` js
if ( window.frames != null ) {
    for ( i = 0; i < window.frames.length; i++ )
        console.log("Child window " + i + " is named " + window.frames(i).name);
}
```

This example shows a simple event handler function for the window's **onload** event. In the absence of a **window** element, the **body** element hosts the following window object events: **onblur**, **onbeforeunload**, **onfocus**, **onload**, and **onunload**.

``` html
<body onload="console.log('Document is loaded!');">
```

## Notes

You can use the **window** object to retrieve information about the state of the window. You also can use this object to gain access to the document in the window, to the events that occur in the window, and to other factors that affect the window. You can apply any window property, method, or collection to any variable or expression that evaluates to a **window** object, regardless of how that window was created. Additionally, you can access all window properties, methods, and collections in the current window by using the property, method, or collection name directly—that is, without prefixing it with an expression that evaluates to the current **window** object. However, to help make more readable code and to avoid potential ambiguities, many authors use the **window** keyword when accessing window properties, methods, and collections for the current window. This keyword always refers to the current window. **Note** The window's properties, methods, and collection names are reserved keywords and cannot be used as the names of variables or routines. The following table lists pertinent information for some of the properties of the **window** object.

|Property|Method|Description|
|:-------|:-----|:----------|
|**opener**|**open**|The **opener** property is available only from a document opened using the **window.open** method.|
|**parent**, **top**|None|The **parent** and **top** properties are available for a window opened inside a **frame** or **iframe**. The two properties return the topmost parent and immediate parent, respectively.|
|**parent**, **top**|**open**|The **parent** and **top** properties are available for a window opened via the **open** method or as a dialog and returns the current window.|
|**length**|None|Regardless of how the window is opened, the **length** property returns the number of frames in a window.|
|**dialogArguments**, **dialogHeight**, **dialogLeft**, **dialogTop**, **dialogWidth**, **returnValue**|**showModalDialog** and **showModelessDialog**|These properties are available only for windows created using the two methods listed, **showModalDialog** and **showModelessDialog**|

Typically, the browser creates one **window** object when it opens an HTML document. However, if a document defines one or more frames (that is, contains one or more **frame** or **iframe** tags), the browser creates one **window** object for the original document and one additional **window** object for each frame. These additional objects are of the original window and can be affected by actions that occur in the original. For example, closing the original window causes all child windows to close. You can also create new windows (and corresponding window objects) using methods such as **open**, **showModalDialog**, and **showModelessDialog**.

