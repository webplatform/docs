---
title: Manipulating content with CSS3 transforms
readiness: 'Ready to Use'
summary: 'CSS transforms allow you to dynamically manipulate the space in which content elements appear. You can move them around on the screen, shrink or expand them, rotate them, or combine all these effects to produce complex movements.  By themselves, transforms produce static visual effects, but you can easily combine them with CSS transitions and keyframe animations to produce vibrant animated interfaces. This tutorial first introduces simple two-dimensional transforms, then shows you how to extend transforms into three-dimensional space.  It ends with step-by-step instructions on how to spin a cube in space.'
tags:
  - Tutorials
  - CSS
uri: 'tutorials/css transforms'

---
**By Mike Sierra**

## <span>Summary</span>

CSS transforms allow you to dynamically manipulate the space in which content elements appear. You can move them around on the screen, shrink or expand them, rotate them, or combine all these effects to produce complex movements. By themselves, transforms produce static visual effects, but you can easily combine them with CSS transitions and keyframe animations to produce vibrant animated interfaces. This tutorial first introduces simple two-dimensional transforms, then shows you how to extend transforms into three-dimensional space. It ends with step-by-step instructions on how to spin a cube in space.

These key points serve as reference:

-   The [**transform**](/css/properties/transform) property specifies a set of transform functions.

-   2D functions include [**translate()**](/css/functions/translate()), [**scale()**](/css/functions/scale()), [**rotate()**](/css/functions/rotate()), and [**skew()**](/css/functions/skew()).

-   The [**translate()**](/css/functions/translate()) function accepts standard CSS measurements; [**scale()**](/css/functions/scale()) accepts a decimal value between 0 and 1; both [**rotate()**](/css/functions/rotate()) and [**skew()**](/css/functions/skew()) specify radial **deg** or **rad** measurements. Except for [**rotate()**](/css/functions/rotate()), each accepts two *x*/*y* parameters.

-   Individual *x*/*y* functions are available: [**translateX()**](/css/functions/translateX()), [**translateY()**](/css/functions/translateY()), [**scaleX()**](/css/functions/scaleX()), [**scaleY()**](/css/functions/scaleY()), [**skewX()**](/css/functions/skewX()), and [**skewY()**](/css/functions/skewY())

-   Combined 2D transforms can be represented with the [**matrix()**](/css/functions/matrix()) function, which uses 6 parameters.

-   3D functions include [**rotateX()**](/css/functions/rotateX()), [**rotateY()**](/css/functions/rotateY()), [**rotate3d()**](/css/functions/rotate3d()), [**translateZ()**](/css/functions/translateZ()), [**translate3d()**](/css/functions/translate3d()), [**scaleZ()**](/css/functions/scaleZ()), and [**scale3d()**](/css/functions/scale3d()).

-   Combined 3D transforms can be represented with the [**matrix3d()**](/css/functions/matrix3d()) function, which uses 16 parameters.

-   The [**transform-origin**](/css/properties/transform-origin) property controls which point of an element the transform appears to emanate from. Adding a pixel measurement for a third parameter, or for the alternate [**transform-origin-z**](/css/properties/transform-origin-z) property, moves the origin point back and forth in 3D space.

-   The [**perspective**](/css/properties/perspective) property situates a 3D scene relative to the viewer, with distance measured in pixels. To appear correctly, it must be applied to a transformed element's ancestor.

-   The [**perspective-origin**](/css/properties/perspective-origin) property allows a 3D scene to be viewed from a diagonal vantage point rather than straight at the center.

-   The [**backface-visibility**](/css/properties/backface-visibility) property hides elements that rotate away from view, rather than rendering them as a mirror image.

-   Setting [**transform-style**](/css/properties/transform-style) to **preserve-3d** on a 3D element renders any nested 3D elements within its own transformed space.

## <span>The transform property</span>

