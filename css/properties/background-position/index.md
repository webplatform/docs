---
title: background-position
code_samples:
  - 'http://chrisdavidmills.github.com/basic-background-position/'
  - 'http://chrisdavidmills.github.com/css-sprites-example/'
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`0% 0%`'
  'Applies to': 'All elements'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'A list, each item consisting of: two keywords representing the origin and two offsets from that origin, each given as an absolute length (if given a \<length\>), otherwise as a percentage.'
  Animatable: 'Yes'
  '[CSS Object Model Property](/css/concepts/cssom)': '`backgroundPosition`'
  Percentages: 'Refer to size of background positioning area minus size of background image'
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'background-position allows you to set the placement of a background-image on the element it is applied to. background-position generally takes two values, which set the horizontal and vertical position of the background image inside the element.'
tags:
  - CSS
  - Properties
uri: css/properties/background-position

---
## <span>Summary</span>

background-position allows you to set the placement of a background-image on the element it is applied to. background-position generally takes two values, which set the horizontal and vertical position of the background image inside the element.

## <span>Overview table</span>

[Initial value](/css/concepts/initial_value)
:   `0% 0%`

Applies to
:   All elements

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   A list, each item consisting of: two keywords representing the origin and two offsets from that origin, each given as an absolute length (if given a \<length\>), otherwise as a percentage.

Animatable
:   Yes

[CSS Object Model Property](/css/concepts/cssom)
:   `backgroundPosition`

Percentages
:   Refer to size of background positioning area minus size of background image

## <span>Syntax</span>

-   `background-position: 30% 15%, 40% 80%, 10px 10px`
-   `background-position: length length`
-   `background-position: percentage percentage`
-   `background-position: percentage`
-   `background-position: bottom length right length`
-   `background-position: left top`

## <span>Values</span>

[length](/css/data_types/length) [length](/css/data_types/length)
:   Any standard CSS units are acceptable as `background-position` values: px, ems, rems, mm, cm etc. Note that unit values specify the distance the top left corner of the background image is away from the top left corner of the element. For more details on these units, read [Length units](/css/data_types/length).

[percentage](/css/data_types/percentage) [percentage](/css/data_types/percentage)
:   Percentages are acceptable for `background-position` values, and specify percentages of the overall width and height of the element in question. Note that percentage values specify the distance the top left corner of the background image is away from the top left corner of the element.

left top
:   `background-position` can also be expressed as keywords: left top, top, right top, left, center, right, left bottom, bottom, right bottom. These values do not relate specifically to the position of the top left hand corner of the background image, but rather the overall position of the background image inside the element. So for example, a value of `right top` will make the background image site flush to the top and right sides of the element it is applied to; the top left corner *won't* be positioned at the top right of the element!

[percentage](/css/data_types/percentage)
:   If only a single value is included, that is taken as the horizontal value, and the vertical value is set as `center`.

30% 15%, 40% 80%, 10px 10px
:   If you have applied multiple background images to an element, you can give each background image a different position by specifying multiple background position values delimited by commas. The values supplied will cycle so that all images are given a `background-position`, for example if four background images are specified and only two position values, position 1 will be applied to images 1 and 3, and position 2 to images 2 and 4.

bottom [length](/css/data_types/length) right [length](/css/data_types/length)
:   CSS3 includes the new four value `background-position` syntax, which allows you to choose which sides of the element you are positioning the background image relative to (values 1 and 3), and then the distance away from those sides (values 2 and 4). So this example says that you want to position the background image 10 pixels from the bottom of the element, and 15 pixels from the right. If you miss out one of the offset values, the other is assumed to be 0.

## <span>Examples</span>

A simple set of five divs.

``` html
<div class="one">One</div>
<div class="two">Two</div>
<div class="three">Three</div>
<div class="four">Four</div>
<div class="five">Five</div>
```

This CSS applies the same background image and basic styling to each div, but then each div is given a different background position to vary where the background image is placed.

