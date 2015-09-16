---
title: 'using web audio'
notes:
  - 'Deletion candidate; is basically the same tutorial as http://docs.webplatform.org/wiki/tutorials/implementing_html5_audio'
readiness: 'Not Ready'
tags:
  - Tutorials
  - Audio
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'Step 1: Wrap your Flash object with the audio tag'
    - 'Step 2: Add the source reference'
    - 'Step 3: Add fallback to Flash'
    - 'Step 4: Add the default controls to show the player'
    - Examples
    - 'online converters'
    - SWFObject
    - 'Google AJAX Libraries API'
    - 'basic one'
    - 'neolao production'
    - Rushus
    - 'Creative Commons Attribution License'
uri: 'tutorials/using web audio'

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

# Implementing the HTML5 Audio Tag

## By Ernest Delgado

      Published Feb. 5, 2010    [[]]

### Table of Contents

-   [Step 1: Wrap your Flash object with the audio tag](/w/index.php?title=Step_1:_Wrap_your_Flash_object_with_the_audio_tag&action=edit&redlink=1)
-   [Step 2: Add the source reference](/w/index.php?title=Step_2:_Add_the_source_reference&action=edit&redlink=1)
-   [Step 3: Add fallback to Flash](/w/index.php?title=Step_3:_Add_fallback_to_Flash&action=edit&redlink=1)
-   [Step 4: Add the default controls to show the player](/w/index.php?title=Step_4:_Add_the_default_controls_to_show_the_player&action=edit&redlink=1)
-   [Examples](/w/index.php?title=Examples&action=edit&redlink=1)

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

*Note:* There are also tools and [online converters](/w/index.php?title=online_converters&action=edit&redlink=1) you can use if you want to create ogg files from your mp3 and add support for ogg too.

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
    <script>
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

To make it easier, we are using the [SWFObject](/w/index.php?title=SWFObject&action=edit&redlink=1) library to insert the Flash player via JavaScript. To include the library you can simply use the [Google AJAX Libraries API](/w/index.php?title=Google_AJAX_Libraries_API&action=edit&redlink=1) inserting these two lines in your header:

    <script src="http://www.google.com/jsapi"></script>
    <script>google.load("swfobject", "2.2");</script>

## Step 4: Add the default controls to show the player

These controls are not customizable (see examples at the end). Since these default controls will show up regardless of the supported format we will need to handle its visibility with the conditional we previously created.

    <audio id="audio_with_controls" controls> <source src="test.mp3" type="audio/mpeg" />

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
    <script>
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

    <script>
      if (document.createElement('audio').canPlayType) {
        if (!document.createElement('audio').canPlayType('audio/mpeg')) {
          ... SWFObject script lines here ...
        } else { // HTML5 audio + mp3 support
          document.getElementById('player').style.display = 'block';
        }
      }
    </script>

## Examples

The following two examples will fallback to the Flash player in those browsers that don't support the audio tag nor can play mp3 in it.

    <!DOCTYPE html>
    <html>
      <head>
        <style>
          h3 {
            font-family: 'Droid Sans', Arial, sans-serif;
            font-size: 14px;
          }
        </style>
      </head>
      <body>
        <h3 id="toc-player-default">Player with default controls</h3>
          <audio id="audio_with_controls" controls>
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

        <script>
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
    </html>​

If you don't want to start your customized player from the scratch you can take a [basic one](/w/index.php?title=basic_one&action=edit&redlink=1) and style it from there.

 You are all set!

 Flash MP3 player is from [neolao production](/w/index.php?title=neolao_production&action=edit&redlink=1). MP3 sample is **Modal Blues** by [Rushus](/w/index.php?title=Rushus&action=edit&redlink=1) and is licensed under a [Creative Commons Attribution License](/w/index.php?title=Creative_Commons_Attribution_License&action=edit&redlink=1).
