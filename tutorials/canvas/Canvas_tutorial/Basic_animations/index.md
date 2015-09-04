---
title: Basic animations
tags:
  - Tutorials
readiness: 'Ready to Use'
summary: 'Timing and movement of shapes are explained in this part of the canvas tutorial. There''s a list of useful external examples at the end of the document.'
uri: 'tutorials/canvas/Canvas tutorial/Basic animations'

---
# Basic animations

## Summary

Timing and movement of shapes are explained in this part of the canvas tutorial. There's a list of useful external examples at the end of the document.

Since we're using script to control `canvas` elements it's also very easy to make (interactive) animations. Unfortunately the canvas element was never designed to be used in this way (unlike Flash) so there are limitations.

Probably the biggest limitation is that once a shape gets drawn it stays that way. If we need to move it we have to redraw it and everything that was drawn before it. It takes a lot of time to redraw complex frames and the performance depends highly on the speed of the computer it's running on.

## Basic animation steps

These are the steps you need to take to draw a frame:

1.  **Clear the canvas**
     Unless the shapes you'll be drawing fill the complete canvas (for instance a backdrop image), you need to clear any shapes that have been drawn previously. The easiest way to do this is using the `clearRect` method.
2.  **Save the canvas state**
     If you're changing any setting (styles, transformations, etc) which affect the canvas state and want to make sure the original state is used each time a frame is drawn, you need to save it.
3.  **Draw animated shapes**
     The step where you do the actual frame rendering.
4.  **Restore the canvas state**
     If you've saved the state, restore it before drawing a new frame.

## Controlling an animation

Shapes are drawn to the canvas by using the canvas methods directly or calling custom functions. In normal circumstances we only see these results appear on the canvas when the script finishes execution. For instance it isn't possible to do an animation from within a `for` loop.

We need a way to execute our drawing functions over a period of time. There are two ways to control an animation like this. First there's the `setInterval` and `setTimeout` functions which can be used to call a specific function over a set period of time (although [/en/DOM/window.requestAnimationFrame requestAnimationFrame] is recommended for these cases).

    setInterval(animateShape,500);
    setTimeout(animateShape,500);

If you don't want any user interaction it's best to use the `setInterval` function which repeatedly executes the supplied code. In the example above the `animateShape` function is executed every 500 miliseconds (half a second). The `setTimeout` function only executes once after the set amount of time.

The second method we can use to control an animation is user input. If we wanted to make a game we could use keyboard or mouse events to control the animation. By setting eventListeners we catch any user interaction and execute our animation functions.

In the examples below I'm using the first method to control the animation. At the bottom of this page are some links to examples which use the second.

#### An animation example 1

In this example I'm going to animate a mini simulation of our solar system.

![A dark universe with a planet orbiting around a sun](/assets/public/e/ea/Canvas_animation1.png)

    var sun = new Image();
    var moon = new Image();
    var earth = new Image();
    function init(){
      sun.src = 'images/sun.png';
      moon.src = 'images/moon.png';
      earth.src = 'images/earth.png';
      setInterval(draw,100);
    }

    function draw() {
      var ctx = document.getElementById('canvas').getContext('2d');

      ctx.globalCompositeOperation = 'destination-over';
      ctx.clearRect(0,0,300,300); // clear canvas

      ctx.fillStyle = 'rgba(0,0,0,0.4)';
      ctx.strokeStyle = 'rgba(0,153,255,0.4)';
      ctx.save();
      ctx.translate(150,150);

      // Earth
      var time = new Date();
      ctx.rotate( ((2*Math.PI)/60)*time.getSeconds() + ((2*Math.PI)/60000)*time.getMilliseconds() );
      ctx.translate(105,0);
      ctx.fillRect(0,-12,50,24); // Shadow
      ctx.drawImage(earth,-12,-12);

      // Moon
      ctx.save();
      ctx.rotate( ((2*Math.PI)/6)*time.getSeconds() + ((2*Math.PI)/6000)*time.getMilliseconds() );
      ctx.translate(0,28.5);
      ctx.drawImage(moon,-3.5,-3.5);
      ctx.restore();

      ctx.restore();

      ctx.beginPath();
      ctx.arc(150,150,105,0,Math.PI*2,false); // Earth orbit
      ctx.stroke();

      ctx.drawImage(sun,0,0,300,300);
    }

#### An animation example 2

