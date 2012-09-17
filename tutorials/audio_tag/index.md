{{Flags}}
{{Summary_Section}}
{{Tutorial
|Content=<h1>Quick Guide to Implementing the HTML5 Audio Tag</h1>
<p>&#60;section class=&#34;byline&#34;&#62;
<a href="/profiles/#ernestd">&#60;script type=&#34;text/javascript&#34;&#62;(function(){var d=window,e=document,f=&#34;documentElement&#34;,g=&#34;scrollTop&#34;,h=&#34;prototype&#34;,j=&#34;body&#34;,k=&#34;&#34;,l=&#34;data&#34;,m=&#34;load&#34;,n=&#34;number&#34;,p=&#34;on&#34;,r=&#34;onload&#34;,s=&#34;pagespeed_lazy_position&#34;,t=&#34;pagespeed_lazy_src&#34;,u=&#34;position&#34;,v=&#34;relative&#34;,w=&#34;scroll&#34;;d.pagespeed=d.pagespeed||{};var x=d.pagespeed,y=function(a){this.b=[];this.d=0;this.a=!1;this.h=a};
y[h].l=function(){var a=0;typeof d.pageYOffset==n?a=d.pageYOffset:e[j]&#38;&#38;e[j][g]?a=e[j][g]:e[f]&#38;&#38;e[f][g]&#38;&#38;(a=e[f][g]);var b=d.innerHeight||e[f].clientHeight||e[j].clientHeight;return{top:a,bottom:a+b,height:b}};y[h].g=function(a){var b=a.getAttribute(s);if(b)return parseInt(b,0);var b=a.offsetTop,c=a.offsetParent;c&#38;&#38;(b+=this.g(c));b=Math.max(b,0);a.setAttribute(s,b);return b};y[h].k=function(a){var b=this.g(a);return{top:b,bottom:b+a.offsetHeight}};
y[h].j=function(a,b){if(a.currentStyle)return a.currentStyle[b];if(e.defaultView&#38;&#38;e.defaultView.getComputedStyle){var c=e.defaultView.getComputedStyle(a,null);if(c)return c.getPropertyValue(b)}return a.style&#38;&#38;a.style[b]?a.style[b]:k};y[h].i=function(a){if(this.j(a,u)==v)return!0;var b=this.l(),c=a.getBoundingClientRect();c?(a=c.top-b.height,b=c.bottom):(c=this.k(a),a=c.top-b.bottom,b=c.bottom-b.top);return a&#60;=this.d&#38;&#38;0&#60;=b+this.d};
y[h].f=function(a){var b=this;d.setTimeout(function(){var c=a.getAttribute(t);if(null!=c)if((b.a||b.i(a))&#38;&#38;a.src==b.h){var i=a.parentNode,q=a.nextSibling;i.removeChild(a);a.removeAttribute(t);a.removeAttribute(r);a.src=c;q?i.insertBefore(a,q):i.appendChild(a)}else b.b.push(a)},0)};y[h].loadIfVisible=y[h].f;y[h].m=function(){this.a=!0;this.c()};y[h].loadAllImages=y[h].m;y[h].c=function(){var a=this.b,b=a.length;this.b=[];for(var c=0;c&#60;b;++c)this.f(a[c])};
x.e=function(a,b,c){if(a.addEventListener)a.addEventListener(b,c,!1);else if(a.attachEvent)a.attachEvent(p+b,c);else{var i=a[p+b];a[p+b]=function(){c.call(this);i&#38;&#38;i.call(this)}}};x.n=function(a,b){var c=new y(b);x.lazyLoadImages=c;0!=b.indexOf(l)&#38;&#38;((new Image).src=b);x.e(d,m,function(){d.setTimeout(function(){c.a=a;c.c()},200)});a||x.e(d,w,function(){c.c()})};x.lazyLoadInit=x.n;})();

pagespeed.lazyLoadInit(false, &#34;<a class="externallink" href="http://1-ps.googleusercontent.com/h/www.gstatic.com/psa/static/1.gif" rel="nofollow" title="http://1-ps.googleusercontent.com/h/www.gstatic.com/psa/static/1.gif">http://1-ps.googleusercontent.com/h/www.gstatic.com/psa/static/1.gif</a>&#34;);
&#60;/script&#62;&#60;img pagespeed_lazy_src=&#34;<a class="externallink" href="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/images/profiles/75/wernestd.75.png.pagespeed.ic.hlfuQmfKSM.jpg" rel="nofollow" title="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/images/profiles/75/wernestd.75.png.pagespeed.ic.hlfuQmfKSM.jpg">http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/images/profiles/75/wernestd.75.png.pagespeed.ic.hlfuQmfKSM.jpg</a>&#34; itemprop=&#34;photo&#34; alt=&#34;Ernest Delgado&#34; title=&#34;Ernest Delgado&#34; width=&#34;75&#34; height=&#34;75&#34; src=&#34;<a class="externallink" href="http://1-ps.googleusercontent.com/h/www.gstatic.com/psa/static/1.gif" rel="nofollow" title="http://1-ps.googleusercontent.com/h/www.gstatic.com/psa/static/1.gif">http://1-ps.googleusercontent.com/h/www.gstatic.com/psa/static/1.gif</a>&#34; onload=&#34;pagespeed.lazyLoadImages.loadIfVisible(this);&#34;&#62;</a>
&#60;hgroup&#62;
</p><h2>
By <strong><a href="/profiles/#ernestd">Ernest Delgado</a></strong>
</h2>
<p>&#60;/hgroup&#62;
</p>
<div class="date">
<p>&#60;time pubdate&#62;Published <strong>Feb. 5, 2010</strong>&#60;/time&#62;
</p></div>
<p>&#60;/section&#62;
&#60;aside id=&#34;html5badge&#34;&#62;
<a href="http://www.w3.org/html/logo/" rel="nofollow">
&#60;img pagespeed_lazy_src=&#34;<a class="externallink" href="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/images/identity/133x64whtml5-badge-h-multimedia.png.pagespeed.ic.4TOw_zhcFG.png" rel="nofollow" title="http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/images/identity/133x64whtml5-badge-h-multimedia.png.pagespeed.ic.4TOw_zhcFG.png">http://1-ps.googleusercontent.com/x/s.html5rocks-hrd.appspot.com/www.html5rocks.com/static/images/identity/133x64whtml5-badge-h-multimedia.png.pagespeed.ic.4TOw_zhcFG.png</a>&#34; width=&#34;133&#34; height=&#34;64&#34; alt=&#34;This article is powered by HTML5 Multimedia&#34; title=&#34;This article is powered by HTML5 Multimedia&#34; src=&#34;<a class="externallink" href="http://1-ps.googleusercontent.com/h/www.gstatic.com/psa/static/1.gif" rel="nofollow" title="http://1-ps.googleusercontent.com/h/www.gstatic.com/psa/static/1.gif">http://1-ps.googleusercontent.com/h/www.gstatic.com/psa/static/1.gif</a>&#34; onload=&#34;pagespeed.lazyLoadImages.loadIfVisible(this);&#34;/&#62;
</a>
&#60;/aside&#62;
&#60;section class=&#34;browser_support&#34;&#62;
</p><h2>Supported browsers:</h2>
<p><span class="browsers">
<span class="browser opera supported">
<span class="browser_name">Opera</span>
<span class="support">
supported
</span>
</span>
<span class="browser ie ">
<span class="browser_name">IE</span>
<span class="support">
unsupported
</span>
</span>
<span class="browser safari supported">
<span class="browser_name">Safari</span>
<span class="support">
supported
</span>
</span>
<span class="browser ff supported">
<span class="browser_name">Firefox</span>
<span class="support">
supported
</span>
</span>
<span class="browser chrome supported">
<span class="browser_name">Chrome</span>
<span class="support">
supported
</span>
</span>
</span>
</p>
<div class="compatible-block">
<p class="hidden" id="notcompatible">
Your browser may not support all of the functionality in this article.
</p>
<p class="hidden" id="compatible">
Your browser appears to support all of the functionality in this article.
</p></div>
<p>&#60;/section&#62;
<a class="disqus_comments" href="#disqus_thread">Leave a comment</a>
&#60;/section&#62;
<span class="share">
</span></p>
<ul>


<li class="googleplus">
<div class="g-plusone" /></li>

<li class="facebook" />

<li class="twitter"><a class="twitter-share-button" href="http://twitter.com/share" rel="nofollow">Tweet</a></li>

</ul>
<p>
&#60;/header&#62;
&#60;article class=&#34;tutorial pattern-bg-lighter&#34;&#62;
</p>
<div class="outline_nav_toggle">
<p>&#60;img class=&#34;show&#34; src=&#34;data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB8AAAAeCAYAAADU8sWcAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyJpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMC1jMDYwIDYxLjEzNDc3NywgMjAxMC8wMi8xMi0xNzozMjowMCAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNSBNYWNpbnRvc2giIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6OTAyRDZFQUJFOEVFMTFFMDg2NkJGNDlCNjE5NENEMzIiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6OTAyRDZFQUNFOEVFMTFFMDg2NkJGNDlCNjE5NENEMzIiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDo5MDJENkVBOUU4RUUxMUUwODY2QkY0OUI2MTk0Q0QzMiIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDo5MDJENkVBQUU4RUUxMUUwODY2QkY0OUI2MTk0Q0QzMiIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/Pprl4SwAAAIcSURBVHjazFfNasJAEI6ptiIGBCUQbfAWxWu96EUfwAY8tg+gD1A8F+99gfoA9ijoA9he9GKvIt5EMRJyEFKKDQidlaSIyW5iYkgHhiyZzX4zk/nbEOWAJpNJGh4V4DudGYttn8Bz4EGxWJw7OTfkALQBXKPOIwTeASXeXYEDcEMH9kLIG21QYu0IHECRS1+BBeoypAI3rX4F7TMwpcdHF86uEsF9AD6mZ1BAsHQ7CJ7g8WB3wmazia1Wq7imaWHjXSaTUbPZrOpAAQn4EX6B+geuR3Wf9NVisWBGo9HtdruNWckjkci+UCjI5XJ5baMAyoLOMfgLPKq43cPhkJ/NZqwT3yYSie96vT6PRqN7QgCKyHpat/ps4FwuR7VaLdN+5JleryfsdrsrQgDWjICrkFzt1OJTBcbjcZqw5d4ArxIKDec2tJHSoMQ1RiygtKZxqYU+lGWZ8ZJb0+k0RRALNKZJUMvlkvGa2JIkxUngYWxNVNUbYy2KokmeSqUObCWDlKQURbGtfDQVIGEtZxjmx1j3++b6g1ItmUxaypw2HFpPehPxPK96tYzjuC9Sz6f1xm9VqTSWZT0pAOVWsQPHThtQAiW3wPl8XkYG4IAP5RUWH7gDUKdCh5wLjOp7qVQiNZhB4I3FAEdVrhtISw10mDhSoOvjGGUaJE8rXBOXeheg9ukEG+jo/L8uDRe8Lr0B6MD1Xc3vi+KvAAMAMUEG36eXLzcAAAAASUVORK5CYII=&#34;&#62;
&#60;img class=&#34;hide&#34; src=&#34;data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAB8AAAAeCAYAAADU8sWcAAAAGXRFWHRTb2Z0d2FyZQBBZG9iZSBJbWFnZVJlYWR5ccllPAAAAyJpVFh0WE1MOmNvbS5hZG9iZS54bXAAAAAAADw/eHBhY2tldCBiZWdpbj0i77u/IiBpZD0iVzVNME1wQ2VoaUh6cmVTek5UY3prYzlkIj8+IDx4OnhtcG1ldGEgeG1sbnM6eD0iYWRvYmU6bnM6bWV0YS8iIHg6eG1wdGs9IkFkb2JlIFhNUCBDb3JlIDUuMC1jMDYwIDYxLjEzNDc3NywgMjAxMC8wMi8xMi0xNzozMjowMCAgICAgICAgIj4gPHJkZjpSREYgeG1sbnM6cmRmPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5LzAyLzIyLXJkZi1zeW50YXgtbnMjIj4gPHJkZjpEZXNjcmlwdGlvbiByZGY6YWJvdXQ9IiIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtcDpDcmVhdG9yVG9vbD0iQWRvYmUgUGhvdG9zaG9wIENTNSBNYWNpbnRvc2giIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6OTAyRDZFQUZFOEVFMTFFMDg2NkJGNDlCNjE5NENEMzIiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6OTAyRDZFQjBFOEVFMTFFMDg2NkJGNDlCNjE5NENEMzIiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDo5MDJENkVBREU4RUUxMUUwODY2QkY0OUI2MTk0Q0QzMiIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDo5MDJENkVBRUU4RUUxMUUwODY2QkY0OUI2MTk0Q0QzMiIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PlXiDkoAAAIdSURBVHjaxFfNasJAEN6sSkUIBOLBFktF0Junek+96wOU3tt76716tw/Q3msfQO8a8GhP3iKIpdJ6MBAIiEWE7shaos1m18SfD4ZFd2a/mc3szqyEBNHtdq/IAJKlsgmDSjufz7dF1pQESG/JcE1ERuL4JtIgTrz4IiekEN0TkVPkH+BEhTjx7jaJGcQlMtQDEiNq/0zX40dOFR/R7lElO9Bgku+ReIWyMxklB/EZGV55iTWbzUL9fl+xbftk9Z8syz+ZTMaKRqMLDrlN5IY48AU/wo6Jey9iINV1/XwwGKhu851OB6XTaVPTtE8PJ2TKU/6LnER9CYnBIh6Px7Fms5mdz+ch3r5GIpFFsVg0EonE1EPtDk7AKttLuyAGgB7og52HWsl51DSWVqvVuhAldjoAdh4qSz5Mt9z1W/d6PdWyrJiftAY7sGd9e+DFjHt6ieFwqAQ5Vxz7LPbK8NFoFIicYy+HRRaJx+NIVVVhUtM00WQy4ephdEQIRQ5RiESyLTC98lyRTCatIItz7G1Muw9XpFKpQOQcewPTQu8afS6XMxVFmfohBjuwZ0XtvF511iKFQuED7uttiEEf7DxUdGe2N1haUCCgUIg6IFhY6pv1vEa7U18lFSBQUhHtbstHbyYkl968tsd7Za2PW7vhaH9VPQQxs2/fQyP5j5j3aIA6X9nBo+GBEBtBnkulLZ2AxHrz/Vw6xEPxV4ABAB9p/+75XTbuAAAAAElFTkSuQmCC&#34;&#62;
&#60;nav class=&#34;outline toc pattern-bg-lighter&#34;&#62;
</p><h3>Table of Contents</h3>
<ul>

<li><a href="#toc-step1">Step 1: Wrap your Flash object with the audio tag</a></li>
<li><a href="#toc-step2">Step 2: Add the source reference</a></li>
<li><a href="#toc-step3">Step 3: Add fallback to Flash</a></li>
<li><a href="#toc-step4">Step 4: Add the default controls to show the player</a></li>
<li><a href="#toc-examples">Examples</a></li>
</ul>
<p>&#60;/nav&#62;
</p></div>
<p>&#60;section&#62;
</p><h2 id="toc-step1">Step 1: Wrap your Flash object with the audio tag</h2>
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