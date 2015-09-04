---
title: Element
tags:
  - API
  - Objects
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs example and compat'
summary: 'Represents an node of type element in the DOM.'
uri: dom/Element

---
# Element

## Summary

Represents an node of type element in the DOM.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[Node](/dom/Node)</span></span>

## Properties

API Name
:   Summary
[XMLDocument](/apis/xhr/properties/XMLDocument)
:
[XMLNS attribute](/apis/xhr/properties/XMLNS_attribute)
:
[childElementCount](/dom/Element/childElementCount)
:   Returns the number of direct children of this node that are elements. Read-only.
[children](/dom/Element/children)
:   Retrieves a live collection of child elements of an element.
[classList](/dom/Element/classList)
:   Reflects the [class](/html/attributes/class) attribute as an ordered list of the whitespace separated class names and has convenience methods for add, remove, contains and more.
[code](/dom/Element/code)
:
[entities](/dom/Element/entities)
:
[error](/dom/Element/error)
:
[firstElementChild](/dom/Element/firstElementChild)
:   Retrieves the first child of this node that is an element, if there is one, or null otherwise. Read-only.
[htmlText](/dom/Element/htmlText)
:
[internalSubset](/dom/Element/internalSubset)
:
[isTextEdit](/dom/Element/isTextEdit)
:
[lastElementChild](/dom/Element/lastElementChild)
:   Retrieves the last child of this node that is an element, if there are any element children, or null otherwise. Read-only.
[media](/dom/Element/media)
:
[nextElementSibling](/dom/Element/nextElementSibling)
:   Retrieves the element node that is a sibling to this element node (a direct child of the same parent) and is immediately after it in the DOM tree, ignoring text nodes, comment nodes and any other non-element nodes. If there is no next element sibling, the property value is null. Read-only.
[notations](/dom/Element/notations)
:
[oneTimeOnly](/dom/Element/oneTimeOnly)
:
[onerror](/dom/Element/onerror)
:
[onload](/dom/Element/onload)
:
[onloadend](/dom/Element/onloadend)
:
[onloadstart](/dom/Element/onloadstart)
:
[onprogress](/dom/Element/onprogress)
:
[ownerElement](/dom/Element/ownerElement)
:
[parent](/dom/Element/parent)
:
[parentElement](/dom/Element/parentElement)
:   Retrieves the parent node of this DOM node, *if* the parent is an element node; null if the parent is not an element or if there is no parent. Read-only.
[parentTextEdit](/dom/Element/parentTextEdit)
:
[previousElementSibling](/dom/Element/previousElementSibling)
:   Retrieves the element node that is a sibling to this element node (a direct child of the same parent) and is immediately previous to it in the DOM tree, ignoring text nodes, comment nodes and any other non-element nodes. If there is no previous element sibling, the property value is null. Read-only.
[readyState](/dom/Element/readyState)
:
[result](/dom/Element/result)
:
[size](/dom/Element/size)
:
[systemLanguage](/dom/Element/systemLanguage)
:
[type](/dom/Element/type)
:

## Methods

