---
title: Node
tags:
  - API
  - Objects
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'The interface for the primary data type for the entire Document Object Model.'
uri: dom/Node
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'html/attributes/text (body element)'

---
# Node

## Summary

The interface for the primary data type for the entire Document Object Model.

<span data-meta="subclass_of" data-type="key">Inherits from <span data-type="value">[EventTarget](/dom/EventTarget)</span></span>

## Overview

The **Node** interface is the primary datatype for the entire Document Object Model (DOM). It represents a single node in the document tree.

## Properties

API Name
:   Summary
[attributes](/dom/Node/attributes)
:   Associatve array containing the attributes of node.
[childNodes](/dom/Node/childNodes)
:   Gets a collection of direct Node descendants of the Node, including [Element](/dom/Element), [Text](/dom/Text) and any other type of nodes.
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

## Methods

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

## Events

*No events.*

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

## Notes

While all objects implementing the **Node** interface expose methods for dealing with children, not all objects implementing the **Node** interface may have children. For example, [**text**](/w/index.php?title=html/attributes/text_(body_element)&action=edit&redlink=1) nodes may not have children, and adding children to such nodes results in a [**DOMException**](/dom/DOMException). The attributes [**nodeName**](/dom/Node/nodeName), [**nodeValue**](/dom/Node/nodeValue) and [**attributes**](/dom/Node/attributes) are included as a mechanism to get at node information without casting down to the specific derived interface. In cases where there is no obvious mapping of these attributes for a specific [**nodeType**](/dom/Node/nodeType) (i.e., **nodeValue** for an Element or attributes for a Comment), this returns **null**. Note that the specialized interfaces may contain additional and more convenient mechanisms to get and set the relevant information.

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Node](https://developer.mozilla.org/en-US/docs/Web/API/Node) Article]

Portions of this content come from the Microsoft Developer Network: [[Basic DOM Reference](http://msdn.microsoft.com/en-us/library/ie/hh771916(v=vs.85).aspx) Article]

