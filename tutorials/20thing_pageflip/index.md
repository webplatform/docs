{{Page_Title|Building the page flip effect from 20thingsilearned.com}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Hakim El Hattab
|URL=http://www.html5rocks.com/profiles/#hakimelhattab
}}
{{Summary_Section|A case study showing basic implementation of a page-flipping effect.}}
{{Tutorial
|Content===Introduction==

In 2010, [http://www.f-i.com F-i.com] and the Google Chrome team collaborated on an HTML5-based educational web app called 20 Things I Learned about Browsers and the Web ([http://www.20thingsilearned.com www.20thingsilearned.com]). One of the key ideas behind this project was that it would best be presented in the [http://chrome.blogspot.com/2010/11/curious-guide-to-browsers-and-web.html context of a book]. Since the book is very much about open web technologies we felt it was important to stay true to that by making the container itself an example of what these technologies allow us to accomplish today.

[[Image:pf01.jpg|Book cover and homepage of '20 Things I Learned About Browsers and the Web']]<br/>
''Book cover and homepage of "20 Things I Learned About Browsers and the Web" ([http://www.20thingsilearned.com www.20thingsilearned.com])''

We decided that the best way to achieve the feeling of a real world book is to simulate the good parts of the analogue reading experience while still leveraging the benefits of the digital realm in areas such as navigation. A lot of effort went into the graphical and interactive treatment of the reading flow &mdash; especially how the pages of the books flip from one page to another.

==Getting Started==

This tutorial will take you through the process of creating your own page flip effect using the canvas element and plenty of JavaScript. Some of the rudimentary code, such as variable declarations and event listener subscription, has been left out of the snippets in this article, so remember to reference the working example.

Before we get started it's a good idea to [http://www.html5rocks.com/static/demos/20things_pageflip/example/index.html check out the demo] so you know what we're aiming to build.

==Markup==

It's always important to remember that what we draw on canvas can't be indexed by search engines, selected by a visitor, or found by in-browser searches. For that reason, the content we will be working with is put directly into the DOM and then manipulated by JavaScript if it is available. The markup required for this is minimal:

<pre>
 <div id="book">
   <canvas id="pageflip-canvas"></canvas>
   <div id="pages">
     <section>
       <div> <!-- Any type of content here --> </div>
     </section>
     <!-- More <section>s here -->
   </div>
 </div>
</pre>

We have one main container element for the book, which in turn contains the different pages of our book and the <code>canvas</code> element that we will be drawing the flipping pages on. Inside the <code>section</code> element there is a <code>div</code> wrapper for the content &mdash; we need this to be able to change the width of the page without affecting the layout of its contents. The <code>div</code> has a fixed width and the <code>section</code> is set to hide its overflow, this results in the width of the <code>section</code> acting as a horizontal mask for the <code>div</code>.

[[Image:pf02.jpg|Open Book]]<br/>
''A background image containing the paper texture and brown book jacket is added to the book element''

==Logic==

The code required to power the page flip is not very complex, but it is quite extensive because it involves a lot of procedurally generated graphics. Let's start by looking at the description of the constant values we'll be using throughout the code.

<pre>
 var BOOK_WIDTH = 830;
 var BOOK_HEIGHT = 260;
 var PAGE_WIDTH = 400;
 var PAGE_HEIGHT = 250;
 var PAGE_Y = ( BOOK_HEIGHT - PAGE_HEIGHT ) / 2;
 var CANVAS_PADDING = 60;
</pre>

The <code>CANVAS_PADDING</code> is added around the canvas so that we can have the paper extend outside of the book when flipping. Note that some of the constants defined here are also set in CSS, so if you want to change the size of the book you will also need to update the values there.

[[Image:pf03.jpg|Constants]]<br/>
''The constant values used throughout the code to track interaction and draw the page flip''

Next we need to define a flip object for each page. These will constantly be updated as we interact with the book to reflect the current status of the flip.

<pre>
 // Create a reference to the book container element
 var book = document.getElementById( "book" );
 
 // Grab a list of all section elements (pages) within the book
 var pages = book.getElementsByTagName( "section" );
 
 for( var i = 0, len = pages.length; i < len; i++ ) {
     pages[i].style.zIndex = len - i;
 
     flips.push( {
     progress: 1,
     target: 1,
     page: pages[i],
     dragging: false
   });
 }
</pre>

First we need to make sure the pages are layered correctly by organizing the z-indexes of the section elements so that the first page is on top and the last page is on the bottom. The most important properties of the flip objects are the <code>progress</code> and <code>target</code> values. These are used to determine how far the page should currently be folded: -1 means all the way to the left, 0 means the dead center of the book and +1 means the right most edge of the book.

[[Image:pf04.jpg|Progress]]<br/>
''The progress and target values of the flips are used to determine where the folding page should be drawn on a -1 to +1 scale''

Now that we have a flip object defined for each page, we need to start capturing and using the user's input to update the state of the flip.

<pre>
 function mouseMoveHandler( event ) {
   // Offset mouse position so that the top of the book spine is 0,0
   mouse.x = event.clientX - book.offsetLeft - ( BOOK_WIDTH / 2 );
   mouse.y = event.clientY - book.offsetTop;
 }
 
 function mouseDownHandler( event ) {
   // Make sure the mouse pointer is inside of the book
   if (Math.abs(mouse.x) < PAGE_WIDTH) {
     if (mouse.x < 0 && page - 1 >= 0) {
       // We are on the left side, drag the previous page
       flips[page - 1].dragging = true;
     }
     else if (mouse.x > 0 && page + 1 < flips.length) {
       // We are on the right side, drag the current page
       flips[page].dragging = true;
     }
   }
 
   // Prevents the text selection
   event.preventDefault();
 }
 
 function mouseUpHandler( event ) {
   for( var i = 0; i < flips.length; i++ ) {
     // If this flip was being dragged, animate to its destination
     if( flips[i].dragging ) {
       // Figure out which page we should navigate to
       if( mouse.x < 0 ) {
         flips[i].target = -1;
         page = Math.min( page + 1, flips.length );
       }
       else {
         flips[i].target = 1;
         page = Math.max( page - 1, 0 );
       }
     }
 
     flips[i].dragging = false;
   }
 }
</pre>

The <code>mouseMoveHandler</code> function updates the <code>mouse</code> object so that we are always working toward the most recent cursor location.

In <code>mouseDownHandler</code> we start by checking if the mouse was pressed down on either the left or the right page so that we know which direction we want to start flipping toward. We also ensure that another page exists in that direction since we might be on the first or last page. If a valid flip option is available after these checks, we set the <code>dragging</code> flag of the corresponding flip object to <code>true</code>.

Once we reach the <code>mouseUpHandler</code> we go through all of the <code>flips</code> and check if any of them were flagged as <code>dragging</code> and should now be released. When a flip is released we set its target value to match the side it should flip to depending on the current mouse position. The page number is also update to reflect this navigation.

==Rendering==

Now that most of our logic is in place we'll go through how to render the folding paper onto the canvas element. Most of this happens inside of the <code>render()</code> function, which is called 60 times per second to update and draw the current state of all active flips.

<pre>
 function render() {
   // Reset all pixels in the canvas
   context.clearRect( 0, 0, canvas.width, canvas.height );
 
   for( var i = 0, len = flips.length; i < len; i++ ) {
     var flip = flips[i];
 
     if( flip.dragging ) {
       flip.target = Math.max( Math.min( mouse.x / PAGE_WIDTH, 1 ), -1 );
     }
 
     // Ease progress toward the target value
     flip.progress += ( flip.target - flip.progress ) * 0.2;
 
     // If the flip is being dragged or is somewhere in the middle
     // of the book, render it
     if( flip.dragging || Math.abs( flip.progress ) < 0.997 ) {
       drawFlip( flip );
     }
 
   }
 }
</pre>

Before we start rendering the <code>flips</code>, we reset the canvas by using the <code>clearRect(x,y,w,h)</code> method. Clearing the whole canvas comes at a big performance expense and it would be much more effecient to clear only the regions that we are drawing on. For the sake of keeping this tutorial on topic, we'll leave it at clearing the whole canvas.

If a flip is being dragged, we update its <code>target</code> value to match the mouse position, but on a -1 to 1 scale rather than actual pixels. We also increment the <code>progress</code> by a fraction of the distance to the <code>target</code>; this will result in a smooth and animated progression of the flip, as it updates on every frame.

Because we are going over all of the <code>flips</code> on every frame, we need to make sure we only redraw the ones that are active. If a flip is not very close to the book edge (within 0.3% of <code>BOOK_WIDTH</code>), or if it is flagged as <code>dragging</code>, it is considered active.

Now that all of the logic is in place, we need to draw the graphical representation of a flip depending on its current state. It's time to look at the first part of the <code>drawFlip(flip)</code> function.

<pre>
 // Determines the strength of the fold/bend on a 0-1 range
 var strength = 1 - Math.abs( flip.progress );
 
 // Width of the folded paper
 var foldWidth = ( PAGE_WIDTH * 0.5 ) * ( 1 - flip.progress );
 
 // X position of the folded paper
 var foldX = PAGE_WIDTH * flip.progress + foldWidth;
 
 // How far outside of the book the paper is bent due to perspective
 var verticalOutdent = 20 * strength;
 
 // The maximum widths of the three shadows used
 var paperShadowWidth = (PAGE_WIDTH*0.5) * Math.max(Math.min(1 - flip.progress, 0.5), 0);
 var rightShadowWidth = (PAGE_WIDTH*0.5) * Math.max(Math.min(strength, 0.5), 0);
 var leftShadowWidth = (PAGE_WIDTH*0.5) * Math.max(Math.min(strength, 0.5), 0);
 
 // Mask the page by setting its width to match the foldX
 flip.page.style.width = Math.max(foldX, 0) + "px";
</pre>

This section of the code starts by calculating a number of visual variables that we need in order to draw the fold in a realistic manner. The <code>progress</code> value of the flip we are drawing plays a big part here, because that is where we want the page fold to appear. To add depth to the page flip effect, we make the paper extend outside of the top and bottom edges of the book. This effect is at its peak when a flip is close to the book's spine.

[[Image:pf05.jpg|Flip]]<br/>
''This is what the page fold looks like when the page is flipping or being dragged''

Now that all of the values are prepared, all that remains is drawing the paper!

<pre>
 context.save();
 context.translate( CANVAS_PADDING + ( BOOK_WIDTH / 2 ), PAGE_Y + CANVAS_PADDING );
 
 // Draw a sharp shadow on the left side of the page
 context.strokeStyle = 'rgba(0,0,0,'+(0.05 * strength)+')';
 context.lineWidth = 30 * strength;
 context.beginPath();
 context.moveTo(foldX - foldWidth, -verticalOutdent * 0.5);
 context.lineTo(foldX - foldWidth, PAGE_HEIGHT + (verticalOutdent * 0.5));
 context.stroke();
 
 // Right side drop shadow
 var rightShadowGradient = context.createLinearGradient(foldX, 0,
               foldX + rightShadowWidth, 0);
 rightShadowGradient.addColorStop(0, 'rgba(0,0,0,'+(strength*0.2)+')');
 rightShadowGradient.addColorStop(0.8, 'rgba(0,0,0,0.0)');
 
 context.fillStyle = rightShadowGradient;
 context.beginPath();
 context.moveTo(foldX, 0);
 context.lineTo(foldX + rightShadowWidth, 0);
 context.lineTo(foldX + rightShadowWidth, PAGE_HEIGHT);
 context.lineTo(foldX, PAGE_HEIGHT);
 context.fill();
 
 // Left side drop shadow
 var leftShadowGradient = context.createLinearGradient(
     foldX - foldWidth - leftShadowWidth, 0, foldX - foldWidth, 0);
 leftShadowGradient.addColorStop(0, 'rgba(0,0,0,0.0)');
 leftShadowGradient.addColorStop(1, 'rgba(0,0,0,'+(strength*0.15)+')');
 
 context.fillStyle = leftShadowGradient;
 context.beginPath();
 context.moveTo(foldX - foldWidth - leftShadowWidth, 0);
 context.lineTo(foldX - foldWidth, 0);
 context.lineTo(foldX - foldWidth, PAGE_HEIGHT);
 context.lineTo(foldX - foldWidth - leftShadowWidth, PAGE_HEIGHT);
 context.fill();
 
 // Gradient applied to the folded paper (highlights & shadows)
 var foldGradient = context.createLinearGradient(
     foldX - paperShadowWidth, 0, foldX, 0);
 foldGradient.addColorStop(0.35, '#fafafa');
 foldGradient.addColorStop(0.73, '#eeeeee');
 foldGradient.addColorStop(0.9, '#fafafa');
 foldGradient.addColorStop(1.0, '#e2e2e2');
 
 context.fillStyle = foldGradient;
 context.strokeStyle = 'rgba(0,0,0,0.06)';
 context.lineWidth = 0.5;
 
 // Draw the folded piece of paper
 context.beginPath();
 context.moveTo(foldX, 0);
 context.lineTo(foldX, PAGE_HEIGHT);
 context.quadraticCurveTo(foldX, PAGE_HEIGHT + (verticalOutdent * 2),
                          foldX - foldWidth, PAGE_HEIGHT + verticalOutdent);
 context.lineTo(foldX - foldWidth, -verticalOutdent);
 context.quadraticCurveTo(foldX, -verticalOutdent * 2, foldX, 0);
 
 context.fill();
 context.stroke();
 
 context.restore();
</pre>

The canvas API's <code>translate(x,y)</code> method is used to offset the co-ordinate system so that we can draw our page flip with the top of the spine acting as the 0,0 position. Note that we also need to <code>save()</code> the current transformation matrix of the canvas and <code>restore()</code> to it when we are done drawing.

[[Image:pdf06.jpg|Translate]]<br/>
''This is the point from which we draw the page flip. The original 0,0 point is in the top left of the image, but by changing that via translate(x,y), we simplify the drawing logic.''

The <code>foldGradient</code> is what we will fill the shape of the folded paper with to give it realistic highlights and shadows. We also add a very thin line around the paper drawing so that the paper doesn't disappear when put against light backgrounds.

All that remains now is drawing the shape of the folded paper using the properties we defined above. The left and right sides of our paper are drawn as straight lines and the top and bottom sides are curved to bring that "bent" feeling of a folding paper sheet across. The strength of this paper bend is determined by the <code>verticalOutdent</code> value.

That's it! You've now got a fully functional page flip navigation in place.

==Page Flip Demo==

The page flip effect is all about communicating the right interactive feel, so looking at images of it doesn't exactly do it justice. Use the links below to play around with the final result!

[http://www.html5rocks.com/static/demos/20things_pageflip/example/index.html View the working example]

[http://www.html5rocks.com/static/demos/20things_pageflip/20Things_PageFlip_Example.zip Download the source code (75k .zip)]

==Next Steps==

[[Image:pf07.jpg|Hrad-flip]]<br/>
''The soft page flip in this tutorial becomes even more powerful when paired with other book-like features such as an interactive hard cover''

This is only one example of what can be accomplished by utilizing HTML5 features such as the canvas element. I recommend you have a look at the more refined book experience, from which this technique is an excerpt, at: [http://www.20thingsilearned.com www.20thingsilearned.com]. There you will see how the page flips can be applied in a real application and how powerful it becomes when paired with other HTML5 features.

==References==

* [http://developers.whatwg.org/the-canvas-element.html#the-canvas-element Canvas] API specification
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Canvas (basic support)
|Chrome_supported=Yes
|Chrome_version=21.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=14.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Feature=Canvas (basic support)
|Android_supported=Yes
|Android_version=2.1
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_phone_supported=Unknown
|IE_phone_version=
|IE_phone_prefixed_supported=Unknown
|IE_phone_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=12.0
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Canvas}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/tutorials/casestudies/20things_pageflip/
}}