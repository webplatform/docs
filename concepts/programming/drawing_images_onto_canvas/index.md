---
title: 'Drawing an Image onto a Canvas'
readiness: 'Not Ready'
summary: "In this article we will explore how to draw Images onto a Canvas. \n"
tags:
  - Concept_Pages
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - DOM
uri: 'concepts/programming/drawing images onto canvas'

---
## Summary

In this article we will explore how to draw Images onto a Canvas.

We will start with a simple example and then explore some issues you might encounter. We'll look at how to load the image from various sources, how to display the image on "retina" displays without bluriness, and at some compatibility and performance problems.

## A simple example

A simple html layout with both the image and the canvas already loaded as DOM elements in our page.

``` html
<!DOCTYPE html>
<html>
    <head>
        <title>Image drawing</title>
        <script type="text/javascript" src="draw.js"></script>
    </head>
    <body>
        <img id="html5" src="http://www.w3.org/html/logo/img/mark-word-icon.png" />
    </body>
</html>
```

 Here is the javascript that will draw the image on to the canvas.

``` js
/** draw.js **/

window.addEventListener("DOMContentLoaded", function()
{
    var image  = document.getElementById("html5");
    var canvas = document.createElement("canvas");
    document.body.appendChild(canvas);

    canvas.width  = image.width;
    canvas.height = image.height;

    var context = canvas.getContext("2d");

    context.drawImage(image, 0, 0);
});
```

## The drawImage function

The function we use for drawing an image onto a canvas is the *drawImage()* function. This function draws an image, canvas, or video onto the canvas. It can also draw parts of an image, and/or increase/reduce the image size.

Position the image on the canvas:

``` js
context.drawImage(img,x,y);
```

 Position the image on the canvas, and specify width and height of the image:

``` js
context.drawImage(img,x,y,width,height);
```

 Clip the image and position the clipped part on the canvas:

``` js
context.drawImage(img,sx,sy,swidth,sheight,x,y,width,height);
```

|Parameter|Required|Description|
|:--------|:-------|:----------|
|img|\*|Specifies the image, canvas, or video element to use|
|sx| |The x coordinate where to start clipping|
|sy| |The y coordinate where to start clipping|
|swidth| |The width of the clipped image|
|sheight| |The height of the clipped image|
|x|\*|The x coordinate where to place the image on the canvas|
|y|\*|The y coordinate where to place the image on the canvas|
|width| |The width of the image to use (stretch or reduce the image)|
|height| |The height of the image to use (stretch or reduce the image)|

## Loading the image programmatically

If the image we want to draw is not in the [DOM](/w/index.php?title=DOM&action=edit&redlink=1) already (we might not even want to add it), we can load an image directly from a URL with a few lines of javascript.

``` js
function loadAndDrawImage(url)
{
    // Create an image object. This is not attached to the DOM and is not part of the page.
    var image = new Image();

    // When the image has loaded, draw it to the canvas
    image.onload = function()
    {
        // draw image...
    }

    // Now set the source of the image that we want to load
    image.src = url;
}
loadAndDrawImage("http://www.w3.org/html/logo/img/mark-word-icon.png");
```

## Reading the Image from the File System

In order to read an arbitrary file from the user's file system we have to let the user choose the file. We do this using a file select input. Let's add one to our HTML.

        <label for="fileChooser">Choose an image to display</label><input type="file" name="fileChooser" id="fileChooser" accept="image/jpeg">

Then we have to detect when the user has chosen a file

        // Get a reference to the file select input field
        var fileChooser = document.getElementById('fileChooser');

        // When a selection is made the "change" event will be fired
        fileChooser.addEventListener('change', handleFileSelect, false);

        function handleFileSelect(event)
        {
            // Get the FileList object from the file select event
            var files = event.target.files;

            // Check if there are files in the FileList
            if(files.length === 0)
            {
                return;
            }

            // For this example we only want one image. We'll take the first.
            var file = files[0];

            // Check that the file is an image
            if(file.type !== '' && !file.type.match('image.*'))
            {
                return;
            }

Now let’s turn this file’s content into a data URL that we can use as the source for our image. After the image has loaded, we don’t need the data URL any more and we will free the memory.

            // The URL API is vendor prefixed in Chrome
            window.URL = window.URL || window.webkitURL;

            // Create a data URL from the image file
            var imageURL = window.URL.createObjectURL(file);

            loadAndDrawImage(imageURL);
        }

**TODO:**

-   draw scaled on Canvas (mention mobile Safari 2MB limit/issue - <https://github.com/SunboX/ios-imagefile-megapixel>)

## "Retina" Canvas

As mentioned in the introduction, "Retina"-Displays will show blurry images by default. This is because of ...

-   Explain "retina" Canvas drawing (<http://html5-mobile.de/blog/retina-display-html-canvas-optimieren>)
-   Two types of retina Canvas, retina Canvas on iOS and on new MacBook Pro
-   window.devicePixelRatio
-   context.webkitBackingStorePixelRatio
-   context.scale(2, 2)

## Alternatives

-   FileReader.readAsDataURL(file) instead of window.URL.createObject(file) - pros/cons

## Using WebWorker for Drawing?

-   Draw inside a Worker so the drawing doesn´t block User interactions

**Comment:** *Is this even possible considering that we cannot pass dom elements to a worker? I've tried this and I get exceptions. We should mention web workers since they can do work for a canvas, but not drawing work I'm afraid. Or...?*

**Comment:** *You are right. We cant draw onto a canvas using a worker. But we should mention, that workers can be used to manipulate the pixel data of a canvas. We can pass the pixel data to a worker, do some work with it and pass it back*

## Using WebGL for Drawing?

-   WebGL is a 2D API!
-   How does it work? (context webgl, shader)
-   pros/cons (contra: no easy way to modify image pixels)
-   Link to WebGL Convolution Matrix, Extended ColorTransform Matrix "best practices"

## Browser Compatibility

## Links to used Object, Function Docs

