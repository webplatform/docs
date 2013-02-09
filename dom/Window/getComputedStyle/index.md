{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Gets the final used values of all the CSS properties of an element. The returned object is of the same type that the object returned from the element's [[css/cssom/style|"style"]] property, however the two objects have different purposes. The object returned from getComputedStyle is read-only and can be used to inspect the element's style (including those set by a <style> element or an external stylesheet). The elt.style object should be used to set styles on a specific element.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=element
|Data type=DOM Node
|Description=The element that contains the desired style settings.
|Optional=No
}}{{Method Parameter
|Name=pseudoElementName
|Data type=String
|Description=The name of a CSS pseudo-element or a null value ("::before" or "::after"). Optional in WebKit based browsers.
|Optional=Yes
}}
|Method_applies_to=dom/window
|Example_object_name=window
|Return_value_name=declaration
|Javascript_data_type=CSSStyleDeclaration
|Return_value_description=A [[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|'''CSSStyleDeclaration''']] object that contains the CSS settings applied to the desired object.

The settings in the returned object account for all applicable style rules and represent the final values for the various CSS properties applied to the specified object.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=var elem1 = document.getElementById("elemId");
var style = window.getComputedStyle(elem1, null);
 
// this is equivalent:
// var style = document.defaultView.getComputedStyle(elem1, null);
}}{{Single Example
|Language=HTML
|Code=&lt;style&gt;<br/> #elem-container{<br/>   position: absolute;<br/>   left:     100px;<br/>   top:      200px;<br/>   height:   100px;<br/> }<br/>&lt;/style&gt;<br/> <br/>&lt;div id=&quot;elem-container&quot;&gt;dummy&lt;/div&gt;<br/>&lt;div id=&quot;output&quot;&gt;&lt;/div&gt;  <br/> <br/>&lt;script&gt;<br/>  function getTheStyle(){<br/>    var elem = document.getElementById(&quot;elem-container&quot;);<br/>    var theCSSprop = window.getComputedStyle(elem,null).getPropertyValue(&quot;height&quot;);<br/>    document.getElementById(&quot;output&quot;).innerHTML = theCSSprop;<br/>   }<br/>  getTheStyle();<br/>&lt;/script&gt;
}}{{Single Example
|Language=HTML
|Description=getComputedStyle can pull style info off of pseudo-elements (for example, ::after, ::before, ::marker, ::line-marker).
|Code=&lt;style&gt;<br/> h3:after {<br/>   content: ' rocks!';<br/> }<br/>&lt;/style&gt;<br/> <br/>&lt;h3&gt;generated content&lt;/h3&gt; <br/> <br/>&lt;script&gt;<br/>  var h3       = document.querySelector('h3'), <br/>      result   = getComputedStyle(h3, ':after').content;<br/> <br/>  console.log('the generated content is: ', result); // returns ' rocks!'<br/>&lt;/script&gt;
}}
}}
{{Notes_Section
|Notes=The first argument must be an Element (passing a non-Element Node, like a #text Node, will throw an error). Starting in Gecko 1.9.2 (Firefox 3.6 / Thunderbird 3.1 / Fennec 1.0), returned URL values now have quotes around the URL, like this: url("http://foo.com/bar.jpg").

The returned object actually represents the CSS 2.1 used values, not the computed values. Originally, CSS 2.0 defined the computed values to be the "ready to be used" values of properties after cascading and inheritance, but CSS 2.1 redefined computed values as pre-layout, and used values as post-layout. The getComputedStyle function returns the old meaning of computed values, now called used values. There is no DOM API to get CSS 2.1 computed values.

The returned value is, in certain known cases, expressly incorrect by deliberate intent. In particular, to avoid the so called CSS History Leak security issue, browsers may expressly "lie" about the used value for a link and always return values as if a user has never visited the linked site, and/or limit the styles that can be applied using the :visited pseudo-selector. See http://blog.mozilla.com/security/2010/03/31/plugging-the-css-history-leak/ and http://hacks.mozilla.org/2010/03/privacy-related-changes-coming-to-css-vistited/ for details of the examples of how this is implemented, most other modern browser have applied similar changes to the application of pseudo-selector styles and the values returned by getComputedStyle.

During a CSS transition, getComputedStyle returns the original property value in FireFox, but the final property value in WebKit.

When the ''pseudoElementName'' is set to a value other than null, the value is interpreted as a CSS pseudo-element with respect to the object specified in the ''element'' parameter.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=DOM Level 2 Style
|URL=http://www.w3.org/TR/2000/REC-DOM-Level-2-Style-20001113/css.html
|Status=Recommendation
|Relevant_changes=Section 2.2.1
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=4
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=9
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=10.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=4
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=CSSOM
|External_links=[Microsoft Test Drive for getComputedStyle http://ie.microsoft.com/testdrive/HTML5/getComputedStyle/]
}}
{{Topics|DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/DOM/window.getComputedStyle
|HTML5Rocks_link=
}}