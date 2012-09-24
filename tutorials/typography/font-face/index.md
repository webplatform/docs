{{Flags
|High-level issues=Needs Flags
}}
{{Summary_Section|An introduction to webfonts and @font-face.}}
{{Tutorial
|Content==Quick Guide to Webfonts Via @font-face=

====original by Paul Irish====
====published Aug. 2, 2010====

==Introduction==

The @font-face feature from CSS3 allows us to use custom typefaces on the web in an accessible, manipulable, and scalable way. "But," you might ask, "why would we use @font-face if we have Cufon, sIFR, and using text in images?"

A few benefits of leveraging @font-face for custom fonts:

* Full searchability by Find (ctrl-F)
* Accessibility to assistive technologies like screen readers
* Text is translatable through in-browser translation or translation services
* CSS has full ability to tweak the typographical display via <code>line-height</code>, <code>letter-spacing</code>, <code>text-shadow</code>, <code>text-align</code>, and selectors like <code>::first-letter</code> and <code>::first-line</code>

[[Image:ff-previewer.jpg]]<br/>
View the [http://code.google.com/webfonts/preview Font Previewer] for a taste of how flexible webfonts are

==@font-face at its essence==

At its most basic, we declare a new custom remote font to be used like so:
<pre>
 @font-face {
   font-family: 'Tagesschrift';
   src: url('tagesschrift.ttf');
 }
</pre>

Then put it to use:
<pre>
 h1, h2, h3 { font-family: 'Tagesschrift', 'Georgia', serif; }
</pre>

In this @font-face declaration we're using the <code>font-family</code> property to explicitly name the font. It can be anything, regardless of what the font is actually called; <code>font-family: 'SuperDuperComicSans';</code> would work just fine, though perhaps not for your reputation. In the <code>src</code> property, we point to where the browser can find the font asset. Depending on the browser, some valid font types are eot, ttf, otf, svg, or a [http://en.wikipedia.org/wiki/Data_URI_scheme data URI] embedding the entire font data inline. 

Of course, nothing is ever as simple as it should be. The initial limitation of the above code was that it did not serve an EOT to IE 6-8. The [http://paulirish.com/2009/bulletproof-font-face-implementation-syntax/ bulletproof @font-face syntax] proposed a way of solving this; a robust version follows.

<pre>
 @font-face {
   font-family: 'Tagesschrift';
   src: url('tagesschrift.eot'); /* IE 5-8 */
   src: local('☺'),             /* sneakily trick IE */
         url('tagesschrift.woff') format('woff'),    /* FF 3.6, Chrome 5, IE9 */
         url('tagesschrift.ttf') format('truetype'), /* Opera, Safari */
         url('tagesschrift.svg#font') format('svg'); /* iOS */
 }
</pre>

Inducing a headache yet? If you'd rather just get this off the ground quickly, head to the [http://www.fontsquirrel.com/fontface/generator Font Squirrel generator], a tool that simplifies the whole process for you, taking your font and preparing its variants and CSS for you. It's indispensable for putting webfonts into practice today.

[[Image:ff-squirrel.png]]<br/>
The [http://www.fontsquirrel.com/fontface/generator Font Squirrel generator]

===Mobile support?===

Some mobile operating systems support SVG webfonts and some don't. But regardless, should your mobile users get this enhanced typographic experience? I'd recommend no. The predominant reason is due to how WebKit handles text that is awaiting a custom font via @font-face: the text is invisible. So on a low-bandwidth mobile connection, your users will see no text at all until the ~50k of font data has loaded. The Webkit team is pursuing a solution of turning on a fallback font after a few seconds have expired, but until that has landed, I wouldn't consider it fair to subject your users to such roadblocks between them and your content.

==Webfont services==

A number of services wrap the @font-face feature in an easy API, often letting you add a single CSS or script line to your HTML and some configuration and you're all done. Many like [http://www.extensis.com/en/WebINK/ WebInk], [http://typekit.com/ Typekit], and [http://www.fontslive.com/ Fontslive] will allow you to use the fonts (sometimes up to a bandwidth cap) for a monthly fee. Using these services is very convenient for the casual developer, handing off some of the complications of serving a cross-browser solution to the service.

The [http://code.google.com/apis/webfonts/ Google Font API] lets you use a small, curated set of freely licensed fonts by just linking to a stylesheet and letting Google handle the cross-browser and performance concerns. It's the fastest way to get off the ground and running with webfonts.

==Finding professional typefaces for @font-face==

A common surprise to designers is that just because you purchase a font license (to use in your graphic design, for example), that doesn't mean you can use it in @font-face. Licenses for @font-face (or web embedding) are typically sold separately. Read the agreement carefully, and feel free to contact the font foundry if you have questions.

[http://fontspring.com Fontspring] is a font boutique, selling hundreds of quality professional fonts, all of them cleared for use with @font-face. [http://fontshop.com FontShop] and other foundries have begun selling @font-face licenses directly, though currently only targeting WOFF and EOT, which leave out a sizable (but shrinking) portion of the browser market. Many foundries are adding webfont licenses to their catalog, but if you can't find one for your chosen typeface, get in touch with them to ask about it.

==Dealing with FOUT==

The [http://paulirish.com/2009/fighting-the-font-face-fout/ Flash of Unstyled Text] is a phenomenon in Firefox and Opera that few web designers are fond of. When you apply a custom typeface via @font-face, there is a brief moment when loading the page where the specified font hasn't been downloaded and applied yet, and so the next font in the <code>font-family</code> stack is used. This causes a flash of a different (typically less good looking) font, before it gets upgraded.

[[Image:ff-fout.jpg]]<br/>
The Flash of Unstyled Text happening to the [http://slides.html5rocks.com HTML5 Slide deck]

Accompanying the Google Font API is the [http://code.google.com/apis/webfonts/docs/webfont_loader.html WebFont Loader], a JavaScript library aiming to provide a number of event hooks giving you a lot of control over the loading. Let's take a look at how you can get other browsers to mimic WebKit's behavior of hiding the fallback text while the @font-face font loads.

<pre>
 &lt;script src="//ajax.googleapis.com/ajax/libs/webfont/1/webfont.js"&gt;&lt;/script&gt;
 &lt;script&gt;
 WebFont.load({
   custom: {
     families: ['Tagesschrift'],
     urls: ['http://paulirish.com/tagesschrift.css']
   }
 });
 &lt;/script&gt;
</pre>
<pre>
 /* we want Tagesschrift to apply to all H2s */
 .wf-loading h2 {
   visibility: hidden;
 }
 .wf-active h2, .wf-inactive h2 {
   visibility: visible;
   font-family: 'Tagesschrift', 'Georgia', serif;
 }
</pre>

If JavaScript is disabled the text will remain visible the whole time, and if the font errors somehow, it'll fall back to a basic serif safely. Consider this a stop-gap measure for now; most webfont experts suggest hiding the fallback text for 2-5 seconds, then revealing it. Low-bandwidth and mobile devices benefit greatly by this timeout. Understandably, Mozilla is looking to rectify this soon.

A more lightweight but less effective solution is the <code>[https://developer.mozilla.org/en/CSS:font-size-adjust font-size-adjust]</code> property, currently only supported in Firefox. It gives you an opportunity to normalize the [http://en.wikipedia.org/wiki/X-height x-height] across a font-stack, reducing the amount of visible change in the FOUT. In fact, the [http://www.fontsquirrel.com/fontface/generator Font Squirrel generator] just added a feature where it tells you the x-height ratio of the fonts you upload, so you can accurately set the <code>font-size-adjust</code> value.

==Summary==

Webfonts deliver quite a bit of freedom to designers, and with upcoming features like [http://hacks.mozilla.org/2009/10/font-control-for-designers/ discretionary ligatures and stylistic alternates], they will have a lot more flexibility. For now, you can feel confident implementing this part of CSS3, as it covers 98% of deployed browsers. Enjoy!
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}