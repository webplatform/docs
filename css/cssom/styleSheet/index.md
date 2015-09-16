---
title: 'styleSheet'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
readiness: 'Ready to Use'
summary: 'A style sheet in the document.'
tags:
  - API
  - Objects
  - DOM
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/methods/fireEvent
uri: css/cssom/styleSheet

---
<p><br/></p>
<h2>Summary</h2>
<p>
A style sheet in the document.</p><p><br/></p>
<h2>Properties</h2>

<dl><dt>API Name</dt>
  <dd>Summary</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/cssRules">cssRules</a></dt>
  <dd>Gets a list of CSS rules of a style sheet.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/cssText">cssText</a></dt>
  <dd>Gets or sets the textual representation of a style sheet.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/ownerNode">ownerNode</a></dt>
  <dd>Returns an element's corresponding <b>link</b> or <b>style</b> node. See Notes.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/ownerRule">ownerRule</a></dt>
  <dd>Gets the CSS Rule that imported the style sheet, if any.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/owningElement">owningElement</a></dt>
  <dd>Non standard. Returns the <b>style</b> or <b>link</b> object that defined the style sheet.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/pages">pages</a></dt>
  <dd/>
</dl><dl><dt><a href="/css/cssom/styleSheet/parentStyleSheet">parentStyleSheet</a></dt>
  <dd>Retrieves an element's parent style sheet.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/readOnly">readOnly</a></dt>
  <dd>Non standard. Indicates if the style sheet is currently in read only mode.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/rules">rules</a></dt>
  <dd>A collection of rules in a document's stylesheet.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/title">title</a></dt>
  <dd>A string used to identify a stylesheet.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/type">type</a></dt>
  <dd>The type of a document's stylesheet.</dd>
</dl><p><br/></p>
<h2>Methods</h2>

<dl><dt>API Name</dt>
  <dd>Summary</dd>
</dl><dl><dt><a href="/css/cssom/methods/addPageRule">addPageRule</a></dt>
  <dd>Not implemented anywhere. Non standard.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/addImport">addImport</a></dt>
  <dd>Non standard. Adds an @import rule to the style sheet.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/blockDirection">blockDirection</a></dt>
  <dd/>
</dl><dl><dt><a href="/css/cssom/styleSheet/deleteRule">deleteRule</a></dt>
  <dd>Deletes a CSS rule from the style sheet.</dd>
</dl><dl><dt><a href="/css/cssom/styleSheet/insertRule">insertRule</a></dt>
  <dd>Adds a new CSS rule to the stylesheet.</dd>
</dl><dl><dt><a href="/css/cssom/stylesheet/removeImport">removeImport</a></dt>
  <dd>Non standard. Removes an @import rule from the style sheet.</dd>
</dl><dl><dt><a href="/css/cssom/stylesheet/removeRule">removeRule</a></dt>
  <dd>Non standard. Removes a rule from a style sheet.</dd>
</dl><p><br/></p>
<h2>Events</h2>
<p><i>No events.</i>
</p>
<h2>Examples</h2>
<p>This example uses the <b>styleSheet</b> object to change the cascading style sheets (CSS) values of inline and imported styles.
</p>
<div class="example">
<pre class="html">
&lt;!doctype html&gt;
&lt;html&gt;
 &lt;head&gt;
  &lt;title&gt;&lt;/title&gt;
  &lt;style&gt;
