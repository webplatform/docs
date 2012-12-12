{{Page_Title|WebGL: a simple shader}}
{{Flags}}
{{Byline
|Name=Erik Möller
|Published=June 27, 2012
}}
{{Summary_Section|This article explains how to create a simple shader, building on the example created in the [tutorials/getting started with webgl | getting started with WebGL] article.}}
{{Tutorial
|Content===Introduction==

In the last part of this article series — [http://dev.opera.com/articles/view/raw-webgl-part1-getting-started/ Raw WebGL 101 — Part 1: getting started], we introduced you to the world of writing raw WebGL (look ma, no libraries). We got you set up and showed you how to create a couple of very basic examples along with some simple error handling, and we explained basic concepts such as the WebGL rendering pipeline.

In this article, we will carry on where we left off, going further with the same example file and building up a simple shader. This article is a transcript of [http://www.youtube.com/watch?v=me3BviH3nZc&t=22m26s time 22:26 to 32.36] in Erik Möller's [http://www.youtube.com/watch?v=me3BviH3nZc WebGL 101] tutorial, available on YouTube.

==Making a rectangle out of our triangle==

To build up this example step by step, start with the [minimal-draw.zip Minimal draw code] from the last article and follow the steps below. You can also [02-minimal-draw.html view the minimal draw example] to see what the code so far does, and [03-minimal-shader.html view the minimal shader example] to see what the end result from this tutorial will be.

First of all, make a copy of the 02-minimal-draw.html file, and save it as 03-minimal-shader.html (or something else of your choosing). In this tutorial we are going to forget about triangles, and instead draw a rectangle that will cover the canvas. To show what we will draw, replace the ascii triangle we currently have in our code with a square, like this:

 <nowiki>/* 
 2 ___ 3
  {{!}}\  {{!}}
  {{!}} \ {{!}}
 0{{!}}__\{{!}}1
 
 */
</nowiki>

and put it into your <code>webgl-utils.js</code> file, at the bottom, wrapped in a function called <code>screenQuad() { ... }</code>. At the bottom of this function, return <code>vertexPosBuffer</code>, like this:

 <code>return vertexPosBuffer;</code>

Where the quad generation code once sat once sat in your main code, put the following line to reference it:

 <code>var vertexPosBuffer = screenQuad();</code>

==Summary==

That's it for now. Check back again soon for more articles.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=DevOpera
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}