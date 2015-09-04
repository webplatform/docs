---
title: beforeunload
tags:
  - Events
readiness: 'In Progress'
notes:
  - 'Needs summary, spec, and compat'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforeunload.htm'
uri: dom/Event/beforeunload

---
# beforeunload

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## Overview Table

Synchronous
:   No
Bubbles
:   No
Target
:   dom/Element
Cancelable
:   No
Default action
:    ?

## Examples

This example uses the **onbeforeunload** event to ask users whether they want to remain on the current document or navigate to a new URL. When the user clicks on the hyperlink or attempts to close the window, the **onbeforeunload** event fires on the **body** and a dialog box displays. If the user chooses **OK**, the document navigates to the new URL (www.microsoft.com) or closes the window; if the user chooses **Cancel**, the document remains the same.

    <HTML>
    <head>
    <script>
    function closeIt()
    {
      return "Any string value here forces a dialog box to \n" +
             "appear before closing the window.";
    }
    window.onbeforeunload = closeIt;
    </script>
    </head>
    <body>
      <a href="http://www.microsoft.com">Click here to navigate to
          www.microsoft.com</a>
    </body>
    </html>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforeunload.htm)

## Notes

### Remarks

When a string is assigned to the **returnValue** property of **window**.**event**, a dialog box appears that gives users the option to stay on the current document and retain the string that was assigned to it. The default statement that appears in the dialog box, "`Are you sure you want to navigate away from this page? ... Press OK to continue, or Cancel to stay on the current page.`", cannot be removed or altered.

#### onbeforeunload in Metro style apps using JavaScript

In Metro style apps using JavaScript, the **returnValue** property of **window**.**event** is always ignored and **onunload** will fire immediately. No dialog is shown to the user and the navigation can't be cancelled. Note that, in most cases, the app should never navigate its top-level document. Metro style apps using JavaScript should use **oncheckpoint** event to determine when they need to save state information.

#### General info

This event signals that the document is about to be unloaded. To invoke this event, do one of the following:

-   Close the current window.
-   Navigate to another location by entering a new address or selecting a Favorite.
-   Click an [**anchor**](/html/elements/a) that refers to another document.
-   Invoke the [**anchor**](/html/elements/a).[**click**](/dom/HTMLElement/click) method.
-   Invoke the [**Document**](/dom/Document).[**write**](/dom/Document/write) method.
-   Invoke the [**Document**](/dom/Document).[**close**](/dom/Document/close) method.
-   Invoke the **window**.[**close**](/dom/Window/close) method.
-   Invoke the [**location**](/dom/Location).[**replace**](/dom/Location/replace) method.
-   Invoke the [**location**](/dom/Location).[**reload**](/dom/Location/reload) method.
-   Specify a new value for the [**location**](/dom/Location).[**href**](/dom/Location/href) property.
-   Submit a **form** to the address specified in the **ACTION** attribute via the **INPUT type=submit** control, or invoke the **form**.[**submit**](/dom/HTMLFormElement/submit) method.
-   Invoke the **window**.[**open**](/dom/Window/open) method, providing the possible value **\_self** for the window name.
-   Invoke the [**Document**](/dom/Document).[**open**](/dom/Document/open) method.
-   Click the Back, Forward, Refresh, or Home button.

The *pEvtObj* parameter is required for the following interfaces:

-   **HTMLAnchorEvents2**
-   **HTMLAreaEvents2**
-   **HTMLButtonElementEvents2**
-   **HTMLControlElementEvents2**
-   **HTMLDocumentEvents2**
-   **HTMLElementEvents2**
-   **HTMLFormElementEvents2**
-   **HTMLImgEvents2**
-   **HTMLFrameSiteEvents2**
-   **HTMLInputFileElementEvents2**
-   **HTMLInputImageEvents2**
-   **HTMLInputTextElementEvents2**
-   **HTMLLabelEvents2**
-   **HTMLLinkElementEvents2**
-   **HTMLMapEvents2**
-   **HTMLMarqueeElementEvents2**
-   **HTMLObjectElementEvents2**
-   **HTMLOptionButtonElementEvents2**
-   **HTMLScriptEvents2**
-   **HTMLSelectElementEvents2**
-   **HTMLStyleElementEvents2**
-   **HTMLTableEvents2**
-   **HTMLTextContainerEvents2**
-   **HTMLWindowEvents2**

### Syntax

### Standards information

There are no standards that apply here.

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

