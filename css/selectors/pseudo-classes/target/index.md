{{Page_Title|:target pseudo-class selector}}
{{Flags
|State=Not Ready
|Editorial notes=No matching spec
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|Refer in the current document to a section that has a matching id}}
{{CSS_Selector
|Content=Some URIs refer to a location within a resource. This kind of URI ends with a "number sign" (<tt>#</tt>) followed by an anchor identifier (called the fragment identifier).

URIs with fragment identifier links to a certain element within the document, known as the target element. For instance, here is a URI pointing to an anchor named <tt>section_2</tt> in an HTML document  (e.g. <tt>&lt;div id="section_2"&gt;...&lt;/div&gt;</tt>), and we can refer to it with its matching URI <tt>http://example.com/html/top.html#section_2</tt>

A target element can be represented by the <code>:target</code> pseudo-class. If the document's URI has no fragment identifier, then the document has no target element.

== Using the selector ==
To use the selector, append the pseudo selector (<tt>:target</tt>) after a selector string.

<syntaxHighlight lang="css">
  .note:target { /* ... */ }
</syntaxHighlight>

In this example, the selector targets an element that has a [[css/selectors/class|''class name'' selector]] <tt>note</tt> and will be used when its matching elements also has an <tt>id</tt> attribute matching the current URI.

Here, the <tt>:target</tt> pseudo-class is used to make the target element red and place an image before it, if there is one:

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
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}