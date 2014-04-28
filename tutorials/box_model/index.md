{{Page_Title|Exploring the CSS box model}}
{{Flags
|Content=Incomplete, Cleanup
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|This article briefly describes the CSS box model and how the elements are layed out when they are displayed.

}}
{{Tutorial
|Content=== Information: Box Model ==
 
When your browser displays an element, the element takes up space. You can think of all HTML elements as boxes. All boxes have  certain dimensions and are specified by four properties: a content area of the element (e.g., a picture, a  text header, etc.) and the optional padding, border and margin properties.

The element is in the center and displays its content. Around that, there is padding. Around that, there is a border. Around that, there is a margin that separates the element from other elements.

The "edges" or the perimeters of each of the previous areas can have different properties defined on them.

Thus the content edge can have a certain width or height, the padding edge that surrounds the content can have a certain width or height etc.

Each property that surrounds the content can be broken down into a top, right, bottom, or a left part for example margin-left, padding-bottom, border-left etc.

        
{{{!}} border="1"
{{!}}-
{{!}} 
margin

 
border

  
padding

  
element

    
''The pale gray shows parts of the layout.''

 
{{!}}       
element

    
''This is what you see in your browser.''

 
{{!}}} 

The padding, border and margin can have different sizes on the top, right, bottom and left of the element. Any or all of these sizes can be zero.

 
=== Coloring ===
 
The padding is always the same color as the element's background. So when you set the background color, you see the color applied to the element itself and its padding. The margin is always transparent.
     
{{{!}} border="1"
{{!}}-
{{!}}  
margin

 
border

  
padding

  
element

    
''The element has a green background.''

 
{{!}}       
element

    
''This is what you see in your browser.''

 
{{!}}}
 
=== Borders ===
 
You can use borders to decorate elements with lines or boxes. To specify the same border all around an element, use the {{ cssxref("border") }} property. Specify the width (usually in pixels for display on a screen), the style, and the color.

The styles are:

                
{{{!}} border="1"
{{!}}-
{{!}}  <code>solid</code> 
{{!}}  <code>dotted</code> 
{{!}}  <code>dashed</code> 
{{!}}  <code>double</code> 
{{!}}-
{{!}}  <code>inset</code> 
{{!}}  <code>outset</code> 
{{!}}  <code>ridge</code> 
{{!}}  <code>groove</code> 
{{!}}} 

You can also set the style to <code>none</code> or <code>hidden</code> to explicitly remove the border, or set the color to <code>transparent</code> to make the border invisible without changing the layout.

To specify borders one side at a time, use the properties: {{ cssxref("border-top") }}, {{ cssxref("border-right") }}, {{cssxref("border-bottom")}}, {{cssxref("border-left")}}. You can use these to specify a border on only one side, or different borders on different sides.

Border example 
This rule sets the background color and the top border of heading elements:

<syntaxhighlight lang="css">h3 {
  border-top: 4px solid #7c7; /* mid green */
  background-color: #efe;     /* pale green */
  color: #050;                /* dark green */
}</syntaxhighlight>
 
The result looks like:

<p class="note">Note: add screenshot to show what this should look like.</p>
 
This rule makes images easier to see by giving them a mid-gray border all round:

<syntaxhighlight lang="css">img {border: 2px solid #ccc;}</syntaxhighlight>
  
The result looks like:

<p class="note">Note: add screenshot to show what this should look like.</p>
   
=== Margins and padding ===
 
You use margins and padding to adjust elements' positions and to create space around them. Use the {{ cssxref("margin") }} property or the {{ cssxref("padding") }} property to set the margin or padding widths respectively.

If you specify one width, it applies all around the element (top, right, bottom and left). If you specify two widths, the first applies to the top and bottom, the second to the right and left. You can specify all four widths in the order: top, right, bottom, left.

===Margin and padding example===

This rule marks out paragraphs with the class <code>remark</code> by giving them a red border all round. Padding all round separates the border from the text a little. A left margin indents the paragraph relative to the rest of the text:

<syntaxhighlight lang="css">p.remark {
  border: 2px solid red;
  padding: 4px;
  margin-left: 24px;
}</syntaxhighlight>
 
The result looks like:

<p class="note">Note: add screenshot to show what this should look like.</p>  

==More details== 

When you use margins and padding to adjust the way elements are laid out, your style rules interact with the browser's defaults in ways that can be complex. Different browsers lay elements out differently. The results might look similar until your stylesheet changes things. Sometimes this can make your stylesheet give surprising results.

To get the result you want, you might have to change your document's markup. The next page of this tutorial has more information on this. For detailed information about padding, margins and borders, see the [[Box model]] reference page.
  
== Action: Adding borders ==
 
<ul>
<li><p>Edit your CSS file, <code>style2.css</code>. Add this rule to draw a line across the page over each heading:</p>

<syntaxhighlight lang="css">h3 {border-top: 1px solid gray;}</syntaxhighlight>
 </li>
<li>
<p>If you took the challenge on the last page, modify the rule you created, otherwise add this new rule to add space underneath each list item:</p>
 
<syntaxhighlight lang="css">li {
  list-style: lower-roman;
  margin-bottom: 8px;
}</syntaxhighlight>
</li>
<li> 
<p>Refresh your browser to see the result:</p>

<p class="note">Need to add in a screenshot to show what this should look like.</p>
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections====Exercise questions===

Add one rule to your stylesheet, making a wide border all around the oceans in a color that reminds you of the sea.
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Boxes
|MSDN_link=
|HTML5Rocks_link=
}}