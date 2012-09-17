{{Flags}}
{{Summary_Section}}
{{Tutorial
|Content=<h1>Quick Guide to Implementing the HTML5 Audio Tag</h1>
<h2>
By Ernest Delgado
</h2>
<h2 id="toc-step1">Step 1: Wrap your Flash object with the audio tag</h2>
<p>Those browsers that don&#39;t recognize the audio tag will load the Flash content instead.</p>
<pre>
&#60;span class=&#34;new&#34;&#62;&#38;lt;audio&#62;
&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;
    &#38;lt;object class=&#34;playerpreview&#34; type=&#34;application/x-shockwave-flash&#34; 
            data=&#34;player_mp3_mini.swf&#34; width=&#34;200&#34; height=&#34;20&#34;&#62;
      &#38;lt;param name=&#34;movie&#34; value=&#34;player_mp3_mini.swf&#34; /&#62;
      &#38;lt;param name=&#34;bgcolor&#34; value=&#34;#085c68&#34; /&#62;
      &#38;lt;param name=&#34;FlashVars&#34; value=&#34;mp3=test.mp3&#34; /&#62;
      &#38;lt;embed href=&#34;player_mp3_mini.swf&#34; bgcolor=&#34;#085c68&#34; width=&#34;200&#34; 
             height=&#34;20&#34; name=&#34;movie&#34; align=&#34;&#34; 
             type=&#34;application/x-shockwave-flash&#34; flashvars=&#34;mp3=test.mp3&#34;&#62;
      &#38;lt;/embed&#62;
    &#38;lt;/object&#62;
&#60;/span&#62;&#60;span class=&#34;new&#34;&#62;
&#38;lt;/audio&#62;&#60;/span&#62;
</pre><h2 id="toc-step2">Step 2: Add the source reference</h2>
<p>We can add as many &#34;source&#34; lines and formats as we want. If the browser doesn&#39;t support one specific format it will fallback to the next one and so forth.</p>
<pre>
&#60;span class=&#34;old&#34;&#62;&#38;lt;audio&#62;&#60;/span&#62;
  &#60;span class=&#34;new&#34;&#62;&#38;lt;source src=&#34;test.mp3&#34; type=&#34;audio/mpeg&#34; /&#62;
  &#38;lt;source src=&#34;test.ogg&#34; type=&#34;audio/ogg&#34; /&#62;&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;
    
  &#38;lt;object class=&#34;playerpreview&#34; type=&#34;application/x-shockwave-flash&#34; 
          data=&#34;player_mp3_mini.swf&#34; width=&#34;200&#34; height=&#34;20&#34;&#62;
    &#38;lt;param name=&#34;movie&#34; value=&#34;player_mp3_mini.swf&#34; /&#62;
    &#38;lt;param name=&#34;bgcolor&#34; value=&#34;#085c68&#34; /&#62;
    &#38;lt;param name=&#34;FlashVars&#34; value=&#34;mp3=test.mp3&#34; /&#62;
    &#38;lt;embed href=&#34;player_mp3_mini.swf&#34; bgcolor=&#34;#085c68&#34; width=&#34;200&#34; 
           height=&#34;20&#34; name=&#34;movie&#34; align=&#34;&#34; 
           type=&#34;application/x-shockwave-flash&#34; flashvars=&#34;mp3=test.mp3&#34;&#62;
    &#38;lt;/embed&#62;
  &#38;lt;/object&#62;
    
&#38;lt;/audio&#62;&#60;/span&#62;</pre><h2 id="toc-step3">Step 3: Add fallback to Flash</h2>
<p>To be safe, we need to add the fallback to a Flash audio player, in case the browser doesn&#39;t support any of the formats we specified. For instance, Firefox 3.5 only supports the audio tag with <em>Ogg</em> format, but we might only have the <em>mp3</em> file available.</p>
<p><em>Note:</em> There are also tools and <a href="http://audio.online-convert.com/convert-to-ogg" rel="nofollow">online converters</a> you can use if you want to create ogg files from your mp3 and add support for ogg too.</p>
<pre>&#60;span class=&#34;old&#34;&#62;&#38;lt;audio&#62;&#60;/span&#62;
    &#60;span class=&#34;new&#34;&#62;&#38;lt;source src=&#34;test.mp3&#34; type=&#34;audio/mpeg&#34; /&#62;&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;
  
  &#38;lt;object class=&#34;playerpreview&#34; type=&#34;application/x-shockwave-flash&#34; 
          data=&#34;player_mp3_mini.swf&#34; width=&#34;200&#34; height=&#34;20&#34;&#62;
    &#38;lt;param name=&#34;movie&#34; value=&#34;player_mp3_mini.swf&#34; /&#62;
    &#38;lt;param name=&#34;bgcolor&#34; value=&#34;#085c68&#34; /&#62;
    &#38;lt;param name=&#34;FlashVars&#34; value=&#34;mp3=test.mp3&#34; /&#62;
    &#38;lt;embed href=&#34;player_mp3_mini.swf&#34; bgcolor=&#34;#085c68&#34; width=&#34;200&#34; 
           height=&#34;20&#34; name=&#34;movie&#34; align=&#34;&#34; 
           type=&#34;application/x-shockwave-flash&#34; flashvars=&#34;mp3=test.mp3&#34;&#62;
    &#38;lt;/embed&#62;
  &#38;lt;/object&#62;
    
&#38;lt;/audio&#62;
&#60;/span&#62;&#60;span class=&#34;new&#34;&#62;
&#38;lt;div id=&#34;player_fallback&#34;&#62;&#38;lt;/div&#62;
&#38;lt;script&#62;
  if (document.createElement(&#39;audio&#39;).canPlayType) {
    if (!document.createElement(&#39;audio&#39;).canPlayType(&#39;audio/mpeg&#39;)) {
      swfobject.embedSWF(
        &#34;player_mp3_mini.swf&#34;, 
        &#34;player_fallback&#34;, 
        &#34;200&#34;, 
        &#34;20&#34;, 
        &#34;9.0.0&#34;, 
        &#34;&#34;, 
        {&#34;mp3&#34;:&#34;test.mp3&#34;}, 
        {&#34;bgcolor&#34;:&#34;#085c68&#34;});
    }
  }
&#38;lt;/script&#62;&#60;/span&#62;</pre>
<p>To make it easier, we are using the <a href="http://code.google.com/p/swfobject/" rel="nofollow">SWFObject</a> library to insert the Flash player via JavaScript. To include the library you can simply use the <a href="http://code.google.com/apis/ajaxlibs/" rel="nofollow">Google AJAX Libraries API</a> inserting these two lines in your header:</p>
<pre>&#60;span class=&#34;new&#34;&#62;&#38;lt;script src=&#34;http://www.google.com/jsapi&#34;&#62;&#38;lt;/script&#62;
&#38;lt;script&#62;google.load(&#34;swfobject&#34;, &#34;2.2&#34;);&#38;lt;/script&#62;&#60;/span&#62;</pre><h2 id="toc-step4">Step 4: Add the default controls to show the player</h2>
<p>These controls are not customizable (see examples at the end). Since these default controls will show up regardless of the supported format we will need to handle its visibility with the conditional we previously created.</p>
<pre>&#60;span class=&#34;old&#34;&#62;&#38;lt;audio &#60;/span&#62;&#60;span class=&#34;new&#34;&#62;id=&#34;audio_with_controls&#34; controls&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;&#62;&#60;/span&#62;
  &#60;span class=&#34;old&#34;&#62;&#38;lt;source src=&#34;test.mp3&#34; type=&#34;audio/mpeg&#34; /&#62;&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;
    
  &#38;lt;object class=&#34;playerpreview&#34; type=&#34;application/x-shockwave-flash&#34; 
          data=&#34;player_mp3_mini.swf&#34; width=&#34;200&#34; height=&#34;20&#34;&#62;
    &#38;lt;param name=&#34;movie&#34; value=&#34;player_mp3_mini.swf&#34; /&#62;
    &#38;lt;param name=&#34;bgcolor&#34; value=&#34;#085c68&#34; /&#62;
    &#38;lt;param name=&#34;FlashVars&#34; value=&#34;mp3=test.mp3&#34; /&#62;
    &#38;lt;embed href=&#34;player_mp3_mini.swf&#34; bgcolor=&#34;#085c68&#34; width=&#34;200&#34; 
           height=&#34;20&#34; name=&#34;movie&#34; align=&#34;&#34; 
           type=&#34;application/x-shockwave-flash&#34; flashvars=&#34;mp3=test.mp3&#34;&#62;
    &#38;lt;/embed&#62;
  &#38;lt;/object&#62;
    
&#38;lt;/audio&#62;
&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;
&#38;lt;div id=&#34;player_fallback&#34;&#62;&#38;lt;/div&#62;
&#38;lt;script&#62;
  if (document.createElement(&#39;audio&#39;).canPlayType) {
    if (!document.createElement(&#39;audio&#39;).canPlayType(&#39;audio/mpeg&#39;)) {
      ... SWFObject script line here ...
      &#60;/span&#62;&#60;span class=&#34;new&#34;&#62;document.getElementsById(&#39;audio_with_controls&#39;).style.display = &#39;none&#39;;&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;
    }
  }
&#38;lt;/script&#62;&#60;/span&#62;</pre>
<p>Alternatively, you can create your own player using JavaScript and CSS.</p>
<pre>&#60;span class=&#34;old&#34;&#62;&#38;lt;audio &#60;/span&#62;&#60;span class=&#34;new&#34;&#62;id=&#34;audio&#34;&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;&#62;&#60;/span&#62;
  &#60;span class=&#34;old&#34;&#62;&#38;lt;source src=&#34;test.mp3&#34; type=&#34;audio/mpeg&#34; /&#62;&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;

  &#38;lt;object class=&#34;playerpreview&#34; type=&#34;application/x-shockwave-flash&#34; 
          data=&#34;player_mp3_mini.swf&#34; width=&#34;200&#34; height=&#34;20&#34;&#62;
    &#38;lt;param name=&#34;movie&#34; value=&#34;player_mp3_mini.swf&#34; /&#62;
    &#38;lt;param name=&#34;bgcolor&#34; value=&#34;#085c68&#34; /&#62;
    &#38;lt;param name=&#34;FlashVars&#34; value=&#34;mp3=test.mp3&#34; /&#62;
    &#38;lt;embed href=&#34;player_mp3_mini.swf&#34; bgcolor=&#34;#085c68&#34; width=&#34;200&#34; 
           height=&#34;20&#34; name=&#34;movie&#34; align=&#34;&#34; 
           type=&#34;application/x-shockwave-flash&#34; flashvars=&#34;mp3=test.mp3&#34;&#62;
    &#38;lt;/embed&#62;
  &#38;lt;/object&#62;
    
&#38;lt;/audio&#62;
&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;
&#38;lt;div id=&#34;player_fallback&#34;&#62;&#38;lt;/div&#62;
&#60;span class=&#34;new&#34;&#62;&#38;lt;div id=&#34;player&#34; style=&#34;display: none&#34;&#62;
  &#38;lt;button onClick=&#34;document.getElementById(&#39;audio&#39;).play()&#34;&#62;Play&#38;lt;/button&#62;
  &#38;lt;button onClick=&#34;document.getElementById(&#39;audio&#39;).pause()&#34;&#62;Pause&#38;lt;/button&#62;
&#38;lt;/div&#62;&#60;/span&#62;

&#38;lt;script&#62;
  if (document.createElement(&#39;audio&#39;).canPlayType) {
    if (!document.createElement(&#39;audio&#39;).canPlayType(&#39;audio/mpeg&#39;)) {
      ... SWFObject script lines here ...
    } &#60;/span&#62;&#60;span class=&#34;new&#34;&#62;else { // HTML5 audio + mp3 support
      document.getElementById(&#39;player&#39;).style.display = &#39;block&#39;;
    }&#60;/span&#62;&#60;span class=&#34;old&#34;&#62;
  }
&#38;lt;/script&#62;&#60;/span&#62;</pre><h2 id="toc-examples">Examples</h2>
<p>The following two examples will fallback to the Flash player in those browsers that don&#39;t support the audio tag nor can play mp3 in it.</p>
<p>&#60;iframe src=&#34;<a class="externallink" href="http://playground.html5rocks.com/?mode=frame&#38;hu=180&#38;hl=180#audio_tag_with_fallback_to_flash" rel="nofollow" title="http://playground.html5rocks.com/?mode=frame&#38;hu=180&#38;hl=180#audio_tag_with_fallback_to_flash">http://playground.html5rocks.com/?mode=frame&#38;hu=180&#38;hl=180#audio_tag_with_fallback_to_flash</a>&#34; style=&#34;border: none; width: 100%; height: 480px;&#34;&#62;&#60;/iframe&#62;
</p>
<p class="last_p">If you don&#39;t want to start your customized player from the scratch you can take a <a href="http://www.jezra.net/code_examples/html5_audio/" rel="nofollow">basic one</a> and style it from there.</p>
<p>You are all set!</p>
<div class="footer">
<p>Flash MP3 player is from <a href="http://flash-mp3-player.net/" rel="nofollow">neolao production</a>.
MP3 sample is <strong>Modal Blues</strong> by <a href="http://freemusicarchive.org/music/Rushus/" rel="nofollow">Rushus</a> and
is licensed under a <a href="http://creativecommons.org/licenses/by/3.0/" rel="nofollow">Creative Commons Attribution License</a>.
</p></div>
<p>&#60;/section&#62;
&#60;/article&#62;
&#60;section class=&#34;cc pattern-bg-lighter&#34;&#62;
</p>
<p>
Except as otherwise <a href="http://code.google.com/policies.html#restrictions" rel="nofollow">noted</a>, the content of this page is licensed under the <a href="http://creativecommons.org/licenses/by/3.0/" rel="nofollow">Creative Commons Attribution 3.0 License</a>, and code samples are licensed under the <a href="http://www.apache.org/licenses/LICENSE-2.0" rel="nofollow">Apache 2.0 License</a>.
</p>
<p>&#60;/section&#62;
&#60;section class=&#34;disqus pattern-bg-lighter&#34;&#62;
</p>
<div id="disqus_thread" />
<p>&#60;noscript&#62;
</p>
<p class="center">
<strong>
<a href="http://disqus.com/?ref_noscript" rel="nofollow">Please enable JavaScript to view the comments powered by Disqus.</a>
</strong>
</p>
<p>&#60;/noscript&#62;
&#60;script&#62;function _prettyPrint(){if(typeof customPrettyPrintLanguage!=&#39;undefined&#39;){customPrettyPrintLanguage();}
prettyPrint();}&#60;/script&#62;
&#60;script async src=&#34;//apis.google.com/js/plusone.js&#34;&#62;&#60;/script&#62;
&#60;script async src=&#34;<a class="externallink" href="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/prettify.min.js.pagespeed.jm.JSZAUYYnh2.js" rel="nofollow" title="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/prettify.min.js.pagespeed.jm.JSZAUYYnh2.js">http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/js/prettify.min.js.pagespeed.jm.JSZAUYYnh2.js</a>&#34; onload=&#34;_prettyPrint()&#34;&#62;&#60;/script&#62;
&#60;script async src=&#34;//platform.twitter.com/widgets.js&#34;&#62;&#60;/script&#62;
&#60;script&#62;var disqus_shortname=&#39;html5rocks&#39;;var disqus_identifier=&#39;<a class="externallink" href="http://www.html5rocks.com/tutorials/audio/quick/&#39;;var" rel="nofollow" title="http://www.html5rocks.com/tutorials/audio/quick/&#39;;var">http://www.html5rocks.com/tutorials/audio/quick/&#39;;var</a> disqus_url=&#39;<a class="externallink" href="http://www.html5rocks.com/tutorials/audio/quick/&#39;;var" rel="nofollow" title="http://www.html5rocks.com/tutorials/audio/quick/&#39;;var">http://www.html5rocks.com/tutorials/audio/quick/&#39;;var</a> disqus_developer=0;var disqus_config=function(){var funky_language_code_mapping={&#39;de&#39;:&#39;de_inf&#39;,&#39;es&#39;:&#39;es_ES&#39;,&#39;pt&#39;:&#39;pt_EU&#39;,&#39;sr&#39;:&#39;sr_CYRL&#39;,&#39;sv&#39;:&#39;sv_SE&#39;,&#39;zh&#39;:&#39;zh_HANT&#39;};this.language=funky_language_code_mapping[&#39;en&#39;]||&#39;en&#39;;};window.addEventListener(&#39;load&#39;,function(e){var c=document.createElement(&#39;script&#39;);c.type=&#39;text/javascript&#39;;c.src=&#39;<a class="externallink" href="http://&#39;+disqus_shortname+&#39;.disqus.com/count.js&#39;;var" rel="nofollow" title="http://&#39;+disqus_shortname+&#39;.disqus.com/count.js&#39;;var">http://&#39;+disqus_shortname+&#39;.disqus.com/count.js&#39;;var</a> dsq=document.createElement(&#39;script&#39;);dsq.type=&#39;text/javascript&#39;;dsq.src=&#39;<a class="externallink" href="http://&#39;+disqus_shortname+&#39;.disqus.com/embed.js&#39;;var" rel="nofollow" title="http://&#39;+disqus_shortname+&#39;.disqus.com/embed.js&#39;;var">http://&#39;+disqus_shortname+&#39;.disqus.com/embed.js&#39;;var</a> s=document.getElementsByTagName(&#39;script&#39;)[0],sp=s.parentNode;sp.insertBefore(c,s);sp.insertBefore(dsq,s);},false);var externLinks=document.querySelectorAll(&#39;article.tutorial a[href^=&#34;http&#34;]:not([target])&#39;);for(var i=0,a;a=externLinks[i];++i){a.target=&#39;_blank&#39;;}&#60;/script&#62;
&#60;/section&#62;
</p></div>
<p>&#60;script&#62;(function(){$(&#39;#features_show a&#39;).click(function(){$(&#39;#search_hide&#39;).click();if($(this).hasClass(&#39;current&#39;)){$(&#39;.subheader.features&#39;).hide();$(this).removeClass(&#39;current&#39;);$(&#39;.watermark&#39;).css(&#39;top&#39;,&#39;30px&#39;);$(&#39;#features_show a&#39;).focus();}else{$(&#39;.main nav .current&#39;).removeClass(&#39;current&#39;);$(this).addClass(&#39;current&#39;);$(&#39;.subheader.features&#39;).show();$(&#39;.watermark&#39;).css(&#39;top&#39;,&#39;100px&#39;);$(&#39;#features&#39;).focus();}
if(/#features$/.test(this.href))return false;});$(&#39;#features_hide&#39;).click(function(){$(&#39;#features_show&#39;).removeClass(&#39;current&#39;);$(&#39;.subheader.features&#39;).hide();$(&#39;.watermark&#39;).css(&#39;top&#39;,&#39;30px&#39;);$(&#39;#features_show a&#39;).focus();});if(window.applicationCache){window.applicationCache.addEventListener(&#39;updateready&#39;,function(e){if(window.applicationCache.status==window.applicationCache.UPDATEREADY){window.applicationCache.swapCache();if(confirm(&#39;A new version of this site is available. Load it?&#39;)){window.location.reload();}}},false);}
window.isCompatible=function(){return null;};if(isCompatible()===false){document.getElementById(&#39;notcompatible&#39;).className=<i>;}else if(isCompatible()===true){document.getElementById(&#39;compatible&#39;).className=</i>;}
if(/^\?utm_/.test(document.location.search)&#38;&#38;window.history.replaceState){window.history.replaceState({},<i>,document.location.href.replace(/\?utm_.*/,</i>));}
if($(window).width()&#60;&#39;1200&#39;&#38;&#38;$(window).width()&#62;&#39;1000&#39;&#38;&#38;$(&#39;.toc&#39;).length){var top=$(&#39;.toc&#39;).offset().top-50;$(window).scroll(function(event){var y=$(this).scrollTop();if(y&#62;=top){$(&#39;.toc&#39;).addClass(&#39;fixed&#39;).removeClass(&#39;bottom&#39;);}else{$(&#39;.toc&#39;).removeClass(&#39;fixed&#39;).removeClass(&#39;bottom&#39;);}});}})();&#60;/script&#62;
&#60;script&#62;var _gaq=_gaq
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
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}