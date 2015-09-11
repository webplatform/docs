---
title: Using CSS 3D transforms
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/tutorials/3d/css/)'
readiness: 'Ready to Use'
summary: 'An introduction to CSS 3D transforms.'
tags:
  - Tutorials
uri: 'tutorials/3d css'

---
**By Paul Kinlan**
Originally published Sept. 7, 2010

## <span>Summary</span>

An introduction to CSS 3D transforms.

## <span>Introduction</span>

For a long time 3D has been the preserve of desktop applications. Recently with the introduction of advanced smart-phones that have access to native GPU acceleration we have started to see 3D used nearly everywhere.

Commonly, 3D is primarily used as a device for gaming or for some advanced user interfaces. It wasn't until the introduction of Perspective transforms in WPF and Silverlight that a suitable model for applying 3D effects to user interface elements became a practical solution for application developers (after all, 3D isn't exactly easy).

The [CSS 3D Transform Model](http://www.w3.org/TR/css3-3d-transforms/) was introduced as a Draft specification in March 2009 to allow web developers to create interesting and compelling user interfaces that take advantage of 3D by allowing application authors to apply 3D perspective transformations to any visual DOM element.

The CSS 3D Transformation Working Draft is a logical extension to the [CSS 2D Transform Model](http://www.w3.org/TR/css3-2d-transforms), introducing some extra properties, including perspectives, rotations, and transforms in a 3D space. Never before have we been able build 3D interfaces so easily. These technologies have lowered the barrier to entry. No longer do you have to be a mathematical whizz to build 3D elements.

It must be noted that the CSS 3D module is designed to help developers build rich and visually interesting applications; it is not designed to enable you to build immersive 3D worlds.

## <span>Browser Support and Hardware Acceleration</span>

An important piece of information to remember is that although a browser may "support" 3D, it might not be able to *render* 3D.

3D scenes based on the DOM can be very computationally expensive and therefore browser vendors have decided that, rather than slow the browsers down with a pure software rendering solution, they instead will take advantage of GPU which might not be available on all platforms.

## <span>Feature Detection</span>

What about feature detection? I was hoping that you weren't going to ask!

Developers have been using tools such as [Modernizr](http://modernizr.com/) to detect support for specific browser features and abilities. Whilst it is possible to detect the presence of support for 3D transformations, it is not possible to detect for the presence of hardware acceleration, and hardware acceleration is the key ingredient.

## <span>Basic Sample</span>

There is nothing better than jumping straight in. In this sample we will apply a basic set of rotations to an arbitrary DOM element. We start by defining a perspective on the root element.

     <div style="-webkit-perspective: 800; perspective: 800; margin: 100px 0 0 50px">

Perspective is important because it defines how the depth of the 3D scene is rendered. Values from 1-1000 will produce a very pronounced effect, and values over 1000 less so.

We then add an iframe and apply a 30 degree rotation around the Z and Y axis.

     <iframe
         src="http://www.html5rocks.com/"
         style="-webkit-transform: rotate3d(0, 1, 1, 30deg)"></iframe>

*A 3D 30 degree rotation* ![3dperspectivetransp.gif](/assets/public/7/76/3dperspectivetransp.gif)

BAM! That is it, the element is fully interactive, and in all respects it is a fully fledged DOM element (except that it now looks even cooler). You can see a live demo in [this HTML5Rocks! article](http://www.html5rocks.com/en/tutorials/3d/css/).

If your browser doesn't support 3D transformations, nothing will happen. You will just see a simple iframe with no rotation applied. If your browser supports 3D transformations but without hardware acceleration, it might look a little odd.

## <span>Animating</span>

The thing that I love about CSS3 3D transformations is that it ties in so beautifully with the CSS Transition module. Animations and transitions are easy to define in CSS, and applying these to 3D is no exception.

To animate elements that have a 3D perspective, simply set the "transition" style to be "transform" and attach a duration and an animation function. From then on, any change to the "transform" style will be animated.

We have re-factored the previous examples to use document styles, rather than inline styles. Not only does it make the example more clear, it allows the sample to take advantage of the the CSS `:hover` pseudo class. By using `:hover`, transitions can be initiated by simply moving the mouse over the element. Awesome!

## <span>Summary</span>

This was just a quick glance over some of the cool effects that can be applied to any visible DOM element using CSS 3D transformations. There are still many things that can be done that have not been covered in this tutorial.

