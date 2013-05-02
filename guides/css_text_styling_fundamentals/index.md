{{Page_Title|CSS text styling fundamentals}}
{{Flags
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|This article covers the fundamentals of styling text on the web, including web fonts, font size, line height, and more.}}
{{Tutorial
|Content=== Introduction ==

The web is composed of a lot of different things, technical, social, and structural, but at its heart is something we all understand — human language. The beauty of the web is that it allows human-readable text to be presented so that it transcends barriers such as disability and geography. Of course, as humans we have been working out ways to format text so that it is legible to others for many centuries, but in printed form.

Web design has a lot of parallels with print design, but it also has a lot of differences and a lot more limitations. In this article we will explore how to style text on the web using CSS. The onrunning example will be a short biography page about [http://people.opera.com/cmills/css-text-styling/zappa.html Frank Zappa].

Note: The earlier article, [http://docs.webplatform.org/wiki/concepts/web_typography typography on the web], lays a good foundation for this chapter by explaining a number of typographic concepts. Make sure you read it before going on to this one.

== Print to web? ==

The main shock that print designers get when coming to the web is the lack of control. In print design, the designer has ultimate control over how their creations will look, and are safe in the knowledge that the space the work appears in will not change dimensions, number of colors available, or any other such property.

On the web however, you can not guarantee that your beautifully crafted design will look identical to you and your users. They might be using a different operating system, or a different device altogether, or they might be visually impaired, meaning that they might be using your site with a lot of magnification, or a custom style sheet that changes your fonts and colors, or a screen reader, which reads the text out to them.

So, you need to accept this uncertainty, and move on. You will discover strategies to make your designs more flexible so they look better in widely varying viewing contexts later on in the course, but for now, review the basics:

== Font styles ==

CSS has a number of properties beginning with <code>font-</code>, which allow you to control many features of the text characters (or glyphs) themselves. Take a look at these in the following sections.

=== Choosing a font with font-family ===

<code>font-family</code> allows you to specify which font, or fonts, a selection of elements will use. Take the Zappa example linked to above and try adding the following CSS line to the existing <code>body</code> rule, then save and reload:

<syntaxhighlight lang="css">font-family: Arial;</syntaxhighlight>

This will apply Arial &mdash; a sans-serif font (no serifs, the little decorative features at the end of the strokes of the text) &mdash; to the whole document, rather than the default serif font (fonts that <em>have</em> got serifs), provided this font is available on user's systems.

It probably will be, because Arial is a ubiquitous font, which means it is likely available on all systems.

==== Web-safe fonts ====

There are about 11 fonts that are installed across almost all systems, termed <strong>web safe fonts</strong> because they are safe for use in your pages. The full list is:

<ul>
  <li><strong>Sans-serif</strong>: fonts without serifs: Verdana, Arial, Trebuchet MS</li>
  <li><strong>Serif</strong>: fonts with serifs: Times new roman, Georgia</li>
  <li><strong>Monospaced</strong>: fonts in which every glyph takes up the same space, like in computer code: Andale mono, Courier new</li>
  <li><strong>Cursive</strong>: fonts that have a decorative, often handwritten-looking style: Comic Sans</li>
  <li><strong>Fantasy</strong>: fonts that have a bold, often ornamental or quirky style, which are meant to be used for headings, not body copy: Impact</li>
</ul>

==== Font stacks ====

If you want, you can also apply a number of fonts to a single element selection, known as a <strong>font stack</strong>. Try changing the line you added above to the following:

<syntaxhighlight lang="css">font-family: 'helvetica neue', arial, verdana, sans-serif;</syntaxhighlight>

You'll probably not see much difference from what was there before, so it is important to understand how it works. When you specify a font stack like this, the browser goes through them from left to right, until it finds a font that is installed on the system, and therefore can be used.

So:

* The browser searches for Helvetica neue on the user's system, and uses this font if it finds it. This is a nicer looking font than the more common ones, so I want to use it if possible.
* If Helvetica neue is not found, the browser searches for Arial on the user's system, and uses it if it finds it. This is still quite a nice sans-serif font.
* If Arial isn't found, we'll use Verdana, which is pretty ugly as fonts go, but better than nothing.
* As a last resort, if none of the fonts in the font stack are found the font falls back to sans-serif, which basically instructs the browser to use whatever font defaults as the system's default sans-serif font. You do not know exactly what will be used in this eventuality, which is an annoying loss of control, but at least this is better than ending up with the browser default &mdash; Times new roman &mdash; which is a serif font.

Note that fonts with more than one word in their name must be surrounded by quotes.

==== Overriding body fonts ====

So far you have set fonts on the <code>&lt;body&gt;</code> element, which sets a page-wide default that affects everything; now you will learn how to override some of the <code>&lt;body&gt;</code>'s child elements to set things up nicely.

For a start, it is often a good idea to use a different font for at least some of your headings, to make them stand out and give your site a bit more character. Add the following to your styles:

<syntaxhighlight lang="css">
h1, h2 {
  font-family: impact; 
}
</syntaxhighlight>

Save and reload and notice that the page now looks very different. 

As for other fonts we could affect, how about the emphasized text? I've used <code>&lt;em&gt;</code> for all references involving dates to make them stand out a bit. As it is, the browser gives emphasis a default italic look, but this does not stand out as much as it could. Add the following rule: 

<syntaxhighlight lang="css">
em {
  font-family: georgia;
}
</syntaxhighlight>

Your fonts (especially your headings) are one of the biggest contributors to the overall personality of your site, so choose them carefully to fit. This may sound difficult to begin with, but you will soon get the hang of it. As a rule, Times new roman is good for corporate sites, whereas a sans-serif like Arial might be better for a less formal site. Cursive fonts need to be used sparingly &mdash; for example comic sans is hated by many designers, but it is suitable in some cases. For example, you can use comic sans to create a chalk on blackboard effect on a children's site.

Headings used to be difficult to deal with. Given that the only web safe fantasy font seems to be Impact (not bad, but imagine if all sites had to use it) and you do not want to be stuck with a default system font, such as the dreadful Papyrus, designers used to use various image techniques for their headings. As you should know by now, using images for text on a web site is really bad because images cannot be read by screen readers or search engines. In the next section, you will find some solutions to resolve this problem.

See [http://people.opera.com/cmills/css-text-styling/zappa2.html zappa2.html] for the additions so far.

=== Image replacement ===

Image replacement is a very common technique to display better looking headings and company logos, while not making the text inaccessible or compromising on search engine optimization. Here is an overview of how it works:

Create an image file of your heading with the desired design. You can [http://people.opera.com/cmills/css-text-styling/zappa.png use my Frank Zappa image]. Add the following rule to your CSS, and then save and reload the page, making sure the image is in the same directory as the zappa.html file:

<syntaxhighlight lang="css">
h1 {
  background-image: url(zappa.png);
  height: 55px;
  text-indent: -9000px;
}
</syntaxhighlight>

There are many variations on image replacement, but this is basically how most of them work: first of all, we include our image as a background image on the element we want to replace, setting the dimensions of the element to make sure the image can be fully seen (I've made the example image 600 x 55 px - the same width as my content column.) Then we use a very large negative text indent to push the actual heading text right off the page so you can not see it, just leaving the background image in view. Do not worry about the unfamiliar CSS properties: you will learn more about these later in the article series.

This works pretty well &mdash; you get the heading look you want displayed on the page, across most browsers (most modern browsers display background images), and the actual text is still there to provide screen readers and search engines with what they need. There are some disadvantages however:

* This technique is very inflexible. You have to create an image for each bit of text you want to replace, and then change them every time you want to change size, color, wording, or anything else. And imagine trying to use image replacement on bits of text inside paragraphs as well as headings? Too fiddly.
* Text scales nicely as you zoom in, images don't. If you try zooming in the example too much, the heading will start to look grainy and pixelated.
* If you try to use too much text replacement, the extra HTTP requests could slow things down a fair amount. Some more sophisticated image replacement techniques can slow down the page even more, as they use Flash ([http://novemberborn.net/sifr3 siFR]) or SVG ([http://cufon.shoqolate.com/generate/ cufon]).

See [http://people.opera.com/cmills/css-text-styling/zappa3.html zappa3.html] for the additions at this point.

=== Web fonts ===

CSS3 introduces Web fonts, a feature that allows us to specify our own custom font files to download along with our web pages. This is great, as it complete gets around the problem of fonts not being available on user's machines. To specify a web font for download on a page, you reference the font in a special <code>@font-face</code> block that goes at the top of the page, and looks something like this:

<syntaxhighlight lang="css">
@font-face {
  font-family: 'My font';
  src: url('myfont.ttf') format('truetype');
}</syntaxhighlight>

There are more available options, but it is best to keep it simple for now. Basically, this involves specifying the name of the font family, and then pointing to the font file you want visitors to download along with your web page. This should always go at the top of your CSS file, so you can use it afterwards.

You then include the font in your page in exactly the same way as you would other fonts:

<syntaxhighlight lang="css">font-family: 'My font';</syntaxhighlight>

Simple huh? Well, not quite. the reality is that not all browsers support the same font formats, so the syntax to make this work across browsers is more complicated. Luckily, it is not necessary to write it yourself, as there are a number of services available that will do the hard work for you. This article describes a free service called [http://www.fontsquirrel.com Font Squirrel], which not only has lot of great fonts available for you to use, but also generates all the CSS and font files you'll need.

Follow these steps:

* Obtain a font file. Almost all formats will work. The font I used for the Frank Zappa heading is called Romantiques, and I got it from http://www.fontspace.com/category/circus. Download the zip file, and then unzip it.

* Visit fontsquirrel.com and choose the [http://www.fontsquirrel.com/fontface/generator @font-face generator].

* Click "add fonts", select the Romantique font file you want to use, and check the disclaimer checkbox agreement.

* Click the "Download your kit" button. After a few seconds, you are prompted to save your web font kit. Save it in your example files.

* Unzip the kit, and you will see several files. The files you are interested in are the different font format files, and the <code>stylesheet.css</code>.

* Copy all the font files (<code>.eot</code>, <code>.svg</code>, <code>.ttf</code> and <code>.woff</code>) to a sensible location in your example files. Saving the files in the same directory as the zappa HTML file is easiest.

* Open the <code>stylesheet.css</code> file and copy the CSS rule inside it into the top of your example file styles. It looks like this:

<syntaxhighlight lang="css">
@font-face {
  font-family: 'RomantiquesRegular';
  src: url('romantiques-webfont.eot');
  src: url('romantiques-webfont.eot?#iefix') format('embedded-opentype'),
       url('romantiques-webfont.woff') format('woff'),
       url('romantiques-webfont.ttf') format('truetype'),
       url('romantiques-webfont.svg#RomantiquesRegular') format('svg');
  font-weight: normal;
  font-style: normal;
}
</syntaxhighlight>

# Again, the <code>font-family</code> dictates the name of the font, used to identify it in the code.
# The <code>src</code> values specify the locations of the font files. Different browsers coming across this keep going through the list until they find a format they understand, at which point they download that font file and use it in the page (although some browsers are a bit buggy, and may download more than just the one they need, wasting bandwidth in the process). IE uses the <code>.eot</code> version; most modern browsers will use the <abbr title="Web Open Font Format"><code>.woff</code></abbr>, which is smaller in file size than the others; older browsers other than IE that do not support <code>.woff</code> will use the <code>.ttf</code> or <code>.svg</code> files.
# the <code>font-weight</code> and <code>font-style</code> specify attributes such as the weight of the font, and if it is italic, but it is not necessary to worry about those for now.

Note: If you didn't save the font files in the same directory as your example file, you will have to update the file paths to match the location of the fonts.

* Delete the <code>h1</code> rule you added previously, and replace it with this:

<syntaxhighlight lang="css">h1, h2 {
  font-family: RomantiquesRegular;
}</syntaxhighlight>

Save the page and reload it. Notice that the font is applied to all first and second level headings in the page. This is a very useful tip, and much more flexible than image replacement. Try adding a color to your headings:

<syntaxhighlight lang="css">color: #530FAD;</syntaxhighlight>

There are some issues with using custom fonts in this manner. Consider the following: 

* <strong>File size</strong>: For the purposes of this article, I deliberately selected a large sized font to highlight file size problems. Most western font file are not this big, but the Romantique files were mostly a few hundred KB, with the SVG weighing in at almost 1MB! This is a lot of extra weight to add to a page, especially for those downloading on slower bandwidth, such as mobile networks. And while Western glyph sets usually only have tens of characters in them, maybe a few hundred if a set is really complete, some language font sets (especially <abbr title="Chinese, Japanese, and Korean">CJK</abbr>) can have literally thousands of characters, and be many MB in size. Be aware!
* <strong>Font size</strong>: You will notice that the font size is a lot smaller than with the image replacement version. Different base font sizes can also vary dramatically, so take that into consideration when setting font sizes, and investigate how fallback font sizes will match up to the primary fonts you want to use.
* <abbr title="Flash of Unstyled Text"><strong>FOUT</strong></abbr>: This occurs when a page is loading, and for a short while, the text displays without the web font applied, before the web font finishes loading. When it does load, the page shifts to show the new font, which can be a jarring experience for the visitor. You can mitigate this using a library such as [Google web font loader http://code.google.com/apis/webfonts/docs/webfont_loader.html] or [http://www.extensis.com/en/WebINK/fout-b-gone/ FOUT-b-Gone].
* <strong>Number of glyphs/font quality</strong>: There are a lot of free fonts available, from sites like [http://www.fontsquirrel.com/ Font squirrel], [http://www.dafont.com/ DaFont], [http://new.myfonts.com/ My Fonts], and [http://www.google.com/webfonts Google web fonts], however they are not all high quality, and some may have a very limited glyph set, so you'll get horrible little blank squares displayed instead of characters if you have characters on a page that are not present in your chosen font. This presents far more of a problem in body text than headings, and you need to be especially careful of this if you are using web fonts on sites with user generated content, because you cannot control exactly which characters visitors enter. Some fonts may also look bad on certain operating systems (they can look bad on Windows if the user does not have cleartype enabled). The only answer here is to test your fonts thoroughly before using them in your design. For example, the comma in the first <code>&lt;h2&gt;</code> looked terrible after I set my fonts to Romantique, so I removed it.

Note: There are professional paid font services you can use for your web font needs, such as [http://fontdeck.com/ Fontdeck] and [https://typekit.com/ Typekit]. If you have the money to spend, their font options provide higher quality.

I also set my emphasis font to a "slab serif" font called Copse, to make things a bit more interesting. 

See [http://people.opera.com/cmills/css-text-styling/zappa4.html zappa4.html] for the additions at this point.

=== Setting units and sizing with font-size ===

The next CSS property to look at is <code>font-size</code>. This allows you to set the size of the text inside selected elements, using any CSS units available, such as pixels, ems, percentage, and more. 

You can also use size keywords: <code>xx-small</code>, <code>x-small</code>, <code>small</code>, <code>medium</code>, <code>large</code>, <code>x-large</code>, and <code>xx-large</code>. These tend to be best used when you want to set font sizes relative to each other. For example, the body size is <code>medium</code>, then you could set the top level heading to <code>xx-large</code>, and then perhaps set the second level heading to <code>x-large</code>.

Using size keywords, headings will always stay proportionate to one another, regardless of the fonts used and the visitor's operating system. But they do not offer a great amount of control &mdash; you do not see them used very often. Check out the following typical font-sizing exercise.

==== Setting a base font size ====

The first thing to do is set a base font size for the whole document. This is usually accomplished by adding a rule to the <code>&lt;body&gt;</code> element. Add the following to your <code>body</code> rule:

<syntaxhighlight lang="css">font-size: 62.5%</syntaxhighlight>

Why 62.5%? The answer is that the default font-size for most browsers is 16px. 62.5% of 16 is 10, so by using this percentage you are setting the base font for the whole site to 10px, which makes subsequent math calculations easier.

==== Setting heading and body sizes ====

Next, turn your attention to the font-sizes for different content. The base font size is 10px, making it easy to work out the sizes of the rest of the page text. For example, if you want the first level headings to be 42px, you can set the font-size to 420%, or 4.2ems. Percentages and ems work almost equivalently for our purposes. The differences are not really that important, at least for now. Both units set sizes proportionately to the size of parent font size, and the added bonus is that you can also set other dimensions in your design to percentages of ems, such as margins, the width of content blocks, and more. It is nice to be able to control a whole site relative to the text sizes.

The other option you often see involves using pixels. Pixel units seem to give more control, as you set an absolute pixel size, but the font size does not change proportionally to anything else. However, this is not a best practice, because older browsers like IE6 cannot resize text that is set to pixel values, which is a big accessibility problem.

For now, stick to using ems when writing rules.

Add the following rules to your styles:

<syntaxhighlight lang="css">h1 {
  font-size: 5.5em;
}
    
h2 {
  font-size: 3em;
}</syntaxhighlight>

If you view the page in different browsers, you will notice that this rather complex font looks better in some browsers than others, and none look quite as good at the image replacement version, with the heading created in Adobe Fireworks. This is the kind of testing you should do before embarking too far into a project with a chosen font. Also, it does not look that great at a smaller size on the <code>h2</code>s. But for the purposes of this example, leave it as-is.

Next, set the body text and list to make it easier to read:

<syntaxhighlight lang="css">p, ul {
  font-size: 1.6em;
}</syntaxhighlight>

The rule above sets the body copy back to the default browser size, but it looks good and is readable.

Next, set the emphasis slightly smaller, to make it stand out even more nicely:

<syntaxhighlight lang="css">em {
  font-size: 0.8em;
}</syntaxhighlight>

If you are wondering why you had to set it to 0.8em to get it slightly smaller, rather than say 1.5 or 1.4, try it and see.

The reason is that the parent elements of <code>&lt;em&gt;</code> (either <code>&lt;p&gt;</code> or <code>&lt;li&gt;</code>) have been set to 1.5em. The sizing is relative to the font size of the immediate parent, so in this context 16px is equal to 1em. We have set 0.8em for the emphasiTed text, so the size comes out as 16px x 0.8 = about 13px.

Note: The pixel sizes I am talking about here are what is called the <strong>computed values</strong>. Regardless of the units and values you use to set your font sizes, computers display graphics display in pixels, so the browser must convert everything into pixel values before it can display them to visitors.

See [http://people.opera.com/cmills/css-text-styling/zappa5.html zappa5.html] for the additions at this point.

=== Changing the details with font-weight, font-style, and font-variant ===

Next, you'll check out these properties:

* <code>font-weight</code> allows you to set the boldness of text in selected elements.
* <code>font-style</code> allows you to set a element's text to be oblique or italic.
* <code>font-variant</code>allows you to set and element's text to be small-caps, also known as copperplate letters.

==== Using font-weight ====

Use this property when you want text to be bolder. Possible values are:

* <code>bold</code> and <code>bolder</code> provide two levels of extra boldness.
* <code>lighter</code> provides a level of less boldness.
* <code>100</code>, <code>200</code> ... all the way up to <code>900</code> provide incremental levels of boldness.
* <code>normal</code> is the default non-bold setting.

Most of these settings don't really make a visual difference, especially when setting small font sizes, and when the font you are using doesn't have different levels of boldness defined in it.

For this example, add the following rule to highlight the first lines below each heading:

<syntaxhighlight lang="css">h1 + p:first-line, h2 + p:first-line {
  font-weight: bold;
}</syntaxhighlight>

And then save the page, reload the browser window, and review the results.

Note: <code>bold</code> is equivalent to <code>700</code>.

==== Setting font-style ====

<code>font-style</code> can take the values <code>italic</code>, <code>oblique</code>, and <code>normal</code>. Normal is the default, as before, <code>italic</code> tells the browser to use the italic version of the font (if available), and <code>oblique</code> tells the browser to use the normal version of the font, but slant it. If you specify <code>italic</code>, unless the font you are using has a specific italic version available the browser will fall back to generate an oblique version to use.

Add the following line to the rule you added in the previous section:

<syntaxhighlight lang="css">font-style: italic;</syntaxhighlight>

==== Working with font-variant ====

<code>font-variant</code> can take two values, <code>normal</code>, which is the default as expected, and <code>small-caps</code>, which uses all capital characters, but large ones for the capital letters, and small ones for the lower case letters. Add the following to the <code>em</code> rule and see what happens:

<syntaxhighlight lang="css">font-variant: small-caps;</syntaxhighlight>

See [http://people.opera.com/cmills/css-text-styling/zappa6.html zappa6.html] for the additions at this point.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}