{{Page_Title|CSS cross-fade() function}}
{{Flags}}
{{Standardization_Status|W3C Working Draft}}
{{API_Name}}
{{Summary_Section|The CSS cross-fade() function lets overlay two images at a defined transparency.}}
{{CSS_Function
|Content===Introduction==
The ability to overlay one image with another and see them both in semi-transparency is a fairly common technique in web pages.
This effect is generally accomplished by carefully positioning two images in the same space, one on top of the other, and then tweaking their opacity. The effect can be further enhanced by using JavaScript to manipulate the positions and/or the opacity.

That approach is of course not optimal, and requires considerable finesse in the CSS coding as well as some scripting ability. 
A straightforward CSS-only solution to image combination would be both easier to understand and simpler to code.

[http://www.w3.org/TR/2012/WD-css4-images-20120911/#cross-fade-functionPart of the "CSS Image Values and Replaced Content Module Level 4" specification] introduces this feature into CSS. 

==Use==
The <code>cross-fade()</code> function takes three parameters: the two images to be combined and the percentage of combination. The percentage may be thought of as a transparency value for the "bottom" image, although technically neither image is really on top of the other, they are merely rendered together.

The <code>cross-fade()</code> function can be used in CSS anywhere that an ordinary image reference can be used. The syntax is straightforward:

<syntaxhighlight language="css">
cross-fade(url(image1), url(image2), percent)
</syntaxhighlight>

The image URLs may be in either order, and may be coded with or without quotes; the percent value must be coded without quotes, must contain the "%" symbol, and its value must be between 0% and 100%.

==Examples==

For the following examples, we will use two images, each sized at 200px by 200px. The first, white.png, is a white-filled box with a 5-pixel blue border. The second, black.png, is a black-filled box with a 5-pixel red border. Thus, cross-fading the two images at different percentages should yield boxes of varying grays with borders of varying magentas. Here are the original images:

[[image:white.png]]<br/>
''white.png''

[[Image:black.png]]<br/>
''black.png''

===A 50% cross-fade===
First, let's set up an empty <code>&lt;div&gt;</code> to contain the images.

<syntaxhighlight language="css">
<div style="width:200px; height:200px;"></div>
</syntaxhighlight>

We could, of course, give the <code>&lt;div&gt;</code> a background image.

<syntaxhighlight language="css">
<div style="width:200px; height:200px; background-image:url('white.png');"></div>
</syntaxhighlight>

But that's kind of boring, so let's replace the simple background image with a cross-faded image pair.

<syntaxhighlight language="css">
<div style="width:200px; height:200px; background-image:cross-fade(url(white.png), url(black.png), 50%);"></div>
</syntaxhighlight>

The 50% cross-fade renders as an evenly-merged black/white (gray) box with an evenly-merged blue/red (magenta) border.

[[Image:fifty.png]]<br/>
''A 50% cross-fade''

===Other cross-fade percentages===
Here are the code samples and their results for the same two images, cross-faded first at 25% and then at 75%. 
(Obviously, a 0% fade effectively yields only the first image, while a 100% fade yields only the second.)
Note that the visual results are exactly what you would intuitively expect based on the original colors.

<syntaxhighlight language="css">
<div style="width:200px; height:200px; background-image:cross-fade(url(white.png), url(black.png), 25%);"></div>
</syntaxhighlight>

[[Image:twentyfive.png]]<br/>
''A 25% cross-fade''

<syntaxhighlight language="css">
<div style="width:200px; height:200px; background-image:cross-fade(url(white.png), url(black.png), 75%);"></div>
</syntaxhighlight>

[[Image:seventyfive.png]]<br/>
''A 75% cross-fade''

==Simplifying the code==
Clearly, that's a lot of code to put on individual HTML elements, especially if the effect is repeated in the page.
It's far more elegant&mdash;and efficient&mdash;to
abstract the cross-fade function into a single CSS style and then apply it to whatever elements require it.
Here, we use an independent selector to define a class with the appropriate size and the appropriate cross-faded background image, and then simply use the class later in the document.

<syntaxhighlight language="css">
<style>
.cfade { background-image:cross-fade(url(white.png), url(black.png), 50%); width:200px; height:200px; }
</style>

. . .

<div class="cfade"></div>
</syntaxhighlight>

It should be noted that, once defined, our ''.cfade'' class is not restricted to <code>&lt;div&gt;</code>s;
we can apply it to any page element and achieve the same effect.

<syntaxhighlight language="css">
<p class="cfade"></p>
</syntaxhighlight>

Nor is the cross-fade effect limited to ''empty'' elements. Consider the following code and its result.

<syntaxhighlight language="css">
<p class="cfade">Four score and seven years ago our fathers brought forth upon this continent a new nation...</p>
</syntaxhighlight>

[[Image:fiftytext.png]]<br/>
''A 50% cross-fade with text''

I didn't say it was pretty, just that it was possible! 

==A final example==
Here, then, is a more practical (and attractive) example.
Let's start with a beautiful full moon.

[[Image:fullmoon.jpg]]<br/>
''Full moon''

Then let's choose a bold wolf silhouette for an overlay.

[[Image:wolf.png]]<br/>
''Wolf silhouette''

Now we'll write the code to cross-fade them (directly on the <code>&lt;div&gt;</code> for simplicity). Note that 
while the images are the same size, they are of different types, one jpg and one png.

<syntaxhighlight language="css">
<div style="background-image:cross-fade(url('fullmoon.jpg'), url('wolf.png'), 50%); width:600px; height:600px;"></div>
</syntaxhighlight>

The result is a classic (if somewhat kitschy) wolf-on-moon combo.

[[Image:wolfmoon.png]]<br/>
''Wolf on moon''
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Image Values and Replaced Content Module Level 4
|URL=http://www.w3.org/TR/css4-images/#cross-fade-function
|Status=W3C Working Draft
}}
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=No
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row}}
}}
{{See_Also_Section
|Topic_clusters=Visual Effects, Background
}}
{{Topics|Graphics, CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}