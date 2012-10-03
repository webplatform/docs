{{Page_Title|Simple Asset Management for HTML5 Games}}
{{Flags}}
{{Byline
|Name=Seth Ladd
|URL=http://www.html5rocks.com/profiles/#sethladd
|Published=July 2, 2011
}}
{{Summary_Section|Centralize and manage the asset downloads for your HTML5 game.}}
{{Tutorial}}
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
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/tutorials/games/assetmanager/
}}
}




}




</pre>

==Bonus: Bug Fix==

Did you spot the bug?  As written above, the isDone method is only called when either load or error events are triggered. But what if the asset manager doesn’t have any assets queued up for download?  The isDone method is never triggered, and the game never starts.

You can accommodate this scenario by adding the following code to <code>downloadAll()</code>:

<pre>AssetManager.prototype.downloadAll = function(downloadCallback) {
  if (this.downloadQueue.length === 0) {
      downloadCallback();
  }
 ...
}
</pre>

If no assets are queued, the callback is called immediately. Bug fixed!

==Example Usage==

Using this asset manager in your HTML5 game is quite straightforward. Here is the most basic way to use the library:

<pre>var ASSET_MANAGER = new AssetManager();

ASSET_MANAGER.queueDownload('img/earth.png');

ASSET_MANAGER.downloadAll(function() {
    var sprite = ASSET_MANAGER.getAsset('img/earth.png');
    ctx.drawImage(sprite, x - sprite.width/2, y - sprite.height/2);
});
</pre>

The above code illustrates:

# Creates a new asset manager
# Queue up assets to be downloaded
# Start the downloads with <code>downloadAll()</code>
# Signal when the assets are ready by invoking the callback function
# Retrieve assets with <code>getAsset()</code>

==Areas for Improvement==

You will no doubt outgrow this simple asset manager as you build out your game, although I hope it provided a basic start. Future features could include:

* signaling which asset had an error
* callbacks to indicate progress
* retrieving assets from the File System API

Please post improvements, forks, and links to code in the comments below.

==Full Source== 

The source for this asset manager, and the game it’s abstracted from, is open source under the Apache License and can be found in the <a href="https://github.com/sethladd/Bad-Aliens">Bad Aliens GitHub account</a>. The <a href="http://bad-aliens.appspot.com/">Bad Aliens game</a> can be played in your HTML5 compatible browser. This game was the subject for my Google IO talk titled Super Browser 2 Turbo HD Remix: Introduction to HTML5 Game Development (<a href="http://io-2011-html5-games-hr.appspot.com">slides</a>, <a href="http://www.youtube.com/watch?v=yEocRtn_j9s">video</a>).

==Summary==

Most games have some sort of asset manager, but HTML5 games require an asset manager that loads assets over a network and handles failures. This article outlined a simple asset manager that should be easy for you to use and adapt for your next HTML5 game. Have fun, and please let us know what you think in the comments below. Thanks!


}}