{{Page_Title|Quick Guide to Implementing the HTML5 Audio Tag}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Ernest Delgado
|URL=http://www.html5rocks.com/profiles/#ernestd
}}
{{Summary_Section|Guide to implementing the audio tag in HTML.

Published '''Feb. 5, 2010'''
}}
{{Tutorial
|Content=== Step 1: Wrap your Flash object with the audio tag ==
 
Those browsers that don't recognize the audio tag will load the Flash content instead.

<pre> &lt;audio>

    &lt;object class="playerpreview" type="application/x-shockwave-flash" 
            data="player_mp3_mini.swf" width="200" height="20">
      &lt;param name="movie" value="player_mp3_mini.swf" />
      &lt;param name="bgcolor" value="#085c68" />
      &lt;param name="FlashVars" value="mp3=test.mp3" />
      &lt;embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200" 
             height="20" name="movie" align="" 
             type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
      &lt;/embed>
    &lt;/object>

&lt;/audio> 
</pre>
 
== Step 2: Add the source reference ==
 
We can add as many "source" lines and formats as we want. If the browser doesn't support one specific format it will fallback to the next one and so forth.

<pre> &lt;audio> &lt;source src="test.mp3" type="audio/mpeg" />
  &lt;source src="test.ogg" type="audio/ogg" />
    
  &lt;object class="playerpreview" type="application/x-shockwave-flash" 
          data="player_mp3_mini.swf" width="200" height="20">
    &lt;param name="movie" value="player_mp3_mini.swf" />
    &lt;param name="bgcolor" value="#085c68" />
    &lt;param name="FlashVars" value="mp3=test.mp3" />
    &lt;embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200" 
           height="20" name="movie" align="" 
           type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
    &lt;/embed>
  &lt;/object>
    
&lt;/audio>
</pre>
 
== Step 3: Add fallback to Flash ==
 
To be safe, we need to add the fallback to a Flash audio player, in case the browser doesn't support any of the formats we specified. For instance, Firefox 3.5 only supports the audio tag with ''Ogg'' format, but we might only have the ''mp3'' file available.

''Note:'' There are also tools and [http://audio.online-convert.com/convert-to-ogg online converters] you can use if you want to create ogg files from your mp3 and add support for ogg too.

<pre>&lt;audio> &lt;source src="test.mp3" type="audio/mpeg" />
  
  &lt;object class="playerpreview" type="application/x-shockwave-flash" 
          data="player_mp3_mini.swf" width="200" height="20">
    &lt;param name="movie" value="player_mp3_mini.swf" />
    &lt;param name="bgcolor" value="#085c68" />
    &lt;param name="FlashVars" value="mp3=test.mp3" />
    &lt;embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200" 
           height="20" name="movie" align="" 
           type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
    &lt;/embed>
  &lt;/object>
    
&lt;/audio>

&lt;div id="player_fallback">&lt;/div>
&lt;script>
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
&lt;/script>
</pre>
 
To make it easier, we are using the [http://code.google.com/p/swfobject/ SWFObject] library to insert the Flash player via JavaScript. To include the library you can simply use the [http://code.google.com/apis/ajaxlibs/ Google AJAX Libraries API] inserting these two lines in your header:

<pre>&lt;script src="http://www.google.com/jsapi">&lt;/script>
&lt;script>google.load("swfobject", "2.2");&lt;/script>
</pre>
 
== Step 4: Add the default controls to show the player ==
 
These controls are not customizable (see examples at the end). Since these default controls will show up regardless of the supported format we will need to handle its visibility with the conditional we previously created.

<pre>&lt;audio id="audio_with_controls" controls> &lt;source src="test.mp3" type="audio/mpeg" />
    
  &lt;object class="playerpreview" type="application/x-shockwave-flash" 
          data="player_mp3_mini.swf" width="200" height="20">
    &lt;param name="movie" value="player_mp3_mini.swf" />
    &lt;param name="bgcolor" value="#085c68" />
    &lt;param name="FlashVars" value="mp3=test.mp3" />
    &lt;embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200" 
           height="20" name="movie" align="" 
           type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
    &lt;/embed>
  &lt;/object>
    
&lt;/audio>

&lt;div id="player_fallback">&lt;/div>
&lt;script>
  if (document.createElement('audio').canPlayType) {
    if (!document.createElement('audio').canPlayType('audio/mpeg')) {
      ... SWFObject script line here ...
      document.getElementsById('audio_with_controls').style.display = 'none';
    }
  }
&lt;/script>
</pre>
 
Alternatively, you can create your own player using JavaScript and CSS.

<pre>&lt;audio id="audio"> &lt;source src="test.mp3" type="audio/mpeg" />

  &lt;object class="playerpreview" type="application/x-shockwave-flash" 
          data="player_mp3_mini.swf" width="200" height="20">
    &lt;param name="movie" value="player_mp3_mini.swf" />
    &lt;param name="bgcolor" value="#085c68" />
    &lt;param name="FlashVars" value="mp3=test.mp3" />
    &lt;embed href="player_mp3_mini.swf" bgcolor="#085c68" width="200" 
           height="20" name="movie" align="" 
           type="application/x-shockwave-flash" flashvars="mp3=test.mp3">
    &lt;/embed>
  &lt;/object>
    
&lt;/audio>

&lt;div id="player_fallback">&lt;/div>
&lt;div id="player" style="display: none">
  &lt;button onClick="document.getElementById('audio').play()">Play&lt;/button>
  &lt;button onClick="document.getElementById('audio').pause()">Pause&lt;/button>
&lt;/div>

&lt;script>
  if (document.createElement('audio').canPlayType) {
    if (!document.createElement('audio').canPlayType('audio/mpeg')) {
      ... SWFObject script lines here ...
    } else { // HTML5 audio + mp3 support
      document.getElementById('player').style.display = 'block';
    }
  }
&lt;/script>
</pre>
 
== Example ==
 
The following example will fallback to the Flash player in those browsers that don't support the audio tag nor can play mp3 in it.

<pre>
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
</pre>

You can play with this code and see it in action in the [http://playground.html5rocks.com/?mode=frame&hu=180&hl=180#audio_tag_with_fallback_to_flash HTML5Rocks! Playground].
  
If you don't want to start your customized player from the scratch you can take a [http://www.jezra.net/code_examples/html5_audio/ basic one] and style it from there.

You are all set!

Flash MP3 player is from [http://flash-mp3-player.net/ neolao productions].
MP3 sample is '''Modal Blues''' by [http://freemusicarchive.org/music/Rushus/ Rushus] and
is licensed under a [http://creativecommons.org/licenses/by/3.0/ Creative Commons Attribution License].
|[];_gaq_push([&#39;_setAccount&#39;,&#39;UA-15028909-1&#39;]);_gaq_push([&#39;_setSiteSpeedSampleRate&#39;,50]);_gaq_push([&#39;_trackPageview&#39;]);(function(){var ga=document.createElement(&#39;script&#39;);ga.type=&#39;text/javascript&#39;;ga.async=true;ga.src=(&#39;https:&#39;==document.location.protocol?&#39;<a class="externallink" href="https://ssl&#39;:&#39;http://www&#39;" rel="nofollow" title="https://ssl&#39;:&#39;http://www&#39;">https://ssl&#39;:&#39;http://www&#39;</a>)+&#39;.google-analytics.com/ga.js&#39;;var s=document.getElementsByTagName(&#39;script&#39;)[0];s.parentNode.insertBefore(ga,s);})();&#60;/script&#62;
&#60;script defer src=&#34;<a class="externallink" href="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/app.min.js.pagespeed.ce.IlL62AP3Y-.js" rel="nofollow" title="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/app.min.js.pagespeed.ce.IlL62AP3Y-.js">http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/app.min.js.pagespeed.ce.IlL62AP3Y-.js</a>&#34;&#62;&#60;/script&#62;
&#60;script defer src=&#34;<a class="externallink" href="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/search.min.js.pagespeed.ce.hdMERthVbk.js" rel="nofollow" title="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/search.min.js.pagespeed.ce.hdMERthVbk.js">http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/search.min.js.pagespeed.ce.hdMERthVbk.js</a>&#34;&#62;&#60;/script&#62;
&#60;script defer src=&#34;<a class="externallink" href="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/3rdpartyinit.min.js.pagespeed.ce.CGINL0KvzE.js" rel="nofollow" title="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/3rdpartyinit.min.js.pagespeed.ce.CGINL0KvzE.js">http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/3rdpartyinit.min.js.pagespeed.ce.CGINL0KvzE.js</a>&#34;&#62;&#60;/script&#62;
&#60;script type=&#39;text/javascript&#39;&#62;(function(){function g(){var ifr=0;var rpi=<i>;if(window.mod_pagespeed_prefetch_start){rpi+=&#39;&#38;nrp=&#39;+window.mod_pagespeed_num_resources_prefetched;rpi+=&#39;&#38;htmlAt=&#39;;rpi+=(window.mod_pagespeed_start-window.mod_pagespeed_prefetch_start);}if(window.parent != window){ifr=1}new Image().src=&#39;<a class="externallink" href="http://1-ps.googleusercontent.com/beacon?org=53_2_vn&#38;ets=load:&#39;+" rel="nofollow" title="http://1-ps.googleusercontent.com/beacon?org=53_2_vn&#38;ets=load:&#39;+">http://1-ps.googleusercontent.com/beacon?org=53_2_vn&#38;ets=load:&#39;+</a>(Number(new Date())-window.mod_pagespeed_start)+&#39;&#38;ifr=&#39;+ifr+</i>+rpi+&#39;&#38;url=&#39;+encodeURIComponent(&#39;<a class="externallink" href="http://www.html5rocks.com/en/tutorials/audio/quick/&#39;" rel="nofollow" title="http://www.html5rocks.com/en/tutorials/audio/quick/&#39;">http://www.html5rocks.com/en/tutorials/audio/quick/&#39;</a>);window.mod_pagespeed_loaded=true;};var f=window.addEventListener;if(f){f(&#39;load&#39;,g,false);}else{f=window.attachEvent;if(f){f(&#39;onload&#39;,g);}}})();&#60;/script&#62;&#60;/body&#62;
&#60;/html&#62;
</p>
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=20
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=12
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
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
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=4.0
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Audio, HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/tutorials/audio/quick/
}}