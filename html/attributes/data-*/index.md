{{Page_Title|dataset and data-*}}
{{Flags
|State=Not Ready
|Editorial notes=Review import; Compatibility table; link examples to our code.webplatform.org playground; fix see also
|Checked_Out=No
|High-level issues=Split Candidate, Unreviewed Import, Needs Review
|Content=Cleanup, Examples Needed
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section}}
{{Markup_Attribute
|Content=<h5 id="embedding-custom-non-visible-data-with-the-data-*-attributes"><span class="secno">3.2.3.9 </span><dfn>Embedding custom non-visible data</dfn> with the <code title="attr-data-*"><a href="#attr-data-*">data-*</a></code> attributes</h5>

  <p>A <dfn id="custom-data-attribute">custom data attribute</dfn> is an attribute in no namespace whose name starts with the
  string "<dfn id="attr-data-*" title="attr-data-*"><code>data-</code></dfn>", has at least one character after the
  hyphen, is <a href="infrastructure.html#xml-compatible">XML-compatible</a>, and contains no <a href="infrastructure.html#uppercase-ascii-letters">uppercase ASCII letters</a>.</p>

  <p class="note">All attribute names on <a href="infrastructure.html#html-elements">HTML elements</a> in <a href="infrastructure.html#html-documents">HTML documents</a>
  get ASCII-lowercased automatically, so the restriction on ASCII uppercase letters doesn't affect
  such documents.</p>

  <p><a href="#custom-data-attribute" title="custom data attribute">Custom data attributes</a> are intended to store custom
  data private to the page or application, for which there are no more appropriate attributes or
  elements.</p>

  <p>These attributes are not intended for use by software that is independent of the site that uses
  the attributes.</p>

  <div class="example">

   <p>For instance, a site about music could annotate list items representing tracks in an album
   with custom data attributes containing the length of each track. This information could then be
   used by the site itself to allow the user to sort the list by track length, or to filter the list
   for tracks of certain lengths.</p>

   <pre>&lt;ol&gt;
 &lt;li data-length="2m11s"&gt;Beyond The Sea&lt;/li&gt;
 ...
&lt;/ol&gt;</pre>

   <p>It would be inappropriate, however, for the user to use generic software not associated with
   that music site to search for tracks of a certain length by looking at this data.</p>

   <p>This is because these attributes are intended for use by the site's own scripts, and are not a
   generic extension mechanism for publicly-usable metadata.</p>

  </div>

  <p>Every <a href="infrastructure.html#html-elements" title="HTML elements">HTML element</a> may have any number of <a href="#custom-data-attribute" title="custom data attribute">custom data attributes</a> specified, with any value.</p>

  <hr><dl class="domintro"><dt><var title="">element</var> . <code title="dom-dataset"><a href="#dom-dataset">dataset</a></code></dt>
   <dd>

    <p>Returns a <code><a href="infrastructure.html#domstringmap-0">DOMStringMap</a></code> object for the element's <code title="attr-data-*"><a href="#attr-data-*">data-*</a></code> attributes.</p>

    <p>Hyphenated names become camel-cased. For example, <code title="">data-foo-bar=""</code>
    becomes <code title="">element.dataset.fooBar</code>.</p>

   </dd>

  </dl><div class="impl">

  <p>The <dfn id="dom-dataset" title="dom-dataset"><code>dataset</code></dfn> IDL attribute provides convenient
  accessors for all the <code title="attr-data-*"><a href="#attr-data-*">data-*</a></code> attributes on an element. On
  getting, the <code title="dom-dataset"><a href="#dom-dataset">dataset</a></code> IDL attribute must return a
  <code><a href="infrastructure.html#domstringmap-0">DOMStringMap</a></code> object, associated with the following algorithms, which expose these
  attributes on their element:</p>
<dl><dt>The algorithm for getting the list of name-value pairs</dt>

   <dd>
    <ol><li>Let <var title="">list</var> be an empty list of name-value
     pairs.</li>

<!--CLEANUP-->
     <li>For each content attribute on the element whose first five characters are the string "<code title="">data-</code>" and whose remaining characters (if any) do not include any
     <a href="infrastructure.html#uppercase-ascii-letters">uppercase ASCII letters</a>,
     in the order that those attributes are listed in the element's <span>attributes list</span>,
     add a name-value pair to <var title="">list</var> whose
     name is the attribute's name with the first five characters removed and whose value is the
     attribute's value.</li>

     <li>For each name <var title="">list</var>, for each "-" (U+002D) character in the
     name that is followed by a <a href="infrastructure.html#lowercase-ascii-letters" title="lowercase ASCII letters">lowercase ASCII letter</a>,
     remove the "-" (U+002D) character and replace the character that followed it by the
     same character <a href="infrastructure.html#converted-to-ascii-uppercase">converted to ASCII uppercase</a>.</li>

     <li>Return <var title="">list</var>.</li>

    </ol></dd>

   <dt>The algorithm for setting names to certain values</dt>

   <dd>
    <ol><li>Let <var title="">name</var> be the name passed to the algorithm.</li>

     <li>Let <var title="">value</var> be the value passed to the algorithm.</li>

     <li>If <var title="">name</var> contains a "-" (U+002D) character followed by a
     <a href="infrastructure.html#lowercase-ascii-letters" title="lowercase ASCII letters">lowercase ASCII letter</a>, throw a
     <code><a href="infrastructure.html#syntaxerror">SyntaxError</a></code> exception and abort these steps.</li>

     <li>For each <a href="infrastructure.html#uppercase-ascii-letters" title="uppercase ASCII letters">uppercase ASCII letter</a> in <var title="">name</var>, insert a "-" (U+002D) character before the character and
     replace the character with the same character <a href="infrastructure.html#converted-to-ascii-lowercase">converted to ASCII lowercase</a>.</li>

     <li>Insert the string <code title="">data-</code> at the front of <var title="">name</var>.</li>

     <li>Set the value of the attribute with the name <var title="">name</var>, to the value <var title="">value</var>, replacing any previous value if the attribute already existed. If <code title="">setAttribute()</code> would have thrown an exception when setting an attribute with
     the name <var title="">name</var>, then this must throw the same exception.</li>

    </ol></dd>

   <dt>The algorithm for deleting names</dt>

   <dd>
    <ol><li>Let <var title="">name</var> be the name passed to the algorithm.</li>

<!--(can't happen while the DOMStringMap deleter has no name)
     <li>If <var title="">name</var> contains a "-" (U+002D) character followed by a
     <span title="lowercase ASCII letters">lowercase ASCII letter</span>, throw a
     <code>SyntaxError</code> exception and abort these steps.</li>
-->

     <li>For each <a href="infrastructure.html#uppercase-ascii-letters" title="uppercase ASCII letters">uppercase ASCII letter</a> in <var title="">name</var>, insert a "-" (U+002D) character before the character and
     replace the character with the same character <a href="infrastructure.html#converted-to-ascii-lowercase">converted to ASCII lowercase</a>.</li>

     <li>Insert the string <code title="">data-</code> at the front of <var title="">name</var>.</li>

     <li>Remove the attribute with the name <var title="">name</var>, if such an attribute exists.
     Do nothing otherwise.</li>

    </ol></dd>

  </dl><p>The same object must be returned each time.</p>

  </div>

  <div class="example">

   <p>If a Web page wanted an element to represent a space ship, e.g. as part of a game, it would
   have to use the <code title="attr-class"><a href="#classes">class</a></code> attribute along with <code title="attr-data-*"><a href="#attr-data-*">data-*</a></code> attributes:</p>

   <pre>&lt;div class="spaceship" data-ship-id="92432"
     data-weapons="laser 2" data-shields="50%"
     data-x="30" data-y="10" data-z="90"&gt;
 &lt;button class="fire"
         onclick="spaceships[this.parentNode.dataset.shipId].fire()"&gt;
  Fire
 &lt;/button&gt;
&lt;/div&gt;</pre>

   <p>Notice how the hyphenated attribute name becomes camel-cased in the API.</p>

  </div>

  <p>Authors should carefully design such extensions so that when the attributes are ignored and any
  associated CSS dropped, the page is still usable.</p>

  <div class="impl">

  <p>User agents must not derive any implementation behavior from these attributes or values.
  Specifications intended for user agents must not define these attributes to have any meaningful
  values.</p>

  </div>

  <p>JavaScript libraries may use the <a href="#custom-data-attribute" title="custom data attribute">custom data
  attributes</a>, as they are considered to be part of the page on which they are used. Authors
  of libraries that are reused by many authors are encouraged to include their name in the attribute
  names, to reduce the risk of clashes. Where it makes sense, library authors are also encouraged to
  make the exact name used in the attribute names customizable, so that libraries whose authors
  unknowingly picked the same name can be used on the same page, and so that multiple versions of a
  particular library can be used on the same page even when those versions are not mutually
  compatible.</p>

  <div class="example">

   <p>For example, a library called "DoQuery" could use attribute names like <code title="">data-doquery-range</code>, and a library called "jJo" could use attributes names like
   <code title="">data-jjo-range</code>. The jJo library could also provide an API to set which
   prefix to use (e.g. <code title="">J.setDataPrefix('j2')</code>, making the attributes have names
   like <code title="">data-j2-range</code>).</p>

  </div>
}}
{{Examples_Section
|Not_required=No
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=24.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=18.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.1
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=5.1
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=Android 3.0
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=iOS 5
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section
|External_links=<ul>
<li>Imported from:  <a href="http://www.w3.org/html/wg/drafts/html/master/dom.html#embedding-custom-non-visible-data-with-the-data-*-attributes">http://www.w3.org/html/wg/drafts/html/master/dom.html#embedding-custom-non-visible-data-with-the-data-*-attributes</a.</li>
</ul>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}