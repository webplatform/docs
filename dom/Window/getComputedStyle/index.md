---
title: getComputedStyle
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[getComputedStyle](https://developer.mozilla.org/en-US/docs/DOM/window.getComputedStyle) Article]'
  - 'Microsoft Developer Network: [[getComputedStyle Method](http://msdn.microsoft.com/en-us/library/ie/ff975168(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
  return_type:
    predicate: 'Returns an object of type  '
    value: CSSStyleDeclaration
    href: /dom/Window
standardization_status: 'W3C Recommendation'
summary: "Gets the values of all the CSS properties of an element after applying the active stylesheets and resolving the basic computations they may contain. \n"
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/getComputedStyle

---
## Summary

Gets the values of all the CSS properties of an element after applying the active stylesheets and resolving the basic computations they may contain.

The returned object is of the same type that the object returned from the element's ["style"](/css/cssom/style) property, however the two objects have different purposes. The object returned from getComputedStyle is read-only and can be used to inspect the element's style (including those set by a \<style\> element or an external stylesheet). The elt.style object should be used to set styles on a specific element.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
var declaration = window.getComputedStyle(/* see parameter list */);
```

## Parameters

### element

 Data-type
:   DOM Node

 The element that contains the desired style settings.

### pseudoElementName

 Data-type
:   String

(Optional)

The name of a CSS pseudo-element or a null value ("::before" or "::after"). Optional in WebKit based browsers.

## Return Value

Returns an object of type CSSStyleDeclarationCSSStyleDeclaration

A [**CSSStyleDeclaration**](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration) object that contains the CSS settings applied to the desired object.

The settings in the returned object account for all applicable style rules and represent the resolved values for the various CSS properties applied to the specified object.

## Examples

``` js
var elem1 = document.getElementById("elemId");
var style = window.getComputedStyle(elem1, null);

// this is equivalent:
// var style = document.defaultView.getComputedStyle(elem1, null);
```

``` html
<style><br/> #elem-container{<br/>   position: absolute;<br/>   left:     100px;<br/>   top:      200px;<br/>   height:   100px;<br/> }<br/></style><br/> <br/><div id="elem-container">dummy</div><br/><div id="output"></div>  <br/> <br/><script><br/>  function getTheStyle(){<br/>    var elem = document.getElementById("elem-container");<br/>    var theCSSprop = window.getComputedStyle(elem,null).getPropertyValue("height");<br/>    document.getElementById("output").innerHTML = theCSSprop;<br/>   }<br/>  getTheStyle();<br/></script>
```

getComputedStyle can pull style info off of pseudo-elements (for example, ::after, ::before, ::marker, ::line-marker).

``` html
<style><br/> h3:after {<br/>   content: ' rocks!';<br/> }<br/></style><br/> <br/><h3>generated content</h3> <br/> <br/><script><br/>  var h3       = document.querySelector('h3'), <br/>      result   = getComputedStyle(h3, ':after').content;<br/> <br/>  console.log('the generated content is: ', result); // returns ' rocks!'<br/></script>
```

## Notes

The first argument must be an Element (passing a non-Element Node, like a \#text Node, will throw an error).

 The returned object actually represents the CSS 2.1 resolved values, not the computed values. While those values are usually equal, some older CSS properties like 'width', 'height' or 'padding' will return their used value instead.

Originally, CSS 2.0 defined the computed values to be the "ready to be used" final values of properties after cascading and inheritance, but CSS 2.1 redefined computed values as pre-layout, and added the used values as post-layout. The differences between pre- and post-layout does include the resolution of percentages relative to the width or the height of an element (its layout).

While the computed style will return percentages values untouched in this case, the getComputedStyle function will sometimes, to preserve backwards compatibility, return the old meaning of computed values (now called used values) for a specific set of CSS 2.0 properties and resolve those percentages anyway.

 The returned value can, in certain known cases, be expressly inaccurate by deliberate intent. In particular, to avoid the so called CSS History Leak security issue, browsers may expressly "lie" about the used value for a link and always return values as if a user has never visited the linked site. See <http://blog.mozilla.com/security/2010/03/31/plugging-the-css-history-leak/> and <http://hacks.mozilla.org/2010/03/privacy-related-changes-coming-to-css-vistited/> for details of the examples of how this is implemented, most other modern browser have applied similar changes to the application of pseudo-selector styles and the values returned by getComputedStyle.

During a CSS transition, getComputedStyle returns the original property value in FireFox, but the final property value in WebKit.

When the *pseudoElementName* is set to a value other than null, the value is interpreted as a CSS pseudo-element with respect to the object specified in the *element* parameter.

Starting in Gecko 1.9.2 (Firefox 3.6 / Thunderbird 3.1 / Fennec 1.0), returned URL values now have quotes around the URL, like this: url("<http://foo.com/bar.jpg>").

## Related specifications

[DOM Level 2 Style](http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html)
:   Recommendation

[CSS Object Model (resolved style)](http://dev.w3.org/csswg/cssom/#resolved-values)
:   Draft

## See also

### Related articles

#### CSSOM

-   [href](/css/cssom/CSSImportRule/href)

-   [media](/css/cssom/CSSImportRule/media)

-   [CSSKeyframeRule](/css/cssom/CSSKeyframeRule)

-   [keyText](/css/cssom/CSSKeyframeRule/keyText)

-   [style](/css/cssom/CSSKeyframeRule/style)

-   [CSSKeyframesRule](/css/cssom/CSSKeyframesRule)

-   [cssRules](/css/cssom/CSSKeyframesRule/cssRules)

-   [deleteRule](/css/cssom/CSSKeyframesRule/deleteRule)

-   [findRule](/css/cssom/CSSKeyframesRule/findRule)

-   [insertRule](/css/cssom/CSSKeyframesRule/insertRule)

-   [name](/css/cssom/CSSKeyframesRule/name)

-   [CSSMediaList](/css/cssom/CSSMediaList/CSSMediaList)

-   [appendMedium](/css/cssom/CSSMediaList/appendMedium)

-   [deleteMedium](/css/cssom/CSSMediaList/deleteMedium)

-   [item](/css/cssom/CSSMediaList/item)

-   [mediaText](/css/cssom/CSSMediaList/mediaText)

-   [CSSMediaRule](/css/cssom/CSSMediaRule/CSSMediaRule)

-   [cssRules](/css/cssom/CSSMediaRule/cssRules)

-   [deleteRule](/css/cssom/CSSMediaRule/deleteRule)

-   [insertRule](/css/cssom/CSSMediaRule/insertRule)

-   [media](/css/cssom/CSSMediaRule/media)

-   [CSSNamespaceRule](/css/cssom/CSSNamespaceRule/CSSNamespaceRule)

-   [namespaceURI](/css/cssom/CSSNamespaceRule/namespaceURI)

-   [prefix](/css/cssom/CSSNamespaceRule/prefix)

-   [CSSOM View](/css/cssom/CSSOM_view)

-   [CSSRule](/css/cssom/CSSRule)

-   [cssText](/css/cssom/CSSRule/cssText)

-   [parentStyleSheet](/css/cssom/CSSRule/parentStyleSheet)

-   [type](/css/cssom/CSSRule/type)

-   [getPropertyPriority](/css/cssom/CSSStyleDeclaration/getPropertyPriority)

-   [clipLeft](/css/cssom/properties/clipLeft)

-   [clipRight](/css/cssom/properties/clipRight)

-   [clipTop](/css/cssom/properties/clipTop)

-   [cssFloat](/css/cssom/properties/cssFloat)

-   [fontWeight](/css/cssom/properties/fontWeight)

-   [hasLayout](/css/cssom/properties/hasLayout)

-   [height](/css/cssom/properties/height)

-   [href](/css/cssom/properties/href)

-   [imports](/css/cssom/properties/imports)

-   [innerWidth](/css/cssom/properties/innerWidth)

-   [isAlternate](/css/cssom/properties/isAlternate)

-   [isPrefAlternate](/css/cssom/properties/isPrefAlternate)

-   [item](/css/cssom/properties/item)

-   [length](/css/cssom/properties/length)

-   [media](/css/cssom/properties/media)

-   [offsetX](/css/cssom/properties/offsetX)

-   [offsetY](/css/cssom/properties/offsetY)

-   [outerHeight](/css/cssom/properties/outerHeight)

-   [outerWidth](/css/cssom/properties/outerWidth)

-   [pageX](/css/cssom/properties/pageX)

-   [pageXOffset](/css/cssom/properties/pageXOffset)

-   [pageY](/css/cssom/properties/pageY)

-   [pageYOffset](/css/cssom/properties/pageYOffset)

-   [pixelBottom](/css/cssom/properties/pixelBottom)

-   [deviceXDPI](/css/cssom/screen/deviceXDPI)

-   [deviceYDPI](/css/cssom/screen/deviceYDPI)

-   [fontSmoothingEnabled](/css/cssom/screen/fontSmoothingEnabled)

-   [height](/css/cssom/screen/height)

-   [style](/css/cssom/style)

-   [type](/css/cssom/style/type)

-   [styleSheet](/css/cssom/styleSheet)

-   [addImport](/css/cssom/styleSheet/addImport)

-   [blockDirection](/css/cssom/styleSheet/blockDirection)

-   [cssRules](/css/cssom/styleSheet/cssRules)

-   [cssText](/css/cssom/styleSheet/cssText)

-   [ownerNode](/css/cssom/styleSheet/ownerNode)

-   [removeImport](/css/cssom/stylesheet/removeImport)

-   [removeRule](/css/cssom/stylesheet/removeRule)

-   [matchMedium](/css/media_queries/apis/matchMedium)

-   **getComputedStyle**

-   [innerHeight](/dom/Window/innerHeight)

-   [styleMedia](/dom/Window/styleMedia)

### External resources

Microsoft Test Drive for getComputedStyle <http://ie.microsoft.com/testdrive/HTML5/getComputedStyle/>
