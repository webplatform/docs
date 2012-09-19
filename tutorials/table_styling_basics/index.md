{{Flags}}
{{Summary_Section|This article describes more advanced selectors, and some specific ways that you can style tables.}}
{{Tutorial
|Content=== Information: Tables ==
 
A table is an arrangement of information in a rectangular grid. Some tables can be complex, and for complex tables different browsers can give different results. When you design your document, use a table to express the [[relationships]] between the pieces of information. Then it does not matter if different browsers present the information in slightly different ways, because the meaning is still clear.
 
Do not use tables in unusual ways to produce particular visual layouts. The techniques on the previous page of this tutorial ('''[[Layout]]''') are better for that purpose.

=== Table structure ===
 
In a table, each piece of information is displayed in a ''cell''. The cells in a line across the page make up a ''row''.

In some tables, the rows might be grouped. A special group of rows at the start of the table is the ''header''. A special group of rows at the end of the table is the ''footer''. The main rows in the table are the ''body'', and they might also be in groups. The cells in a line down the page make up a ''column'', but columns have limited use in CSS tables.

====Table example====
 
The table of [[Selectors based on relationships]] in the [[Selectors]] page has ten cells in five rows. The first row is the header. The other four rows are the body. There is no footer. It has two columns.

This tutorial only covers simple tables, where the results are fairly predictable. In a simple table, every cell occupies only one row and column. You can use CSS for complex tables where cells ''span'' (extend across) more than one row or column, but tables like that are beyond the scope of this basic tutorial.

=== Borders ===
 
Cells have no margins.

Cells do have borders and padding. By default, the borders are separated by the value of the table's <code>[[border-spacing]]</code> property. You can also remove the spacing completely by setting the table's <code>[[border-collapse]]</code> property to <code>collapse</code>.
  
Table border example 

Here are three tables.

The table on the left has 0.5 em border spacing. The table in the center has zero border spacing. The table on the right has collapsed borders:

{{{!}} border="1"
{{!}}-
{{!}}            
{{{!}} border="1"
{{!}}-
{{!}}Clubs
{{!}}Hearts
{{!}}-
{{!}}Diamonds
{{!}}Spades
{{!}}} 
{{!}}            
{{{!}} border="1"
{{!}}-
{{!}}Clubs
{{!}}Hearts
{{!}}-
{{!}}Diamonds
{{!}}Spades
{{!}}} 
{{!}}            
{{{!}} border="1"
{{!}}-
{{!}}Clubs
{{!}}Hearts
{{!}}-
{{!}}Diamonds
{{!}}Spades
{{!}}} 
{{!}}}  
        
=== Captions ===
 
A <code>&lt;caption&gt;</code> element is a label that applies to the entire table. By default, it is displayed at the top of the table.
 
To move it to the bottom, set its <code>[[caption-side]]</code> property to <code>bottom</code>. The property is inherited, so alternatively you can set it on the table or another ancestor element.
 
To style the text of the caption, use any of the usual properties for text.
 
====Caption example==== 

This table has a caption at the bottom

<pre>#demo-table &gt; caption {
  caption-side: bottom;
  font-style: italic;
  text-align: right;
}</pre>
       
{{{!}} border="1"
{{!}}-
{{!}}        
{{{!}} border="1"
{{!}}+
              Suits
{{!}}-
{{!}}            
{{{!}} border="1"
{{!}}-
{{!}}Clubs
{{!}}Hearts
{{!}}-
{{!}}Diamonds
{{!}}Spades
{{!}}} 
{{!}}} 
{{!}}}  

=== Empty cells ===
 
You can display empty cells (that is, their borders and backgrounds) by specifying <code>[[empty-cells]]</code>: show; for the table element. You can hide them by specifying <code>empty-cells: hide;</code>. Then, if a cell's parent element has a background, it shows through the empty cell.
  
Empty cells example 

These tables have a pale green background. Their cells have a pale gray background and dark gray borders. In the table on the left, the empty cell is shown. On the right, it is hidden:
        
{{{!}} border="1"
{{!}}-
{{!}}            
{{{!}} border="1"
{{!}}-
{{!}} 
{{!}}Hearts
{{!}}-
{{!}}Diamonds
{{!}}Spades
{{!}}} 
{{!}}            
{{{!}} border="1"
{{!}}-
{{!}} 
{{!}}Hearts
{{!}}-
{{!}}Diamonds
{{!}}Spades
{{!}}} 
{{!}}}   
  
== Action: Styling a table ==

<ol>
<li><p>Make a new HTML document, <code>doc3.html</code>. Copy and paste the content from here, making sure that you scroll to get all of it:</p>

<pre>&lt;!DOCTYPE html&gt;
 &lt;html&gt;
   &lt;head&gt;
     &lt;title&gt;Sample document 3&lt;/title&gt;
     &lt;link rel="stylesheet" href="style3.css"&gt;
   &lt;/head&gt;
   &lt;body&gt;
     &lt;table id="demo-table"&gt;
       &lt;caption&gt;Oceans&lt;/caption&gt;
       &lt;thead&gt;
         &lt;tr&gt;
           &lt;th&gt;&lt;/th&gt;
           &lt;th&gt;Area&lt;/th&gt;
           &lt;th&gt;Mean depth&lt;/th&gt;
         &lt;/tr&gt;
         &lt;tr&gt;
           &lt;th&gt;&lt;/th&gt;
           &lt;th&gt;million km&lt;sup&gt;2&lt;/sup&gt;&lt;/th&gt;
           &lt;th&gt;m&lt;/th&gt;
         &lt;/tr&gt;
       &lt;/thead&gt;
       &lt;tbody&gt;
         &lt;tr&gt;
           &lt;th&gt;Arctic&lt;/th&gt;
           &lt;td&gt;13,000&lt;/td&gt;
           &lt;td&gt;1,200&lt;/td&gt;
         &lt;/tr&gt;
         &lt;tr&gt;
           &lt;th&gt;Atlantic&lt;/th&gt;
           &lt;td&gt;87,000&lt;/td&gt;
           &lt;td&gt;3,900&lt;/td&gt;
         &lt;/tr&gt;
         &lt;tr&gt;
           &lt;th&gt;Pacific&lt;/th&gt;
           &lt;td&gt;180,000&lt;/td&gt;
           &lt;td&gt;4,000&lt;/td&gt;
         &lt;/tr&gt;
         &lt;tr&gt;
           &lt;th&gt;Indian&lt;/th&gt;
           &lt;td&gt;75,000&lt;/td&gt;
           &lt;td&gt;3,900&lt;/td&gt;
         &lt;/tr&gt;
         &lt;tr&gt;
           &lt;th&gt;Southern&lt;/th&gt;
           &lt;td&gt;20,000&lt;/td&gt;
           &lt;td&gt;4,500&lt;/td&gt;
         &lt;/tr&gt;
       &lt;/tbody&gt;
       &lt;tfoot&gt;
         &lt;tr&gt;
           &lt;th&gt;Total&lt;/th&gt;
           &lt;td&gt;361,000&lt;/td&gt;
           &lt;td&gt;&lt;/td&gt;
         &lt;/tr&gt;
         &lt;tr&gt;
           &lt;th&gt;Mean&lt;/th&gt;
           &lt;td&gt;72,000&lt;/td&gt;
           &lt;td&gt;3,800&lt;/td&gt;
         &lt;/tr&gt;
       &lt;/tfoot&gt;
     &lt;/table&gt;
   &lt;/body&gt;
 &lt;/html&gt;</pre>
</li>
<li>
<p>Make a new stylesheet, <code>style3.css</code>. Copy and paste the content from here, making sure that you scroll to get all of it:</p>

<pre>/*** Style for doc3.html (Tables) ***/
 
 #demo-table {
   font: 100% sans-serif;
   background-color: #efe;
   border-collapse: collapse;
   empty-cells: show;
   border: 1px solid #7a7;
 }
 
 #demo-table &gt; caption {
   text-align: left;
   font-weight: bold;
   font-size: 200%;
   border-bottom: .2em solid #4ca;
   margin-bottom: .5em;
 }
 
 
 /* basic shared rules */
 #demo-table th,
 #demo-table td {
   text-align: right;
   padding-right: .5em;
 }
 
 #demo-table th {
   font-weight: bold;
   padding-left: .5em;
 }
 
 /* header */
 #demo-table &gt; thead &gt; tr:first-child &gt; th {
   text-align: center;
   color: blue;
 }
 
 #demo-table &gt; thead &gt; tr + tr &gt; th {
   font-style: italic;
   color: gray;
 }
 
 /* fix size of superscript */
 #demo-table sup {
   font-size: 75%;
 }
 
 /* body */
 #demo-table td {
   background-color: #cef;
   padding:.5em .5em .5em 3em;
 }
 
 #demo-table tbody th:after {
   content: ":";
 }
 
 /* footer */
 #demo-table tfoot {
   font-weight: bold;
 }
 
 #demo-table tfoot th {
   color: blue;
 }
 
 #demo-table tfoot th:after {
   content: ":";
 }
 
 #demo-table &gt; tfoot td {
   background-color: #cee;
 }
 
 #demo-table &gt; tfoot &gt; tr:first-child td {
   border-top: .2em solid #7a7;
 }</pre>
