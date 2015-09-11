---
title: position
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/CSS/position)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://jsfiddle.net/DqxfR/'
  - 'http://jsfiddle.net/58ybJ/1/'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`static`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'As specified'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`position`'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The position property controls the type of positioning used by an element within its parent elements. The effect of the position property depends on a lot of factors, for example the position property of parent elements.'
tags:
  0: CSS
  1: Properties
  3: Design
uri: css/properties/position

---
## <span>Summary</span>

The position property controls the type of positioning used by an element within its parent elements. The effect of the position property depends on a lot of factors, for example the position property of parent elements.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `static`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   As specified

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `position`

## <span>Syntax</span>

-   `position: absolute`
-   `position: fixed`
-   `position: inherit`
-   `position: relative`
-   `position: static`

## <span>Values</span>

static
:   Default. Object has no special positioning; it follows the layout rules of HTML. Values of [top](/css/properties/top), [bottom](/css/properties/bottom), [left](/css/properties/left) and [right](/css/properties/right) have no impact.

absolute
:   Object is positioned relative to nearest positioned ancestor—or to the initial containing block if no positioned ancestor exists—using the [**top**](/css/properties/top) and [**left**](/css/properties/left) properties.

relative
:   Object is positioned according to the normal flow, and then offset by the [**top**](/css/properties/top) and [**left**](/css/properties/left) properties.

fixed
:   Object is positioned relative to the viewport containing the content. Object stays in the viewport when scrolling. Usually used for navigation on mobile devices. Limited support.

inherit
:   Inherits the value of the parent element.

## <span>Examples</span>

The example shows how a child element’s position depends on the position value of its parent, as well as its own position value.

``` html
<section class="parent static">
    <div class="child absolute">
        <p>absolute</p>
    </div>
    <p>static</p>
</section>

<section class="parent static">
    <div class="child static">
        <p>static</p>
    </div>
    <p>static</p>
</section>

<section class="parent static">
    <div class="child relative">
        <p>relative</p>
    </div>
    <p>static</p>
</section>

<section class="parent relative">
    <div class="child absolute">
        <p>absolute</p>
    </div>
    <p>relative</p>
</section>
```

[View live example](http://jsfiddle.net/DqxfR/)

Watch how the child positions itself relative to the parent, depending on the value of position for both elements.

``` css
.static {
    position: static;
}

.relative {
    position: relative;
}

.absolute {
    position: absolute;
}

.fixed {
    position: fixed;
}

.child {
    top: 30px;
    left: 20px;

    background-color: #ff3856;
    width: 100px;
    height: 100px;
}

.parent {
    background-color: #6acc18;
    margin: 80px;
    width: 160px;
    height: 160px;
}
```

A typical navigation menu with **position: fixed**.

``` html
<nav class="nav nav-fixed">
    <a href="#">Home</a>
    <a href="#">Something</a>
    <a href="#">Contact</a>
</nav>

<section class="long-scrollable"></section>
```

[View live example](http://jsfiddle.net/58ybJ/1/)

While the .long-scrollable section is scrolled down, the .nav-fixed stays fixed at the top of the viewport.

``` css
.long-scrollable {
    border: 2px dotted #999;
    height: 2000px;
}

.nav {
    background-color: #000;
    color: #fff;
    width: 100%;
    height: 40px;
}

.nav-fixed {
    position: fixed;
}
```

## <span>Usage</span>

     ===Static (Default)===

The element is laid out according to normal HTML flow.

### <span>Relative</span>

Setting the property to **relative** places the object in the natural HTML flow of the document, but offsets the position of the object from its normal position. The following syntax shows how to create superscript text by placing the text in a span that is positioned relative to its original position.

``` html
<p>The superscript in this name
    <span style="position: relative; top: -3px">xyz</span>
    is "xyz".</p>
```

The superscript in this name <span style="position: relative; top: -3px">xyz</span> is "xyz".

* * * * *

Text and objects that follow a relatively positioned object occupy their own space and do not overlap the natural space for the positioned object. In contrast, text and objects that follow an absolutely positioned object occupy what would have been the natural space for the positioned object before it was pulled out of the flow. Placing an absolutely positioned object beyond the viewable area of the window causes a scroll bar to appear. When relatively positioned objects are placed beyond the viewable area, a scroll bar is not shown. The size of the content determines the size of objects with layout. For example, setting the height and position properties on a div object gives it layout. The content of the div determines the size. In this case, the content determines the size of the width.

### <span>Absolute</span>

Setting the property to **absolute** pulls the object out of the "flow" of the document and positions it regardless of the layout of surrounding objects. If other objects already occupy the given position, they do not affect the positioned object, nor does the positioned object affect them. Instead, all objects are drawn at the same place, causing the objects to overlap. (This overlap is controlled by using the [z-index](/css/properties/z-index) property.)

Absolutely positioned elements are positioned relative to their containing blocks. The containing block for an absolutely positioned element is formed by the padding edge of the element’s nearest positioned ancestor-- the closest parent element that has a position value of **relative**, **absolute**, or **fixed**. If no positioned ancestor exists, the containing block is the initial containing block-- the viewport or the page box.

The edges of the element can be specified relative to the edges of the containing block by using the [top](/css/properties/top), [bottom](/css/properties/bottom), [left](/css/properties/left) and [right](/css/properties/right) properties.

Absolutely positioned objects do not have **margins**, but they do have borders and padding.

#### <span>Side Note</span>

Input from pointing devices, such as the mouse, does not penetrate through overlapping elements even if the elements are not visible. This is also true for positioned elements with a negative z-index unless:

-   The parent is a scrolling container (that is, its overflow property is set to auto or scroll).
-   The parent is positioned (that is, its position property is set to absolute or relative).

### <span>Fixed</span>

An element with a **fixed** position is positioned relative to the visible viewport. It does not move away if the browser window is scrolled but appears to be fixed in the viewport. A common pattern and example is to use position: fixed on navigation elements that should be visible on the whole page regardless of the scrollbar position. Fixed positioning is only supported for pages using a strict \<!DOCTYPE\> directive.

## <span>Notes</span>

### <span>Layout Float</span>

**static** The positioned float is laid out according to normal HTML flow.

**absolute** The positioned float is laid out relative to its containing block, but the positioned float will affect the normal flow of its container. Inline content wraps around the positioned float; the positioned float is not laid out on top of inline content.

**relative** The positioned float is laid out relative to where it would fall in the normal flow. The bottom, top, left, and right properties can be used to calculate an offset from the element's position in the normal flow. Content will flow around the original position of the element, and the actual positioned float will be superimposed on top of inline content.

**fixed** The positioned float is laid out relative to the initial position of the viewport, or browser window. (The positioned float's position is not updated as the viewport moves due to scrolling.)

## <span>Related specifications</span>

[CSS 2.1](http://www.w3.org/TR/CSS2/visuren.html#choose-position)
:   W3C Recommendation

## <span>See also</span>

## <span>Related Tutorials</span>

-   [Static and relative positioning](/tutorials/static_and_relative_positioning)
-   [Absolute and fixed positioning](/tutorials/absolute_and_fixed_positioning)