Transforms alter a block element's coordinates in several ways so that they vary from where they would ordinarily appear. The [**transform**](/css/properties/transform) CSS property specifies a handful of transformation *functions* that can be combined any way you wish: [**translate()**](/css/functions/translate()), [**scale()**](/css/functions/scale()), [**rotate()**](/css/functions/rotate()), and [**skew()**](/css/functions/skew()). Here is how you specify a combination of most of the two-dimensional transforms discussed below, along with a view of how the effect renders relative to the element's default position:

    div.card {
       -moz-transform    : translate(50%, 10%) rotate(20deg) scale(0.75);
       -o-transform      : translate(50%, 10%) rotate(20deg) scale(0.75);
       -webkit-transform : translate(50%, 10%) rotate(20deg) scale(0.75);
       transform         : translate(50%, 10%) rotate(20deg) scale(0.75);
    }

![transform combo.png](//static.webplatformstaging.org/w/public/4/4b/transform_combo.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_2d_combo.html))

Transform properties were implemented recently enough that many browsers only support them with *vendor prefixes* such as **-moz-**, **-o-**, and **-webkit-** as shown above. Throughout this tutorial, CSS examples only show the un-prefixed property name, but for widest support you should apply all of them.

Functions are separated by spaces, but any additional arguments are separated by commas.

While you can specify any number of these functions, values can't be inherited from other style sheets. So you can't apply both of these CSS classes to an element at the same time and expect both effects to apply:

    div.spin   { transform: rotate(20deg); }
    div.tabled { transform: translate(100%) scale(0.5); }

Wherever you apply a transformation, any function left unspecified is assigned a default value, so these work out the same as the less verbose examples above:

    div.spin { transform: rotate(20deg) translate(0,0), scale(1) skew(0,0) }
    div.tabled { transform: rotate(0deg) translate(100%,0) scale(0.5) skew(0.0) }

You can also apply transforms directly to an object from JavaScript. Here's an example in which tilting a mobile handset controls the tilt of a screen element, using the 3D transforms described below:

    var gestural = document.querySelector('#gestural');
    window.addListener('deviceorientation', orientationHandler);
    orientationHandler = function(e) {
       gestural.style.transform = 'rotateX(' + (e.beta * -1) + 'deg) ' + 'rotateY(' + e.gamma + 'deg)';
       gestural.style.WebkitTransform = 'rotateX(' + (e.beta * -1) + 'deg) ' + 'rotateY(' + e.gamma + 'deg)';
    }

Several different technologies such as SVG and the **canvas** element implement transforms, and are all conceptually similar despite slight differences in how they are implemented.

## <span>2D transform functions</span>

The following isolates how each 2D function works. The [**translate()**](/css/functions/translate()) function simply moves an element around on the screen, much the same as when using [**top**](/css/properties/top) and [**left**](/css/properties/left) to position an element. This example moves the card over to the right more than it moves it downward:

    transform: translate(50%, 10%);

![transform translate.png](//static.webplatformstaging.org/w/public/d/db/transform_translate.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_2d_translate.html))

The [**translate()**](/css/functions/translate()) function accepts up to two *x* and *y* values to move to the right and downward. These can specify any CSS measurement, including negative values to move left and upward. Percentages refer to the size of the transformed element. If you specify a single value, it's interpreted as *x* and only moves the element horizontally. Otherwise you can specify separate [**translateX()**](/css/functions/translateX()) and [**translateY()**](/css/functions/translateY()) functions. Here's another way to express the same translation as above:

    transform: translateX(50%) translateY(10%);

The [**scale()**](/css/functions/scale()) function sizes an element in decimal terms relative to a default value of 1. An element whose scale is 2 doubles in size, while a scale of 0 vanishes into a point. A single **scale** value applies to the whole element, but setting two values lets you scale each axis independently, as you can also get with separate [**scaleX()**](/css/functions/scaleX()) and [**scaleY()**](/css/functions/scaleY()) functions. The following pairs offer different ways to produce the effects shown below:

    /* first card */
    transform: scale(0.75);
    transform: scale(0.75, 0.75);
    /* second card */
    transform: scale(0.75, 1.25);
    transform: scaleX(0.75) scaleY(1.25);

![transform scale.png](//static.webplatformstaging.org/w/public/2/20/transform_scale.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_2d_scale.html))

The [**rotate()**](/css/functions/rotate()) function spins an element around its *z* axis. It accepts a degree (**deg**) or radian (**rad**) measurement. (Radians are equivalent to the number of degrees multiplied by π/180.) Radial measurements can wrap around, so the following values are equivalent:

    transform: rotate(20deg);
    transform: rotate(380deg);  /*   360  + 20 */
    transform: rotate(-340deg); /* (-360) + 20 */

![transform rotate.png](//static.webplatformstaging.org/w/public/7/79/transform_rotate.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_2d_rotate.html))

The [**skew()**](/css/functions/skew()) function leans an element over, altering its corner angle relative to the default 90° and transforming the underlying rectangle into a parallelogram. It accepts up to two degree (**deg**) or radian (**rad**) measurements. The separate [**skewX()**](/css/functions/skewX()) function tips the side edges of the element, while [**skewY()**](/css/functions/skewY()) tips the top and bottom. Setting a single [**skew()**](/css/functions/skew()) value affects only the *x* axis.

    transform: skewX(10deg);               /* 1st */
    transform: skewY(-30deg);              /* 2nd */
    transform: skew(10deg, -30deg);        /* 3rd */
    transform: skewX(10deg) skewY(-30deg); /* 3rd, alternate syntax */

![transform skew.png](//static.webplatformstaging.org/w/public/3/34/transform_skew.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_2d_skew.html))

Skewing along both *x* and *y* makes the element appear to move into three-dimensional space, but the transformation actually occurs within a flat plane. Skip below for information about 3D transforms.

**Note:** Browsers internally represent all of the transformations described above as a single *matrix* expression, which for 2D transforms consist of six values. Using the web inspector feature, you can view any transformed element's computed style for an example, and use the the alternative [**matrix()**](/css/functions/matrix()) function to specify those values. Here is how the ace of spades in the example above is represented as a matrix value:

    transform: matrix(1, -0.577, 0.176, 1, 0, 0);

## <span>Changing the transform origin</span>

By default, transforms *originate* from the center of the element, or 50% along both *x* and *y*. If you scale it down, it shrinks towards the center, or else you rotate it around its center point. The [**transform-origin**](/css/properties/transform-origin) property allows you to place this origin point elsewhere, even outside the element, changing how transforms respond, especially in animations. It accepts a pair of *x*/*y* measurements.

This shows a series of transforms that rotate around a point near the bottom right corner:

    div {
        transform-origin   : 80% 90% ;
    }
    div:nth-of-type(1) { transform : rotate(10deg) ; }
    div:nth-of-type(2) { transform : rotate(20deg) ; }
    div:nth-of-type(3) { transform : rotate(30deg) ; }

![origin rotate.png](//static.webplatformstaging.org/w/public/1/16/origin_rotate.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_2d_origin_rotate.html))

In this example, placing the origin of a skew transform at the bottom makes it appear to tip over:

    div {
       transform          : skewX(15deg);
       transform-origin   : bottom;
    }

![origin skew.png](//static.webplatformstaging.org/w/public/6/60/origin_skew.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_2d_origin_skew.html))

The property accepts the keywords **top** and **left** for **0%**, **bottom** and **right** for **100%**, and **center** for **50% 50%**.

In the first of the following examples, placing the origin of a [**scaleX()**](/css/functions/scaleX()) transform along one edge makes it appear to pivot along that edge. In the second, placing the origin far outside the element's boundaries moves it across the screen with no need for the [**translate()**](/css/functions/translate()) function:

    div:first-of-type {
       transform        : scale(0.35, 1);
       transform-origin : 0%;
       transform-origin : left; /* same as 0% */
    }
    div:last-of-type {
       transform-origin : 210% -20%;
       transform        : scale(0.5);
    }

![origin scale.png](//static.webplatformstaging.org/w/public/0/0f/origin_scale.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_2d_origin_scale.html))

## <span>You need some perspective</span>

You really do. Though they often take on the illusion of three dimensions, 2D transforms are strictly superficial, inhabiting the plane of the display screen. Three dimensional transforms allow ordinary web content, which is still inherently flat, to shift onto other planes. But before applying the 3D transform functions discussed below, you need to position the scene relative to the viewer.

Applying *perspective* to an an element indicates the viewer's perceived distance to any transformed descendent elements. The [**perspective**](/css/properties/perspective) property sets a number of CSS pixels along the *z* axis that leads from the screen to the viewer. Since ordinary web content is inherently flat, all measurements along the *z* axis *must* specify absolute units such as pixels, rather than relative percentages that make sense along *x* and *y*.

The default [**perspective**](/css/properties/perspective) value of **none** indicates an infinite perspective, which appears flat. A value in the range of 1000 to 2000 mimics the distance at which people typically view their screen. Perspective values of less than 1000 appear increasingly distorted, but may be desirable for immersive virtual reality applications in which the viewer appears to mingle among displaying elements.

The first scene in the example below shows a 3D rotation that appears flat before applying [**perspective**](/css/properties/perspective), while the second shows a distance of 1000. The ancestor element's [**border**](/css/properties/border) reveals how the descendant's plane has shifted.

    .parent {
        border             : thin solid #000;
        perspective          : 1000px;
        perspective-origin   : 50% 50%;
    }
    .child {
        transform          : rotateY(45deg);
    }

![transform perspective.png](//static.webplatformstaging.org/w/public/f/fa/transform_perspective.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_3d_perspective.html))

While [**perspective**](/css/properties/perspective) affects the perceived distance to an object along the *z* axis, the [**perspective-origin**](/css/properties/perspective-origin) property allows you to shift the perceived location along *x* and *y* from which it is viewed. The second scene reflects the default **center** value in which the viewpoint is centered straight out from the screen. Altering these values positions the viewer diagonally from the scene. The third scene shows the same rotation, but with the viewpoint shifted to the right:

    perspective-origin-x : 500px;

Note that since percentages refer to the size of the transformed element, pixel units may be easier to use. Fixed *x*/*y* values for [**perspective-origin**](/css/properties/perspective-origin) along with *z* values for [**perspective**](/css/properties/perspective) allow you to maintain a Cartesian coordinate system.

Keep in mind several things to help understand how perspective corresponds to how output actually renders:

-   Don't confuse the *perspective* point with the scene's three *vanishing points.* Changing the single perspective point from which you observe the scene may affect where these vanishing points appear to fall, but they are not the same thing.

-   The repositioned perspective point affects the appearance of the transformed element, *not* the ancestor that specifies the perspective.

-   Unlike real life, changing the distance to the scene does *not* change its perceived size. Imagine walking towards a large, recessed bookcase. As you approach it, it appears larger, and its interior angles appear more dramatically skewed towards a vanishing point. Conversely, when you use CSS to reduce the value of [**perspective**](/css/properties/perspective) to approach such a scene, the angles still change, but the overall size appears oddly constant. (The 3D translation functions discussed below allow you to make the distance appear more realistic.)

-   CSS transforms don't allow the viewer to look away from the scene, no matter from where the viewpoint is positioned.

-   From the perspective point, you're actually looking at the element's [**transform-origin**](/css/properties/transform-origin) point, which you may set to fall well *outside* the rendering element.

-   The [**perspective**](/css/properties/perspective) property doesn't allow negative values, so while you may start to simulate traveling around the scene by offsetting the [**perspective-origin**](/css/properties/perspective-origin) while reducing the [**perspective**](/css/properties/perspective) value, you can't actually get to the other side.

## <span>3D transforms</span>

To extend into three-dimensional space, enhanced functions allow rotations around *x* and *y*, and translations into *z* space.

The [**rotateX()**](/css/functions/rotateX()) and [**rotateY()**](/css/functions/rotateY()) functions spin elements around their horizontal or vertical axis, while the [**rotateZ()**](/css/functions/rotateZ()) function behaves the same as the 2D [**rotate()**](/css/functions/rotate()) function.

An alternative [**rotate3d()**](/css/functions/rotate3d()) function requires four arguments. The first three measurements specify a point defining a 3D vector in *x*/*y*/*z* terms from the origin of the element. (For example, setting the vector to **-0.2,1,0.2** spins the object as if it were a child's top leaning slightly forward and to the left, while setting it to **0,1,0** would straighten it.) The fourth argument specifies the angle of rotation around that vector, using **deg** or **rad** measurements.

The [**translate3d()**](/css/functions/translate3d()) function requires three *x*, *y* and *z* measurements. Otherwise, use any combination of [**translateX()**](/css/functions/translateX()), [**translateY()**](/css/functions/translateY()), and [**translateZ()**](/css/functions/translateZ()) functions. The *z* translation must specify absolute measurements. The perceived movement towards or away from the viewer depends on how much perspective has been applied.

The [**scale3d()**](/css/functions/scale3d()) function accepts three *x*, *y* and *z* measurements, otherwise they can be specified separately with [**scaleX()**](/css/functions/scaleX()), [**scaleY()**](/css/functions/scaleY()), and [**scaleZ()**](/css/functions/scaleZ()). Scaling along the *z* axis ordinarily has no effect for flat web content, but does affect the sort of nested 3D objects described in the next section.

The [**transform-origin**](/css/properties/transform-origin) property accepts an additional third **z** measurement to place the transformation point behind or in front of where the element displays, in absolute units. (Alternately, specify the [**transform-origin-z**](/css/properties/transform-origin-z) property.) This example shows a series of elements that rotate to various degrees from an origin point within the gray parent box that is far behind them:

![3d originZ.png](//static.webplatformstaging.org/w/public/4/4a/3d_originZ.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_3d_origin.html))

    .parent {
       perspective          : 10000px;
       perspective-origin-y : -3000px;  /* view from above */
       background-color     : #aaa;
    }
    .child {
       transform-origin-z   : -620px;
       transform-origin     : 50% 50% -620px;  /* same */
    }
    .child:nth-of-type(1) { transform: rotateY(-50deg); }
    .child:nth-of-type(2) { transform: rotateY(-30deg); }
    .child:nth-of-type(3) { transform: rotateY(-10deg); }
    .child:nth-of-type(4) { transform: rotateY(10deg); }
    .child:nth-of-type(5) { transform: rotateY(30deg); }
    .child:nth-of-type(6) { transform: rotateY(50deg); }

By default, elements that rotate away from view display as a mirror image. Changing the [**backface-visibility**](/css/properties/backface-visibility) property to **hidden** (from the default **visible**) enables flip-panel effects in which elements only appear if they face the viewer.

This example shows a pair of child elements positioned at the same coordinates within the parent *card*, but one of which is rotated to face the other way. As described below, you can rotate the entire card along with its children. In this case, with the backface hidden, only one of the child *face* elements displays at a time:

```
 <div class="card">
   <div class="face" id="jackheart"></div>
   <div class="face"></div>
 </div>
```

![3d backface.png](//static.webplatformstaging.org/w/public/b/b0/3d_backface.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_3d_backface.html))

    body {
        background         : #ddd;
        perspective          : 1200px;
    }
    div {
        position           : absolute;
        width                : 280px;
        height                 : 400px;
        border                   : thin solid #777;
        border-radius            : 0.5em;
    }
    .card {
        left               : 0px;
        transform            : rotateY(45deg);    /* vary this to rotate the entire card */
        transform-style      : preserve-3d;    /* this allows each face to rotate within the card */
    }
    .face {
        background-size    : 100% 100%;
        backface-visibility  : hidden;    /* only display when facing viewer */
    }
    .face:first-of-type {
        transform          : rotateY(0deg);
    }
    .face:last-of-type {
        transform          : rotateY(180deg);
        background-image   : url(cardBack2.jpeg);
    }
    #jackheart {
        background-image   : url(JackHeart.jpeg);
    }

While 2D transforms can be represented as a 6-element [**matrix()**](/css/functions/matrix()) function, 3D transforms correspond to 16-element [**matrix3d()**](/css/functions/matrix3d()) functions. Here's how an element might appear within the web inspector's computed style panel:

    transform: matrix3d(0.642, 0, 0.766, 0, 0, 1, 0, 0, -0.766, 0, 0.642, 0, 0, 0, 0, 1);

## <span>Nested 3D transforms</span>

Applying a 3D rotation to an element aligns it to a different plane than that of the viewing screen. Applying 3D translations and scale effects also overrides the default coordinate system. The [**transform-style**](/css/properties/transform-style) property allows you to transform nested content independently within that already modified space.

To clarify how to use this feature, this extended example builds a cube representing playing dice that can spin freely. The markup is implemented as a series of nested elements:

```
 <div class="scene">
     <div class="dice">
         <div class="centered">
             <div class="face"></div>
             <div class="face"></div>
             <div class="face"></div>
             <div class="face"></div>
             <div class="face"></div>
             <div class="face"></div>
         </div>
     </div>
 </div>
```

Global styles define absolutely positioned 100-pixel-square boxes. The outlines will help clarify each nested transform:

    div {
        box-sizing     : border-box;
        position       : absolute;
        width          : 100px;
        height         : 100px;
        outline-offset : 20px;
        outline-width  : 3px;
        outline-style  : solid;
    }

The outermost *scene* element defines the overall perspective:

    .scene {
        perspective   : 500px;
        outline-color : pink;
    }

![3Dnest scene.png](//static.webplatformstaging.org/w/public/8/80/3Dnest_scene.png)

The next *dice* element is rotated arbitrarily:

    .dice {
        transform       : rotateX(30deg) rotateY(50deg) rotateZ(20deg);
        transform-style : preserve-3d;
        outline-color   : lightgreen;
    }

![3Dnest dice.png](//static.webplatformstaging.org/w/public/1/18/3Dnest_dice.png)

The **preserve-3d** above renders any child element's transforms in three dimensions relative to the *dice* element's own transformed space. Otherwise the default **flat** value would make them appear on the *dice* element's surface as if on a display screen.

In this case, the nested *centered* element is there simply as a convenience to drop the cube back to accommodate its full volume:

    .centered {
        transform       : translateZ(-50px);
        transform-style : preserve-3d;
        outline-color   : gold;
    }

![3Dnest centered.png](//static.webplatformstaging.org/w/public/e/ee/3Dnest_centered.png)

Various properties define the dice's edges with rounded corners, along with the small dot images that will be arranged to form a pattern on each face. Only one dot displays in the first face's pattern, and the rest are pushed outside the displaying area:

    .face {
        border-radius       : 6px;
        border              : 2px solid #777;
        background-color    : #fff;
        background-repeat   : no-repeat;
        background-image    : url(dot.png), url(dot.png), url(dot.png),
                              url(dot.png), url(dot.png), url(dot.png);
        outline-color       : transparent;
    }
    .face:nth-of-type(1) {
        background-position : 40px 40px, -20px -20px, -20px -20px,
                             -20px -20px, -20px -20px, -20px -20px;
    }

![3Dnest face1.png](//static.webplatformstaging.org/w/public/4/49/3Dnest_face1.png)

The next four faces use [**transform-origin**](/css/properties/transform-origin) to pivot outward at right angles along each edge of the first face:

    .face:nth-of-type(2) {
        transform           : rotateY(-90deg);
        transform-origin    : left;
        background-position : 10px 10px, -20px -20px, -20px -20px,
                             -20px -20px, -20px -20px, 70px 70px;
    }
    .face:nth-of-type(3) {
        transform           : rotateY(90deg);
        transform-origin    : right;
        background-position : 10px 10px, 40px 40px, -20px -20px,
                             -20px -20px, -20px -20px, 70px 70px;
    }
    .face:nth-of-type(4) {
        transform           : rotateX(90deg);
        transform-origin    : top;
        background-position : 10px 10px, -20px -20px, 10px 70px,
                              70px 10px, -20px -20px, 70px 70px;
    }
    .face:nth-of-type(5) {
        transform           : rotateX(-90deg);
        transform-origin    : bottom;
        background-position : 10px 10px, -20px -20px, 10px 70px,
                              70px 10px, 40px 40px, 70px 70px;
    }

![3Dnest face5.png](//static.webplatformstaging.org/w/public/d/d9/3Dnest_face5.png)

Note that all the backfaces are visible, and only become hidden when other opaque boxes appear in front of them.

The sixth face simply uses **translateZ()** to drop it back to close off the cube:

    .face:nth-of-type(6) {
        transform           : translateZ(-100px);
        transform-origin    : center;
        background-position : 10px 10px, 10px 40px, 10px 70px,
                              70px 10px, 70px 40px, 70px 70px;
    }

![3Dnest face6.png](//static.webplatformstaging.org/w/public/b/b7/3Dnest_face6.png)

Applying different rotations to the *dice* element causes nested transform spaces to render relative to it, thus spinning the entire object. Here is how a script can control the spin:

    var diceStyle = document.querySelector('.dice').style;
    diceStyle.transform = 'rotateX(' + spin() + ') ' + 'rotateY(' +
           spin() + ') ' + 'rotateZ(' + spin() + ') ' ;
    // ...or diceStyle.WebkitTransform, diceStyle.MozTransform, etc.

    function spin() { return( Math.floor( Math.random() * 360 ) + 'deg') }

![3Dnest spin.png](//static.webplatformstaging.org/w/public/2/2e/3Dnest_spin.png)

Once such a complex 3D object takes up space, the effect of the [**scaleZ()**](/css/functions/scaleZ()) or [**scale3d()**](/css/functions/scale3d()) functions becomes apparent. An animated transition between **scale3d(0,0,0)** and **scale3d(1,1,1)** sizes the object in all three dimensions:

![scaleZ.png](//static.webplatformstaging.org/w/public/a/a1/scaleZ.png)

([View live sample](http://letmespellitoutforyou.com/samples/trans_3d_nest.html))

While there are limits to what you can accomplish when transforming flat web content, this technique of building 3D shapes such as cubes may form the basis of simple virtual reality scenes, such as the following (suitable for a mobile browser) that pans to view the surface of Mars:

![mars.png](//static.webplatformstaging.org/w/public/2/2a/mars.png)

View the sample to see how the viewer is positioned within the display elements:

([View sample here](http://letmespellitoutforyou.com/samples/trans_3d_virtual.html))

This example places an element randomly within a coordinate space, and rotates it to face the path to travel there. When viewed on WebKit nightly builds that support custom CSS filters, something amusing happens along the way. (As of this writing, Canary requires the *Enable CSS Shaders* flag enabled under **chrome://flags**)

![custom filter random path.png](//static.webplatformstaging.org/w/public/f/f7/custom_filter_random_path.png)

([View sample here](http://letmespellitoutforyou.com/samples/custom_path.html))