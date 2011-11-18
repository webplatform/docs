== Introduction ==
 
In this [http://www.w3.org/wiki/Web_Standards_Curriculum Web Standards Curriculum] article, I will look at the art of creating animations using JavaScript — animation is often used to add to the user experience, for people using browsers than can support it. Common uses are things such as smoothly expanding and collapsing panels, progress bars, and visual feedback in forms.
 
As anyone who's seen a cartoon or a flickbook knows, animation is actually done in lots of small steps that make it look like something is moving. Animation is a powerful technique; it's good at grabbing attention. The flaw here is that it grabs attention whether you want it to or not. Animated effects can make a web app feel like a more consistent experience, but it's like hot chilli: don't add too much of it.
 
== A simple example: yellow fade technique ==
 
One common use of animation is the [http://www.37signals.com/svn/archives/000558.php Yellow fade technique], where a changed area on a page is given a yellow background colour which then fades back to the background. It's a nice, unobtrusive way of highlighting that something has changed (eg more content has appeared, or some form feedback messages) without obstructing what the user is doing. [http://dev.opera.com/articles/view/javascript-animation/yft_pure_js.html Take a look at a yellow fade example] to see how it looks.
 
The principle behind the fade is that you set the background colour of your fading element to be yellow and then, in a series of steps, set it back to what it was originally. So if the original background colour was red, then the colour is set to yellow, then orangey-yellow, then orange, then reddish-orange, then red. The number of steps you take dictates how smooth the colour change is, and the time between steps dictates how long the total colour change takes. In changing colours, we can take advantage of a useful CSS fact: a colour can be defined as a triplet of ordinary numbers as well as a hexadecimal string. So <code>#FF0000</code> (red) can also be specified as <code>rgb(255,0,0)</code>. Changing from yellow to red in five steps, then, means going from <code>rgb(255,255,0)</code> (yellow) to <code>rgb(255,0,0)</code> in the following steps:

<pre>rgb(255,255,0)
rgb(255,192,0)
rgb(255,128,0)
rgb(255,64,0)
rgb(255,0,0)</pre>
 
You set the background colour of your element to <code>rgb(255,255,0)</code>, then after a period of time (say, 100 milliseconds), change the background colour to <code>rgb(255,192,0)</code>, and then after 100ms set the colour to <code>rgb(255,128,0)</code>, and so on:
              
{| border="1"
|-
!Colour
!Time
|-
|rgb(255,255,0)
| 
|-
|rgb(255,192,0)
|100ms
|-
|rgb(255,128,0)
|200ms
|-
|rgb(255,64,0)
|300ms
|-
|rgb(255,0,0)
|400ms
|} 

The whole process takes 400ms (just under half a second), and there's a smooth fade between yellow and red. Conveniently here we're only changing one part of the colour (the green channel; the three parts of an rgb colour are the red, green, and blue channels), but changing more than one channel at once is perfectly possible. In this example, you're changing the green channel from 255 to 0 in four steps, which means changing it by 64 in each step.
 
Triggering an action after a certain period of time is done in JavaScript with the <code>setTimeout</code> and <code>setInterval</code> functions. The <code>setTimeout</code> function runs your action once after a certain time delay; <code>setInterval</code> runs the action over and over again, with each instance separated by the time delay; this is ideal for animation. In essence, then, the way to do this fade is to work out what each of the steps are and then use <code>setInterval</code> to call them, one after another. The <code>setInterval</code> function takes two parameters: a function to call as your action, and the time delay in milliseconds.

Obviously, you don't want to always change from yellow to red, so the function needs to be generic. If you know the start and end colours and the number of steps then it's a matter of mathematics to work out how much to change each colour by in each step. If you define a <code>startcolour</code> array as a list of three numbers (<code>[255,255,0]</code>) and <code>endcolour</code> as a similar list (<code>[255,0,0]</code>), then the amount to change each colour by in each step is:
 
<pre>var red_change = (startcolour[0] - endcolour[0]) / steps;
var green_change = (startcolour[1] - endcolour[1]) / steps;
var blue_change = (startcolour[2] - endcolour[2]) / steps;</pre>
 
So, use <code>setInterval</code> to change the background colour of the element in steps:
 
<pre>var currentcolour = [255,255,0];
var timer = setInterval(function(){
    currentcolour[0] = parseInt(currentcolour[0] - red_change);
    currentcolour[1] = parseInt(currentcolour[1] - green_change);
    currentcolour[2] = parseInt(currentcolour[2] - blue_change);
    element.style.backgroundColor = 'rgb(' + currentcolour.toString() + ')';
}, 50);</pre>
 
In each step, take <code>currentcolour</code> and change the red channel by amount <code>red_change</code>, the green channel by amount <code>green_change</code>, and the blue channel by amount <code>blue_change</code>. Then, set the actual background colour of the element to the new colour: <code>[255,255,0].toString()</code> is "255,255,0", so to get the colour <code>rgb(255,255,0)</code> we use <code>toString()</code> to create <code>rgb(255,255,0)</code> and set that as the background colour of the element.

However, <code>setInterval</code> will call your action functon indefinitely; it won't stop when the destination colour is reached. To stop an interval, use <code>clearInterval()</code>; the following code counts the number of times that the action has been called and clears the interval after the correct number of steps:
 
<pre>var currentcolour = startcolour;
var stepcount = 0;
var timer = setInterval(function(){
    currentcolour[0] = parseInt(currentcolour[0] - red_change);
    currentcolour[1] = parseInt(currentcolour[1] - green_change);
    currentcolour[2] = parseInt(currentcolour[2] - blue_change);
    element.style.backgroundColor = 'rgb(' + currentcolour.toString() + ')';
    stepcount += 1;
    if (stepcount &gt;= steps) {
        element.style.backgroundColor = 'rgb(' + endcolour.toString() + ')';
        clearInterval(timer);
    }
}, 50);</pre>
 
And that's how you do animation: one step at a time.

How do <code>startcolour</code> and <code>endcolour</code> get set? One easy way is to wrap the above code up in a <code>fade</code> function:
 
<pre>fade: function(element, startcolour, endcolour, time_elapsed) {
   ''...code from above...''
}</pre>
 
and then you can trigger the yellow fade on an element with a function call like:

<pre>fade(document.getElementById("yft"), [255,255,60], [0,0,255], 750);</pre>
 
or a "red fade", which sets the element to red and then fades to blue (the element's background colour), like:

<pre>fade(document.getElementById("yft"), [255,0,0], [0,0,255], 750);</pre>
 
This example changed the background colour, but it could be anything that's changed: foreground colour (for eye-pulsing 1960s psychedelic text effects), opacity (to make something fade out or fade in), position (to make an element move around the page), height and width (to grow an element, or shrink it down to nothing before it disappears).

== Animation with JavaScript libraries ==
 
Animation is a commonly used effect, and so most JavaScript libraries have some sort of support for it, including in-built support for common animations. For example, [http://jquery.com/ jQuery] has built-in support for making an element fade to transparent:
 
<pre>$("#myelement").fadeOut();</pre>
 
and an <code>animate()</code> function for more complicated custom work:

<pre>$("#block").animate({ 
    width: "70%",
}, 1500 );</pre>
 
This is pretty intuitive - it will take the element and change the CSS <code>width</code> attribute, over 1500 milliseconds, from whatever it is now to 70% - the [http://docs.jquery.com/Effects animate function is documented here].

[http://script.aculo.us/ Prototype's scriptaculous framework] offers similar facilities, such as <code>Effect.Fade('id_of_element')</code>, and many, many others. The [http://developer.yahoo.com/yui/3/animation/ Yahoo UI library can also do similar effects]:
 
<pre>new Y.Anim({ node: '#demo', to: { width: 70%, }}).run();</pre>
 
If you've already used a JavaScript library in your code, you'll already know that they offer much simpler animation facilities than managing animations yourself with <code>setInterval</code>. However, I think it is important to understand what is going on under the hood - it will make your scripting skills stronger in the long run. This is why I went through an example from first principles before getting into libraries.

You can find more resources about using the different JavaScript libraries at the dev.opera.com [http://dev.opera.com/articles/view/introduction-to-javascript-toolkits/ Introduction to JavaScript toolkits].

== A more complex example: moving and changing size ==
 
While the Yellow Fade Technique does demonstrate animation, it's a bit, well, boring. When most people think of animation they think of ''movement''. Wile E. Coyote would have been way less amusing if all he ever did was change colour.
 
A nice trick to alert the user to something that's happened without interrupting their workflow is a ''non-modal message''. Instead of popping up an <code>alert()</code> dialog, which requires the user to click OK before they can carry on, simply put the message in a floating div on the page which unobtrusively stays there until they acknowledge it. A second rather nice thing, then, might be to allow the user to get back the message that they acknowledged to read it again. So, let's implement a floating message that, when clicked, "zooms" off to the corner of the screen, and then can be clicked on again to get it back. You can see a [http://dev.opera.com/articles/view/javascript-animation/moving_messages_jq.html brief demo of this "zooming message"] to get the idea.
 
If you're doing any serious animation work, or any serious JavaScript work, it will almost always be worth using a JavaScript library. This will allow you to get on with providing the user experience that you want without having to worry about the nitty-gritty of the math required to run the animations. (You know ''how'' to do the math and how to use <code>setInterval</code> now, having read through the first example above, but you'll save time and brain-cells letting someone else do the heavy lifting for you.)
 
The above demo uses the [http://jquery.com/ jQuery] library to do the work, but as mentioned most libraries provide a fairly similar concept of animation and so you should be able to re-implement the principle using the library that you prefer. In essence, we want to do the following:
 
# Show a floating message centered on the screen
# When it's clicked on:
## Move its horizontal position to the far right
## Move its vertical position to the top
## Change its width to 20px wide
## Change its height to 20px high
## Change its opacity to 20% so it's nearly transparent
# and hide the text in it
# When this "mini" version of the message is clicked, bring it back to the centre of the screen (ie, the opposite of what we did to shrink it)
 
and so the user gets a clear picture of what's happened to their message, the transition from full-sized message to mini-message should be animated (so they see that their message has "shrunk" into the corner of the window).
 
Performing the animation with jQuery is simple: just use the <code>.animate()</code> function and provide what you want the end result of the animation to be (and how long you want it to take):
 
<pre>$(ourObject).animate({
    width: "20px", height: "20px", top: "20px",
    right: "20px", marginRight: "0px", opacity: "0.2"
  }, 300);</pre>
 
which will take <code>ourObject</code> and, over 300 milliseconds, change its width and height to 20px, its top and right positions to 20px, its <code>margin-right</code> style property to 0px, and its opacity (in browsers that support opacity) to 20%. It's then just a matter of programming in jQuery style to make this animation happen when the message is clicked:

<pre>$(ourObject.click, function(){
  $(this).animate({
    width: "20px", height: "20px", top: "20px",
    right: "20px", marginRight: "0px", opacity: "0.2"
  }, 300)
});</pre>
 
Restoring the message when clicked on again just requires another <code>.animate()</code> call:

<pre>$(ourObject).animate({
    width: "400px", height: "75px", top: "50px",
    right: "50%", marginRight: "-200px", opacity: "0.9"
  }, 300);</pre>
 
and with a little bit of logic to dictate whether the message is currently showing or shrunk (so you know which animation to run), and some CSS to describe the initial style of the message (large, green, horizontally centred), that's all that's needed. A mere thirty lines of script. This is why libraries are a good idea!

== CSS Transitions ==
 
Finally, some (not all) animations can actually be set up without any JavaScript at all! Safari and other Webkit-based browsers, and the upcoming Firefox 3.1, can perform transitions from one CSS value to another smoothly without using any JavaScript. This code:
 
<pre>div { opacity: 1; -webkit-transition: opacity 1s linear; }
div:hover { opacity: 0; }</pre>
 
will make the <code>div</code> smoothly fade out over one second in a supporting browser when it is hovered over. These CSS transitions are very new, however, and are not supported in anything but the most up-to-date browsers, so if you want your animation to work for most of your public then you'll need to use DOM scripting to do it.

== Summary ==
 
This concludes our look at animating web page functionality using JavaScript - I've taken you through some animation examples created from first principles using the <code>setTimeout</code> and <code>setInterval</code> functions, and then looked at how you can use JavaScript libraries to create animations more quickly.

== Exercise questions ==
 
# What's the difference between <code>setTimeout</code> and <code>setInterval</code>?
# If <code>setInterval</code> didn't exist, how could you emulate it?
# How would you make an element fade from fully visible to fully invisible in 20 steps over the course of 1.5 seconds?
# How would you make an element fade from fully visible to fully invisible ''and then back to visible again'' in 20 steps over the course of 1.5 seconds?
 
Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [http://dev.opera.com/articles/view/javascript-animation/ 50: JavaScript animation], written by Stuart Langridge. Like the original, it is published under the [http://creativecommons.org/licenses/by-nc-sa/2.5/ Creative Commons Attribution, Non Commercial - Share Alike 2.5] license.

[[Category:Tutorials]]
[[Category:WSC]]