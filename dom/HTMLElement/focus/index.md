---
title: 'focus'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, compatibility, standards, clean-up of MSDN sections'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLElement/focus

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var object = object.focus();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This method raises the ****onfocus**** event. The effect depends on the object calling the method. When called for child windows (such as those created with the [**open**](/dom/Window/open) method of a **window** object), **focus** brings the target window to the foreground. Elements cannot receive focus until the document finishes loading. Windows Internet Explorer 8 and later. The **focus** method no longer brings child windows (such as those created with the **open** method) to the foreground. Child windows now request focus from the user, usually by flashing the title bar. To directly bring the window to the foreground, add script to the child window that calls the **focus** method of its **window** object.

Windows Internet Explorer 7 and later. For security reasons, child windows will only respond to the focus method when the following conditions are true:

-   The child window does not have multiple tabs open.
-   The focus method was not triggered by a double-click action.

If any of these conditions are true, the child window ignores the focus event. As of Microsoft Internet Explorer 5, elements that expose the **focus** method must have the [**TABINDEX**](/html/attributes/tabIndex) attribute set.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
