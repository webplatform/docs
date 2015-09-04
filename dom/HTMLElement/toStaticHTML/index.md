---
title: toStaticHTML
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up MSDN import'
uri: dom/HTMLElement/toStaticHTML

---
# toStaticHTML

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLElement](/dom/HTMLElement)*

## Syntax

``` {.js}
var object = object.toStaticHTML(bstrHTML, pbstrStaticHTML);
```

## Parameters

### bstrHTML

 Data-typeÂ
:   BSTR

 An HTML fragment.

### pbstrStaticHTML

 Data-typeÂ
:   BSTR

 An HTML fragment consisting of static elements only.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

String

An HTML fragment consisting of static elements only.

## Examples

The following script demonstrates how **toStaticHTML** sanitizes script and dynamic HTML attributes. The result of the operation is: `<span>Click Me</span>`.

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

## Notes

### Remarks

The **toStaticHTML** method can be used to remove event attributes and script from user input before it is displayed as HTML. Malicious HTML can be passed on a URL, in form parameters, or across domains by **XDomainRequest** or [**postMessage**](/dom/Window/postMessage). Always validate user input before adding it as an HTML fragment to a webpage or storing it in a database. **Note**Â Â Â This method does not filter the attributes of the **base** element. This can cause potentially unwanted redirect requests for **link** and [**anchor**](/html/elements/a) elements injected into a webpage. For best results, only use **toStaticHTML** to modify elements in the body of a webpage.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages (MSDN)

-   `window`
-   `innerHTML`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

