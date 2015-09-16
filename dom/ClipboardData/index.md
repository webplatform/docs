---
title: 'ClipboardData'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clipboardDataEX.htm'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Retrieves the information from the clipboard as part of clipboard operation events.'
tags:
  - API
  - Objects
  - DOM
uri: dom/ClipboardData

---
## Summary

Retrieves the information from the clipboard as part of clipboard operation events.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Examples

This example uses the [**setData**](/dom/DataTransfer/setData) and [**getData**](/dom/DataTransfer/getData) methods with the **clipboardData** object to perform a cut-and-paste operation through the shortcut menu.

``` html
<!doctype html>
<html>
 <head>
  <style>
BODY {
 margin-top: 0;
 margin-left: 0;
 background: #ffffff;
}
A, A:link, A:active {
 color: #000000;
}
A:visited {
 color: #808080;
}
  </style>
  <script>
var bResult, oSource;
// Select the text to be cut. Trailing spaces in a text
// selection in cut events cause the Cut shortcut menu item to
// remain disabled.
function fnLoad() {
    var r = document.body.createTextRange();
    oSource = document.getElementById("oSource");
    r.findText(oSource.textContent);
    r.select();
}
// Enable the Cut shortcut menu item over the DIV. Cut is disabled by default.
// Once Cut is enabled, Internet Explorer automatically copies the data to the
// clipboard and removes the selected text from the document.
function fnBeforeCut(event) {
    event.preventDefault();
}
//Assign data in text format to the window.clipboardData object.
//Display the result (Boolean) from the setData method in the input box below.
function fnCut(event){
    event.preventDefault();
    bResult = window.clipboardData.setData("Text", oSource.textContent);
    oSource.textContent= "";
    document.getElementById("tText").textContent += bResult;
}
// Enable the Paste shortcut menu item over the DIV. Paste is disabled by default.
function fnBeforePaste(event) {
    event.preventDefault();
}
// Prevent the default action in onpaste for the text input, which
// has a default behavior.
function fnPaste(event) {
    event.preventDefault();
    document.getElementById("oTarget").textContent = window.clipboardData.getData("Text");
}
  </script>
 </head>
 <body onload="fnLoad()">
  <div class="clsSource" id="oSource"
          onbeforecut="fnBeforeCut(event)" oncut="fnCut(event)">
    Select and cut this text
  </div>
  <div class="clsTarget" id="oTarget"
          onbeforepaste="fnBeforePaste(event)" onpaste="fnPaste(event)">
    Paste the Text Here
  </div><br/>
  <span class="clsData">setData Result: </span>
  <input class="clsText" id="tText" type="text"
            readonly="readonly" value="" size="6"
            tabindex="-1">
 </body>
</html>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/clipboardDataEX.htm)

## Notes

The **clipboardData** object is reserved for copy/cut/paste operations. It transfers information using the system clipboard, and retains it until data from the next editing operation replaces it. This form of data transfer is particularly suited to multiple pastes of the same data.

## Related specifications

[Clipboard API and Events](http://www.w3.org/TR/clipboard-apis/)
:   W3C Working Draft
