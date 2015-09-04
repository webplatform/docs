---
title: css filters
tags:
  - Tutorials
  - CSS
  - Graphics
  - SVG
readiness: 'Ready to Use'
summary: 'This article is an introduction to CSS filter effects.'
uri: 'tutorials/css filters'

---
# Understanding CSS filter effects

**By [Alex Danilo](http://www.html5rocks.com/profiles/#alexdanilo)**
Originally published May 25, 2012, updated May 29, 2012

## Summary

This article is an introduction to CSS filter effects.

**Caution:** This article discusses APIs that are not yet fully standardized and still in flux. Be cautious when using experimental APIs in your own projects. See the compatibility tables at the end of this article for the latest information.

## Introduction

Filters are a powerful tool that web authors can use to achieve interesting visual effects. In this article we'll cover the history of filter effects, what they do, and how to use them. We'll cover examples of the predefined filters defined for CSS, with some examples. We'll also cover performance considerations for using them on desktop and mobile devices, because knowing the speed impact of filters is an important consideration for designing a good user experience. Finally, we'll review the current state of implementation in modern browsers.

## The past, present, and future of filter effects

Filter effects originated as part of the Scalable Vector Graphics (SVG) specification. They were created to apply a number of different pixel-based image effects to a vector drawing. Over time, as browser vendors added SVG capabilities to their browsers, the usefulness of filters became evident. Robert O'Callahan from Mozilla came up with the [brilliant idea](http://robert.ocallahan.org/2008/06/applying-svg-effects-to-html-content_04.html) of using SVG filters by the application of CSS to normal HTML content. Robert prototyped an early version that showed how powerful the combination of filters and CSS styling could be. The CSS and SVG working groups in the W3C decided to harmonize the use of filters for both HTML and SVG via CSS styling, and thus the `filter` property for CSS was born. Right now a joint task force of people working on CSS and SVG is doing a ton of work to make filters universally useful. Check out the [current specification](https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html) for more details.

## A new life for the filter CSS property

*DÃ©jÃ  vu* sometimes strikes a web developer when seeing `filter` in CSS styles. This is due to the fact that old versions of Internet Explorer had a `filter` property exposed via CSS to perform some platform-specific functionality. This has been [deprecated](http://www.fred.net/dhark/demos/css/css_filter_examples.html) in favor of the standard `filter` property which is now part of CSS3. So when you see "filter" out in the wild on some old web pages, there's no need to be confused. The new `filter` property is where all the action is, and new versions of IE are implementing it just the same as all modern browsers.

## How filters work

What does a filter do exactly? The easiest way to think of a filter is as a post-processing step that does something magical after all your page content has been laid out and drawn.

When a browser loads a web page it needs to apply styles, perform layout, and then render the page so there's something to look at. Filters kick in after all those steps are complete and just before the page is rendered on the screen. Filters take a snapshot of the rendered page as a bitmap image, then perform some graphics magic on the pixels in the snapshot and then draw the result over the top of the original page image. One way to think of them is like a filter placed on the front of a camera lens. The image you see through the lens is the outside world modified by the effect of the filter.

This process requires some time when drawing a page with filters applied, but if used properly, it will have minimal impact on the speed of your site.

Also, just as you can stack a number of filters in front of each other on your camera lens, you can apply an arbitrary number of filters one after the other to achieve all sorts of interesting effects.

## Filters defined using SVG and CSS

Because filters originally came from SVG, there are different ways to define and use them. SVG itself has an element that wraps up definitions of various filter effects using XML syntax. The filters defined by CSS take advantage of the same graphics model, but they are much simpler definitions and are easier to use in a style sheet.

Most of the CSS filters can be expressed in terms of SVG filters, and CSS also allows you to reference a filter specified in SVG if you want. The CSS filter designers have taken great pains to make the application of a filter easier for web authors, and so this article will just cover the filters available directly from CSS, ignoring the SVG definitions for the time being.

## How to apply a CSS filter

**Important:** The descriptions and examples below all use the official W3C syntax that will be available in all modern browsers eventually. To use filters now, you need to use the vendor prefixed version of the `filter` property. See the compatibility tables at the end of the article for the latest information.

Using CSS, you can apply the `filter` property to any visible element on your web page. For a very simple example, you could write something like:

``` {.html}
div { filter: grayscale(100%); }
```

 This will make the content inside all `<div>` elements on the page turn gray. Great for making your page look like a TV image from the 1940s!

Â
*Original image (left); grayscale filtered image (right)* ![f01-pencil.jpg](/assets/thumb/a/a8/f01-pencil.jpg/300px-f01-pencil.jpg)![f02-gray.jpg](/assets/thumb/2/26/f02-gray.jpg/300px-f02-gray.jpg)

Most filters take some form of parameter to control how much filtering is done. So, for example, if you wanted to style your content to be halfway between the original color and a grayscale version, use the following code:

``` {.html}
div { filter: grayscale(50%); }
```

*Original image 50% gray filtered* ![f03-gray50.jpg](/assets/thumb/3/34/f03-gray50.jpg/300px-f03-gray50.jpg)

If you want to apply a number of different filters one after another, it is easy â€” just place them one after the other in your CSS, like this:

``` {.html}
div { filter: grayscale(100%) sepia(100%); }
```

 This example will first make all the original color grayscale and then apply a sepia effect, and results in an image that looks like this:

*Grayscale plus sepia* ![f04-graysepia.jpg](/assets/thumb/2/25/f04-graysepia.jpg/300px-f04-graysepia.jpg)

With the flexibility available for applying filters one after the other, all sorts of effects can be achieved â€” it's totally up to your imagination to experiment with creating amazing results.

## What filter effects are available using CSS?

The original SVG filter mechanism is powerful but, at the same time, can be daunting to use. Because of that, CSS introduces a bunch of standard filter effects that make using them really easy.

Let's take a look at each of them and see what they do.

 grayscale(amount)
:   This converts color in an input image to a shade of gray. The `amount` controls how much gray conversion is applied. If set to 100% then all of the colors will be a shade of gray; if set to 0% the colors are unchanged. You can use a floating point number instead of percentages if you prefer; that is, 0 works the same as 0% whilst 1.0 produces the same result as 100%.

Â
*Original (left); grayscale 100% (right)* ![f05-boatonlake.jpg](/assets/thumb/3/37/f05-boatonlake.jpg/300px-f05-boatonlake.jpg)![f06-boatonlakegray.jpg](/assets/thumb/7/7e/f06-boatonlakegray.jpg/300px-f06-boatonlakegray.jpg)

 sepia(amount)
:   This gives the colors passed in a sepia tinge like in old photographs. The `amount` applied works in the same way as for the `grayscale` filter â€” namely 100% makes all the colors completely sepia toned and smaller values allow the effect to be applied in smaller proportions.

Â
*Original (left); sepia 100% (right)* ![f07-lenna.jpg](/assets/thumb/e/e6/f07-lenna.jpg/300px-f07-lenna.jpg)![f08-lennasepia.jpg](/assets/thumb/7/70/f08-lennasepia.jpg/300px-f08-lennasepia.jpg)

 saturate(amount)
:   This applies a saturation effect to the colors, which makes them look more vivid. It is a cool effect that can make photos look like posters or cartoons. This effect also allows you to use a value greater than 100% (the default) to really emphasize the saturation. This is an effect that can make things look pretty funky!

Â
*Original (left); saturate 1000% (right)* ![f09-tiffany.jpg](/assets/thumb/2/2d/f09-tiffany.jpg/300px-f09-tiffany.jpg)![f10-tiffanysaturate.jpg](/assets/thumb/b/be/f10-tiffanysaturate.jpg/300px-f10-tiffanysaturate.jpg)

**Note:** In Chrome version 19 the `saturate()` filter takes an integer (without the percentage sign) instead of the decimal or percentage as defined in the W3C spec. Not to worry, this is a known bug that will be fixed soon, if it hasn't been already.

 hue-rotate(angle)
:   This filter provides a color-geek effect that can be used for interesting results. It shifts the colors around to make an image look completely different. Imagine a color spectrum going from red to violet around a [color wheel](http://colorschemedesigner.com/). This effect uses the original color on the wheel as input and rotates it by the `angle` parameter to produce the output color value. This effect is applied throughout the image so that all the colors are shifted by the same amount on the wheel. This is a simplification of what actually occurs, but hopefully close enough to describe the resulting effect.

Â
*Original (left); hue-rotate 90 degrees (right)* ![f11-mandrill.jpg](/assets/thumb/8/80/f11-mandrill.jpg/300px-f11-mandrill.jpg)![f12-mandrillhuerotate.jpg](/assets/thumb/d/d5/f12-mandrillhuerotate.jpg/300px-f12-mandrillhuerotate.jpg)

 invert(amount)
:   This effect flips the colors, so that if the `amount` applied is 100% the output looks like a photo negative from an old 35mm film camera! Using values smaller than 100% will progressively apply the invert effect.

Â
*Original (left); invert 100% (right)* ![f13-peppers.jpg](/assets/thumb/1/11/f13-peppers.jpg/300px-f13-peppers.jpg)![f14-peppersinvert.jpg](/assets/thumb/1/19/f14-peppersinvert.jpg/300px-f14-peppersinvert.jpg)

 opacity(amount)
:   If you want the content being filtered to look semi-transparent, use this effect. The 'amount' value defines how opaque the output will be. A value of 100% is completely opaque, so the output will be exactly the same as the input. As the value drops below 100% the output image becomes less opaque (more transparent) and you'll see less and less of it. This means that if the element overlaps other elements on the page, the content underneath will start to become visible. You can set the `amount` to 0% and it will completely disappear â€” but note: the element still receives events (such as mouse clicks) that fire on completely transparent objects. This effect is useful for creating clickable areas without displaying the button. In general, the CSS `opacity` property isn't hardware accelerated, but some browsers that implement filters using hardware acceleration will accelerate the filter version of opacity to provide much better performance.

Â
*Original (left); opacity 50% (right)* ![f15-splash.jpg](/assets/thumb/0/04/f15-splash.jpg/300px-f15-splash.jpg)![f16-splashopacity50.jpg](/assets/public/6/68/f16-splashopacity50.jpg)

 brightness(amount)
:   This effect works like the brightness control on your TV. It adjusts the colors between completely black and the original color in proportion to the `amount` parameter. If you set the amount to 0% you'll see nothing but black, but as the value increases toward 100% more and more of the original image brightens until you hit 100%, to match the input image. You can continue increasing the amount value â€” setting a value of 200% makes the image twice as bright as the original. This is useful when adjusting low light images.

Â
*Original (left); brightness 140% (right)* ![f17-boatonlake2.jpg](/assets/thumb/1/15/f17-boatonlake2.jpg/300px-f17-boatonlake2.jpg)![f18-boatonlake2bright.jpg](/assets/thumb/6/67/f18-boatonlake2bright.jpg/300px-f18-boatonlake2bright.jpg)

 contrast(amount)
:   This is another control simular to a TV set. Use contrast to adjust the difference between the darkest and lightest parts of the input image. A setting of 0% results in black, similar to the `brightness` effect, so it is not very interesting. However, as the value increases toward 100%, the difference in darkness (contrast) changes until you hit 100% and the original image is displayed again. If set above 100%, this effect increases the difference between light and dark colors even more profoundly.

Â
*Original (left); contrast 200% (right)* ![f19-jellybeans.jpg](/assets/public/b/b5/f19-jellybeans.jpg)![f20-jellybeancontrast.jpg](/assets/public/a/a5/f20-jellybeancontrast.jpg)

 blur(radius)
:   To create a soft edge on content, add a blur. This effect looks like the classic Vaseline-on-a-sheet-of-glass look that was a popular cinematic technique. The blur effect smudges the colors together and spreads them out, to provide an out of focus appearance. The `radius` parameter affects how many pixels on the screen blend together. A larger value creates more blur. When set to 0%, the original image remains unchanged.

Â
*Original (left); blur 10px (right)* ![f21-peppers2.jpg](/assets/thumb/a/ad/f21-peppers2.jpg/300px-f21-peppers2.jpg)![f22-peppers2blur.jpg](/assets/thumb/5/52/f22-peppers2blur.jpg/300px-f22-peppers2blur.jpg)

 drop-shadow(shadow)
:   The `drop-shadow` effect makes content appear as though it is an object outside in the sun with a shadow falling on the ground behind it. The filter takes a snapshot of the image, converts it to a single color, blurs it, then offsets the result a bit to create a shadow of the original content. The `shadow` parameter is more complicated than just a single value. For this effect, you enter a series of values separated by a space â€” and some of the values are optional. The `shadow` values control where the shadow is placed (expressed as two measurements for *x* and *y*), how much blur is applied (another measurement), and the color of the shadow. For full details of these values, see the [CSS Text Decoration](http://www.w3.org/TR/css-text-decor-3/#text-shadow-property) specification, which defines `text-shadow` in great detail. The examples provided below highlight some of the possibilities.

Â
*Drop-shadow 16px 16px 20px black (left); drop-shadow 10px -16px 30px purple (right)* ![f23-mandrilldrop1.jpg](/assets/thumb/c/c2/f23-mandrilldrop1.jpg/300px-f23-mandrilldrop1.jpg)![f24-mandrillshadow2.jpg](/assets/thumb/a/a7/f24-mandrillshadow2.jpg/300px-f24-mandrillshadow2.jpg)

<dl>
<dd>
This is another filter operation that is similar to existing CSS functionality available via the `box-shadow` property. Using the filter approach means that it may be hardware accelerated by some browsers, as described in the section above on using the `opacity` filter.

</dd>
</dl>
 url referencing SVG filters
:   Because filters originated as part of SVG, it makes sense that you can style content using an SVG filter. This is easy with the current `filter` property proposal. All filters in SVG are defined with an `id` attribute that can be used to reference the filter effect. To use any SVG filter via CSS, you can reference it using the `url` syntax. For example, the SVG markup for a filter could look like: `<filter id=â€fooâ€>...</filter>`. Then, in the CSS, you could add a simple rule: `div { filter: url(#foo); }` to ensure the `<div>` content in your document is styled with the SVG filter definitions.

 custom (coming soon)
:   Stay tuned to learn more about working with custom filters. Custom filters leverage the power of the computer's graphics GPU to use a special [shading technique](http://www.adobe.com/devnet/html5/articles/css-shaders.html) to perform amazing effects limited only by your imagination. This part of the `filter` specification is still in flux, but will start being supported by browsers in the near future.

## Performance considerations

The performance of web pages and applications is always important when developing online content. CSS filters are a powerful tool for visual effects, but at the same time might impact the performance of a site.

It is important to determine how specific filters affect site performance, especially if your goal is to build sites that display as expected on mobile devices that support CSS filters.

Filters differ in how they run. Most filters will run quickly on any platform and have very minor performance impact. However, filters that include blurring, such as `blur` and `drop-shadow`, tend to be slower. This doesn't mean you shouldn't use them, but it is helpful to understanding how they work.

When you use a `blur` filter, it mixes the colors from pixels all around the output pixel to generate a blurred result. So, if your `radius` parameter is 2, then the filter uses 2 pixels in every direction around each output pixel to generate the mixed color. This process occurs for each output pixel, and the number of calculations grows exponentially as you increase the `radius`. Since `blur` reviews pixels in every direction, doubling the `radius` causes the filter to work with four times as many pixels, so it is four times slower each time you double the `radius` value. The `drop-shadow` filter uses blurring as part of its effect, so it too behaves just like `blur` when you adjust the *radius* and *spread* values of the `shadow` parameter.

On some platforms, it is possible to use the CPU to accelerate the `blur` filter, but that strategy may not be available in every targeted browser. Try experimenting with the `radius` value to create the effect you desire, and then reduce it as much as possible while still maintaining an acceptable visual effect. You can fine tune filter parameters to make the site experience better, especially when viewed on a mobile device.

If you're using URL-based filters that reference SVG filters, they can contain any arbitrary filter effect, so be aware that they may also slow down a site. Test filter effects and experiment by viewing the site on a mobile device to ensure the site performance is acceptable.

## Other good resources

-   Try using this awesome [interactive abstract painting with filters application](http://cssfilters.appspot.com/) to experiment and share your artwork.
-   Check out Eric Bidelman's excellent [interactive filter](http://html5-demos.appspot.com/static/css/filters/index.html) page.
-   Follow along with this great [tutorial about filters](http://net.tutsplus.com/tutorials/html-css-techniques/say-hello-to-css3-filters/) that includes examples.
-   Review the official W3C Filter Effects 1.0 [draft specification](https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html).
-   See this [UI example](http://lab.simurai.com/stars/#bruno) created with filters.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/filters/understanding-css/)

