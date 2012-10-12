{{Page_Title|Drawing an Image onto a Canvas}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Cleanup, Compatibility Incomplete, Accessibility
}}
{{API_Name}}
{{Summary_Section}}
{{Concept_Page
|Content=We will start with a simple example and then explore some issues you might encounter. We'll look at how to load the image from various sources, how to display the image on "retina" displays without bluriness, and at some compatibility and performance problems.

==A simple example==
A simple html layout with both the image and the canvas already loaded as DOM elements in our page.
 
<syntaxhighlight lang="html5">
<!DOCTYPE html>
<html>
    <head>
        <title>Image drawing</title>
    </head>
    <body>
        <img id="w3c" src="http://www.w3.org/Icons/w3c_home.png" />
        <canvas></canvas>
    </body>
</html>
</syntaxhighlight>

Here is the javascript that will draw the image on to the canvas.

<syntaxhighlight lang="javascript">
// First we need to make sure that the image has loaded and that the DOM is ready.
window.addEventListener("DOMContentLoaded", function()
{
    var image  = document.getElementById("w3c");
    var canvas = document.getElementsByTagName('canvas')[0];

    canvas.width  = image.width;
    canvas.height = image.height;

    // Get the 2D drawing context
    var context = canvas.getContext("2d");

    // Now draw the logo onto the top-left corner of the canvas
    context.drawImage(image, 0, 0);
};
</syntaxhighlight>

==Loading the image programmatically==
While that is very simple, there is a flaw - we have to add the image to the DOM first. However, we can load an image directly from a URL with a few lines of javascript.

 <nowiki>
    function loadAndDrawImage(url)
    {
        // Create an image object. This is not attached to the DOM and is not part
        // of the page.
        var image = new Image();

        // When the image has loaded, draw it to the canvas
        image.onload = function()
        {
            drawImage(this);
        }

        // Now set the source of the image that we want to load
        image.src = url;
    }

    loadAndDrawImage("http://www.w3.org/html/logo/img/mark-word-icon.png");
</nowiki>

==Reading the Image from the File System==

In order to read an arbitrary file from the user's file system we have to let the user choose the file. We do this using a file select input. Let's add one to our HTML.

 <nowiki>
    <label for="fileChooser">Choose an image to display</label><input type="file" name="fileChooser" id="fileChooser" accept="image/jpeg">
</nowiki>

Then we have to detect when the user has chosen a file

 <nowiki>
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
</nowiki>

Now let’s turn this file’s content into a data URL that we can use as the source for our image. After the image has loaded, we don’t need the data URL any more and we will free the memory.

 <nowiki>
        // The URL API is vendor prefixed in Chrome
        window.URL = window.URL || window.webkitURL;

        // Create a data URL from the image file
        var imageURL = window.URL.createObjectURL(file);

        loadAndDrawImage(imageURL);
    }
</nowiki>


'''TODO:''' 

* draw scaled on Canvas (mention mobile Safari 2MB limit/issue - https://github.com/SunboX/ios-imagefile-megapixel)

=="Retina" Canvas==

As mentioned in the introduction, "Retina"-Displays will show blurry images by default. This is because of ...

* Explain "retina" Canvas drawing (http://html5-mobile.de/blog/retina-display-html-canvas-optimieren)
* Two types of retina Canvas, retina Canvas on iOS and on new MacBook Pro
* window.devicePixelRatio
* context.webkitBackingStorePixelRatio
* context.scale(2, 2)

==Alternatives==

* FileReader.readAsDataURL(file) instead of window.URL.createObject(file) - pros/cons

==Using WebWorker for Drawing?==

* Draw inside a Worker so the drawing doesn´t block User interactions

==Using WebGL for Drawing?==

* WebGL is a 2D API!
* How does it work? (context webgl, shader)
* pros/cons (contra: no easy way to modify image pixels)
* Link to WebGL Convolution Matrix, Extended ColorTransform Matrix "best practices"

==Browser Compatibility==

==Links to used Object, Function Docs==
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
[[Category:Concept Pages]]