{{Page_Title|CSS variables}}
{{Flags
|High-level issues=Move Candidate
|Editorial notes={{Editorial/Move_Candidate
| Currently future tech.  Only in experimental stages.
}}
}}
{{Byline
|Name=Dave Gash
|URL=http://docs.webplatform.org/wiki/User:Dgash
|Published=October 10, 2012
}}
{{Summary_Section|CSS variables allow to re-use a given value across several CSS rules.}}
{{Guide
|Content===Introduction==
One of the fundamental features of procedural programming languages such as JavaScript is the ability to create a named element called a ''variable'', assign a value to it, and then later retrieve the value by referring to the variable by name. Variables lend power and flexibility to processes, allowing individual values to be abstracted from the code that uses them, and localizing the values for ease of maintenance and reuse. 

Historically, this feature has not been available in most declarative languages. In CSS, for example, in order to use a single value (e.g., a color) throughout a document, the value must be coded separately each time it is used. This scatters the various instances of the value, making it difficult to maintain and impossible to reuse.

The CSS Cascading Variables Module ([http://dev.w3.org/csswg/css-variables/ W3C spec]) introduces this feature into CSS. 

==Use==
This module describes a family of author-defined properties, called ''custom properties'', that allow you to assign arbitrary values to a property with a name of your choice, and a way to use them, called ''cascading variables'', that allow you to later use those values elsewhere in the document. This feature improves functionality and readability by replacing previously arbitrary values with descriptive, semantic names. It also simplifies maintenance and reuse by requiring only one instance of the actual value in the code, replacing later instances with the descriptive name.

'''Note:''' Rather than using different terms (''custom property'' and ''cascading variable'') for the declaration and retrieval of values, this article uses the simpler term ''variable'' throughout.

As with procedural language variables, using CSS variables is a two-step process. First, declare the variable by name and assign it a value; second, retrieve the value by using the variable name.

To declare a variable, prefix it with the string "var-" and assign it a value as you would any property. Thus <code>var-rightmargin: 50px;</code> creates the named variable "rightmargin" and assigns it a value of "50px".

To access the variable's value, use the notation syntax <code>var(''varname'')</code> as the value for a regular CSS property. Thus using <code>margin-right: var(rightmargin)</code> on an element assigns the "rightmargin" variable's current value of "50px" to the element's <code>margin-right</code> property.

==Examples==

===Swapping colors===
A common practice for hyperlinks in HTML is to swap the foreground and background colors of the link text during the hover state to indicate their potential for user interaction. This might be accomplished by rules similar to these:

<syntaxhighlight language="css">
a { text-decoration: none; color: #008080; background-color: #ddeeff; }
a:hover { color: #ddeeff; background-color: #008080; }
a:visited { color: #008080; background-color: #ddeeff; }
</syntaxhighlight>

This coding establishes all links as having dark teal text on a light blue background, changing to the inverse scheme, light blue text on a dark teal background, on hover. It also sets visited links to maintain the original unvisited dark teal on light blue combination, rather than changing to the default magenta color.

However, care must be taken to code the foreground and background colors correctly, especially when swapping them in the <code>:hover</code> pseudo-class rule, and to use them consistently in their original positions in the <code>:visited</code> pseudo-class rule. This minor complexity is compounded if the colors are used elsewhere in the style sheet or HTML document, as in containers, tables, or other elements.

Such complexity and its attendant errors can be avoided by using CSS variables. Using this technique, the rules above might be rewritten as:

<syntaxhighlight language="css">
:root { var-fgcolor: #008080; var-bgcolor: #ddeeff; }
a { text-decoration: none; color: var(fgcolor); background-color: var(bgcolor); }
a:hover { color: var(bgcolor); background-color: var(fgcolor); }
a:visited { color: var(fgcolor); background-color: var(bgcolor); }
</syntaxhighlight>

Here we use the variable names "fgcolor" for the foreground (text) color and "bgcolor" for the background color. 
Creating the variables in the <code>:root</code> rule has no immediate effect; the values are merely assigned and ready to be used. The effect is only actualized when the various <code>a</code> rules are applied to the document's hyperlinks.

Changing to a different color scheme for links now becomes trivial. Simply modify the values for var-fgcolor and var-bgcolor in the first rule, and the colors will be accurately propagated throughout the style sheet or document. It is clear from reading the code that the "fg" and "bg" colors are swapped on hover.

===Simplifying margins===
Consider a document where the major headers should each be of a different color but should all have the same left margin. For example:

<syntaxhighlight language="css">
h1 { color: red; margin-left: 20px; }
h2 { color: green; margin-left: 20px; }
h3 { color: blue; margin-left: 20px; }
</syntaxhighlight>

If the headers' margins need to change, all three rules must be edited. While that seems a straightforward task, this kind of repetitive maintenance can be error-prone, particularly if the various rules are not physically adjacent (as might be the case with nested or imported style sheets). 

Also, it can be time-consuming and frustrating, especially if you are tweaking the margins to get them just right; for every adjustment, however minor, you must correctly and consistently edit every header's rule. (And global search-and-replace is obviously problematic, as there may be numerous non-header, "20px" values in the document that you ''don't'' want to change.)

This problem can be avoided with the simple addition of a variable to set the margin, thus:

<syntaxhighlight language="css">
body { var-head-left-margin: 20px; }
. . .
h1 { color: red; margin-left: var(head-left-margin); }
h2 { color: green; margin-left: var(head-left-margin); }
h3 { color: blue; margin-left: var(head-left-margin); }
</syntaxhighlight>

Now, to tweak the margins of all the headers, you need only edit one instance of the value. Additionaly, the use of the variable provides a descriptive and semantically meaningful name, so that the header rules&mdash;wherever they are located&mdash;become more readable and the true value becomes easy to locate when a change is required.

==Gotchas==

===Variables are not property names===
Remember that variables are property ''values'', not property ''names'', and cannot be used as such. Thus the following code is invalid:

<syntaxhighlight language="css">
body { var-head-left-margin: margin-left; }
. . .
h1 { var(head-left-margin): 20px; }
</syntaxhighlight>

The <code>h1</code> rule now contains a syntax error and will be discarded.

===Values must match property types===
As with all property values, values provided via variables must match the property to which they are assigned. Thus the following code is also invalid:

<syntaxhighlight language="css">
body { var-head-color: 20px; }
. . .
h1 { color: var(head-color); }
</syntaxhighlight>

While syntactically correct, "20px" is not a valid value for the <code>color</code> property, so the <code>h1</code> rule will be discarded.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=No
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=No
|Internet_explorer_prefixed_version=
|Opera_supported=No
|Opera_version=
|Opera_prefixed_supported=No
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=No
|Android_version=
|Android_prefixed_supported=No
|Android_prefixed_version=
|Blackberry_supported=No
|Blackberry_version=
|Blackberry_prefixed_supported=No
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=No
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=No
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=No
|IE_mobile_version=
|IE_mobile_prefixed_supported=No
|IE_mobile_prefixed_version=
|Opera_mobile_supported=No
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=No
|Opera_mobile_prefixed_version=
|Opera_mini_supported=No
|Opera_mini_version=
|Opera_mini_prefixed_supported=No
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Note=Needs to turn the "Enable CSS variables" flag in about:flags
}}
}}
{{See_Also_Section
|External_links=[http://dev.w3.org/csswg/css-variables/ W3C CSS Cascading Variables Module Level 1 spec]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Notes_Section}}