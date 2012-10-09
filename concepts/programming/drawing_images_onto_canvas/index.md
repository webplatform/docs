Drawing a Image on a Canvas seems to be a easy task. That´s true if you already have a Image Element (<img/>) to draw. If you want to load it from a URL first it´s getting a bit more difficult, because you have to listen for the image to be fully loaded. More difficult it will get, if your Image is on the local file system. There are different ways to get this done, this one will show the best practice.

If you finished your basic drawing and release it into the wild, you will recognise some problems. First one - so called “Retina”-Displays. All Images drawn on them will look blurry, but not if you know the “Tricks”. Second one will be performance issues. Cameras are getting more Mega-Pixel and Screens are getting bigger every year. People starting to load huge Images into your App. It´s good to know how to use not only CPU but also GPU Power to render and manipulate a Image.
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


'''TODO:''' Add Descriptions and sample Code

* handle file select (e.target.files)
* window.URL.createObject(file) - plus polyfill
* create Image Element and load Object URL
* window.URL.removeObjectURL(img.src) - cleanup memory on-image-load
* draw scaled on Canvas (mention mobile Safari 2MB limit/issue - https://github.com/SunboX/ios-imagefile-megapixel)
* delete Image Element

'''"Retina" Canvas'''

* Explain "retina" Canvas drawing (http://html5-mobile.de/blog/retina-display-html-canvas-optimieren)

'''Alternatives'''

* FileReader.readAsDataURL(file) instead of window.URL.createObject(file) - pros/cons

'''Using WebGL for drawing?'''

* WebGL is a 2D API!
* How does it work? (context 3d, shader)
* pros/cons (contra: no easy way to modify image pixels)
* Link to WebGL Convolution Matrix, Extended ColorTransform Matrix "best practices"

'''Browser Compatibility'''

'''Links to used Object, Function Docs'''