---
title: tagUrn
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up MSDN import'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/tagUrn.htm'
uri: dom/HTMLElement/tagUrn

---
# tagUrn

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.tagUrn;
element.tagUrn = value;
```

## Examples

This example uses the values returned by the **scopeName** and **tagUrn** properties to create a simple HelloWorld custom tag.

The browser's status bar displays the property values.

**Note**  For IE8Standards mode to render correctly, make sure there is no spaces in your call to the HTC file.

    <HTML XMLNS:InetSDK='http://msdn.microsoft.com/workshop'>

    <STYLE>
    @media all {
       InetSDK\:HelloWorld { behavior:url(simple.htc) }
    }
    </STYLE>
    <SCRIPT>
       function window.onload()
       {
          window.status = 'scopeName = ' + hello.scopeName +
                          '; tagUrn = '  + hello.tagUrn;
       }
    </SCRIPT>
    <BODY>
       <InetSDK:HelloWorld ID='hello'></InetSDK:HelloWorld>

    </BODY>
    </HTML>

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/tagUrn.htm)

An alternative call to the HTC can also be made as an attribute, as shown in the following code example.

    <HTML XMLNS:InetSDK='http://msdn.microsoft.com/workshop'>

    <SCRIPT>
       function window.onload()
       {
          window.status = 'scopeName = ' + hello.scopeName +
                          '; tagUrn = '  + hello.tagUrn;
       }
    </SCRIPT>
    <BODY>
       <InetSDK:HelloWorld ID='hello' style="behavior:url(simple.htc)"></InetSDK:HelloWorld>

    </BODY>
    </HTML>

[**Note**  Make sure there are no spaces in your style's declaration. View live example]

## Notes

### Remarks

To declare the namespace in the document, use the [**XMLNS**](/apis/xhr/properties/XMLNS_attribute) attribute of the **html** element. Download the HTC for the sample below: [simple.htc](http://go.microsoft.com/fwlink/p/?linkid=203827)

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