BODY {background-color: #CFCFCF;}
@import url("otherStyleSheet.css");
  &lt;/style&gt;
  &lt;script&gt;
window.onload=fnInit;
function fnInit() {
   // Access a rule in the styleSheet, change backgroundColor to blue.
   var stylesheet = document.styleSheets[0];
   var rule = stylesheet.rules[0];
   rule.style.backgroundColor = "#0000FF";
   // Add a rule for P elements to have yellow backgrounds.
   stylesheet.addRule("P", "background-color: #FFFF00;");
   // Change and imported rule:
   stylesheet.imports[0].color = "#000000";
}
  &lt;/script&gt;
 &lt;/head&gt;
 &lt;body&gt;
 &lt;/body&gt;
&lt;/html&gt;

</pre>
<p><br/></p>
</div>
<h2>Notes</h2>
<p>You can use this object to retrieve style sheet information, such as the URL of the source file for the style sheet and the element in the document that owns (defines) the style sheet. You can also use it to modify style sheets.
You can retrieve a <b>styleSheet</b> object from the <a href="/css/cssom/styleSheets"><b>styleSheets</b></a> collection or from the <a href="/css/cssom/imports"><b>imports</b></a> collection. Each item in these collections is a style sheet. A <b>styleSheet</b> object is available for a style sheet only if it is included in a document with a <b>style</b> or <b>link</b> element, or with an <a href="/css/atrules/@import"><b>@import</b></a> statement in a <b>style</b> element.
</p>
<h4>Non Standard Methods</h4>
<p>The <b>styleSheet</b> object has these methods.
</p>
<table class="wikitable"><tr><th>Method
</th>
<th>Description
</th></tr><tr><td><a href="/css/cssom/methods/addRule"><b>addRule</b></a>
</td>
<td>Non standard. Creates a new rule for a style sheet.
</td></tr><tr><td><a href="/w/index.php?title=dom/methods/fireEvent&amp;action=edit&amp;redlink=1" class="new"><b>fireEvent</b></a>
</td>
<td>Fires a specified event on the object.
</td></tr></table><p> 
</p>
<h4>Non Standard Properties</h4>
<p>The <b>styleSheet</b> object has these properties.
</p>
<table class="wikitable"><tr><th>Property
</th>
<th>Description
</th></tr><tr><td><a href="/html/attributes/disabled"><b>disabled</b></a>
</td>
<td>Sets or retrieves a value that indicates whether the user can interact with the object.
</td></tr><tr><td><a href="/css/cssom/properties/href"><b>href</b></a>
</td>
<td>Sets or retrieves the URL of the linked style sheet.
</td></tr><tr><td><a href="/html/attributes/id"><b>id</b></a>
</td>
<td>Sets or retrieves the string identifying the object.
</td></tr><tr><td><a href="/css/cssom/properties/isAlternate"><b>isAlternate</b></a>
</td>
<td>Retrieves a value that indicates whether the styleSheet object is an alternative  style sheet.
</td></tr><tr><td><a href="/css/cssom/properties/isPrefAlternate"><b>isPrefAlternate</b></a>
</td>
<td>Retrieves a value that indicates whether the style sheet is the preferred style sheet.
</td></tr><tr><td><a href="/css/cssom/properties/media"><b>media</b></a>
</td>
<td>Sets or retrieves the media type.
</td></tr><tr><td><a href="/css/cssom/styleSheet/ownerNode"><b>ownerNode</b></a>
</td>
<td>Retrieves the node that associates this style sheet with the document.
</td></tr><tr><td><a href="/css/cssom/styleSheet/parentStyleSheet"><b>parentStyleSheet</b></a>
</td>
<td>Retrieves the style sheet that imported the current style sheets.
</td></tr><tr><td><a href="/css/properties/text-autospace"><b>textAutospace</b></a>
</td>
<td>Sets or retrieves  the autospacing and narrow space width adjustment of text.
</td></tr><tr><td><a href="/css/cssom/styleSheet/title"><b>title</b></a>
</td>
<td>Sets or retrieves the title of the style sheet.
</td></tr><tr><td><a href="/css/cssom/styleSheet/type"><b>type</b></a>
</td>
<td>Retrieves the CSS language in which the style sheet is written.
</td></tr></table><p> 
</p><p><br/></p>
<h2>See also</h2>
<h3>Related articles</h3>
<h4>CSSOM</h4>
<ul><li> <a href="/css/cssom/CSSImportRule/href">href</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSImportRule/media">media</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframeRule">CSSKeyframeRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframeRule/keyText">keyText</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframeRule/style">style</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule">CSSKeyframesRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/cssRules">cssRules</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/deleteRule">deleteRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/findRule">findRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/insertRule">insertRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSKeyframesRule/name">name</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/CSSMediaList">CSSMediaList</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/appendMedium">appendMedium</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/deleteMedium">deleteMedium</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/item">item</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaList/mediaText">mediaText</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/CSSMediaRule">CSSMediaRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/cssRules">cssRules</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/deleteRule">deleteRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/insertRule">insertRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSMediaRule/media">media</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSNamespaceRule/CSSNamespaceRule">CSSNamespaceRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSNamespaceRule/namespaceURI">namespaceURI</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSNamespaceRule/prefix">prefix</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSOM_view">CSSOM View</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSRule">CSSRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSRule/cssText">cssText</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSRule/parentStyleSheet">parentStyleSheet</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSRule/type">type</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/CSSStyleDeclaration/getPropertyPriority">getPropertyPriority</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/clipLeft">clipLeft</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/clipRight">clipRight</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/clipTop">clipTop</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/cssFloat">cssFloat</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/fontWeight">fontWeight</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/hasLayout">hasLayout</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/height">height</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/href">href</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/imports">imports</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/innerWidth">innerWidth</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/isAlternate">isAlternate</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/isPrefAlternate">isPrefAlternate</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/item">item</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/length">length</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/media">media</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/offsetX">offsetX</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/offsetY">offsetY</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/outerHeight">outerHeight</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/outerWidth">outerWidth</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pageX">pageX</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pageXOffset">pageXOffset</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pageY">pageY</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pageYOffset">pageYOffset</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/properties/pixelBottom">pixelBottom</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/screen/deviceXDPI">deviceXDPI</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/screen/deviceYDPI">deviceYDPI</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/screen/fontSmoothingEnabled">fontSmoothingEnabled</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/screen/height">height</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/style">style</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/style/type">type</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">styleSheet</strong></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/addImport">addImport</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/blockDirection">blockDirection</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/cssRules">cssRules</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/cssText">cssText</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/styleSheet/ownerNode">ownerNode</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/stylesheet/removeImport">removeImport</a></li></ul><p><br/></p>
<ul><li> <a href="/css/cssom/stylesheet/removeRule">removeRule</a></li></ul><p><br/></p>
<ul><li> <a href="/css/media_queries/apis/matchMedium">matchMedium</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/Window/getComputedStyle">getComputedStyle</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/Window/innerHeight">innerHeight</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/Window/styleMedia">styleMedia</a></li></ul>