</li>
<li>
<p>Open the document in your browser. It should look very similar to this:</p>

{{{!}} border="1" {{!}}- {{!}}  Oceans                                                    {{{!}} border="1" {{!}}- ! !Area !Mean depth {{!}}- ! !million km<sup>2</sup> !m {{!}}- !Arctic: {{!}}13,000 {{!}}1,200 {{!}}- !Atlantic: {{!}}87,000 {{!}}3,900 {{!}}- !Pacific: {{!}}180,000 {{!}}4,000 {{!}}- !Indian: {{!}}75,000 {{!}}3,900 {{!}}- !Southern: {{!}}20,000 {{!}}4,500 {{!}}- !Total: {{!}}361,000 {{!}} {{!}}- !Mean: {{!}}72,000 {{!}}3,800 {{!}}}   {{!}}}
</li>
<li><p>Compare the rules in the stylesheet with the displayed table, to ensure that you understand the effect of each rule. If you find a rule that you are not sure about, comment it out and refresh your browser to see what happens. Here are some notes about this table:</p>
<ul>
  <li>
    <p>The caption lies outside the table border.</p>
  </li>
  <li>
    <p>If you have a minimum point size set in Options, it might affect the superscript in km<sup>2</sup>.</p>
  </li>
  <li>
    <p>There are three empty cells. Two of them allow the table background to show through. The third has a background and a top border.</p>
  </li>
  <li>
    <p>The colons are added by the stylesheet.</p>
  </li>
</ul>
</li>
</ol>
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|External_links=For detailed information about tables, see [[Tables]] in the CSS Specification. The information there goes further than this tutorial, but it does not cover differences between browsers that can affect complex tables.
|Manual_sections====Exercise question=== 

Change the stylesheet to make the table look like this:
       
{{{!}} border="1"
{{!}}-
{{!}}                                                   
{{{!}} border="1"
{{!}}-
! 
!Area
!Mean depth
{{!}}-
! 
!million km<sup>2</sup>
!m
{{!}}-
!Arctic:
{{!}}13,000
{{!}}1,200
{{!}}-
!Atlantic:
{{!}}87,000
{{!}}3,900
{{!}}-
!Pacific:
{{!}}180,000
{{!}}4,000
{{!}}-
!Indian:
{{!}}75,000
{{!}}3,900
{{!}}-
!Southern:
|20,000
{{!}}4,500
{{!}}-
!Total:
{{!}}361,000
{{!}} 
{{!}}-
!Mean:
{{!}}72,000
{{!}}3,800
{{!}}}  
Oceans

  
{{!}}}
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=Yes
|Sources=MDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Tables
|MSDN_link=
|HTML5Rocks_link=
}}