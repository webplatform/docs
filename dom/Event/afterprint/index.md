---
title: afterprint
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforeprint.htm'
notes:
  - 'Needs summary, specs, and compat'
readiness: 'In Progress'
tags:
  - Events
  - DOM
uri: dom/Event/afterprint

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

## <span>Overview Table</span>

<table class="wikitable">
<tr>
<th>
Synchronous

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Bubbles

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Target

</th>
<td>
dom/Element

</td>
</tr>
<tr>
<th>
Cancelable

</th>
<td>
No

</td>
</tr>
<tr>
<th>
Default action

</th>
<td>
 ?

</td>
</tr>
</table>
## <span>Examples</span>

This example uses the **onafterprint** event to return the document to its pre-print state. In this case, because the [**onbeforeprint**](/dom/Event/beforeprint) event handler makes all currently hidden sections of the document visible for printing, the **onafterprint** event sets those sections back to hidden.

``` html
function window.onafterprint()
{
    // Walk through all the elements in the doc with CLASS="expanded"
    // and set it to "collapsed" if expanded just for
    // printing.
   var coll = document.all.tags("DIV");
   if (coll!=null)
   {
      for (i=0; i<coll.length; i++)
         if ((coll[i].className == "expanded") &&
             (coll[i].bExpandedForPrinting))
         {
           coll[i].className = "collapsed";
           coll[i].bExpandedForPrinting = false;
         }
   }
}
function window.onbeforeprint()
{
    // Walk through all the elements in the doc with CLASS="collapsed"
    // and set it to "expanded" just for printing.
   var coll = document.all.tags("DIV");
   if (coll!=null)
   {
      for (i=0; i<coll.length; i++)
         if (coll[i].className == "collapsed")
         {
           coll[i].className = "expanded";

        // After printing, make sure to set
        // CLASS="collapsed" only for those that were
        // expanded just for printing.
           coll[i].bExpandedForPrinting = true;
         }
         else if (coll[i].className == "expanded")
            coll[i].bExpandedForPrinting = false;
   }
}
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforeprint.htm)

## <span>Notes</span>

### <span>Remarks</span>

This event is usually used with the [**onbeforeprint**](/dom/Event/beforeprint) event. Use the **onbeforeprint** event to make changes to the document just before it prints or previews for printing. Use the **onafterprint** event to undo those changes, reverting the document back to its pre-print or pre-preview state.

To invoke this event, do one of the following:

-   Choose Print or Print Preview from the File menu.
-   Press CTRL+P.
-   Right-click anywhere on a document, and choose Print.
-   Right-click a link on a document, and choose Print.
-   From Windows Explorer, select an .htm file, and then choose Print from the File menu.
-   From Windows Explorer, right-click an .htm file, and then choose Print.

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

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.

### <span>Event handler parameters</span>

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `window`
-   `body`
-   `frameSet`
-   `Reference`
-   `onbeforeprint`
-   `print`