API Name
:   Summary
[msWriteProfilerMark](/apis/timing/methods/msWriteProfilerMark)
:
[querySelector](/css/selectors_api/querySelector)
:   Returns the first element that matches the provided selector.
[querySelectorAll](/css/selectors_api/querySelectorAll)
:   Returns a list of elements that match a provided selector.
[RangeException](/dom/Element/RangeException)
:
[createControlRange](/dom/Element/createControlRange)
:
[getAdjacentText](/dom/Element/getAdjacentText)
:   Non standard. Gets a text from a given location around the edges of the element.
[getAttribute](/dom/Element/getAttribute)
:   Returns the value of the content attribute.
[getAttributeNS](/dom/Element/getAttributeNS)
:   Returns the value of the content attribute within a specified namespace.
[getAttributeNode](/dom/Element/getAttributeNode)
:   Retrieves an attribute node by name.
[getAttributeNodeNS](/dom/Element/getAttributeNodeNS)
:   Gets an attribute node that matches the specified namespace and name.
[hasAttribute](/dom/Element/hasAttribute)
:   Determines whether a content attribute exists on an element.
[hasAttributeNS](/dom/Element/hasAttributeNS)
:   Determines whether a content attribute in a specified namespace exists on an element.
[inRange](/dom/Element/inRange)
:
[insertAdjacentHTML](/dom/Element/insertAdjacentHTML)
:   Parses and inserts HTML code at or beyond the edges of an element within the document hierarchy.
[isEqual](/dom/Element/isEqual)
:
[item](/dom/Element/item)
:
[releasePointerCapture](/dom/Element/releasePointerCapture)
:   Releases a pointer captured by an element (using the [setPointerCapture](/dom/Element/setPointerCapture) method).
[removeAttribute](/dom/Element/removeAttribute)
:   Removes a specified content attribute from an element.
[removeAttributeNS](/dom/Element/removeAttributeNS)
:   Removes a specified content attribute in a specified namespace from an element.
[removeAttributeNode](/dom/Element/removeAttributeNode)
:
[requestFullscreen](/dom/Element/requestFullscreen)
:   The requestFullscreen method provides a way for presenting web content using the user’s entire screen. The API lets you easily direct the browser to make an element — and its children, if any — occupy the full available screen space, without borders or other chrome elements.
[requestPointerLock](/dom/Element/requestPointerLock)
:   requestPointerLock lets you lock the target of mouse events to a single element while hiding the cursor.
[scrollByLines](/dom/Element/scrollByLines)
:
[scrollByPages](/dom/Element/scrollByPages)
:
[scrollIntoView](/dom/Element/scrollIntoView)
:   Scrolls the page to the point where the element shows up.
[scrollIntoViewIfNeeded](/dom/Element/scrollIntoViewIfNeeded)
:
[setAttribute](/dom/Element/setAttribute)
:   Sets the value of a content attribute.
[setAttributeNS](/dom/Element/setAttributeNS)
:   Sets the value of a content attribute in a specified namespace.
[setAttributeNode](/dom/Element/setAttributeNode)
:
[setAttributeNodeNS](/dom/Element/setAttributeNodeNS)
:
[setPointerCapture](/dom/Element/setPointerCapture)
:   Assigns a specified pointer to an element. This method is used to ensure that an element continues to receive pointer events even if the contact moves off the element.

## Events

API Name
:   Summary
[error](/apis/xhr/events/error)
:   The **onerror** event occurs when the request could not be completed because of an error.
[load](/apis/xhr/events/load)
:   After the **onload** event has occurred,

    **responseText** contains the complete server response.

[progress](/apis/xhr/events/progress)
:   When the **onprogress** event occurs,

    partial data can be retrieved using **responseText**.

[timeout](/apis/xhr/events/timeout)
:   The **ontimeout** event occurs if the **ontimeout** period elapses before the **onload** event occurs.
[change](/dom/Element/change)
:
[cuechange](/dom/Element/cuechange)
:
[durationchange](/dom/Element/durationchange)
:
[emptied](/dom/Element/emptied)
:
[ended](/dom/Element/ended)
:
[hashchange](/dom/Element/hashchange)
:
[help](/dom/Element/help)
:
[input](/dom/Element/input)
:
[layoutcomplete](/dom/Element/layoutcomplete)
:
[load](/dom/Element/load)
:
[loadeddata](/dom/Element/loadeddata)
:
[loadedmetadata](/dom/Element/loadedmetadata)
:
[loadstart](/dom/Element/loadstart)
:
[losecapture](/dom/Element/losecapture)
:
[move](/dom/Element/move)
:
[moveend](/dom/Element/moveend)
:
[movestart](/dom/Element/movestart)
:
[offline](/dom/Element/offline)
:
[online](/dom/Element/online)
:
[page](/dom/Element/page)
:
[paste](/dom/Element/paste)
:
[pause](/dom/Element/pause)
:
[play](/dom/Element/play)
:
[playing](/dom/Element/playing)
:
[propertychange](/dom/Element/propertychange)
:
[ratechange](/dom/Element/ratechange)
:
[readystatechange](/dom/Element/readystatechange)
:
[reset](/dom/Element/reset)
:
[resize](/dom/Element/resize)
:
[resizeend](/dom/Element/resizeend)
:
[resizestart](/dom/Element/resizestart)
:
[seeked](/dom/Element/seeked)
:
[seeking](/dom/Element/seeking)
:
[stalled](/dom/Element/stalled)
:
[submit](/dom/Element/submit)
:
[suspend](/dom/Element/suspend)
:
[timeupdate](/dom/Element/timeupdate)
:
[unload](/dom/Element/unload)
:
[volumechange](/dom/Element/volumechange)
:
[waiting](/dom/Element/waiting)
:
[error](/svg/events/error)
:
[load](/svg/events/load)
:
[onabort](/svg/events/onabort)
:
[onzoom](/svg/events/onzoom)
:
[resize](/svg/events/resize)
:
[scroll](/svg/events/scroll)
:

