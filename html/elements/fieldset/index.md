---
title: 'fieldset'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://code.webplatform.org/gist/f77f0a06304503ecddd6'
  - 'http://code.webplatform.org/gist/fc26d3507ee33bdd6043'
  - 'http://code.webplatform.org/gist/91bca1371d394bf3c52d'
compatibility:
  feature: fieldset
  topic: html
notes:
  - 'Require manual conversion! See https://github.com/webplatform/mediawiki-conversion/issues/24'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLFieldSetElement](/dom/HTMLFieldSetElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The fieldset element is used to group related fields within a form.'
tags:
  - Markup_Elements
  - HTML
uri: html/elements/fieldset

---
<p>
</p>
<h2>Summary</h2>
<p>
The fieldset element is used to group related fields within a form.</p><p><br/></p>
<h2>Overview Table</h2>

<dl><dt><a href="/dom/interface"> DOM Interface</a></dt>
  <dd><a href="/dom/HTMLFieldSetElement">HTMLFieldSetElement</a></dd>
</dl><p>The <i>fieldset</i> element represents a set of form controls. Optionally given a name with a child <b>legend</b> element.
</p>
<h3>attributes</h3>
<p><b>NOTE</b>: Those attributes are considered valid since HTML5
</p>
<dl><dt> disabled </dt>
<dd> If this Boolean attribute is set, the form controls that are its descendants, except descendants of its first optional <b>legend</b> element, are disabled, i.e., not editable. They won't receive any browsing events, like mouse clicks or focus-related ones. Often browsers display such controls as gray.</dd>
<dt> form </dt>
<dd> This attribute has the value of the id attribute of the <b>form</b> element its related to. Its default value is the id of the nearest &lt;form&gt; element it is a descendant of.</dd>
<dt> name </dt>
<dd> The name associated with the group. This is for use in the <code>form.elements</code> API.</dd></dl><h2>Examples</h2>
<p>Simple form with fieldset, legend, and label elements.
</p>
<div class="example">
<pre class="html">
&lt;form action="" method="post"&gt;
  &lt;fieldset&gt;
    &lt;legend&gt;Title&lt;/legend&gt;
    &lt;label for="radio"&gt;Click me&lt;/label&gt;
    &lt;input type="radio" name="radio" id="radio"&gt;
  &lt;/fieldset&gt;
&lt;/form&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://code.webplatform.org/gist/f77f0a06304503ecddd6">View live example</a>
</p>
</div>
<p>The following snippet shows a <b>fieldset</b> with a checkbox in the legend that controls whether or not the fieldset is enabled.
</p>
<div class="example">
<pre class="html">
&lt;form&gt;
  &lt;fieldset name="clubfields" disabled&gt;
    &lt;legend&gt;
      &lt;label for="club"&gt;Use Club Card&lt;/label&gt;
      &lt;input type="checkbox" id="club" name="club" onchange="form.clubfields.disabled = !checked"&gt;
    &lt;/legend&gt;
    &lt;div&gt;
      &lt;label for="clubname"&gt;Name on card:&lt;/label&gt;
      &lt;input name="clubname" type="text"&gt;
    &lt;/div&gt;
    &lt;div&gt;
      &lt;label for="clubnum"&gt;Card number:&lt;/label&gt;
      &lt;input name="clubnum" type="number"&gt;
    &lt;/div&gt;
    &lt;div&gt;
      &lt;label for="clubnum"&gt;Expiry date:&lt;/label&gt;
      &lt;input name="clubexp" type="date"&gt;
    &lt;/div&gt;
  &lt;/fieldset&gt;
&lt;/form&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://code.webplatform.org/gist/fc26d3507ee33bdd6043">View live example</a>
</p>
</div>
<p>Example with nested <b>fieldset</b> elements.
</p>
<div class="example">
<pre class="html">
&lt;form action=""&gt;
  &lt;fieldset name="clubfields" disabled&gt;
    &lt;legend&gt;
      &lt;label for="club"&gt;Use Club Card&lt;/label&gt;
      &lt;input type="checkbox" name="club" id="club" onchange="form.clubfields.disabled = !checked"&gt;
    &lt;/legend&gt;
    &lt;div&gt;
      &lt;label for=""&gt;Name on card:&lt;/label&gt;
      &lt;input name="clubname"&gt;
    &lt;/div&gt;
    &lt;fieldset name="numfields"&gt;
      &lt;legend&gt;
        &lt;label for="clubtype"&gt;My card has numbers on it&lt;/label&gt;
        &lt;input type="radio" checked name="clubtype" id="clubtype" onchange="form.numfields.disabled = !checked"&gt;
      &lt;/legend&gt;
      &lt;div&gt;
        &lt;label for="clubnum"&gt;Card number:&lt;/label&gt;
        &lt;input name="clubnum" id="clubnum" type="text"&gt;
      &lt;/div&gt;
    &lt;/fieldset&gt;
    &lt;fieldset name="letfields" disabled&gt;
      &lt;legend&gt;
        &lt;label&gt;My card has letters on it&lt;/label&gt;
        &lt;input type="radio" name="clubtype" id="clubtype" onchange="form.letfields.disabled = !checked"&gt;
      &lt;/legend&gt;
      &lt;div&gt;
        &lt;label for="clublet"&gt;Card code:&lt;/label&gt;
        &lt;input name="clublet" id="clublet"&gt;
      &lt;/div&gt;
    &lt;/fieldset&gt;
  &lt;/fieldset&gt;
&lt;/form&gt;

</pre>
<p><a rel="nofollow" class="external text" href="http://code.webplatform.org/gist/91bca1371d394bf3c52d">View live example</a>
</p>
</div>
<h2>Usage</h2>
<pre> Fieldsets are not required but useful for grouping elements in a form to enhance the visual flow and usability of complex forms. optionally you can use a <a href="/html/elements/legend"><b>legend</b></a> element to give your <b>fieldset</b> element a caption.
</pre>
<h2>Notes</h2>
<h3>Default layout</h3>
<p>Typically, the browser draws a box around the containing elements of every fieldset. This border can be disabled via CSS <code>border: none;</code> The border contains the legend by default. See <a href="/html/elements/legend"><b>legend</b></a> for details.
</p><p>The <a rel="nofollow" class="external text" href="https://html.spec.whatwg.org/multipage/rendering.html#the-fieldset-and-legend-elements">"Rendering" section of the WHATWG HTML specification</a> suggests <a href="/css/properties/min-width"><code>min-width</code></a><code>: min-content</code> as part of the default style for <b>fieldset</b>, and many browsers implement such styling (or something that approximates it); almost no other element shares this default style. See also <a rel="nofollow" class="external text" href="http://stackoverflow.com/questions/17408815/fieldset-resizes-wrong-appears-to-have-unremovable-min-width-min-content">StackOverflow</a>, <a rel="nofollow" class="external text" href="https://bugzilla.mozilla.org/show_bug.cgi?id=504622">Mozilla bug #504622</a>, and <a rel="nofollow" class="external text" href="https://bugs.webkit.org/show_bug.cgi?id=123507">WebKit bug #123507</a>.
</p>
<h3>Nesting fieldsets</h3>
<p>It’s also possible and in certain use cases pretty useful to nest fieldsets.
</p>
<h3>Compatibility</h3>
<p>Not all form control descendants of a disabled <b>fieldset</b> are properly disabled in IE11; see <a rel="nofollow" class="external text" href="https://connect.microsoft.com/IE/feedbackdetail/view/817488">IE bug 817488: <code>input[type="file"]</code> not disabled inside disabled <code>fieldset</code></a> and <a rel="nofollow" class="external text" href="https://connect.microsoft.com/IE/feedbackdetail/view/962368/can-still-edit-input-type-text-within-fieldset-disabled">IE bug 962368: Can still edit <code>input[type="text"]</code> within <code>fieldset[disabled]</code></a>.
</p><p><br/></p>
<h2>Related specifications</h2>

<dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html51/forms.html#the-fieldset-element">HTML 5.1</a></dt>
  <dd>W3C Working Draft</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html5/forms.html#the-fieldset-element">HTML 5</a></dt>
  <dd>W3C Recommendation</dd>
</dl><dl><dt><a rel="nofollow" class="external text" href="http://www.w3.org/TR/html401/interact/forms.html#edef-FIELDSET">HTML 4.01</a></dt>
  <dd>W3C Recommendation</dd>
</dl><h2>See also</h2>
<h3>Related articles</h3>
<h4>HTML</h4>
<ul><li> <a href="/css/properties/user-modify">user-modify</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/HTMLTextAreaElement/textLength">textLength</a></li></ul><p><br/></p>
<ul><li> <a href="/dom/HTMLTextAreaElement/value">value</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/accept">accept</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/action">action</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/alt">alt</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/autocomplete">autocomplete</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/autofocus">autofocus</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/checked">checked</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/crossorigin">crossorigin</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/form">form</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/formEnctype">formEnctype</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/height">height</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/list">list</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/max_(HTMLInputElement)">max (HTMLInputElement)</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/maxLength">maxLength</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/min">min</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/multiple">multiple</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/readonly">readonly</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/size">size</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/standby">standby</a></li></ul><p><br/></p>
<ul><li> <a href="/html/attributes/step">step</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements">HTML Elements</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/!DOCTYPE">!DOCTYPE</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/!DOCTYPE/ja">!DOCTYPE</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/acronym">acronym</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/b">b</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/b/ja">b</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/br">br</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/br/ja">br</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/button">button</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/button/ja">button</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/caption">caption</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/cite">cite</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/code">code</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/col">col</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/colgroup">colgroup</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/datalist">datalist</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/del">del</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/dfn">dfn</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/div">div</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/em">em</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/embed">EMBED</a></li></ul><p><br/></p>
<ul><li> <strong class="selflink">fieldset</strong></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/font">font</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/footer">footer</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/head">head</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/hn">hn</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/hr">hr</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/html">html</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/i">i</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/img">img</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/input">input</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/ins">ins</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/kbd">kbd</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/legend">legend</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/mark">mark</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/option">option</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/p">p</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/samp">samp</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/script">script</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/span">span</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/strong">strong</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/table">table</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/tbody">tbody</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/td">td</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/tfoot">tfoot</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/th">th</a></li></ul><p><br/></p>
<ul><li> <a href="/html/elements/time">time</a></li></ul><p><br/></p>
<h3>Other articles</h3>
<ul><li> <a href="/html/elements/legend"><b>legend</b></a> element</li>
<li> <a href="/html/elements/form"><b>form</b></a> element</li></ul><h3>External resources</h3>
<ul><li> <a rel="nofollow" class="external free" href="http://www.w3.org/TR/html5/forms.html#the-fieldset-element">http://www.w3.org/TR/html5/forms.html#the-fieldset-element</a></li>
<li> <a rel="nofollow" class="external free" href="http://www.w3.org/TR/html5/rendering.html#the-fieldset-and-legend-elements">http://www.w3.org/TR/html5/rendering.html#the-fieldset-and-legend-elements</a></li>
<li> <a rel="nofollow" class="external free" href="http://www.w3.org/TR/html-markup/fieldset.html#fieldset">http://www.w3.org/TR/html-markup/fieldset.html#fieldset</a></li></ul>
