---
title: 'toStaticHTML'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up MSDN import'
readiness: 'In Progress'
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
  - API_Object_Methods
  - DOM
  - Needs_Summary
uri: dom/HTMLElement/toStaticHTML

---
Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var object = object.toStaticHTML(bstrHTML, pbstrStaticHTML);
```

## Parameters

### bstrHTML

 Data-type
:   BSTR

 An HTML fragment.

### pbstrStaticHTML

 Data-type
:   BSTR

 An HTML fragment consisting of static elements only.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

String

An HTML fragment consisting of static elements only.

## Examples

The following script demonstrates how **toStaticHTML** sanitizes script and dynamic HTML attributes. The result of the operation is: `Click Me`.

``` html
<script type="text/javascript">
function sanitize()
{
    var szInput = myDiv.innerHTML;
    var szStaticHTML = toStaticHTML(szInput);
    ResultComment = "\ntoStaticHTML sanitized the HTML fragment as follows:\n"
        + "Original Content:\n" + szInput + "\n"
        + "Static Content:\n" + szStaticHTML + "\n";
    myDiv.innerText = ResultComment;
}
</script>
</head>
<body onload="sanitize()">
    <div id="myDiv">
    <script>function test() { alert("Testing, Testing, 123..."); }</script>
    <span onclick="test()">Click Me</span>
    </div>
</body>
```

## Notes

### Remarks

The **toStaticHTML** method can be used to remove event attributes and script from user input before it is displayed as HTML. Malicious HTML can be passed on a URL, in form parameters, or across domains by **XDomainRequest** or [**postMessage**](/dom/Window/postMessage). Always validate user input before adding it as an HTML fragment to a webpage or storing it in a database. **Note**   This method does not filter the attributes of the **base** element. This can cause potentially unwanted redirect requests for **link** and [**anchor**](/html/elements/a) elements injected into a webpage. For best results, only use **toStaticHTML** to modify elements in the body of a webpage.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages

-   `window`
-   innerHTML[innerHTML](/dom/HTMLElement/innerHTML)
