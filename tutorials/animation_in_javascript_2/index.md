---
title: 'JavaScript animation'
notes:
  - 'Merge into another page, or create a separate tutorial'
readiness: 'Not Ready'
summary: 'Javascript can be used to create animation effects on a web page as simple as highlighting new content in yellow and then fading it back to normal, creating transitions, or moving elements on the page (think popup windows).  Creative use of techniques and tools such as common Javascript libraries allows us to create user interfaces that are unobtrusive and responsive to user behavior.  We begin by using JavaScript''s setInterval() function to create our own animations by manipulating DOM elements'' CSS properties to create effects.  Later, we illustrate the use of code libraries like jQuery to create more complex animations or create simple effects more easily than using by Javascript alone.'
tags:
  - CSS
  - JavaScript
  - UI
  - Merge_Candidate
  - Needs_Examples
uri: 'tutorials/animation in javascript 2'

---
## Summary

Javascript can be used to create animation effects on a web page as simple as highlighting new content in yellow and then fading it back to normal, creating transitions, or moving elements on the page (think popup windows). Creative use of techniques and tools such as common Javascript libraries allows us to create user interfaces that are unobtrusive and responsive to user behavior. We begin by using JavaScript's setInterval() function to create our own animations by manipulating DOM elements' CSS properties to create effects. Later, we illustrate the use of code libraries like jQuery to create more complex animations or create simple effects more easily than using by Javascript alone.

## Introduction

In this [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum) article, I will look at the art of creating animations using JavaScript — animation is often used to add to the user experience for people using browsers that support it. Common uses are: smoothly expanding and collapsing panels, progress bars, and visual feedback in forms.

As anyone who's seen a cartoon or a flickbook knows, animation is actually done in a series of small steps that, when viewed in quick succession, make it look like something is moving. Animation is a powerful technique; it's good at grabbing attention. Its weakness is that animations grab attention whether you want them to or not. Animated effects can make a web app feel like a more consistent experience, but they're like hot chili: don't add too many of them.

## A simple example: yellow fade technique

