---
title: 'beforeprint'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforeprint.htm'
notes:
  - 'Needs summary, spec, and compat'
readiness: 'In Progress'
tags:
  - Events
  - DOM
  - Needs_Summary
uri: dom/Event/beforeprint

---
## Overview Table

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
## Examples

This example uses the **onbeforeprint** to make all hidden sections of the document visible just before the document prints. The [**onafterprint**](/dom/Event/afterprint) event is processed after the document prints to return the document to its original state.

``` html
function window.onbeforeprint()
{
    // Walk through all the elements in the document with
    // CLASS="collapsed" and set it to "expanded" just for printing.
   var coll = document.all.tags("DIV");
   if (coll!=null)
   {
      for (i=0; i<coll.length; i++)
         if (coll[i].className == "collapsed")
         {
           coll[i].className = "expanded";

        // After printing, make sure to set CLASS="collapsed"
        // only for those that were expanded just for printing.
           coll[i].bExpandedForPrinting = true;
         }
         else if (coll[i].className == "expanded")
            coll[i].bExpandedForPrinting = false;
   }
}
function window.onafterprint()
{
   // Walk through all the elements in the doc with CLASS="expanded"
   // and set it to "collapsed" if expanded just for
   // printing.
   var coll = document.all.tags("DIV");
   if (coll!=null)
   {
      for (i=0; i < coll.length; i++)
         if ((coll[i].className == "expanded") &&
             (coll[i].bExpandedForPrinting))
         {
           coll[i].className = "collapsed";
           coll[i].bExpandedForPrinting = false;
         }
   }
}
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/onbeforeprint.htm)

## Notes

### Remarks

Use this event to modify the document just before it prints or previews for printing. In most cases it is used to make all the information on the document visible just before printing. Use the event in conjunction with the [**onafterprint**](/dom/Event/afterprint) event to undo the changes made to the document in the **onbeforeprint** event. Prints the document associated with the object for which the event is specified. To invoke this event, do one of the following:

-   Choose Print or Print Preview from the File menu.
-   Press CTRL+P.
-   Right-click anywhere on a document, and choose Print.
-   Right-click a link on a document, and choose Print.
-   From Windows Explorer, select an .htm file and choose Print from the File menu.
-   From Windows Explorer, right-click an .htm file and choose Print.

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
