---
title: domain
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, compatibility, standards, clean-up of MSDN sections'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
summary: 'Insecure. Use the web messaging API (postMessage and the message event) instead. Gets or sets the security domain of the document.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/domain

---
## Summary

Insecure. Use the web messaging API (postMessage and the message event) instead. Gets or sets the security domain of the document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var domain = document.domain;
document.domain = topLevelDomain;
```

## Return Value

Returns an object of type StringString

The current security domain of the document.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The property initially returns the host name of the server from which the page is served. The property can be assigned the domain suffix to allow sharing of pages across frames. For example, a page in one frame from home.microsoft.com and a page from www.microsoft.com initially cannot communicate with each other. However, by setting the **domain** property of both pages to the suffix "microsoft.com," you ensure that both pages are considered secure and access is available between the pages. When you set the **domain** property, use the domain name determined by the server instead of the domain name determined by the client. All the pages on different hosts must have the **domain** property explicitly set to the same value to communicate successfully with each other. For example, the value of the **domain** property of a page on the host microsoft.com is "microsoft.com" by default. It might seem logical that if you set the **domain** property of a page on another host named msdn.microsoft.com to "microsoft.com," that the two pages could communicate with each other. However, this is not the case, unless you explicitly set the **domain** property of the page on microsoft.com to "microsoft.com." This property cannot be used to enable cross-frame communication among frames with different domain suffixes. For example, a page in one frame from www.microsoft.com and a page in another frame from www.msn.com cannot communicate with each other, even if the **domain** property of both pages is set to the suffix "microsoft.com." **Security Warning:  **If you use this property incorrectly, you can compromise the security of your Web site. Set the **domain** property only if you must allow cross-domain scripting. Use a value determined on the server. If you set this property to a value determined on the client, such as through the [**location**](/dom/Location) object, you might expose your site to attack from another site through Domain Name System (DNS) manipulation. For more information, see Security Considerations: Hosting and Reuse. **Security Warning:  ** If you use this property incorrectly, you can compromise the security of your Web site. Set the **domain** property only if you must allow cross-domain scripting. Use a value determined on the server. If you set this property to a value determined on the client, such as through the [**location**](/dom/Location) object, you might expose your site to attack from another site through DNS manipulation. For more information, see Security Considerations: Dynamic HTML. For more information on domain security, see About Cross-Frame Scripting and Security.

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.4