One common use of animation is the [Yellow fade technique](http://www.37signals.com/svn/archives/000558.php), where a changed area on a page is given a yellow background color which then fades back to the original color. It's a nice, unobtrusive way of drawing attention to the fact that something has changed without obstructing what the user is doing (e.g. indicate that more content has appeared, or provide form submission feedback). [Take a look at a yellow fade example](http://dev.opera.com/articles/view/javascript-animation/yft_pure_js.html) to see how it looks.

The principle behind the fade is that you set the background color of your fading element to be yellow and then, in a series of steps, set the element's color back to the original. For example, if a background's original color was red, the effect changes the color to yellow, then orangey-yellow, then orange, then reddish-orange, then red. The number of steps you take dictates how smooth the color change is, and the time between steps dictates how long the total color change takes.

In changing colors, we can take advantage of a useful CSS fact: a color can be defined as a triplet of ordinary numbers as well as a hexadecimal string. So `#FF0000` (red) can also be specified as `rgb(255,0,0)`. Changing from yellow to red in five steps, then, means going from `rgb(255,255,0)` (yellow) to `rgb(255,0,0)` in the following steps:

    rgb(255,255,0)
    rgb(255,192,0)
    rgb(255,128,0)
    rgb(255,64,0)
    rgb(255,0,0)

You set the background color of your element to `rgb(255,255,0)`, then after a period of time (say, 100 milliseconds), change the background color to `rgb(255,192,0)`, and then after 100ms set the color to `rgb(255,128,0)`, and so on:

|color|Time|
|:----|:---|
|rgb(255,255,0)||
|rgb(255,192,0)|100ms|
|rgb(255,128,0)|200ms|
|rgb(255,64,0)|300ms|
|rgb(255,0,0)|400ms|

The whole process takes 400ms (just under half a second), and there's a smooth fade between yellow and red. Conveniently here we're only changing one part of the color (the green channel; the three parts of an rgb color are the red, green, and blue channels), but changing more than one channel at once is perfectly possible. In this example, you're changing the green channel from 255 to 0 in four steps, which means changing it by 64 in each step.

Triggering an action after a certain period of time is done in JavaScript with the `setTimeout` and `setInterval` functions. The `setTimeout` function runs your action once after a certain time delay; `setInterval` runs the action over and over again, with each instance separated by the time delay; this is ideal for animation. In essence, then, the way to do this fade is to work out what each of the steps are and then use `setInterval` to call them, one after another. The `setInterval` function takes two parameters: a function to call as your action, and the time delay in milliseconds.

Obviously, you don't want to always change from yellow to red, so the function needs to be generic. If you know the start and end colors and the number of steps then it's a matter of mathematics to work out how much to change each color by in each step. If you define a `startcolor` array as a list of three numbers (`[255,255,0]`) and `endcolor` as a similar list (`[255,0,0]`), then the amount to change each color by in each step is:

    var red_change = (startcolor[0] - endcolor[0]) / steps;
    var green_change = (startcolor[1] - endcolor[1]) / steps;
    var blue_change = (startcolor[2] - endcolor[2]) / steps;

So, use `setInterval` to change the background color of the element in steps:

    var currentcolor = [255,255,0];
    var timer = setInterval(function(){
        currentcolor[0] = parseInt(currentcolor[0] - red_change);
        currentcolor[1] = parseInt(currentcolor[1] - green_change);
        currentcolor[2] = parseInt(currentcolor[2] - blue_change);
        element.style.backgroundColor = 'rgb(' + currentcolor.toString() + ')';
    }, 50);

In each step, take `currentcolor` and change the red channel by amount `red_change`, the green channel by amount `green_change`, and the blue channel by amount `blue_change`. Then, set the actual background color of the element to the new color: `[255,255,0].toString()` is "255,255,0", so to get the color `rgb(255,255,0)` we use `toString()` to create `rgb(255,255,0)` and set that as the background color of the element.

However, `setInterval` will call your action functon indefinitely; it won't stop when the destination color is reached. To stop an interval, use `clearInterval()`; the following code counts the number of times that the action has been called and clears the interval after the correct number of steps:

    var currentcolor = startcolor;
    var stepcount = 0;
    var timer = setInterval(function(){
        currentcolor[0] = parseInt(currentcolor[0] - red_change);
        currentcolor[1] = parseInt(currentcolor[1] - green_change);
        currentcolor[2] = parseInt(currentcolor[2] - blue_change);
        element.style.backgroundColor = 'rgb(' + currentcolor.toString() + ')';
        stepcount += 1;
        if (stepcount >= steps) {
            element.style.backgroundColor = 'rgb(' + endcolor.toString() + ')';
            clearInterval(timer);
        }
    }, 50);

And that's how you do animation: one step at a time.

How do `startcolor` and `endcolor` get set? One easy way is to wrap the above code up in a `fade` function:

    fade: function(element, startcolor, endcolor, time_elapsed) {
       ''...code from above...''
    }

and then you can trigger the yellow fade on an element with a function call like:

    fade(document.getElementById("yft"), [255,255,60], [0,0,255], 750);

or a "red fade", which sets the element to red and then fades to blue (the element's background color), like:

    fade(document.getElementById("yft"), [255,0,0], [0,0,255], 750);

This example changed the background color, but it could be anything that's changed: foreground color (for eye-pulsing 1960s psychedelic text effects), opacity (to make something fade out or fade in), position (to make an element move around the page), height and width (to grow an element, or shrink it down to nothing before it disappears).

## Animation with JavaScript libraries

Animation is a commonly used effect, and so most JavaScript libraries have some sort of support for it, including in-built support for common animations. For example, [jQuery](http://jquery.com/) has built-in support for making an element fade to transparent:

    $("#myelement").fadeOut();

and an `animate()` function for more complicated custom work:

    $("#block").animate({
        width: "70%",
    }, 1500 );

This is pretty intuitive - it will take the element and change the CSS `width` attribute, over 1500 milliseconds, from whatever it is now to 70% - the [animate function is documented here](http://docs.jquery.com/Effects).

[Prototype's scriptaculous framework](http://script.aculo.us/) offers similar facilities, such as `Effect.Fade('id_of_element')`, and many, many others. The [Yahoo UI library can also do similar effects](http://developer.yahoo.com/yui/3/animation/):

    new Y.Anim({ node: '#demo', to: { width: 70%, }}).run();

If you've already used a JavaScript library in your code, you'll already know that they offer much simpler animation facilities than managing animations yourself with `setInterval`. However, I think it is important to understand what is going on under the hood - it will make your scripting skills stronger in the long run. This is why I went through an example from first principles before getting into libraries.

You can find more resources about using the different JavaScript libraries at the dev.opera.com [Introduction to JavaScript toolkits](http://dev.opera.com/articles/view/introduction-to-javascript-toolkits/).

## A more complex example: moving and changing size

While the Yellow Fade Technique does demonstrate animation, it's a bit, well, boring. When most people think of animation they think of *movement*. Wile E. Coyote would have been way less amusing if all he ever did was change color.

A nice trick to alert the user to something that's happened without interrupting their workflow is a *non-modal message*. Instead of popping up an `alert()` dialog, which requires the user to click OK before they can carry on, simply put the message in a floating div on the page which unobtrusively stays there until they acknowledge it. A second rather nice thing, then, might be to allow the user to get back the message that they acknowledged to read it again. So, let's implement a floating message that, when clicked, "zooms" off to the corner of the screen, and then can be clicked on again to get it back. You can see a [brief demo of this "zooming message"](http://dev.opera.com/articles/view/javascript-animation/moving_messages_jq.html) to get the idea.

If you're doing any serious animation work, or any serious JavaScript work, it will almost always be worth using a JavaScript library. This will allow you to get on with providing the user experience that you want without having to worry about the nitty-gritty of the math required to run the animations. (You know *how* to do the math and how to use `setInterval` now, having read through the first example above, but you'll save time and brain-cells letting someone else do the heavy lifting for you.)

The above demo uses the [jQuery](http://jquery.com/) library to do the work, but as mentioned most libraries provide a fairly similar concept of animation and so you should be able to re-implement the principle using the library that you prefer. In essence, we want to do the following:

1.  Show a floating message centered on the screen
2.  When it's clicked on:
    1.  Move its horizontal position to the far right
    2.  Move its vertical position to the top
    3.  Change its width to 20px wide
    4.  Change its height to 20px high
    5.  Change its opacity to 20% so it's nearly transparent

3.  and hide the text in it
4.  When this "mini" version of the message is clicked, bring it back to the centre of the screen (ie, the opposite of what we did to shrink it)

and so the user gets a clear picture of what's happened to their message, the transition from full-sized message to mini-message should be animated (so they see that their message has "shrunk" into the corner of the window).

Performing the animation with jQuery is simple: just use the `.animate()` function and provide what you want the end result of the animation to be (and how long you want it to take):

    $(ourObject).animate({
        width: "20px", height: "20px", top: "20px",
        right: "20px", marginRight: "0px", opacity: "0.2"
      }, 300);

which will take `ourObject` and, over 300 milliseconds, change its width and height to 20px, its top and right positions to 20px, its `margin-right` style property to 0px, and its opacity (in browsers that support opacity) to 20%. It's then just a matter of programming in jQuery style to make this animation happen when the message is clicked:

    $(ourObject.click, function(){
      $(this).animate({
        width: "20px", height: "20px", top: "20px",
        right: "20px", marginRight: "0px", opacity: "0.2"
      }, 300)
    });

Restoring the message when clicked on again just requires another `.animate()` call:

    $(ourObject).animate({
        width: "400px", height: "75px", top: "50px",
        right: "50%", marginRight: "-200px", opacity: "0.9"
      }, 300);

and with a little bit of logic to dictate whether the message is currently showing or shrunk (so you know which animation to run), and some CSS to describe the initial style of the message (large, green, horizontally centred), that's all that's needed. A mere thirty lines of script. This is why libraries are a good idea!

## CSS Transitions

Finally, some (not all) animations can actually be set up without any JavaScript at all! Safari and other Webkit-based browsers, and the upcoming Firefox 3.1, can perform transitions from one CSS value to another smoothly without using any JavaScript. This code:

    div { opacity: 1; -webkit-transition: opacity 1s linear; }
    div:hover { opacity: 0; }

will make the `div` smoothly fade out over one second in a supporting browser when it is hovered over. These CSS transitions are very new, however, and are not supported in anything but the most up-to-date browsers, so if you want your animation to work for most of your public then you'll need to use DOM scripting to do it.

## Summary

This concludes our look at animating web page functionality using JavaScript - I've taken you through some animation examples created from first principles using the `setTimeout` and `setInterval` functions, and then looked at how you can use JavaScript libraries to create animations more quickly.

## Exercise questions

1.  What's the difference between `setTimeout` and `setInterval`?
2.  If `setInterval` didn't exist, how could you emulate it?
3.  How would you make an element fade from fully visible to fully invisible in 20 steps over the course of 1.5 seconds?
4.  How would you make an element fade from fully visible to fully invisible *and then back to visible again* in 20 steps over the course of 1.5 seconds?

## See also

### Related articles

#### Animation

-   [Web Animations API](/apis/web_animations)

-   [clone](/apis/web_animations/AnimationEffect/clone)

-   [AnimationNode](/apis/web_animations/AnimationNode)

-   [timing](/apis/web_animations/AnimationNode/timing)

-   [currentTime](/apis/web_animations/AnimationPlayer/currentTime)

-   [reverse](/apis/web_animations/AnimationPlayer/reverse)

-   [source](/apis/web_animations/AnimationPlayer/source)

-   [AnimationPlayerEvent](/apis/web_animations/AnimationPlayerEvent)

-   [currentTime](/apis/web_animations/AnimationTimeline/currentTime)

-   [play](/apis/web_animations/AnimationTimeline/play)

-   [@keyframes](/css/atrules/@keyframes)

-   [CSSKeyframeRule](/css/cssom/CSSKeyframeRule)

-   [keyText](/css/cssom/CSSKeyframeRule/keyText)

-   [style](/css/cssom/CSSKeyframeRule/style)

-   [CSSKeyframesRule](/css/cssom/CSSKeyframesRule)

-   [cssRules](/css/cssom/CSSKeyframesRule/cssRules)

-   [deleteRule](/css/cssom/CSSKeyframesRule/deleteRule)

-   [findRule](/css/cssom/CSSKeyframesRule/findRule)

-   [insertRule](/css/cssom/CSSKeyframesRule/insertRule)

-   [name](/css/cssom/CSSKeyframesRule/name)

-   [cubic-bezier](/css/functions/cubic-bezier)

-   [Animations](/css/properties/animations)

-   [transition](/css/properties/transition)

-   **JavaScript animation**

#### Background

-   [background](/css/cssom/properties/background)

-   [background](/css/properties/background)

-   [background-attachment](/css/properties/background-attachment)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-clip](/css/properties/background-clip)

-   [background-color](/css/properties/background-color)

-   [background-image](/css/properties/background-image)

-   [background-origin](/css/properties/background-origin)

-   [background-position](/css/properties/background-position)

-   [background-position-x](/css/properties/background-position-x)

-   [background-position-y](/css/properties/background-position-y)

-   [background-repeat](/css/properties/background-repeat)

-   [background-size](/css/properties/background-size)

-   **JavaScript animation**

#### CSS Attributes

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [background-position](/css/properties/background-position)

-   [break-before](/css/properties/break-before)

-   [height](/css/properties/height)

-   [list-style](/css/properties/list-style)

-   [list-style-position](/css/properties/list-style-position)

-   [text-overflow-ellipsis](/css/properties/text-overflow-ellipsis)

-   [text-overflow-mode](/css/properties/text-overflow-mode)

-   [text-rendering](/css/properties/text-rendering)

-   [user-select](/css/properties/user-select)

-   [equality](/css/selectors/attributes/equality)

-   [Attribute selector](/css/selectors/attributes/existence)

-   [hyphen](/css/selectors/attributes/hyphen)

-   [prefix](/css/selectors/attributes/prefix)

-   [substring](/css/selectors/attributes/substring)

-   [suffix](/css/selectors/attributes/suffix)

-   [baseline-shift](/svg/attributes/baseline-shift)

-   **JavaScript animation**

#### Responsive Web Design

-   [break-before](/css/properties/break-before)

-   [column-count](/css/properties/column-count)

-   **JavaScript animation**

#### Transforms

-   [inverse](/css/cssom/MSCSSMatrix/methods/inverse)

-   [multiply](/css/cssom/MSCSSMatrix/methods/multiply)

-   [rotate](/css/cssom/MSCSSMatrix/methods/rotate)

-   [rotate3d()](/css/functions/rotate3d())

-   [scale3d()](/css/functions/scale3d())

-   [skew()](/css/functions/skew())

-   [translate()](/css/functions/translate())

-   [translate3d()](/css/functions/translate3d())

-   [translateX()](/css/functions/translateX())

-   [translateY()](/css/functions/translateY())

-   [translateZ()](/css/functions/translateZ())

-   [backface-visibility](/css/properties/backface-visibility)

-   [transform-origin-z](/css/properties/transform-origin-z)

-   [MSCSSMatrix](/css/transforms/MSCSSMatrix)

-   [translate](/css/transforms/MSCSSMatrix/translate)

-   **JavaScript animation**

#### Transitions

-   [cubic-bezier](/css/functions/cubic-bezier)

-   [transition](/css/properties/transition)

-   [transition-delay](/css/properties/transition-delay)

-   [transition-duration](/css/properties/transition-duration)

-   [transition-property](/css/properties/transition-property)

-   **JavaScript animation**

#### Visual Effects

-   [color](/css/color)

-   [Colors by Hue](/css/color/colors_by_hue)

-   [Colors by Name](/css/color/colors_by_name)

-   [Colors by Saturation](/css/color/colors_by_saturation)

-   [User-Defined System Colors](/css/color/user-defined_system_colors)

-   [-ms-high-contrast](/css/high_contrast_mode/properties/-ms-high-contrast)

-   [ms-high-contrast-adjust](/css/high_contrast_modeapis/properties/ms-high-contrast-adjust)

-   [-ms-progress-appearance](/css/properties/-ms-progress-appearance)

-   [background-blend-mode](/css/properties/background-blend-mode)

-   [clip](/css/properties/clip)

-   [cursor](/css/properties/cursor)

-   [opacity](/css/properties/opacity)

-   [zoom](/css/properties/zoom)

-   [height](/html/attributes/height)

-   [blink](/html/elements/blink)

-   [filter](/svg/elements/filter)

-   **JavaScript animation**
