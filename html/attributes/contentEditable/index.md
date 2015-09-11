---
title: contentEditable
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/contentEditableEX2.htm'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
summary: 'Sets or retrieves the string that indicates whether the user can edit the content of the object.'
tags:
  - Markup
  - Attributes
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/designMode
    - 'dom/properties/disabled (redundant)'
    - dom/Event/input
    - dom/defaultSelected
uri: html/attributes/contentEditable

---
## <span>Summary</span>

Sets or retrieves the string that indicates whether the user can edit the content of the object.

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
</td>
</tr>
</table>
## <span>Examples</span>

In the following example, setting the **DIV** elements to have `100%` [**height**](/css/properties/height) and [**width**](/css/properties/width) makes all content within the borders of the cells editable.

``` html
<P>Table 1 Editable</P><BR/>
<TABLE BORDER=1 WIDTH=80%>
<THEAD>
<TR>
<TH><DIV CONTENTEDITABLE STYLE="height: 100%; width: 100%;">Heading 1 <DIV></TH>
<TH><DIV CONTENTEDITABLE STYLE="height: 100%; width: 100%;">Heading 2 <DIV></TH>
</TR>
</THEAD>
<TBODY>
<TR>
<TD><DIV CONTENTEDITABLE STYLE="height: 100%; width: 100%;">Row 1, Column 1 text.<DIV></TD>
<TD><DIV CONTENTEDITABLE STYLE="height: 100%; width: 100%;">Row 1, Column 2 text.<DIV></TD>
</TR>
<TR>
<TD><DIV CONTENTEDITABLE STYLE="height: 100%; width: 100%;">Row 2, Column 1 text.<DIV></TD>
<TD><DIV CONTENTEDITABLE STYLE="height: 100%; width: 100%;">Row 2, Column 2 text.<DIV></TD>
</TR>
</TBODY>
</TABLE>
```

The following example shows how to use the **contentEditable** property to control whether the user can edit the content of the object.

``` html
<HEAD>
<SCRIPT>
function chgSpan() {
    currentState = oSpan.isContentEditable;
    newState = !currentState;
    oSpan.contentEditable = newState;
    oCurrentValue.innerText = newState;
    newState==false ? oBtn.innerText="Enable Editing" :
        oBtn.innerText="Disable Editing"
}
</SCRIPT>
</HEAD>
<BODY onload="oCurrentValue.innerText = oSpan.isContentEditable;">
<P>Click the button to enable or disable SPAN content editing.</P>
<P>
<BUTTON ID="oBtn" onclick="chgSpan()">Enable Editing</BUTTON>
</P>
<P><SPAN ID="oSpan">You can edit this text.</SPAN></P>
SPAN can be edited: <SPAN ID="oCurrentValue"></SPAN>
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/contentEditableEX2.htm)

## <span>Notes</span>

### <span>Remarks</span>

Child elements do not inherit this attribute unless they have layout. Use the [**hasLayout**](/css/cssom/properties/hasLayout) property to determine if an object has layout. If this attribute is applied to a **BODY** element, it has the same effect as setting the [**designMode**](/w/index.php?title=dom/properties/designMode&action=edit&redlink=1) property of the [**Document**](/dom/Document) object. Elements with the [**disabled**](/w/index.php?title=dom/properties/disabled_(redundant)&action=edit&redlink=1) attribute set to `false` do not respond to the **contentEditable** attribute. If this attribute is applied to the [**A**](/html/elements/a) element, the default functionality of the **A** element will be lost while *p* is set to the value of `true`. If this attribute is applied to the **MARQUEE** element, the default functionality of the **MARQUEE** element will be lost while *p* is set to the value of `true`. Though the [**TABLE**](/html/elements/table), **COL**, **COLGROUP**, **TBODY**, **TD**, **TFOOT**, **TH**, **THEAD**, and **TR** elements cannot be set as content editable directly, a content editable **SPAN**, or **DIV** element can be placed inside the individual table cells (**TD** and **TH** elements). See the example below. **Security Warning:  **Users can change the contents of a document when the **contentEditable** property is set to TRUE. Using this property incorrectly can compromise the security of your application. Incorrect use of the **contentEditable** property might include not validating user input. If you do not validate user input, a malicious user can inject control characters or script that can harm your data. You should take routine precautions against displaying unvalidated user input. For more information, see Security Considerations: Dynamic HTML. Windows Internet Explorer 8 and later. When a webpage is displayed in IE8 Standards mode, an object cannot receive focus when *p* is set to `false`. When pages are displayed in earlier document compatibility modes, objects can receive focus when *p* is `false`.

### <span>Compatibility</span>

-   [IE bug 809254](https://connect.microsoft.com/IE/feedbackdetail/view/809254): IE9-10 window freezes when using mousewheel while dragging
-   [IE bug 801770](https://connect.microsoft.com/IE/feedbackdetail/view/801770): IE10 crashes after selecting "Cut" from the context menu
-   [IE bug 796187](https://connect.microsoft.com/IE/feedback/details/796187/internet-explorer-10-crash-with-contenteditable-list): IE10 crashes in some cases when editing lists
-   [IE bug 774350](https://connect.microsoft.com/IE/feedbackdetail/view/774350): IE10 does not fire `contextmenu` event when right-clicking on misspelled words
-   [IE bug 794285](https://connect.microsoft.com/IE/feedbackdetail/view/794285): IE10-11 does not fire the `input` event
-   [IE bug 807199](https://connect.microsoft.com/IE/feedbackdetail/view/807199): IE11+ does not allow placing the caret in an empty table cell
-   [IE bug 864804](https://connect.microsoft.com/IE/feedbackdetail/view/864804): IE11 appends `<br>` elements to the `<body>` when showing/hiding an `<iframe>` with `contenteditable` document inside
-   [IE bug 907422](https://connect.microsoft.com/IE/feedbackdetail/view/907422): IE11 does not allow disabling resize handles for images/inputs
-   [IE bug 858749](https://connect.microsoft.com/IE/feedback/details/858749): IE11+ uses invalid positioning for caret when an element is floated

## <span>See also</span>

### <span>External resources</span>

-   [Contenteditable Demo](http://demo.xpertdeveloper.com/contenteditable-attribute/)

### <span>Related pages (MSDN)</span>

-   `defaults`
-   `a`
-   `abbr`
-   `acronym`
-   `address`
-   `b`
-   `bdo`
-   `big`
-   `blockQuote`
-   `body`
-   `button`
-   `center`
-   `cite`
-   `code`
-   `custom`
-   `dd`
-   `del`
-   `dfn`
-   `dir`
-   `div`
-   `dl`
-   `dt`
-   `em`
-   `fieldSet`
-   `font`
-   `form`
-   `hn`
-   `i`
-   `input type=button`
-   `input type=password`
-   `input type=radio`
-   `input type=reset`
-   `input type=submit`
-   `input type=text`
-   `ins`
-   `isIndex`
-   `kbd`
-   `label`
-   `legend`
-   `li`
-   `listing`
-   `marquee`
-   `menu`
-   `noBR`
-   `ol`
-   `p`
-   `plainText`
-   `pre`
-   `q`
-   `rt`
-   `ruby`
-   `s`
-   `samp`
-   `small`
-   `span`
-   `strike`
-   `strong`
-   `sub`
-   `sup`
-   `textArea`
-   `tt`
-   `u`
-   `ul`
-   `var`
-   `xmp`
