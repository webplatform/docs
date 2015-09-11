---
title: longdesc
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Review import; Remove MS bias; Update/improve example; Update descriptions; Fix lists & compatibility info'
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
summary: 'Links an image to a description of its content, for enhanced accessibility'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/longdesc

---
## <span>Summary</span>

Links an image to a description of its content, for enhanced accessibility

<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
dom/HTMLImageElement

</td>
</tr>
</table>
## <span>Examples</span>

The description is somewhere on the same page as the image

``` html

<img src="http://example.com/graph1" alt="Drinks are getting sweeter"
    longdesc="#graph1Explained"/>
<p id="graph1Explained">A blue capital letter "W" with kerning so it touches a blue 3, followed by a black shadow of a white capital letter C all on a white background</p>

```

The description is one of several within an external page

``` html

<img src="ExampleImage" alt="example" longdesc="http://example.com/descs#item3"/>

```

The description is included in a data: URI

``` html
<img src="logo" alt="W3C" longdesc="data:text/html;charset=utf-8;,%3C!DOCTYPE%20html%3E
%3Chtml%3E%3Chead%3E%3Ctitle%3EDescription%20of%20the%20W3C%20Logo%3C/title%3E%3C/head%3E
%3Cbody%3E%3Cp%3EA%20blue%20capital%20letter%20%22W%22%20with%20kerning%20so%20it%20
touches%20a%20blue%203%2C%20followed%20by%20a%20black%20shadow%20of%20a%20white%20
capital%20letter%20C%20all%20on%20a%20white%20background%3C/body%3E%3C/html%3E"/>
```

## <span>Notes</span>

### <span>Remarks</span>

The long description supplements the shorter description specified by the [**alt**](/html/attributes/alt) attribute. Windows Internet Explorer 8 or later. In IE8 Standards mode, the value of the **longDesc** attribute for the **frame**, **iframe**, and **img** elements depends on the context of the reference to the attribute. When read as a Document Object Model (DOM) attribute, **longDesc** returns an absolute URL. The value specified by the page author is returned when **longDesc** is read as a content attribute, when the page is displayed in an earlier document compatibility mode, or when the page is viewed with an earlier version of the browser. For more information, see Attribute Differences in Internet Explorer 8. The [**alt**](/html/attributes/alt) attribute is no longer displayed as the image tooltip for pages displayed in IE8 mode. The target of the **longDesc** attribute is now displayed as the tooltip, if present; otherwise, the [**title**](/html/attributes/title) is displayed. However, the **alt** attribute is displayed as the Microsoft Active Accessibility (MSAA) tooltip. If this attribute is not present, the title attribute is displayed instead. For more information, see Accessibility section in What's New in Internet Explorer 8. **longDesc** was introduced in Microsoft Internet Explorer 6.

## <span>Related specifications</span>

[HTML5 Image Description Extension](http://www.w3.org/TR/html-longdesc/)
:   W3C Recommendation

## <span>See also</span>

### <span>Other articles</span>

-   [img](/html/elements/img)