![An analog clock with hour, minute, and second hands](/assets/public/a/a3/Canvas_animation2.png)

    function init(){
      clock();
      setInterval(clock,1000);
    }
    function clock(){
      var now = new Date();
      var ctx = document.getElementById('canvas').getContext('2d');
      ctx.save();
      ctx.clearRect(0,0,150,150);
      ctx.translate(75,75);
      ctx.scale(0.4,0.4);
      ctx.rotate(-Math.PI/2);
      ctx.strokeStyle = "black";
      ctx.fillStyle = "white";
      ctx.lineWidth = 8;
      ctx.lineCap = "round";

      // Hour marks
      ctx.save();
      for (var i=0;i<12;i++){
        ctx.beginPath();
        ctx.rotate(Math.PI/6);
        ctx.moveTo(100,0);
        ctx.lineTo(120,0);
        ctx.stroke();
      }
      ctx.restore();

      // Minute marks
      ctx.save();
      ctx.lineWidth = 5;
      for (i=0;i<60;i++){
        if (i%5!=0) {
          ctx.beginPath();
          ctx.moveTo(117,0);
          ctx.lineTo(120,0);
          ctx.stroke();
        }
        ctx.rotate(Math.PI/30);
      }
      ctx.restore();

      var sec = now.getSeconds();
      var min = now.getMinutes();
      var hr  = now.getHours();
      hr = hr>=12 ? hr-12 : hr;

      ctx.fillStyle = "black";

      // write Hours
      ctx.save();
      ctx.rotate( hr*(Math.PI/6) + (Math.PI/360)*min + (Math.PI/21600)*sec )
      ctx.lineWidth = 14;
      ctx.beginPath();
      ctx.moveTo(-20,0);
      ctx.lineTo(80,0);
      ctx.stroke();
      ctx.restore();

      // write Minutes
      ctx.save();
      ctx.rotate( (Math.PI/30)*min + (Math.PI/1800)*sec )
      ctx.lineWidth = 10;
      ctx.beginPath();
      ctx.moveTo(-28,0);
      ctx.lineTo(112,0);
      ctx.stroke();
      ctx.restore();

      // Write seconds
      ctx.save();
      ctx.rotate(sec * Math.PI/30);
      ctx.strokeStyle = "#D40000";
      ctx.fillStyle = "#D40000";
      ctx.lineWidth = 6;
      ctx.beginPath();
      ctx.moveTo(-30,0);
      ctx.lineTo(83,0);
      ctx.stroke();
      ctx.beginPath();
      ctx.arc(0,0,10,0,Math.PI*2,true);
      ctx.fill();
      ctx.beginPath();
      ctx.arc(95,0,10,0,Math.PI*2,true);
      ctx.stroke();
      ctx.fillStyle = "#555";
      ctx.arc(0,0,3,0,Math.PI*2,true);
      ctx.fill();
      ctx.restore();

      ctx.beginPath();
      ctx.lineWidth = 14;
      ctx.strokeStyle = '#325FA2';
      ctx.arc(0,0,142,0,Math.PI*2,true);
      ctx.stroke();

      ctx.restore();
    }

#### An animation example 3

This is the code for a left-to-right looping panoramic image scroller. Make sure the image is larger than the canvas.
 Using this file for this example
[http://commons.wikimedia.org/wiki/File:Capitan\_Meadows,\_Yosemite\_National\_Park.jpg](http://commons.wikimedia.org/wiki/File:Capitan_Meadows,_Yosemite_National_Park.jpg)

    var img = new Image();

    //User Variables
    img.src = 'Capitan_Meadows,_Yosemite_National_Park.jpg';
    var CanvasXSize = 800;
    var CanvasYSize = 200;
    var speed = 30; //lower is faster
    var scale = 1.05;
    var y = -4.5; //vertical offset
    //End User Variables

    var dx = 0.75;
    var imgW = img.width*scale;
    var imgH = img.height*scale;
    var x = 0;
    if (imgW > CanvasXSize) { x = CanvasXSize-imgW; } // image larger than canvas
    var clearX;
    var clearY;
    if (imgW > CanvasXSize) { clearX = imgW; } // image larger than canvas
    else { clearX = CanvasXSize; }
    if (imgH > CanvasYSize) { clearY = imgH; } // image larger than canvas
    else { clearY = CanvasYSize; }
    var ctx;

    function init() {
       //Get Canvas Element
       ctx = document.getElementById('canvas').getContext('2d');
       //Set Refresh Rate
       return setInterval(draw, speed);
    }

    function draw() {
       //Clear Canvas
       ctx.clearRect(0,0,clearX,clearY);
       //If image is <= Canvas Size
       if (imgW <= CanvasXSize) {
          //reset, start from beginning
          if (x > (CanvasXSize)) { x = 0; }
          //draw aditional image
          if (x > (CanvasXSize-imgW)) { ctx.drawImage(img,x-CanvasXSize+1,y,imgW,imgH); }
       }
       //If image is > Canvas Size
       else {
          //reset, start from beginning
          if (x > (CanvasXSize)) { x = CanvasXSize-imgW; }
          //draw aditional image
          if (x > (CanvasXSize-imgW)) { ctx.drawImage(img,x-imgW+1,y,imgW,imgH); }
       }
       //draw image
       ctx.drawImage(img,x,y,imgW,imgH);
       //amount to move
       x += dx;
    }

html code. Canvas width and height should match the CanvasXSize, CanvasYSize.

    <body onload="init();">
    <canvas id="canvas" width="800" height="200"></canvas>

## Other examples

-   [Gartic](http://www.gartic.net/)
     Multi-player drawing game
-   [Canvascape
    ](http://www.abrahamjoffe.com.au/ben/canvascape/)A 3D adventure game (first-person shooter).
-   [Freeciv.net](http://www.freeciv.net/)
     A multiplayer strategy game with isometric graphics, created using HTML5 canvas.
-   [https://developer.mozilla.org/en/A\_Basic\_RayCaster](https://developer.mozilla.org/en/A_Basic_RayCaster) A Basic RavCaster]
     A good example of how to do animations using keyboard controls.
-   [canvas adventure](http://andrewwooldridge.com/canvas/canvasgame001/canvasgame002.html)
     Also a nice example that uses keyboard controls.
-   [An interactive Blob](http://www.blobsallad.se/)
     Have fun with the blob.
-   [Flying through a starfield](http://arapehlivanian.com/wp-content/uploads/2007/02/canvas.html)
     Fly through stars, circles or squares.
-   [iGrapher](http://igrapher.com/)
     An example of charting stock market data.

[\<\<Previous](/tutorials/canvas/Canvas_tutorial/Compositing)

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/Canvas_tutorial/Basic_animations)

