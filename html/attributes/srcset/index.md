---
title: srcset
code_samples:
  - 'http://codepen.io/justincavery/pen/tliGE'
  - 'http://codepen.io/justincavery/full/osDGt/'
readiness: 'Ready to Use'
standardization_status: 'W3C Editor''s Draft'
summary: 'The srcset attribute is an extension of the image element. It provides  additional image related information to the browser to help decide the most appropriate image to load. Most commonly used for delivering the best image for high device pixel ratio and responsive images.'
tags:
  - Markup
  - Attributes
  - HTML
uri: html/attributes/srcset

---
## <span>Summary</span>

The srcset attribute is an extension of the image element. It provides additional image related information to the browser to help decide the most appropriate image to load. Most commonly used for delivering the best image for high device pixel ratio and responsive images.

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
As attribute of the [image element](/html/elements/img) element, **srcset** provides webpages the ability to inform the browser on size and pixel density information about the image before it begins the prefetch process.

**srcset** submits the preferred size of the image with the corresponding viewport **[sizes](/html/attributes/sizes)** informing the browser the best image to use for the best viewport. Alternatively you can also omit the **[sizes](/html/attributes/sizes)** attribute and just use the **srcset** attribute to target images for specific device pixel ratios.

Targeting images based on device pixel ratio only can be accomplished by using the `x` descriptor.

The standard **[src](/html/attributes/src_(input,_img))** attribute is always used to provide a fallback for all browsers that do not support **srcset**

       <img srcset="small.jpg 1x, large.jpg 2x"
       src="small.jpg" />

The **srcset** attribute can also take a comma separated list of URL's for each of the available image sizes. The image widths are defined using **w** descriptor. If you save out three different sizes of your image at 300px, 600px, 1024px this is what your code would look like.

       <img srcset="large.jpg 1024w,
               medium.jpg 600w,
               small.jpg 300w"
               src="small.jpg"
               alt="A picture of a small thing" />

## <span>Examples</span>

Example of srcset using only device pixel ratio

``` html
<img
      srcset="http://placehold.it/600x250&text=1x+Medium.jpg 1x,
              http://placehold.it/1024x500&text=2x+Large.jpg 2x"
      src="http://placehold.it/300x150&text=Small.jpg+No+Picture+Support"
      alt="Picture SRCSET" />
```

[View live example](http://codepen.io/justincavery/pen/tliGE)

Example of the SRCSET and SIZES attributes

``` html
<img
      srcset="http://placehold.it/1024x500&text=1024+Large.jpg 1024w,
              http://placehold.it/600x250&text=600+Medium.jpg 600w,
          http://placehold.it/300x150&text=500+Small.jpg 500w"
      sizes="(min-width:500px) 33.3vw,
             (min-width:1000px) 50vw,
             100vw"
      src="http://placehold.it/300x150&text=Small.jpg+No+Picture+Support"
      alt="Picture SRCSET" />
```

[View live example](http://codepen.io/justincavery/full/osDGt/)

## <span>Usage</span>

     When using srcset with the w descriptor you must also include the sizes attribute.

## <span>Related specifications</span>

[HTML5 APIs](http://www.w3.org/html/wg/drafts/srcset/w3c-srcset/)
:   Editor’s Draft