<!-- -->

    … further results

## Inherited from Node

### Properties

API Name
:   Summary
[attributes](/dom/Node/attributes)
:   Associatve array containing the attributes of node.
[childNodes](/dom/Node/childNodes)
:   Gets a collection of direct Node descendants of the Node, including **Element**, [Text](/dom/Text) and any other type of nodes.
[firstChild](/dom/Node/firstChild)
:   Gets a reference to the first child node in the childNodes collection of the object.

    If the node is childless, null is returned.

[lastChild](/dom/Node/lastChild)
:   Gets a reference to the last child in the childNodes collection of an object.
[localName](/dom/Node/localName)
:   Retrieves the local name of the fully qualified XML declaration for a node.
[namespaceURI](/dom/Node/namespaceURI)
:   Retrieves the namespace URI of the fully qualified XML declaration for a node.
[nextSibling](/dom/Node/nextSibling)
:   Retrieves the next child node of the parent of the node.
[nodeName](/dom/Node/nodeName)
:   Gets the name of a particular type of node.
[nodeType](/dom/Node/nodeType)
:   Retrieves the type of the requested node.
[nodeValue](/dom/Node/nodeValue)
:   Gets or sets the value of a Node, if the type of Node supports it.
[ownerDocument](/dom/Node/ownerDocument)
:   Retrieves the document object associated with the node.
[parentNode](/dom/Node/parentNode)
:   Retrieves the parent node in the document hierarchy.
[prefix](/dom/Node/prefix)
:   Sets or retrieves the prefix of the fully qualified XML declaration for a node.
[previousSibling](/dom/Node/previousSibling)
:   Retrieves the previous child node of the parent of the node.
[textContent](/dom/Node/textContent)
:   Sets or retrieves the text content of a node and any child nodes.

### Methods

API Name
:   Summary
[appendChild](/dom/Node/appendChild)
:   Appends an element as a child to the object.
[cloneNode](/dom/Node/cloneNode)
:   Copies a reference to the object from the document hierarchy.
[compareDocumentPosition](/dom/Node/compareDocumentPosition)
:   Compares the position of two nodes in a document.
[empty](/dom/Node/empty)
:   Cancels the current selection, sets the selection type to none, and sets the item property to null.
[hasAttributes](/dom/Node/hasAttributes)
:   Returns whether this node (if it is an element) has any attributes
[hasChildNodes](/dom/Node/hasChildNodes)
:   Gets a value that indicates whether the Node has any direct Node descendant of any type.
[insertBefore](/dom/Node/insertBefore)
:   Inserts a child into the node, immediately before the specified reference child node.
[isDefaultNamespace](/dom/Node/isDefaultNamespace)
:   Indicates whether or not a namespace is the default namespace for a document.
[isEqualNode](/dom/Node/isEqualNode)
:   Determines whether two nodes are equal in their type, name and namespace.
[isSameNode](/dom/Node/isSameNode)
:   Determines if two nodes are the same node.
[isSupported](/dom/Node/isSupported)
:   Returns a value indicating whether or not the object supports a specific DOM standard.
[lookupNamespaceURI](/dom/Node/lookupNamespaceURI)
:   Gets the URI of the namespace associated with a namespace prefix, if any.
[lookupPrefix](/dom/Node/lookupPrefix)
:   Gets the namespace prefix associated with a URI, if any.
[normalize](/dom/Node/normalize)
:   Merges adjacent DOM objects to produce a normalized document object model.
[removeChild](/dom/Node/removeChild)
:   Removes a child node from a node.
[replaceChild](/dom/Node/replaceChild)
:   Replaces an existing child node with a new child node.

### Events

*No events.*

**Needs Examples**: This section should include examples.

## Notes

Elements may have attributes associated with them; use the [attributes](/dom/Node/attributes) property to retrieve the set of all attributes for an element. There are methods on this object to retrieve either an attribute by name ([getAttributeNode](/dom/Element/getAttributeNode)) or an attribute value by name ([getAttribute](/dom/Element/getAttribute)). In XML, where an attribute value may contain entity references, an **attribute** should be retrieved to examine the possibly fairly complex sub-tree representing the attribute value. On the other hand, in HTML, where all attributes have simple string values, methods to directly access an attribute value can safely be used as a convenience.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

