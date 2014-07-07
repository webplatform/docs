{{Page_Title|:target pseudo-class selector}}
{{Flags
|State=Not Ready
|Editorial notes=No matching spec
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The <tt>:target</tt> pseudo-class (note the ":") represents an element in the current document, if any, that has id attribute set to a name that is matching the fragment identifier of the current URI.}}
{{CSS_Selector
|Content=An URI fragment is what follows the "number sign" (<tt>#</tt>).

[[File:example-css-target-pseudo-activated.png]]

URIs with fragment identifier can be used to link to a specific part of a document, known as the target element. This also how we can navigate directly to a section of a page long without scrolling manually.

Scrolling automatically to a fragment is not the only benefit; It is also possible to target and style those elements through CSS.

Let us say you have a section in a document called "<tt>foo</tt>" (e.g. <tt>&lt;div id="foo"&gt;...&lt;/div&gt;</tt>), and you want to style it differently when it gets linked. When somebody navigates to that page with the appropriate URI fragment in the address bar (e.g. <tt>http://example.com/some/page.html#foo</tt>) we then can adjust the style to suit our requirements.

Any element can be a target, as long as it has the <tt>id=".."</tt> attribute set, and the current URI matches it. To use the selector, we use the <code>:target</code> pseudo-class notation. If the document's URI has no fragment identifier, then the document has no target element.

== Using the selector ==

To use the selector, append the pseudo selector (<tt>:target</tt>) after a selector string.

<syntaxHighlight lang="css">
  .note:target { /* ... */ }
</syntaxHighlight>

In this example, the selector targets an element that has a [[css/selectors/class|''class name'' selector]] <tt>note</tt> and will be used when its matching elements also has an <tt>id</tt> attribute matching the current URI.

Since it is a pseudo selector, it has to be at the end of the chain (e.g. <tt>tagName#idName.className:pseudo-selector</tt>).

For example, to change the background color of ANY tag that happens to be refered in the URI, you can do like the following:

<syntaxHighlight lang="css">
*:target { background-color: red }
</syntaxHighlight>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=Changing background color of an element that has an id attribute with a name that matches the current URI after the pound (#)
|Code=*:target {
  background-color: #f06;
 /* any element that has an id attribute matching
    in the URI will have the background color
    affected to pink */
}
|LiveURL=http://code.webplatform.org/gist/6f2803eda8ad3c66aaf4
}}
}}
{{Notes_Section
|Notes=The <tt>id</tt> attribute was new in HTML 4 (December 1997). Before that, we were using the name attribute in an ahcnor tag (e.g. &lt;a name="foo"&gt;.  The <tt>:target</tt> pseudo-class applies to those targets as well.
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Pseudo-Classes
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}