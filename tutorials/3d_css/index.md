{{Page_Title|3D and CSS}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Paul Kinlan
|Published=Sept. 7, 2010
}}
{{Summary_Section|An introduction to CSS 3D transforms.}}
{{Tutorial
|Content===Introduction==

For a long time 3D has been the preserve of desktop applications. Recently with the introduction of advanced smart-phones that have access to native GPU acceleration we have started to see 3D used nearly everywhere.

Commonly, 3D is primarily used as a device for gaming or for some advanced user interfaces. It wasn't until the introduction of Perspective transforms in WPF and Silverlight that a suitable model for applying 3D effects to user interface elements became a practical solution for application developers (after all, 3D isn't exactly easy).

The [http://www.w3.org/TR/css3-3d-transforms/ CSS 3D Transform Model] was introduced as a Draft specification in March 2009 to allow web developers to create interesting and compelling user interfaces that take advantage of 3D by allowing application authors to apply 3D perspective transformations to any visual DOM element.

The CSS 3D Transformation Working Draft is a logical extension to the [http://www.w3.org/TR/css3-2d-transforms CSS 2D Transform Model], introducing some extra properties, including perspectives, rotations, and transforms in a 3D space.
Never before have we been able build 3D interfaces so easily. These technologies have lowered the barrier to entry. No longer do you have to be a mathematical whizz to build 3D elements.

It must be noted that the CSS 3D module is designed to help developers build rich and visually interesting applications; it is not designed to enable you to build immersive 3D worlds.

==Browser Support and Hardware Acceleration==

An important piece of information to remember is that although a browser may "support" 3D, it might not be able to ''render'' 3D.

3D scenes based on the DOM can be very computationally expensive and therefore browser vendors have decided that, rather than slow the browsers down with a pure software rendering solution, they instead will take advantage of GPU which might not be available on all platforms.

==Feature Detection==

What about feature detection? I was hoping that you weren't going to ask!

Developers have been using tools such as [http://modernizr.com/ Modernizr] to detect support for specific browser features and abilities. Whilst it is possible to detect the presence of support for 3D transformations, it is not possible to detect for the presence of hardware acceleration, and hardware acceleration is the key ingredient.

==Basic Sample==

There is nothing better than jumping straight in. In this sample we will apply a basic set of rotations to an arbitrary DOM element. We start by defining a perspective on the root element.

<pre>
 &lt;div style="-webkit-perspective: 800; perspective: 800; margin: 100px 0 0 50px"&gt;
</pre>

Perspective is important because it defines how the depth of the 3D scene is rendered. Values from 1-1000 will produce a very pronounced effect, and values over 1000 less so.

We then add an iframe and apply a 30 degree rotation around the Z and Y axis.

<pre>
 &lt;iframe
     src="http://www.html5rocks.com/"
     style="-webkit-transform: rotate3d(0, 1, 1, 30deg)"&gt;&lt;/iframe&gt;
</pre>

[[Image:3dperspectivetransp.gif]]<br/>
''A 3D 30 degree rotation''

BAM! That is it, the element is fully interactive, and in all respects it is a fully fledged DOM element (except that it now looks even cooler). You can see a live demo in [http://www.html5rocks.com/en/tutorials/3d/css/ this HTML5Rocks! article].

If your browser doesn't support 3D transformations, nothing will happen. You will just see a simple iframe with no rotation applied. If your browser supports 3D transformations but without hardware acceleration, it might look a little odd.

==Animating==

The thing that I love about CSS3 3D transformations is that it ties in so beautifully with the CSS Transition module. Animations and transitions are easy to define in CSS, and applying these to 3D is no exception.

To animate elements that have a 3D perspective, simply set the "transition" style to be "transform" and attach a duration and an animation function. From then on, any change to the "transform" style will be animated.

We have re-factored the previous examples to use document styles, rather than inline styles. Not only does it make the example more clear, it allows the sample to take advantage of the the CSS <code>:hover</code> pseudo class. By using <code>:hover</code>, transitions can be initiated by simply moving the mouse over the element. Awesome!

==Summary==

This was just a quick glance over some of the cool effects that can be applied to any visible DOM element using CSS 3D transformations. There are still many things that can be done that have not been covered in this tutorial.
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=CSS 3D Transforms
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=20.0
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Yes
|Firefox_prefixed_version=12.0
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Yes
|Internet_explorer_prefixed_version=10.0
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Yes
|Safari_prefixed_version=5.1
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=CSS 3D Transforms
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Yes
|Android_prefixed_version=3.0
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
|Safari_mobile_prefixed_version=3.2
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
|HTML5Rocks_link=http://www.html5rocks.com/tutorials/3d/css/
}}