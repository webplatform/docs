==Summary==
The <code>fullscreenElement</code> property exposes the current full-screen state. If it is <code>null</code>, no document element is in full-screen mode; if it is not <code>null</code>, a document element is in full-screen mode.

==Value==
Returns the element that is currently displayed fullscreen, or 
<code>null</code> if there is no such element.

==Example==
<syntaxhighlight lang="javascript">
function queryFullScreen() {
  if (document.fullscreenElement == null) {
    // no element is in full-screen mode
    return false;
  }
  else {
    // an element is in full-screen mode
    return true;
  }
}
</syntaxhighlight>

==Related specifications==
[http://www.w3.org/TR/fullscreen/ W3C fullscreen working draft]

==See also==
Tutorial: [http://docs.webplatform.org/wiki/tutorials/using_the_full-screen_api Using the full-screen API]