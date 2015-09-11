---
title: list-style-position
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-position)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/5841706'
  - 'http://gist.github.com/6949116'
  - 'http://gist.github.com/5598129'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`outside`'
  'Applies to': 'elements with ''display: list-item'''
  '[Inherited](/css/concepts/inherited)': 'Yes'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'as specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`listStylePosition`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Specifies if the list-item markers should appear inside or outside the content flow.'
tags:
  - CSS
  - Properties
uri: css/properties/list-style-position

---
## <span>Summary</span>

Specifies if the list-item markers should appear inside or outside the content flow.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `outside`

Applies to
:   elements with 'display: list-item'

[Inherited](/css/concepts/inherited)
:   Yes

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   as specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `listStylePosition`

## <span>Syntax</span>

-   `list-style-position: inherit`
-   `list-style-position: inside`
-   `list-style-position: outside`

## <span>Values</span>

outside
:   Default. Marker is placed outside the list item, and any wrapping text is not aligned under the marker.

inside
:   Marker is placed inside the text, and any wrapping text is aligned under the marker.

inherit
:   Takes the same specified value as the property for the element's parent. (Acts similarly to other uses of inherit in CSS.)

## <span>Examples</span>

The following example uses the **list-style-position** attribute and the **list-style-position** property to set the position for markers.

``` css
.firstlist { list-style-position:inside }
.secondlist { list-style-position:outside }
```

[View live example](http://code.webplatform.org/gist/5841706)

The following example shows how to change the value dynamically using JavaScript. The value changes from outside to inside when the mouse is over the list

``` js
var ul = document.getElementById('list-hover');

// When the mouse is over the list, the position changes to inside
ul.addEventListener('mouseover', function () {
    ul.style.listStylePosition = 'inside';
});

// When the mouse is not longer over the list, we revert back the value to outside
ul.addEventListener('mouseout', function () {
    ul.style.listStylePosition = 'outside';
});
```

[View live example](http://code.webplatform.org/gist/6949116)

An example to show how setting padding-left to 0 when position is set to outside will produce the market not being shown at all. A ul contained in a div with overflow hidden might run into this issue.

``` css
ul {
    padding-left: 0;
}

.list-position-outside {
    list-style-position: outside;
}

.list-position-inside {
    list-style-position: inside;
}
```

[View live example](http://code.webplatform.org/gist/5598129)

## <span>Usage</span>

     ===Remarks===

If a list-style-position is set to outside and padding-left is set to 0, the marker will not show.

## <span>Related specifications</span>

[CSS Level 2 (Revision 1)](http://www.w3.org/TR/CSS21/generate.html#propdef-list-style-position)
:   Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>CSS Attributes</span>

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   **list-style-position**

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-select](/css/properties/user-select)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [baseline-shift](/svg/attributes/baseline-shift)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### <span>Related pages (MSDN)</span>

-   `CSSStyleDeclaration`
-   `currentStyle`
-   `runtimeStyle`
-   `style`
