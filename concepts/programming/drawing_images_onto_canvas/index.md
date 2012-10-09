{{Page_Title|Drawing a large Image onto a Canvas}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Grammar/Spelling, Cleanup, Compatibility Incomplete, Accessibility
}}
{{API_Name}}
{{Summary_Section}}
{{Concept_Page
|Content=Drawing an Image on a Canvas seems to be an easy task. That´s true if you already have an Image Element (<img>) to draw. If you want to load it from a URL first it´s getting a bit more difficult, because you have to listen for the image to be fully loaded. More difficult it will get, if your Image is on the local file system. There are different ways to get it done, this one will show the best practice.

If you finished your basic drawing and released it into the wild, you will recognize some problems. First one - so called “Retina”-Displays. All Images drawn on them will look blurry, but not if you know the “Tricks”. Second one will be performance issues. Cameras are getting more Mega-Pixel and Screens are getting bigger every year. People starting to load huge Images into your App. It´s good to know how to use not only CPU but also GPU Power to render and manipulate a Image.
Last but not least there are device specific issues making Image Drawing even harder. Like the [http://stackoverflow.com/questions/12554947/mobile-safari-renders-img-src-dataimage-jpegbase64-scaled-on-canvas/ 2MB Image file down scaling bug] on iOS.

==Reading the Image from the File System==

First we need some simple HTML with a file select input field. We will give the input field an ID, so we could access it easily later on:

 <nowiki><!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <title>Image drawing Example</title>
</head>
<body>
    <input type="file" name="choosePicture" id="choosePicture" accept="image/jpeg">
</body>
</html></nowiki>

Now let´s get to the funny part, let´s write some JavaScript. First we need to listen to file select event and get a reference to the local file. But first we have to listen for the file select input field to be ready, this´s after the DOM content loaded event:

 <nowiki>document.addEventListener('DOMContentLoaded', function(){

    // get a reference to the file select input field
    var fileSelect = document.querySelector('#choosePicture');

    // listen for the onChange event that get´s fired after the user had choosed a file
    fileSelect.addEventListener('change', handleFileSelect, false);
    
}, false);

function handleFileSelect(e){

    // get the FileList object from the file select event
    var files = e.target.files;
    
    // check if there are files in the FileList
    if(files.length === 0){
        return;
    }
    
    // we just need one file and ignore the others
    var file = files[0];
    
    // make sure we got a image file
    if(file.type !== '' && !file.type.match('image.*')){
        return;
    }
    
    // let´s see what we got
    console.log(file);
}</nowiki>

Ok, you should see the file object in the console, after you select a new file.
Now lets turn this file´s content into a data URL we can load into a <img> Element. After the Image has loaded, we don´t need the data URL any more and we will free the memory. So we extend the code into this:

 <nowiki>document.addEventListener('DOMContentLoaded', function(){

    // get a reference to the file select input field
    var fileSelect = document.querySelector('#choosePicture');

    // listen for the onChange event that get´s fired after the user had choosed a file
    fileSelect.addEventListener('change', handleFileSelect, false);
    
}, false);

// vendor prefixed in Chrome
window.URL = window.webkitURL
|window_URL;

function handleFileSelect(e){

    // get the FileList object from the file select event
    var files=e.target.files;
    
    // check if there are files in the FileList
    if(files.length === 0){
        return;
    }
    
    // we just need one file and ignore the others
    var file = files[0];
    
    // make sure we got a image file
    if(file.type !== '' && !file.type.match('image.*')){
        return;
    }
    
    // create a data URL from the image file
    var imageData = window.URL.createObjectURL(file);
    
    // create a image element and load the data URL into it
    var img = document.createElement('img');
    document.body.appendChild(img);
    
    // we don´t want to see the image on the screen, so let´s move it out of view (we can´t just hide it!)
    img.style.position = 'absolute';
    img.style.left = '-9999px';
    
    // now listen for the onLoad event of the image before we can work on
    // you should use img.onload instead of img.addEventListener('load') because the eventListener fires to early in some Browsers!
    img.onload = function(){
        
        // free some memory by removing the data URL
        window.URL.revokeObjectURL(img.src);
      
        // create a Canvas and draw on it
        drawOnCanvas(img);
    };
    img.src = imageData;
}

function drawOnCanvas(img){
    
    // create a Canvas to draw on
    var canvas = document.createElement('canvas');
    document.body.appendChild(canvas);
  
    // get the drawing Context
    var context = canvas.getContext('2d');
    
    // set Canvas width/height to Image width/height
    canvas.width = img.naturalWidth;
    canvas.height = img.naturalHeight;
    
    // finally draw the Image on the Canvas
    context.drawImage(img, 0, 0, canvas.width, canvas.height);
    
    // remove the Image from the DOM, we don´t need it any more
    document.body.removeChild(img);
}</nowiki>


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
* How does it work? (context 3d, shader)
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