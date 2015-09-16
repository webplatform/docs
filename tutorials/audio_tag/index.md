---
title: 'Implementing the HTML5 audio tag'
attributions:
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/tutorials/audio/quick/)'
readiness: 'Ready to Use'
summary: 'A quick guide to implementing the audio tag in HTML.'
tags:
  - Tutorials
  - Audio
  - HTML
uri: 'tutorials/audio tag'

---
**By [Ernest Delgado](http://www.html5rocks.com/profiles/#ernestd)**
Originally published Feb. 5, 2010

## Summary

A quick guide to implementing the audio tag in HTML.

## Step 1: Wrap your Flash object with the audio tag

Those browsers that don't recognize the audio tag will load the Flash content instead.

     <audio>

        <object class="playerpreview" type="application/x-shockwave-flash"
                data="player_mp3_mini.swf" width="200" height="20">
          <param name="movie" value="player_mp3_mini.swf" />
          <param name="bgcolor" value="#085c68" />
          <param name="FlashVars" value="mp3=test.mp3" />
          <embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200"
                 height="20" name="movie" align=""
                 type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
          </embed>
        </object>

    </audio>

## Step 2: Add the source reference

We can add as many "source" lines and formats as we want. If the browser doesn't support one specific format it will fallback to the next one and so forth.

     <audio> <source src="test.mp3" type="audio/mpeg" />
      <source src="test.ogg" type="audio/ogg" />

      <object class="playerpreview" type="application/x-shockwave-flash"
              data="player_mp3_mini.swf" width="200" height="20">
        <param name="movie" value="player_mp3_mini.swf" />
        <param name="bgcolor" value="#085c68" />
        <param name="FlashVars" value="mp3=test.mp3" />
        <embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200"
               height="20" name="movie" align=""
               type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
        </embed>
      </object>

    </audio>

## Step 3: Add fallback to Flash

To be safe, we need to add the fallback to a Flash audio player, in case the browser doesn't support any of the formats we specified. For instance, Firefox 3.5 only supports the audio tag with *Ogg* format, but we might only have the *mp3* file available.

*Note:* There are also tools and [online converters](http://audio.online-convert.com/convert-to-ogg) you can use if you want to create ogg files from your mp3 and add support for ogg too.

    <audio> <source src="test.mp3" type="audio/mpeg" />

      <object class="playerpreview" type="application/x-shockwave-flash"
              data="player_mp3_mini.swf" width="200" height="20">
        <param name="movie" value="player_mp3_mini.swf" />
        <param name="bgcolor" value="#085c68" />
        <param name="FlashVars" value="mp3=test.mp3" />
        <embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200"
               height="20" name="movie" align=""
               type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
        </embed>
      </object>

    </audio>

    <div id="player_fallback"></div>
    <script type="application/javascript">
      if (document.createElement('audio').canPlayType) {
        if (!document.createElement('audio').canPlayType('audio/mpeg')) {
          swfobject.embedSWF(
            "player_mp3_mini.swf",
            "player_fallback",
            "200",
            "20",
            "9.0.0",
            "",
            {"mp3":"test.mp3"},
            {"bgcolor":"#085c68"});
        }
      }
    </script>

To make it easier, we are using the [SWFObject](http://code.google.com/p/swfobject/) library to insert the Flash player via JavaScript. To include the library you can simply use the [Google AJAX Libraries API](http://code.google.com/apis/ajaxlibs/) inserting these two lines in your header:

    <script src="http://www.google.com/jsapi" type="application/javascript"></script>
    <script type="application/javascript">google.load("swfobject", "2.2");</script>

## Step 4: Add the default controls to show the player

These controls are not customizable (see examples at the end). Since these default controls will show up regardless of the supported format we will need to handle its visibility with the conditional we previously created.

    <audio id="audio_with_controls" controls="controls"> <source src="test.mp3" type="audio/mpeg" />

      <object class="playerpreview" type="application/x-shockwave-flash"
              data="player_mp3_mini.swf" width="200" height="20">
        <param name="movie" value="player_mp3_mini.swf" />
        <param name="bgcolor" value="#085c68" />
        <param name="FlashVars" value="mp3=test.mp3" />
        <embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200"
               height="20" name="movie" align=""
               type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
        </embed>
      </object>

    </audio>

    <div id="player_fallback"></div>
    <script type="application/javascript">
      if (document.createElement('audio').canPlayType) {
        if (!document.createElement('audio').canPlayType('audio/mpeg')) {
          ... SWFObject script line here ...
          document.getElementsById('audio_with_controls').style.display = 'none';
        }
      }
    </script>

Alternatively, you can create your own player using JavaScript and CSS.

    <audio id="audio"> <source src="test.mp3" type="audio/mpeg" />

      <object class="playerpreview" type="application/x-shockwave-flash"
              data="player_mp3_mini.swf" width="200" height="20">
        <param name="movie" value="player_mp3_mini.swf" />
        <param name="bgcolor" value="#085c68" />
        <param name="FlashVars" value="mp3=test.mp3" />
        <embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200"
               height="20" name="movie" align=""
               type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
        </embed>
      </object>

    </audio>

    <div id="player_fallback"></div>
    <div id="player" style="display: none">
      <button onClick="document.getElementById('audio').play()">Play</button>
      <button onClick="document.getElementById('audio').pause()">Pause</button>
    </div>

    <script type="application/javascript">
      if (document.createElement('audio').canPlayType) {
        if (!document.createElement('audio').canPlayType('audio/mpeg')) {
          ... SWFObject script lines here ...
        } else { // HTML5 audio + mp3 support
          document.getElementById('player').style.display = 'block';
        }
      }
    </script>

## Example

The following example will fallback to the Flash player in those browsers that don't support the audio tag nor can play mp3 in it.

    <!DOCTYPE html>
    <html>
      <head>
        <style type="text/css">
          h3 {
            font-family: 'Droid Sans', Arial, sans-serif;
            font-size: 14px;
          }
        </style>
      </head>
      <body>
        <h3 id="toc-player-default">Player with default controls</h3>
          <audio id="audio_with_controls" controls="controls">
            <source src="http://www.html5rocks.com/en/tutorials/audio/quick/test.mp3" type="audio/mpeg" />
            <source src="http://www.html5rocks.com/en/tutorials/audio/quick/test.ogg" type="audio/ogg" />
            <object class="playerpreview" type="application/x-shockwave-flash" data="http://www.html5rocks.com/en/tutorials/audio/quick/player_mp3_mini.swf" width="200" height="20">
              <param name="movie" value="http://www.html5rocks.com/en/tutorials/audio/quick/player_mp3_mini.swf" />
              <param name="bgcolor" value="#085c68" />
              <param name="FlashVars" value="mp3=http://www.html5rocks.com/en/tutorials/audio/quick/test.mp3" />
              <embed href="http://www.html5rocks.com/en/tutorials/audio/quick/player_mp3_mini.swf" bgcolor="#085c68" width="200" height="20" name="movie" align="" type="application/x-shockwave-flash" flashvars="mp3=http://www.html5rocks.com/en/tutorials/audio/quick/test.mp3" />
            </object>
          </audio>
        <div id="default_player_fallback"></div>

        <h3 id="toc-player-custom">Player with customized controls</h3>
        <audio id="audio">
          <source src="http://www.html5rocks.com/en/tutorials/audio/quick/test.mp3" type="audio/mpeg" />
          <source src="http://www.html5rocks.com/en/tutorials/audio/quick/test.ogg" type="audio/ogg" />
          <object id="flash_obj" class="playerpreview" type="application/x-shockwave-flash" data="http://www.html5rocks.com/en/tutorials/audio/quick/player_mp3_mini.swf" width="200" height="20">
            <param name="movie" value="http://www.html5rocks.com/en/tutorials/audio/quick/player_mp3_mini.swf" /><param name="bgcolor" value="#085c68" />
            <param name="FlashVars" value="mp3=http://www.html5rocks.com/en/tutorials/audio/quick/test.mp3" />
            <embed href="http://www.html5rocks.com/en/tutorials/audio/quick/player_mp3_mini.swf" bgcolor="#085c68" width="200" height="20" name="movie" align="" type="application/x-shockwave-flash" flashvars="mp3=http://www.html5rocks.com/en/tutorials/audio/quick/test.mp3" />
          </object>
        </audio>
        <div id="custom_player_fallback"></div>
        <div id="player" style="display: none">
          <button onClick="document.getElementById('audio').play()">Play</button>
          <button onClick="document.getElementById('audio').pause()">Pause</button>
        </div>

        <script type="application/javascript">
          if (document.createElement('audio').canPlayType) {
            if (!document.createElement('audio').canPlayType('audio/mpeg') &&
                !document.createElement('audio').canPlayType('audio/ogg')) {
              swfobject.embedSWF("http://www.html5rocks.com/en/tutorials/audio/quick/player_mp3_mini.swf",
                                 "default_player_fallback", "200", "20", "9.0.0", "",
                                 {"mp3":"http://www.html5rocks.com/en/tutorials/audio/quick/test.mp3"},
                                 {"bgcolor":"#085c68"}
                                );
              swfobject.embedSWF("http://www.html5rocks.com/en/tutorials/audio/quick/player_mp3_mini.swf",
                                 "custom_player_fallback", "200", "20", "9.0.0", "",
                                 {"mp3":"http://www.html5rocks.com/en/tutorials/audio/quick/test.mp3"},
                                 {"bgcolor":"#085c68"}
                                );
              document.getElementById('audio_with_controls').style.display = 'none';
            } else {
              // HTML5 audio + mp3 support
              document.getElementById('player').style.display = 'block';
            }
          }
        </script>

      </body>
    </html>​​

You can play with this code and see it in action in the [HTML5Rocks! Playground](http://playground.html5rocks.com/?mode=frame&hu=180&hl=180#audio_tag_with_fallback_to_flash).

If you don't want to start your customized player from the scratch you can take a [basic one](http://www.jezra.net/code_examples/html5_audio/) and style it from there.

You are all set!

Flash MP3 player is from [neolao productions](http://flash-mp3-player.net/). MP3 sample is **Modal Blues** by [Rushus](http://freemusicarchive.org/music/Rushus/) and is licensed under a [Creative Commons Attribution License](http://creativecommons.org/licenses/by/3.0/).