``` css
div {
  background-image: url(images/icon.png);
  background-repeat: no-repeat;
  font-family: sans-serif;
  font-size: 16px;
  letter-spacing: -1px;
  width: 200px;
  height: 100px;
  margin-right: 10px;
  border: 1px solid #aaa;
  float: left;
  line-height: 100px;
  text-align: center;
  border-radius: 10px;
  text-transform: uppercase;
  text-shadow: 1px 1px 1px black;
  box-shadow: 2px 2px 5px #ccc;
  padding-top: 2px;
}


.one {
  background-position: top left; /* positioned at the top left of the element */
}

.two {
  background-position: 2rem 1rem; /* positioned 2rems from the left of the element, and 1rem from the top */
}

.three {
  background-position: 40% 80%; /* positioned 40% of the element's width away from the left side, and 80% of the element's height down from the top */
}

.four {
  background-position: 30px; /* positioned 30px from the left of the element, and vertically centered (the assumed value when no second value is specified) */
}

.five {
  background-position: bottom 30px right 50px; /* positioned 30px from the bottom of the element and 50px from the right */
}
```

[View live example](http://chrisdavidmills.github.com/basic-background-position/)

An outer container div with several inner divs.

``` html
<div id="outer">
    <div id="save"></div>
    <div id="settings"></div>
    <div id="people"></div>
    <div id="search"></div>
    <div id="cancel"></div>
    <div id="ok"></div>
    <div id="back"></div>
    <div id="forward"></div>
  </div>
```

Every inner div is given the same basic styling, and has the same background image applied to it. Each individual div is then given different top and left values to position it in a different place, and a different background-position value to display a different sprite. Each sprite is 128 x 128 px, and the inners divs are set to 128 x 128 px in size, so only a single sprite will be displayed at once by each of them. You need to get the background positions right, so that a whole sprite is displayed, not a part of two sprites.

``` css
body > div { /* Basic styling for the outer container div */
  width: 1024px;
  height: 640px;
  margin : 5rem auto;
  background: linear-gradient(top right, rgba(0,0,0,0),rgba(0,0,0,0.4));
  background-color: #ccc;
  border-radius: 64px;
  box-shadow: 0px 0px 30px black;
  position: relative;
}

div div { /* all the inner divs are given the same width and height, background image, and absolute positioning */
  width: 128px;
  height: 128px;
  position: absolute;
  background: url(sprites.png);
}

#save { /* each individual div is then given different top and left values to position it in a different place,
                  and a different background-position value to display a different sprite. Each sprite is 128 x 128 px, and
    the inners divs are set to 128 x 128 px in size, so only a single sprite will be displayed at once by
    each of them. You need to get the background positions right, so that a whole sprite is displayed, not
    a part of two sprites  */
  top: 64px;
  left: 64px;
  background-position: 0px 0px;
}

#settings {
  top: 192px;
  left: 192px;
  background-position: -128px 0px;
}

#people {
  top: 320px;
  left: 448px;
  background-position: -256px 0px;
}

#search {
  top: 320px;
  left: 64px;
  background-position: -384px 0px;
}

#cancel {
  top: 448px;
  left: 576px;
  background-position: -512px 0px;
}

#ok {
  top: 448px;
  left: 704px;
  background-position: -640px 0px;
}

#back {
  top: 192px;
  left: 832px;
  background-position: -768px 0px;
}

#forward {
  top: 320px;
  left: 832px;
  background-position: -896px 0px;
}
```

[View live example](http://chrisdavidmills.github.com/css-sprites-example/)

## <span>Usage</span>

     * background-position has good support across browsers. Be aware however that some CSS data types are recent additions to the language and are not supported across older browsers.

-   CSS sprites is a very common technique used to display multiple small images on a web page while cutting down on file size and HTTP requests. The images in question are all stored in a single image file which is applied to multiple different elements on the page; different parts of that file are then displayed by varying the `background-position` values. See example 2 for this in action.
-   The four value syntax is not supported very widely across browsers.

## <span>Related specifications</span>

[CSS 2.1 Colors and Backgrounds](http://www.w3.org/TR/CSS2/colors.html)
:   W3C Recommendation

[CSS Backgrounds and Borders Module Level 3](http://www.w3.org/TR/css3-background/#background-position)
:   W3C Candidate Recommendation

## <span>See also</span>

### <span>Related articles</span>

#### <span>Background</span>

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   **background-position**

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

#### <span>CSS Attributes</span>

-   [background-blend-mode](/css/properties/background-blend-mode)

-   **background-position**

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

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

### <span>Other articles</span>

-   [Using CSS background images](/tutorials/using_css_background_images)
