---
title: showModalDialog
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/showModalDialog2.htm'
notes:
  - 'summary, clean-up MSDN import, move IE-specific content to compatibility'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
  return_type:
    predicate: 'Returns an object of type  '
    value: any
    href: /dom/Window
summary: 'Do not use. Use &lt;dialog&gt; or a popup window instead. Halts the script execution, creates a popup window, passes it parameters and returns a value when the new window is closed.'
tags:
  - API
  - Object
  - Methods
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/HTMLElement/showModelessDialog
uri: dom/Window/showModalDialog

---
## <span>Summary</span>

Do not use. Use &lt;dialog&gt; or a popup window instead. Halts the script execution, creates a popup window, passes it parameters and returns a value when the new window is closed.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## <span>Syntax</span>

``` js
var returnValue = window.showModalDialog(url, argumentsToPass, windowOptions);
```

## <span>Parameters</span>

### <span>url</span>

 Data-type
:   String

**String** that specifies the URL of the document to load and display.

### <span>argumentsToPass</span>

 Data-type
:   any

 The arguments to use when displaying the new document. Use this parameter to pass a value of any type, including an array of values. The dialog box can extract the values passed by the caller from the [**dialogArguments**](/dom/WindowModal/dialogArguments) property.

### <span>windowOptions</span>

 Data-type
:   String

 Specifies the window ornaments for the dialog box, using one or more of the following semicolon-delimited values:

## <span>Return Value</span>

Returns an object of type anyany

The value of the **returnValue** property as set by the window of the document specified in *url*.

## <span>Examples</span>

This example uses the **showModalDialog** method to open a customized dialog box.

``` html
<script type="text/javascript">
function fnRandom(iModifier){
   return parseInt(Math.random()*iModifier);
}
function fnSetValues(){
   var iHeight=oForm.oHeight.options[
      oForm.oHeight.selectedIndex].text;
   if(iHeight.indexOf("Random")>-1){
      iHeight=fnRandom(document.body.clientHeight);
   }
   var sFeatures="dialogHeight: " + iHeight + "px;";
   return sFeatures;
}
function fnOpen(){
   var sFeatures=fnSetValues();
   window.showModalDialog("showModalDialog_target.htm", "",
      sFeatures)
}
</script>
<form name="oForm">
    Dialog Height
  <select name="oHeight">
    <option>-- Random --</option>
    <option>150</option>
    <option>200</option>
    <option>250</option>
    <option>300</option>
  </select>
    Create Modal Dialog Box
  <input type="button" value="Push To Create" onclick="fnOpen()">
</form>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/showModalDialog2.htm)

## <span>Usage</span>

     Do not use. This API is being phased out. Chrome and Opera have already removed it by default and Firefox also considers following suit.

## <span>Notes</span>

A modal dialog box retains the input focus while open. The user cannot switch windows until the dialog box is closed. Because a modal dialog box can include a URL to a resource in a different domain, do not pass information through the *varArgIn* parameter that the user might consider private. The *varArgIn* parameter can be referenced within the modal dialog box using the [**dialogArguments**](/dom/WindowModal/dialogArguments) property of the **window** object. If the *varArgIn* parameter is defined as a string, the maximum string length that can be passed to the modal dialog box is 4096 characters; longer strings are truncated. You can set the default font settings the same way you set Cascading Style Sheets (CSS) attributes (for example, `"font:3;font-size:4"`). To define multiple font values, use multiple font attributes. To override `center`, even though the default for `center` is `yes`, you can specify either `dialogLeft` and/or `dialogTop`. When Windows Internet Explorer opens a window from a modal or modeless HTML dialog box by using the **showModalDialog** method or by using the [**showModelessDialog**](/w/index.php?title=dom/HTMLElement/showModelessDialog&action=edit&redlink=1) method, Internet Explorer uses Component Object Model (COM) to create a new instance of the window. Typically, the window is opened by using the first instance of an existing Internet Explorer process. When Internet Explorer opens the window in a new process, all the memory cookies are no longer available, including the session ID. This process is different from the process that Windows Internet Explorer uses to open a new window by using the [**open**](/dom/Window/open) method. For Windows Internet Explorer 7, `dialogHeight` and `dialogWidth` return the height and width of the content area and no longer includes the height and width of the frame. Internet Explorer 7. Although a user can manually adjust the height of a dialog box to a smaller value —provided the dialog box is resizable— the minimum `dialogHeight` you can specify is 100 pixels, and the minimum `dialogWidth` you can define is 250 pixels. In versions earlier than Internet Explorer 7 the minimum value of the `dialogWidth` that can be specified is 100 pixels.

**Note**  For Internet Explorer 7, `help` is not a valid value for `sFeatures`. In previous versions, `help:{ yes | no | 1 | 0 | on | off }` specified whether the dialog window displays the context-sensitive Help icon. This method must use a user-initiated action, such as clicking on a link or tabbing to a link and pressing enter, to open a pop-up window. The Pop-up Blocker feature in Microsoft Internet Explorer 6 blocks windows that are opened without being initiated by the user. Microsoft Internet Explorer 5 and later allows further control over modal dialog boxes through the `status` and `resizable` values in the *varOptions* parameter of the **showModalDialog** method. Turn off the status bar by calling the dialog box from a trusted application, such as Microsoft Visual Basic or an HTML Application (HTA), or from a trusted window, such as a trusted modal dialog box. These applications are considered to be trusted because they use Internet Explorer interfaces instead of the browser. Any dialog box generated from a trusted source has the status bar turned off by default. Resizing is turned off by default, but you can turn it on by specifying `resizable=yes` in the *varOptions* string of the **showModalDialog** method. The default unit of measure for `dialogHeight` and `dialogWidth` in Internet Explorer 5 and later is the pixel. The value can be an integer or floating-point number, followed by an absolute units designator (`cm`, `mm`, `in`, `pt`, or `pc`) or a relative units designator (`em`, `ex`, or `px`). For consistent results, specify the `dialogHeight` and `dialogWidth` in pixels when designing modal dialog boxes. As of Microsoft Internet Explorer 4.0, you can eliminate scroll bars on dialog boxes. To turn off the scroll bar, set the [**SCROLL**](/html/attributes/scroll) attribute to `false` in the **body** element for the dialog window, or call the modal dialog box from a trusted application.