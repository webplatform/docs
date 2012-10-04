{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Compatibility Incomplete, Examples Best Practices, Cleanup
}}
{{Standardization_Status|}}
{{API_Name}}
{{CSS_Selector
|Content=
}}
{{Topics|CSS}}
{{Examples_Section
|Not_required=No
|Examples={{Single_Example
|Description=The following examples show how to use the '''::first-line''' pseudo-element.

The following rule changes to uppercase the letters of the first line of elements with the specified [[dom/properties/className|'''className''']] property.

[http://samples.msdn.microsoft.com/workshop/samples/author/dhtml/refs/firstLine.htm Click to view sample.]

<span codelanguage{{=}}"CSS"><table>
<tr>
<th>CSS</th>
</tr>
<tr>
<td>
<pre>&lt;style&gt;
.CapFirst::first-line { text-transform: uppercase }
&lt;/style&gt;
&lt;p class{{=}}"CapFirst"&gt;The first line in this paragraph will be in 
all uppercase letters. Subsequent lines will render normally.  The 
first line in this paragraph will have uppercase letters. 
Subsequent lines will render normally.&lt;/p&gt;</pre>
</td>
</tr>
</table></span>

The following rules illustrate the cumulative effect of attaching '''::first-line''' and [[css/selectors/pseudo-elements/::first-letter|'''::first-letter''']] pseudo-elements to an element.

[http://go.microsoft.com/fwlink/p/?linkid{{=}}237892 Click to view sample.]

<span codelanguage{{=}}"CSS"><table>
<tr>
<th>CSS</th>
</tr>
<tr>
<td>
<pre>&lt;style&gt;
.LetterAndLine::first-line   { text-transform: uppercase }
.LetterAndLine::first-letter { font-size: 200%; float: left }
&lt;/style&gt;
&lt;p class{{=}}"LetterAndLine"&gt;The first letter in this paragraph will 
be twice the size of the other letters in the paragraph.  The 
first line in this paragraph will have uppercase letters.   
Subsequent lines will render normally.  The first letter in this 
paragraph will be twice the size of the other letters in the 
paragraph.  The first line in this paragraph will have uppercase 
letters. Subsequent lines will render normally.&lt;/p&gt;</pre>
</td>
</tr>
</table></span>

The following example uses the '''::first-line''' pseudo-element to create a typographical effect that looks like a column in a newspaper.
|LiveURL=Click to view sample.
|Code=
&lt;style&gt;
    .col1 { border-right: black 1px solid; 
        padding-right: 10px; 
        padding-left: 5px; 
        width: 140px;
        text-justify: newspaper
        }
    .newsitem::first-line { font-size: 14pt; 
        left: 0px; 
        float: left; 
        position: absolute; 
        top: 100px
        }
&lt;/style&gt;
&lt;div class{{=}}"col1"&gt;
&lt;div class{{=}}"newsitem"&gt;New features in Internet Explorer 5.5 include 
the first-line pseudo-element. This allows authors to create
typographical effects that are applied to the first line of a block 
of text.&lt;/div&gt;
&lt;/div&gt;
}}}}
{{Notes_Section
|Notes=
===Remarks===
The [[css/cssom/properties/background|'''background''']], [[css/properties/clear|'''clear''']], [[css/properties/color|'''color''']], [[css/properties/font|'''font''']], 
[[css/properties/font-family|'''font-family''']], [[css/properties/font-size|'''font-size''']], [[css/properties/font-style|'''font-style''']], [[css/fonts/font-variant|'''font-variant''']], [[css/properties/font-weight|'''font-weight''']], 
[[css/properties/line-height|'''line-height''']], [[css/properties/text-decoration|'''text-decoration''']], 
[[css/properties/text-transform|'''text-transform''']], [[css/properties/vertical-align|'''vertical-align''']], and [[css/text/word-spacing/word-spacing|'''word-spacing''']] properties apply to the '''::first-line''' pseudo-element.
The length of the first line depends on a number of factors, such as the width of the document and the font size.
The '''::first-line''' pseudo-element can be attached to block-level elements. It can be attached to inline elements if you set the corresponding [[css/properties/display|'''display''']] property to ''block''.
In versions of Windows Internet Explorer prior to Windows Internet Explorer 9, as well as in IE8 Standards mode and earlier, only the one-colon form of this pseudo-element is recognized—that is, ''':first-line'''.
Beginning with Internet Explorer 9, the '''::first-line''' pseudo-element requires two colons, though the one-colon form is still recognized and behaves identically to the two-colon form. Microsoft and the World Wide Web Consortium (W3C) encourage web authors to use the two-colon form of the '''::first-line''' pseudo-element. For more information, see the [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241611 Pseudo-elements] section of the W3C's [http://go.microsoft.com/fwlink/p/?LinkId{{=}}241612 CSS3 Selectors] specification.
|Import_Notes=
===Syntax===

sel
::first-line
===Parameters===
;''sel'':A simple selector.
===Standards information===
*[http://go.microsoft.com/fwlink/p/?linkid{{=}}203757 CSS 2.1], Section 5.12.1


}}
{{See_Also_Section
|Manual_sections=
===Related pages (MSDN)===
*<code>[[css/selectors/pseudo-elements/::first-letter|::first-letter]]</code>
|Topic_clusters=Selectors, Pseudo-Elements
}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|MDN_link=
|HTML5Rocks_link=
}}