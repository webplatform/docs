---
title: 'DataTransfer'
notes:
  - 'New listing page with proper object capitalization; replaces dataTransfer.'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: "Represents an object associated with drag and drop or clipboard events.\nDataTransfer objects are used to expose the drag data store that underlies a drag-and-drop operation.\n"
tags:
  - API_Objects
  - DOM
uri: dom/DataTransfer

---
## Summary

Represents an object associated with drag and drop or clipboard events. DataTransfer objects are used to expose the drag data store that underlies a drag-and-drop operation.

## Properties

[dropEffect](/dom/DataTransfer/dropEffect)
:   Gets the type of drag-and-drop operation currently selected or sets the operation to a new type.

[effectAllowed](/dom/DataTransfer/effectAllowed)
:   Gets which kinds of data transfer operations are allowed for the object. Can be set (during the dragstart event) to change the allowed operations.

[files](/dom/DataTransfer/files)
:   Returns a FileList of the files being dragged, if any.

[items](/dom/DataTransfer/items)
:   Returns a DataTransferItemList object containing the drag data.

[types](/dom/DataTransfer/types)
:   Returns an array listing the formats that were set in the **dragstart** event. If any files are being dragged, one of the types will be the string "Files".

## Methods

[clearData](/dom/DataTransfer/clearData)
:   Removes one or more data formats (or all data) from the clipboard through the **DataTransfer** object or the [**ClipboardData**](/dom/ClipboardData) object.

[getData](/dom/DataTransfer/getData)
:   Gets the data in the specified format from the clipboard through the **DataTransfer** object or the [**ClipboardData**](/dom/ClipboardData) object.

    If there is no data, returns an empty string.

[setData](/dom/DataTransfer/setData)
:   Adds data in a specified format to the **DataTransfer** object or the [**ClipboardData**](/dom/ClipboardData) object.

[setDragImage](/dom/DataTransfer/setDragImage)
:   Uses the given element to update the drag feedback image, replacing any previously specified feedback image.

## Events

*No events.*

## Related specifications

[HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation

