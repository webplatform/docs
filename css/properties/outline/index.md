{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete, Examples Best Practices
|Checked_Out=No
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The CSS <code>outline</code> property is a shorthand property for setting one or more of the individual outline properties [[css/properties/outline-style|outline-style]], [[css/properties/outline-width|outline-width]] and [[css/properties/outline-color|outline-color]] in a single rule. In most cases the use of this shortcut is preferable and more convenient.}}
{{CSS_Selector
|Content=Outlines differ from [[css/properties/border|borders]] in the following ways:

* Outlines do not take up space, they are drawn above the content.
* Outlines may be non-rectangular. They are rectangular in Gecko/Firefox. Internet Explorer attempts to place the smallest contiguous outline around all elements or shapes that are indicated to have an outline. Opera draws a non-rectangular shape around a construct like this:

<strong style="color: green; outline: 1px dotted;">Web<span style="font-size: xx-large;">Platform</span>Docs</strong>
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=A simple example showing multiple '''div'''s, identical in style except that they have different '''outline''' properties applied to them.
|Code=&lt;div class=&quot;one&quot;&gt;I &amp;hearts; WebPlatform.org!&lt;/div&gt;
&lt;div class=&quot;two&quot;&gt;I &amp;hearts; WebPlatform.org!&lt;/div&gt;
&lt;div class=&quot;three&quot;&gt;I &amp;hearts; WebPlatform.org!&lt;/div&gt;
&lt;div class=&quot;four&quot;&gt;I &amp;hearts; WebPlatform.org!&lt;/div&gt;
&lt;div class=&quot;five&quot;&gt;I &amp;hearts; WebPlatform.org!&lt;/div&gt;
|LiveURL=http://code.webplatform.org/gist/5546931
}}{{Single Example
|Language=CSS
|Code=/**
 * outline example
 */

.one {
	/* The most basic border example you can show. */ 
	outline: 1px solid #000; 
}

.two {
	/* If you don't explicitly set a color, currentColor is used, which
     equates to the text colour of the element, in this case black.   */
	outline: 4px dashed;
}

.three {
 	/* When no width is specified, the default width medium is used */
	outline: dotted #f00; 
}

.four {
 	/* When no outline style is specified, the outline won't appear,
     as the default outline style is none. */
	outline: 5px #f00;
}

.five {
	/* A more interesting outline example to round things off. */
	outline: 10px inset #0f0;
}
|LiveURL=http://code.webplatform.org/gist/5546931
}}{{Single Example
|Language=CSS
|Description=Even though the syntax of outline and border is similar they differ in the way how they are drawn
|Code=/* Outlines do not take up space, they are drawn above the content */
.outline { outline: 10px solid #f00; }

/* Borders do */
.border { border: 10px solid #f00; }
|LiveURL=http://code.webplatform.org/gist/5546728
}}{{Single Example
|Language=HTML
|Description=An example of how outline and border behave when applied to an inline element which spans on multiple lines.
|Code=&lt;p&gt;Web Platform Docs is a community-driven site that aims to become &lt;span class=&quot;outline&quot;&gt;a comprehensive and authoritative source for web developer documentation.&lt;/span&gt;&lt;/p&gt;
&lt;p&gt;Web Platform Docs is a community-driven site that aims to become &lt;span class=&quot;border&quot;&gt;a comprehensive and authoritative source for web developer documentation.&lt;/span&gt;&lt;/p&gt;
&lt;p&gt;Web Platform Docs is a community-driven site that aims to become &lt;span class=&quot;outline border&quot;&gt;a comprehensive and authoritative source for web developer documentation.&lt;/span&gt;&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/5547019
}}{{Single Example
|Language=CSS
|Code=/**
 * Outline vs Border on multiline text
 */

.outline {
	/* The outline is drawn all around the spanning element. */
	outline: 2px solid #f06;
}

.border {
	/* The border does not close at the edge of the element
	 behaving as if it was a box. */
	border: 2px solid #00f;
}

/* The third paragraph has both outline and border */
|LiveURL=http://code.webplatform.org/gist/5547019
}}{{Single Example
|Language=HTML
|Description=Browsers place an outline around the element that currently has focus.
|Code=&lt;p&gt;Press the TAB key to navigate through the links below and focus them.&lt;/p&gt;
&lt;a href=&quot;http://webplatform.org&quot;&gt;I &amp;#9829; WebPlatform.org!&lt;/p&gt;
&lt;a class=&quot;two&quot; href=&quot;http://webplatform.org&quot;&gt;I &amp;hearts; WebPlatform.org!&lt;/p&gt;
|LiveURL=http://code.webplatform.org/gist/5547072
}}{{Single Example
|Language=CSS
|Code=/**
 * Outline, links and focus status
 */

/* Browsers place an outline around the element that currently has focus */

a {
	color: #f06;
	font: italic 200% Georgia, serif;
	text-decoration: none;	
}

.two:focus { 
	/* A different outline on focus for the second link */
	outline: 5px dotted #C67606; 
}

a:active,
a:hover {
	/* Improve readability when focused 
	and also mouse hovered in all browsers. */
	outline: 0;
}
|LiveURL=http://code.webplatform.org/gist/5547072
}}
}}
{{Notes_Section
|Notes====Remarks===
Displaying an outline does not cause reflow, no matter how wide the
outline is. The outline frame is drawn over an element, and does
not influence the position or size of the box, or of any other boxes.
This property requires Windows Internet Explorer to be in
IE8 Standards mode rendering.
|Import_Notes====Syntax===
<code>outline:  [ &lt;outline-width&gt; {{!}}{{!}} &lt;outline-style&gt; {{!}}{{!}} &lt;outline-color&gt; ] {{!}} inherit</code>

===Standards information===
*[http://www.w3.org/TR/CSS2/ui.html#dynamic-outlines CSS 2.1], Section 18.4
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
|Topic_clusters=Visual Effects
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Languages|css/properties/outline}}