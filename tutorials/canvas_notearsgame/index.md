{{Page_Title|No Tears Guide to HTML5 Games}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline}}
{{Summary_Section|An intermediate tutorial for creating games using HTML5 and Canvas.}}
{{Tutorial
|Content==No Tears Guide to HTML5 Games=

====original by Daniel X. Moore====
====published Feb. 1, 2011====

==Introduction==

This tutorial shows you how to build a game using HTML5 and the <canvas> element, and assumes you have an intermediate level of knowledge of JavaScript.

[[File:space-demo.png]]

Before you get started, try [http://strd6.com/space_demo/ playing the game] and [http://strd6.com/wp-content/uploads/2010/12/space_demo.zip viewing the source code for the game].

==Creating the canvas==

To draw objects on the page, we'll need to first create a canvas. Because this is a No Tears guide, we'll use jQuery.

 
 var CANVAS_WIDTH = 480;
 var CANVAS_HEIGHT = 320;
 
 var canvasElement = $("<canvas width='" + CANVAS_WIDTH +
                       "' height='" + CANVAS_HEIGHT + "'></canvas>");
 var canvas = canvasElement.get(0).getContext("2d");
 canvasElement.appendTo('body');

==Game loop==

To simulate the appearance of smooth and continuous gameplay, let's update the game and redraw the screen just faster than the human mind and eye can perceive.
 
 var FPS = 30;
 setInterval(function() {
   update();
   draw();
 }, 1000/FPS);

For now we can leave the update() and draw() methods blank, since <code>setInterval()</code>, calls them periodically.

 
 function update() { ... }
 function draw() { ... }

==Hello world==

Now, let's update the draw() method to draw text on the screen.

 
 function draw() {
   canvas.fillStyle = "#000"; // Set color to black
   canvas.fillText("Sup Bro!", 50, 50);
 }

Pro Tip: Be sure to run your app after making changes. It's much easier to debug a few lines of code than a completed app.
What you see now is pretty cool for stationary text. Since we have a game loop already set up, let's enhance this text by making it move.

 
 var textX = 50;
 var textY = 50;
 
 function update() {
   textX += 1;
   textY += 1;
 }
 
 function draw() {
   canvas.fillStyle = "#000";
   canvas.fillText("Sup Bro!", textX, textY);
 }

Try running the app now. You should see the text move, but you may be seeing some odd results. Because we are not clearing the screen, the previous drawings are being left behind.

Let's add code to the draw() method to clear the screen.

 
 function draw() {
   canvas.clearRect(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT);
   canvas.fillStyle = "#000";
   canvas.fillText("Sup Bro!", textX, textY);
 }

Now that you've created a canvas and added text that moves around on the screen, let's turn this into a game with players and interaction between the players.

==Creating the player==

Create an object to hold the player data and be responsible for things like drawing. 
 
 var player = {
   color: "#00A",
   x: 220,
   y: 270,
   width: 32,
   height: 32,
   draw: function() {
     canvas.fillStyle = this.color;
     canvas.fillRect(this.x, this.y, this.width, this.height);
   }
 };

At the moment, we're using a simple colored rectangle to represent the player. When we draw the game, we'll clear the canvas and draw the player.

 
 function draw() {
   canvas.clearRect(0, 0, CANVAS_WIDTH, CANVAS_HEIGHT);
   player.draw();
 }

==Keyboard controls==

===Using jQuery Hotkeys===

The [https://github.com/tzuryby/jquery.hotkeys jQuery Hotkeys plugin] makes key handling across browsers very easy. Instead of using difficult-to-use cross-browser <code>keyCode</code> and <code>charCode</code>, we can bind events like so:

 
 $(document).bind("keydown", "left", function() { ... });

By binding events, we don't have to worry specifically about key and code combinations. Instead, we can use jQuery Hotkeys to add events like "when the player presses the Up arrow leu, move forward." 

===Player movement===

Because the way JavaScript handles keyboard events is completely event driven, there is no built-in query for checking whether a key is pressed. To address this, we'll create our own query.

Pro Tip: The reason why we don't use an event-driven way of handling keys is because the keyboard repeat rate varies across systems. Since these rates are not bound to the timing of the game loop, gameplay could vary greatly from system to system. To create a consistent experience, it is important to tightly integrate the keyboard event detection with the game loop.

With the source code, I've included a 16-line JaveScript wrapper called key_status.js that will make event querying available. With this wrapper, you can query the status of a key at any time. For example, you can check <code>keydown.left</code>.

Now that we have the ability to query the status of keys, we can use this simple update() method to move the player on the canvas.

 
 function update() {
   if (keydown.left) {
     player.x -= 2;
   }
 
   if (keydown.right) {
     player.x += 2;
   }
 }

When you test this snippet, you may notice that you can move player off the screen. Let's clamp the player's position to keep it within the bounds. We can also increase the speed of the player's movement on the screen.

 
 function update() {
   if (keydown.left) {
     player.x -= 5;
   }
 
   if (keydown.right) {
     player.x += 5;
   }
 
   player.x = player.x.clamp(0, CANVAS_WIDTH - player.width);
 }

Let's start working with sample projectiles to see how the key binding works.

 
 function update() {
   if (keydown.space) {
     player.shoot();
   }
 
   if (keydown.left) {
     player.x -= 5;
   }
 
   if (keydown.right) {
     player.x += 5;
   }
 
   player.x = player.x.clamp(0, CANVAS_WIDTH - player.width);
 }
 
 player.shoot = function() {
   console.log("Pew pew");
   // :) Well at least adding the key binding was easy...
 };

==Adding more game objects==

===Projectiles===

Now, let's add proper projectiles (or bullets, since this is, after all, a game). First, create a collection to store them:

 
 var playerBullets = [];

Next, create a constructor to create bullet instances.

 
 function Bullet(I) {
   I.active = true;
 
   I.xVelocity = 0;
   I.yVelocity = -I.speed;
   I.width = 3;
   I.height = 3;
   I.color = "#000";
 
   I.inBounds = function() {
     return I.x >= 0 && I.x <= CANVAS_WIDTH &&
       I.y >= 0 && I.y <= CANVAS_HEIGHT;
   };
 
   I.draw = function() {
     canvas.fillStyle = this.color;
     canvas.fillRect(this.x, this.y, this.width, this.height);
   };
 
   I.update = function() {
     I.x += I.xVelocity;
     I.y += I.yVelocity;
 
     I.active = I.active && I.inBounds();
   };
 
   return I;
 }

When the player shoots, create a bullet instance and add it to the collection of bullets.

 
 player.shoot = function() {
   var bulletPosition = this.midpoint();
 
   playerBullets.push(Bullet({
     speed: 5,
     x: bulletPosition.x,
     y: bulletPosition.y
   }));
 };
 
 player.midpoint = function() {
   return {
     x: this.x + this.width/2,
     y: this.y + this.height/2
   };
 };

Finally, we need to add the status of the bullets to the update step function. To prevent the collection of bullets from filling up indefinitely, we filter the list of bullets to only include the active bullets. Filtering this list also allows us to remove bullets that have collided with an enemy.

 
 function update() {
   ...
   playerBullets.forEach(function(bullet) {
     bullet.update();
   });
 
   playerBullets = playerBullets.filter(function(bullet) {
     return bullet.active;
   });
 }

The final step is to draw the bullets:

 
 function draw() {
   ...
   playerBullets.forEach(function(bullet) {
     bullet.draw();
   });
 }

===Enemies===

Now that we have bullets, let's add enemies to interact with our players.
 
   enemies = [];
 
 function Enemy(I) {
   I = I {{!}}{{!}} {};
 
   I.active = true;
   I.age = Math.floor(Math.random() * 128);
 
   I.color = "#A2B";
 
   I.x = CANVAS_WIDTH / 4 + Math.random() * CANVAS_WIDTH / 2;
   I.y = 0;
   I.xVelocity = 0
   I.yVelocity = 2;
 
   I.width = 32;
   I.height = 32;
 
   I.inBounds = function() {
     return I.x >= 0 && I.x <= CANVAS_WIDTH &&
       I.y >= 0 && I.y <= CANVAS_HEIGHT;
   };
 
   I.draw = function() {
     canvas.fillStyle = this.color;
     canvas.fillRect(this.x, this.y, this.width, this.height);
   };
 
   I.update = function() {
     I.x += I.xVelocity;
     I.y += I.yVelocity;
 
     I.xVelocity = 3 * Math.sin(I.age * Math.PI / 64);
 
     I.age++;
 
     I.active = I.active && I.inBounds();
   };
 
   return I;
 };
 
 function update() {
   ...
 
   enemies.forEach(function(enemy) {
     enemy.update();
   });
 
   enemies = enemies.filter(function(enemy) {
     return enemy.active;
   });
 
   if(Math.random() < 0.1) {
     enemies.push(Enemy());
   }
 };
 
 function draw() {
   ...
 
   enemies.forEach(function(enemy) {
     enemy.draw();
   });
 }

==Loading and drawing images==

Now that we have the enemy-player interaction set with box images, let's draw actual players to make this game more interesting. To avoid what is usually a painful experience with loading and drawing images on canvas, we can use a simple utility class.

 
 player.sprite = Sprite("player");
 
 player.draw = function() {
   this.sprite.draw(canvas, this.x, this.y);
 };
 
 function Enemy(I) {
   ...
 
   I.sprite = Sprite("enemy");
 
   I.draw = function() {
     this.sprite.draw(canvas, this.x, this.y);
   };
 
   ...
 }

==Collision detection==

Now that we have images flying around on the screen, notice that they're not interacting with each other. Let's add collision detection to let the objects know when they've collided, and therefore when to blow up.

Let's use a simple rectangular collision detection algorithm:

 
 function collides(a, b) {
   return a.x < b.x + b.width &&
          a.x + a.width > b.x &&
          a.y < b.y + b.height &&
          a.y + a.height > b.y;
 }

There are a couple collisions we want to check:

# Player Bullets => Enemy Ships
# Player => Enemy Ships

Now, create a method to handle the collisions which we can call from the update method.
 
 function handleCollisions() {
   playerBullets.forEach(function(bullet) {
     enemies.forEach(function(enemy) {
       if (collides(bullet, enemy)) {
         enemy.explode();
         bullet.active = false;
       }
     });
   });
 
   enemies.forEach(function(enemy) {
     if (collides(enemy, player)) {
       enemy.explode();
       player.explode();
     }
   });
 }
 
 function update() {
   ...
   handleCollisions();
 }

Finally, to make the interaction realistic, we'll add the explode() methods to the player and the enemies to remove the players and enemies that have been hit, and to display an explosion graphic.

 
 function Enemy(I) {
   ...
 
   I.explode = function() {
     this.active = false;
     // Extra Credit: Add an explosion graphic
   };
 
   return I;
 };
 
 player.explode = function() {
   this.active = false;
   // Extra Credit: Add an explosion graphic and then end the game
 };

==Sound==

To round out the experience, we''ll add some sweet sound effects. Sounds, like images, can be somewhat of a pain to use in HTML5, but thanks to our magic no-tears formula sound.js, sound can be made very easily.

 
 player.shoot = function() {
   Sound.play("shoot");
   ...
 }
 
 function Enemy(I) {
   ...
 
   I.explode = function() {
     Sound.play("explode");
     ...
   }
 }

Although the API is now tear-free, adding sounds is currently the quickest way to crash your application. It's not uncommon for sounds to cut out or take down the entire browser tab.

You can also play with the [http://strd6.com/space_demo/ full working game demo] online.

==Source Code==

You can download [http://strd6.com/wp-content/uploads/2010/12/space_demo.zip the source code as a zip]. 

==Summary==

I hope you enjoyed learning the basics of making a simple game in JavaScript and HTML5. By programming at the right level of abstraction, we can insulate ourselves from the more difficult parts of the APIs, as well as be resilient in the face of future changes.

==References==

* [http://blog.nihilogic.dk/2009/02/html5-canvas-cheat-sheet.html HTML5 Canvas Cheat Sheet]
* [https://gist.github.com/768272 HTML5 Game Engines]
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=Canvas
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
|Feature=Canvas
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
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/canvas/notearsgame/
}}