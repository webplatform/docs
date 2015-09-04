---
title: XMLNS attribute
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec reference, standardization status'
code_samples:
  - 'http://samples.msdn.microsoft.com/workshop/samples/author/behaviors/clientcaps/addDataBinding.htm'
uri: 'apis/xhr/properties/XMLNS attribute'

---
# XMLNS attribute

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Element](/dom/Element)</span></span>

## Syntax

``` {.js}
var result = element.XMLNS attribute;
element.XMLNS attribute = value;
```

## Examples

This example shows how to declare a namespace when one of the default behaviors in Internet Explorer, clientCaps, is used as a custom tag in an HTML document. Note that the declared namespace (in this case, MSIE) is a prefix to the name of the default behavior in the custom tag. This example also shows how the clientCaps behavior can be used to install the Internet Explorer Data Binding component, if the component does not already exist in the user's system.

``` {.html}
<HTML XMLNS:MSIE>
<HEAD>
<STYLE>
@media all {
   MSIE\:clientCaps {behavior:url(#default#clientcaps);}
}
</STYLE>
<SCRIPT>
function window.onload()
{
   var bDataBindingAvailable  = false;
   var sDataBindingVersion = ;
   var sDataBindingID =
       "{333C7BC4-460F-11D0-BC04-0080C7055A83}";
   bDataBindingAvailable =
       oClientCaps.isComponentInstalled(sDataBindingID,"clsid");
   // if data binding is unavailable, install it
   if (!bDataBindingAvailable)
   {
      oClientCaps.addComponentRequest (sDataBindingID,
          "componentid");
      bDataBindingAvailable = oClientCaps.doComponentRequest();
   }
   :
}
</SCRIPT>
</HEAD>
<BODY BGCOLOR="#FFFFFF">
   :
   <MSIE:CLIENTCAPS ID="oClientCaps" />
   :
</BODY>
```

[View live example](http://samples.msdn.microsoft.com/workshop/samples/author/behaviors/clientcaps/addDataBinding.htm)

## Notes

### Remarks

You can declare multiple namespaces on the **html** tag, as shown in the following syntax.

    <HTML XMLNS:Prefix1 XMLNS:Prefix2="www.microsoft.com">

The syntax for **XMLNS** is based on the [W3C XML Namespace Spec](http://go.microsoft.com/fwlink/p/?linkid=203781). Although the World Wide Web Consortium (W3C) document allows you to declare namespaces on all tags, Microsoft Internet Explorer 5 supports namespace declaration only on the **html** tag.

## See also

### Related pages (MSDN)

-   `html`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

