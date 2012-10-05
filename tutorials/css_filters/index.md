{{Page_Title|Understanding CSS filter effects}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Alex Danilo
|URL=http://www.html5rocks.com/profiles/#alexdanilo
|Published=May 25, 2012, updated May 29, 2012
}}
{{Summary_Section|An introduction to CSS filter effects.}}
{{Tutorial
|Content='''Caution:''' This article discusses APIs that are not yet fully standardized and still in flux. Be cautious when using experimental APIs in your own projects. See the compatibility tables at the end of this article for the latest information.

==Introduction==

Filters are a powerful tool that web authors can use to achieve interesting visual effects. In this article we'll cover the history of filter effects, what they do, and how to use them. We'll cover examples of the predefined filters defined for CSS, with some examples. We'll also cover performance considerations for using them on desktop and mobile devices, because knowing the speed impact of filters is an important consideration for designing a good user experience. Finally, we'll review the current state of implementation in modern browsers.

==The past, present, and future of filter effects==

Filter effects originated as part of the Scalable Vector Graphics (SVG) specification. They were created to apply a number of different pixel-based image effects to a vector drawing. Over time, as browser vendors added SVG capabilities to their browsers, the usefulness of filters became evident. Robert O'Callahan from Mozilla came up with the [http://robert.ocallahan.org/2008/06/applying-svg-effects-to-html-content_04.html brilliant idea] of using SVG filters by the application of CSS to normal HTML content. Robert prototyped an early version that showed how powerful the combination of filters and CSS styling could be. The CSS and SVG working groups in the W3C decided to harmonize the use of filters for both HTML and SVG via CSS styling, and thus the <code>filter</code> property for CSS was born. Right now a joint task force of people working on CSS and SVG is doing a ton of work to make filters universally useful. You can find the current specification for all this stuff [https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html here].

==A new life for the <code>filter</code> CSS property==

''Déjà vu'' sometimes strikes a web developer when seeing <code>filter</code> in CSS styles. This is due to the fact that old versions of Internet Explorer had a <code>filter</code> property exposed via CSS to perform some platform-specific functionality. This has been [http://www.fred.net/dhark/demos/css/css_filter_examples.html deprecated] in favor of the standard <code>filter</code> property which is now part of CSS3. So when you see "filter" out in the wild on some old web pages, there's no need to be confused. The new <code>filter</code> property is where all the action is, and new versions of IE are implementing it just the same as all modern browsers.

==How filters work==

What does a filter do exactly? The easiest way to think of a filter is as a post-processing step that does something magical after all your page content has been laid out and drawn.

When a browser loads a web page it needs to apply styles, perform layout, and then render the page so there's something to look at. Filters kick in after all those steps are complete and just before the page is copied to the screen. What they do is take a snapshot of the rendered page as a bitmap image, then perform some graphics magic on the pixels in the snapshot and then draw the result over the top of the original page image. One way to think of them is like a filter placed on the front of a camera lens. What you're seeing through the lens is the outside world modified by the effect of the filter.

This of course means that there's time consumed when drawing a page with filters on it, but using them properly will have minimal impact on the speed of your site.

Also, just as you can stack a number of filters in front of each other on your camera lens, you can apply an arbitrary number of filters one after the other to achieve all sorts of effects.

==Filters defined using SVG and CSS==

Because filters originally came from SVG, there are different ways to define and use them. SVG itself has an element that wraps up definitions of various filter effects using XML syntax. The filters defined by CSS take advantage of the same graphics model, but they are much simpler definitions and are easier to use in a style sheet.

Most of the CSS filters can be expressed in terms of SVG filters, and CSS also allows you to reference a filter specified in SVG if you want. The CSS filter designers have taken great pains to make the application of a filter easier for web authors, and so this article will just cover the filters available directly from CSS, ignoring the SVG definitions for the time being.

==How to apply a CSS filter==

'''Note:''' The description and examples below use the official W3C syntax that will be available in all modern browsers eventually. To use filters now, you need to use the vendor prefixed version of the 'filter' property. But don't worry, there's an easy way to handle that discussed later. And again, see the compatibility tables at the end of the article for the latest information. 

Using filters from CSS is done by applying the <code>filter</code> property to any visible element on your web page. For a very simple example, you could write something like:

<syntaxhighlight language="css">
div { +filter: grayscale(100%); }
</syntaxhighlight>

This will make the content inside all <code>&lt;div&gt;</code> elements on the page turn gray. Great for making your page look like a TV image from the 1940s!

[[Image:f01-pencil.jpg]]&nbsp;[[Image:f02-gray.jpg]]<br/>
''Original image (left); grayscale filtered image (right)''

Most filters take some form of parameter to control how much filtering is done. So, for example, if you wanted to style your content to be halfway between the original color and a grayscale version you'd do it like this:

<syntaxhighlight language="css">
div { +filter: grayscale(50%); }
</syntaxhighlight>

[[Image:f03-gray50.jpg]]<br/>
''Original image 50% gray filtered''

If you want to apply a number of different filters one after another, it's easy &mdash; just place them one after the other in your CSS, like so:

<syntaxhighlight language="css">
div { +filter: grayscale(100%) sepia(100%); }
</syntaxhighlight>

This example will first make all the original color grayscale and then apply a sepia effect, and will end up looking like this:

[[Image:f04-graysepia.jpg]]<br/>
''Grayscale plus sepia''

With the flexibility available for applying filters one after the other, all sorts of effects can be achieved &mdash; it's totally up to your imagination to experiment with creating amazing results.

==What filter effects are available using CSS?==

The original SVG filter mechanism is powerful but, at the same time, can be daunting to use. Because of that, CSS introduces a bunch of standard filter effects that make using them really easy.

Let's take a look at each of them and see what they do.

; grayscale(amount)
: This converts color in our input image to a shade of gray. The <code>amount</code> controls how much gray conversion is applied. If it's 100% then everything will be a shade of gray; if it's 0% the colors are unchanged. You can use a floating point number here if you prefer it over percentages; that is, 0 works the same as 0% whilst 1.0 works the same as 100%.

[[Image:f05-boatonlake.jpg]]&nbsp;[[Image:f06-boatonlakegray.jpg]]<br/>
''Original (left); grayscale 100% (right)''

; sepia(amount)
: This gives the colors passed in a sepia tinge like in old photographs. The <code>amount</code> applied works in the same way as for the <code>grayscale</code> filter &mdash; namely 100% makes all the colors completely sepia toned and smaller values allow the effect to be applied in smaller proportions.

[[Image:f07-lenna.jpg]]&nbsp;[[Image:f08-lennasepia.jpg]]<br/>
''Original (left); sepia 100% (right)''

; saturate(amount)
: This applies a saturation effect to the colors, which makes them look more vivid. It's a cool effect that can make photos look like posters or cartoons. This effect also allows you to use a value greater than 100% to really emphasize the saturation. Definitely an effect that can make things look pretty funky!

[[Image:f09-tiffany.jpg]]&nbsp;[[Image:f10-tiffanysaturate.jpg]]<br/>
''Original (left); saturate 10% (right)''

'''Note:''' In Chrome version 19 the <code>saturate()</code> filter takes an integer (without the percentage sign) instead of the decimal or percentage as defined in the W3C spec. Not to worry, this known bug will be fixed, if it hasn't been already.

; hue-rotate(angle)
: This one is a bit of a color-geek effect that can be used for interesting results. What it does is shift the colors around to make an image look completely different. If you can imagine a color spectrum going from red to violet around a [http://colorschemedesigner.com/ color wheel], then this effect takes the original color on the wheel as input and rotates it by the <code>angle</code> parameter to produce the output color value. This effect is applied throughout the image such that all the colors are shifted by the same amount on the wheel. This is of course a simplification of what it does, but hopefully close enough that it makes sense.

[[Image:f11-mandrill.jpg]]&nbsp;[[Image:f12-mandrillhuerotate.jpg]]<br/>
''Original (left); hue-rotate 90 degrees (right)''

; invert(amount)
: This effect flips the colors, so that if the <code>amount</code> applied is 100% the output looks like a photo negative back from the old film days of cameras! Just like before, using values smaller than 100% will progressively apply the invert effect.

[[Image:f13-peppers.jpg]]&nbsp;[[Image:f14-peppersinvert.jpg]]<br/>
''Original (left); invert 100% (right)''

; opacity(amount)
: If you want the content being filtered to look semi-transparent, this is the one for you. The 'amount' value defines how opaque the output will be. A value of 100% is completely opaque, so the output will be exactly the same as the input. As the value drops below 100% the output image becomes less opaque (more transparent) and you'll see less and less of it. This of course means that if it overlaps something else on the page, the content underneath will start to become visible. An <code>amount</code> of 0% means it will completely disappear &mdash; but note: you can still get events (like mouse clicks, etc.) to fire on completely transparent objects, so this is handy if you want to create clickable areas without displaying anything. In general, the CSS <code>opacity</code> property isn't hardware accelerated, but some browsers that implement filters using hardware acceleration will accelerate the filter version of opacity for much better performance.

[[Image:f15-splash.jpg]]&nbsp;[[Image:f16-splashopacity50.jpg]]<br/>
''Original (left); opacity 50% (right)''

; brightness(amount)
: This is just like the brightness control on your TV. It adjusts the colors between completely black and the original color in proportion to the <code>amount</code> parameter. If you set this one to 0% you'll see nothing but black, but as the value goes up toward 100% you see more and more of the original image brightening up until you hit 100%, where it's the same as the input image. Of course you can just keep going &mdash; so setting something like 200% will make the image twice as bright as the original. Great for adjusting those low light shots!

[[Image:f17-boatonlake2.jpg]]&nbsp;[[Image:f18-boatonlake2bright.jpg]]<br/>
''Original (left); brightness 140% (right)''

; contrast(amount)
: More controls from your TV set! This will adjust the difference between the darkest and lightest parts of the input image. If you use 0% you end up with black just like with <code>brightness</code>, so that's not too interesting. However, as you increase the value toward 100%, the difference in darkness (contrast) changes until you hit 100% and it's the original image again. You can go beyond 100% for this effect too, which increases the difference between light and dark colors even more.

[[Image:f19-jellybeans.jpg]]&nbsp;[[Image:f20-jellybeancontrast.jpg]]<br/>
''Original (left); contrast 200% (right)''

; blur(radius)
: If you want a soft edge for your content, you can add a blur. This one looks like the classic Vaseline-on-a-sheet-of-glass look that used to be a popular movie technique. It smudges the colors together and spreads out their effect, kind of like when your eyes are out of focus. The <code>radius</code> parameter affects how many pixels on the screen blend into each other, so a larger value creates more blur. Zero, of course, leaves the image unchanged.

[[Image:f21-peppers2.jpg]]&nbsp;[[Image:f22-peppers2blur.jpg]]<br/>
''Original (left); blur 10px (right)''

; drop-shadow(shadow)
: It's so nice to be able to make your content look like it's outside in the sun with a shadow on the ground behind it, and that of course is what <code>drop-shadow</code> does. It takes a snapshot of the image, makes it a single color, blurs it, then offsets the result a bit so it looks like a shadow of the original content. The <code>shadow</code> parameter passed in is a bit more complicated than just a single value. It is a series of values separated by a space &mdash; and some values are optional! The <code>shadow</code> values control where the shadow is placed, how much blur is applied, the color of the shadow, etc. For full details of what the values do, the [http://www.w3.org/TR/css3-background/#the-box-shadow CSS3 Backgrounds] specification defines <code>box-shadow</code> in great detail. A few examples below should give you a decent idea of the various possibilities.

[[Image:f23-mandrilldrop1.jpg]]&nbsp;[[Image:f24-mandrillshadow2.jpg]]<br/>
''Drop-shadow 16px 16px 20px black (left); drop-shadow 10px -16px 30px purple (right)''

:This is another filter operation that is similar to existing CSS functionality available via the <code>box-shadow</code> property. Using the filter approach means that it may be hardware accelerated by some browsers as we described for the <code>opacity</code> operation above.

; url referencing SVG filters
: Because filters originated as part of SVG, it's only logical that you should be able to style your content using an SVG filter. This is easy with the current <code>filter</code> property proposal. All filters in SVG are defined with an <code>id</code> attribute that can be used to reference the filter effect. So to use any SVG filter from CSS, all you need to do is reference it using the <code>url</code> syntax. For example, the SVG markup for a filter could be something like: <code>&lt;filter id=”foo”&gt;...&lt;/filter&gt;</code>. Then from CSS, you could do something as simple as: <code>div { +filter: url(#foo); }</code>, and voila! All the <code>&lt;div&gt;</code>s in your document will be styled with the SVG filter definitions.

; custom (coming soon)
: Coming soon on the horizon are custom filters. These tap into the power of your graphics GPU to use a special [http://www.adobe.com/devnet/html5/articles/css-shaders.html shading technique] to perform amazing effects bounded only by your own imagination. This part of the <code>filter</code> specification is still in flux, but is sure to come to a browser near you soon.

==Performance considerations==

One thing that every web developer cares about is performance of their web page or application. CSS filters are a powerful tool for visual effects, but at the same time might have an impact on the performance of your site.

Understanding what they do and how this affects performance matters, especially if you want your site to work well on mobile devices that support CSS filters.

Firstly, not all filters are created equal! In fact, most filters will run quickly on any platform and have very minor performance impact. However, filters that do any kind of blurring, such as <code>blur</code> and <code>drop-shadow</code>, tend to be slower. This doesn't mean you shouldn't use them, but understanding how they work might help.

When you do a <code>blur</code>, it mixes the colors from pixels all around the output pixel to generate a blurred result. So, if your <code>radius</code> parameter is 2, then the filter needs to look at 2 pixels in every direction around each output pixel to generate the mixed color. This happens for each output pixel, so that means a lot of calculations that just get bigger when you increase the <code>radius</code>. Since <code>blur</code> looks in every direction, doubling the <code>radius</code> means you need to look at 4 times as many pixels, so in fact it's 4 times slower for each doubling of the <code>radius</code>. The <code>drop-shadow</code> filter contains blurring as part of its effect, so it too behaves just like <code>blur</code> when you change the ''radius'' and ''spread'' parts of the <code>shadow</code> parameter.

All is not lost with <code>blur</code>, as on some platforms it's possible to use the CPU to accelerate it, but that's not necessarily going to be available in every browser. When in doubt, the best thing is to experiment with the <code>radius</code> that gives you the effect you want, then try to reduce it as much as possible while still maintaining an acceptable visual effect. Tuning this way will make your users happier, especially if they are viewing your site on a mobile device.

If you're using URL-based filters that reference SVG filters, they can contain any arbitrary filter effect, so be aware that they too could be slow. Try to make sure you know what the filter effect does and experiment on a mobile device to make sure the performance is acceptable.

<!-- support/speed paragraphs and table omitted-->

==Other good resources==

*Here's an awesome [http://cssfilters.appspot.com/ interactive abstract painting with filters] application that lets you experiment and share your artwork.
*Be sure to check out Eric Bidelman's excellent [http://html5-demos.appspot.com/static/css/filters/index.html interactive filter] page.
*A great [http://net.tutsplus.com/tutorials/html-css-techniques/say-hello-to-css3-filters/ tutorial about filters] with examples.
*The official W3C Filter Effects 1.0 [https://dvcs.w3.org/hg/FXTF/raw-file/tip/filters/index.html draft specification]. 
*An example [http://lab.simurai.com/stars/#bruno UI] created with filters.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21.0
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=6.0
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Yes
|Safari_mobile_prefixed_version=6.0
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/filters/understanding-css/
}}