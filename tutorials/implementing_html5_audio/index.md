{{Page_Title}}
{{Flags
|State=Not Ready
|Editorial notes={{Editorial/Deletion_Candidate
| Duplicate of http://docs.webplatform.org/wiki/tutorials/audio_tag
}}
|Checked_Out=No
|High-level issues=Deletion Candidate
|Compatibility=Incomplete
}}
{{Byline
|Name=Ernest Delgado
|Published=Feb. 5, 2010
}}
{{Summary_Section|A step-by-step guide on how to implement the HTML5 audio-tag.}}
{{Tutorial
|Content==Implementing the HTML5 Audio Tag =  

    
== Step 1: Wrap your Flash object with the audio tag ==
 
Those browsers that don't recognize the audio tag will load the Flash content instead.

 
<syntaxhighlight lang="html5">
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
</syntaxhighlight>
 
== Step 2: Add the source reference ==
 
We can add as many "source" lines and formats as we want. If the browser doesn't support one specific format it will fallback to the next one and so forth.

 
<syntaxhighlight lang="html5" highlight="2,3">
<audio>
  <source src="test.mp3" type="audio/mpeg" />
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
</syntaxhighlight>
 
== Step 3: Add fallback to Flash ==
 
To be safe, we need to add the fallback to a Flash audio player, in case the browser doesn't support any of the formats we specified. For instance, Firefox 3.5 only supports the audio tag with ''Ogg'' format, but we might only have the ''mp3'' file available.

 
''Note:'' There are also tools and [[online converters]] you can use if you want to create ogg files from your mp3 and add support for ogg too.

 
<syntaxhighlight lang="html5">
<audio>
  <source src="test.mp3" type="audio/mpeg" />
  
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
</syntaxhighlight>
 
To make it easier, we are using the [[SWFObject]] library to insert the Flash player via JavaScript. To include the library you can simply use the [[Google AJAX Libraries API]] inserting these two lines in your header:

 
<syntaxhighlight lang="html5">
<script src="http://www.google.com/jsapi"></script>
<script>google.load("swfobject", "2.2");</script>
</syntaxhighlight>
 
== Step 4: Add the default controls to show the player ==
 
These controls are not customizable (see examples at the end). Since these default controls will show up regardless of the supported format we will need to handle its visibility with the conditional we previously created.

 
<syntaxhighlight lang="html5">
<audio id="audio_with_controls" controls>
  <source src="test.mp3" type="audio/mpeg" />
    
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
</syntaxhighlight>
 
Alternatively, you can create your own player using JavaScript and CSS.

 
<syntaxhighlight lang="html5">
<audio id="audio">
  <source src="test.mp3" type="audio/mpeg" />

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
  <button onClick="document.getElementById('audio').play()">Play&lt;/button>
  <button onClick="document.getElementById('audio').pause()">Pause&lt;/button>
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
</syntaxhighlight>
 
== Examples ==
 
The following two examples will fallback to the Flash player in those browsers that don't support the audio tag nor can play mp3 in it.

<syntaxhighlight lang="html5">
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
</syntaxhighlight>
  
If you don't want to start your customized player from the scratch you can take a [[basic one]] and style it from there.

 
You are all set!

  
Flash MP3 player is from [[neolao production]].
MP3 sample is '''Modal Blues''' by [[Rushus]] and
is licensed under a [[Creative Commons Attribution License]].
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=HTML5 Audio
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Audio
}}
{{Topics|Audio}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}