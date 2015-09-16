---
title: sizes
code_samples:
  - 'http://codepen.io/justincavery/full/vjAgF/'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The sizes attribute is an extension of the image element. It provides additional image related information to the browser to help decide the most appropriate image to load based on the viewport. Most commonly used for delivering the best image for responsive images. It can only be used in conjunction with srcset'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/sizes

---
## Summary

The sizes attribute is an extension of the image element. It provides additional image related information to the browser to help decide the most appropriate image to load based on the viewport. Most commonly used for delivering the best image for responsive images. It can only be used in conjunction with srcset

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
**sizes** attribute is an extension of the of the [image element](/html/elements/img) and is used to inform the browser which [srcset](/html/attributes/srcset) image source to render based on the rules set out. **sizes** do not provide an instruction to the browser (*must* use *this* image *here*) but rather“*here is a viewport condition, use the best suited image based on your viewport, device pixel ration along with the width I said the image is going to be*”.

       sizes="[media query] [length], [media query] [length]"

Lengths can be declared using fixed widths (pixels) or relative units (**vw** or viewport width). When declaring **sizes** it is recommended that the final **vw** unit be declared as 100vw to cover all of the **sizes** you do not consider.

       sizes="(min-width:30em) 300px, (min-width:60em) 500px, 100vw"

## Examples

Sizes attribute used in conjunction with SRCSET

``` html
<img
 srcset="http://placehold.it/1024x500&text=1024+Large.jpg 1024w, http://placehold.it/600x250&text=600+Medium.jpg 600w, http://placehold.it/300x150&text=500+Small.jpg 500w"
 sizes="(min-width:1000px) 33.3vw,(min-widthh:500px) 50vw, 100vw" src="http://placehold.it/300x150&text=Small.jpg+No+Picture+Support"

     alt="Picture SRCSET" />
```

[View live example](http://codepen.io/justincavery/full/vjAgF/)

## Usage

     sizes attribute is used along side scrset.

## Notes

It is recommended that the final sizes value is

      sizes="[first sizes], [second to last sizes], 100vw"

## Related specifications

[HTML5 APIs](http://www.w3.org/html/wg/drafts/html/master/embedded-content.html)
:   W3C Editor's draft
