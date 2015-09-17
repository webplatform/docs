---
title: 'TextRange'
attributions:
  - 'Microsoft Developer Network: [[TextRange Object](http://msdn.microsoft.com/en-us/library/ie/ms535872(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
standardization_status: Non-Standard
summary: 'Represents text in an HTML element.'
tags:
  - API_Objects
  - DOM
uri: dom/TextRange

---
## Summary

Represents text in an HTML element.

## Properties

[boundingHeight](/dom/TextRange/boundingHeight)
:   Retrieves the height of the rectangle that bounds the TextRange object.

[boundingLeft](/dom/TextRange/boundingLeft)
:   Retrieves the distance between the left edge of the rectangle that bounds the TextRange object and the left side of the object that contains the TextRange.

[boundingTop](/dom/TextRange/boundingTop)
:   Retrieves the distance between the top edge of the rectangle that bounds the TextRange object and the top side of the object that contains the TextRange.

[boundingWidth](/dom/TextRange/boundingWidth)
:   Retrieves the width of the rectangle that bounds the TextRange object

[text](/dom/TextRange/text)
:   Sets or retrieves the text contained within the range.

## Methods

[duplicate](/dom/TextRange/duplicate)
:   Returns a duplicate of the TextRange.

[getBookmark](/dom/TextRange/getBookmark)
:   Retrieves a bookmark (opaque string) that can be used with moveToBookmark to return to the same range.

[item](/dom/TextRange/item)
:

[move](/dom/TextRange/move)
:   Collapses the given text range and moves the empty range by the given number of units.

[moveEnd](/dom/TextRange/moveEnd)
:   Changes the end position of the range.

[moveStart](/dom/TextRange/moveStart)
:   Changes the start position of the range.

[moveToBookmark](/dom/TextRange/moveToBookmark)
:   Moves to a bookmark.

[moveToElementText](/dom/TextRange/moveToElementText)
:   Moves the text range so that the start and end positions of the range encompass the text in the given element.

[moveToPoint](/dom/TextRange/moveToPoint)
:   Moves the start and end positions of the text range to the given point.

[parentElement](/dom/TextRange/parentElement)
:   Retrieves the parent element for the given text range.

[pasteHTML](/dom/TextRange/pasteHTML)
:   Pastes HTML text into the given text range, replacing any previous text and HTML elements in the range.

[queryCommandEnabled](/dom/TextRange/queryCommandEnabled)
:   Returns a Boolean value that indicates whether a specified command can be successfully executed using execCommand, given the current state of the document.

[queryCommandIndeterm](/dom/TextRange/queryCommandIndeterm)
:   Returns a Boolean value that indicates whether the specified command is in the indeterminate state.

[queryCommandState](/dom/TextRange/queryCommandState)
:   Returns a Boolean value that indicates the current state of the command.

[queryCommandSupported](/dom/TextRange/queryCommandSupported)
:   Returns a Boolean value that indicates whether the current command is supported on the current range.

[queryCommandValue](/dom/TextRange/queryCommandValue)
:   Returns the current value of the document, range, or current selection for the given command.

[scrollIntoView](/dom/TextRange/scrollIntoView)
:   Causes the object to scroll into view, aligning it either at the top or bottom of the window.

[select](/dom/TextRange/select)
:   Makes the selection equal to the current object.

[setEndPoint](/dom/TextRange/setEndPoint)
:   Sets the endpoint of one range based on the endpoint of another range.

## Events

*No events.*

## Examples

This example changes the text of a **button** element to "Clicked" through the **TextRange** object.

``` js
<script type="text/javascript">
var b = document.all.tags("button");
if (b!=null) {
    var r = b[0].createTextRange();
    if (r != null) {
        r.text = "Clicked";
    }
}
</script>
```

## Usage

     Use this object to retrieve and modify text in an element, to locate specific strings in the text, and to carry out commands that affect the appearance of the text.

## Notes

### Remarks

To retrieve a text range object, apply the [**createRange**](/dom/Document/createRange) method to a **body**, **button**, or **textArea** element or an **input** element that has [**TYPE**](/html/attributes/type) text. Modify the extent of the text range by moving its start and end positions with methods such as [**move**](/dom/TextRange/move) and [**moveToElementText**](/dom/TextRange/moveToElementText). Within the text range, you can retrieve and modify plain text or HTML text. These forms of text are identical except that HTML text includes HTML tags, and plain text does not.
