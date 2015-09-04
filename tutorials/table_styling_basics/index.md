---
title: table styling basics
tags:
  - Tutorials
  - CSS
readiness: 'Ready to Use'
summary: 'This article describes more advanced selectors, and some specific ways that you can style tables.'
uri: 'tutorials/table styling basics'

---
# Table styling basics

## Summary

This article describes more advanced selectors, and some specific ways that you can style tables.

## Information: Tables

A table is an arrangement of information in a rectangular grid. Some tables can be complex, and for complex tables different browsers can give different results. When you design your document, use a table to express the relationships among the pieces of information. Then it does not matter if different browsers present the information in slightly different ways, because the meaning is still clear.

Do not use tables in unusual ways to produce particular visual layouts.

### Table structure

In a table, each piece of information is displayed in a *cell*. The cells in a line across the page make up a *row*.

In some tables, the rows might be grouped. A special group of rows at the start of the table is the *header*. A special group of rows at the end of the table is the *footer*. The main rows in the table are the *body*, and they might also be in groups. The cells in a line down the page make up a *column*, but columns have limited use in CSS tables.

#### Table example

This tutorial only covers simple tables, where the results are fairly predictable. In a simple table, every cell occupies only one row and column. You can use CSS for complex tables where cells *span* (extend across) more than one row or column, but tables like that are beyond the scope of this basic tutorial.

### Borders

Cells have no margins.

Cells do have borders and padding. By default, the borders are separated by the value of the table's `border-spacing` property. You can also remove the spacing completely by setting the table's `border-collapse` property to `collapse`.

Table border example

Here are three tables.

The table on the left has 0.5 em border spacing. The table in the center has zero border spacing. The table on the right has collapsed borders:

<dl>
<dt>
||
|Clubs|Hearts|
|Diamonds|Spades|

</dt>
<dd>
||
|Clubs|Hearts|
|Diamonds|Spades|

</dd>
</dl>
### Captions

A `<caption>` element is a label that applies to the entire table. By default, it is displayed at the top of the table.

To move it to the bottom, set its `caption-side` property to `bottom`. The property is inherited, so alternatively you can set it on the table or another ancestor element.

To style the text of the caption, use any of the usual properties for text.

#### Caption example

This table has a caption at the bottom

    #demo-table > caption {
      caption-side: bottom;
      font-style: italic;
      text-align: right;
    }

<table>
<col width="100%" />
<tbody>
<tr class="odd">
<td align="left"><table>
<caption> Suits </caption>
<col width="100%" />
<tbody>
<tr class="odd">
<td align="left"><dl>
<dt>Clubs</dt>
<dd>Hearts
</dd>
<dt>Diamonds</dt>
<dd>Spades
</dd>
</dl></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

### Empty cells

You can display empty cells (that is, their borders and backgrounds) by specifying `empty-cells`: show; for the table element. You can hide them by specifying `empty-cells: hide;`. Then, if a cell's parent element has a background, it shows through the empty cell.

Empty cells example

These tables have a pale green background. Their cells have a pale gray background and dark gray borders. In the table on the left, the empty cell is shown. On the right, it is hidden:

<dl>
<dt>
||
||Hearts|
|Diamonds|Spades|

</dt>
<dd>
||
||Hearts|
|Diamonds|Spades|

</dd>
</dl>
## Action: Styling a table

1.  Make a new HTML document, `doc3.html`. Copy and paste the content from here, making sure that you scroll to get all of it:

        <!DOCTYPE html>
         <html>
           <head>
             <title>Sample document 3</title>
             <link rel="stylesheet" href="style3.css">
           </head>
           <body>
             <table id="demo-table">
               <caption>Oceans</caption>
               <thead>
                 <tr>
                   <th></th>
                   <th>Area</th>
                   <th>Mean depth</th>
                 </tr>
                 <tr>
                   <th></th>
                   <th>million km<sup>2</sup></th>
                   <th>m</th>
                 </tr>
               </thead>
               <tbody>
                 <tr>
                   <th>Arctic</th>
                   <td>13,000</td>
                   <td>1,200</td>
                 </tr>
                 <tr>
                   <th>Atlantic</th>
                   <td>87,000</td>
                   <td>3,900</td>
                 </tr>
                 <tr>
                   <th>Pacific</th>
                   <td>180,000</td>
                   <td>4,000</td>
                 </tr>
                 <tr>
                   <th>Indian</th>
                   <td>75,000</td>
                   <td>3,900</td>
                 </tr>
                 <tr>
                   <th>Southern</th>
                   <td>20,000</td>
                   <td>4,500</td>
                 </tr>
               </tbody>
               <tfoot>
                 <tr>
                   <th>Total</th>
                   <td>361,000</td>
                   <td></td>
                 </tr>
                 <tr>
                   <th>Mean</th>
                   <td>72,000</td>
                   <td>3,800</td>
                 </tr>
               </tfoot>
             </table>
           </body>
         </html>

2.  Make a new stylesheet, `style3.css`. Copy and paste the content from here, making sure that you scroll to get all of it:

        /*** Style for doc3.html (Tables) ***/

         #demo-table {
           font: 100% sans-serif;
           background-color: #efe;
           border-collapse: collapse;
           empty-cells: show;
           border: 1px solid #7a7;
         }

         #demo-table > caption {
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
         #demo-table > thead > tr:first-child > th {
           text-align: center;
           color: blue;
         }

         #demo-table > thead > tr + tr > th {
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

         #demo-table > tfoot td {
           background-color: #cee;
         }

         #demo-table > tfoot > tr:first-child td {
           border-top: .2em solid #7a7;
         }

3.  Open the document in your browser. It should look very similar to this:

    <table>
    <col width="100%" />
    <tbody>
    <tr class="odd">
    <td align="left">Oceans
    <dl>

    <dd>Area
    </dd>

    <dd>million km<sup>2</sup>
    </dd>
    <dt>Arctic:</dt>
    <dd>13,000
    </dd>
    <dt>Atlantic:</dt>
    <dd>87,000
    </dd>
    <dt>Pacific:</dt>
    <dd>180,000
    </dd>
    <dt>Indian:</dt>
    <dd>75,000
    </dd>
    <dt>Southern:</dt>
    <dd>20,000
    </dd>
    <dt>Total:</dt>
    <dd>361,000
    </dd>
    <dt>Mean:</dt>
    <dd>72,000
    </dd>
    </dl></td>
    </tr>
    </tbody>
    </table>

4.  Compare the rules in the stylesheet with the displayed table, to ensure that you understand the effect of each rule. If you find a rule that you are not sure about, comment it out and refresh your browser to see what happens. Here are some notes about this table:

    -   The caption lies outside the table border.

    -   If you have a minimum point size set in Options, it might affect the superscript in km<sup>2</sup>.

    -   There are three empty cells. Two of them allow the table background to show through. The third has a background and a top border.

    -   The colons are added by the stylesheet.

## See also

### External resources

For detailed information about tables, see [Tables in the CSS Specification](http://www.w3.org/TR/CSS21/tables.html). The information there goes further than this tutorial, but it does not cover differences between browsers that can affect complex tables.

### Exercise question

Change the stylesheet to make the table look like this:

<table>
<col width="100%" />
<tbody>
<tr class="odd">
<td align="left"><dl>

<dd>Area
</dd>

<dd>million km<sup>2</sup>
</dd>
<dt>Arctic:</dt>
<dd>13,000
</dd>
<dt>Atlantic:</dt>
<dd>87,000
</dd>
<dt>Pacific:</dt>
<dd>180,000
</dd>
<dt>Indian:</dt>
<dd>75,000
</dd>
<dt>Southern:</dt>
<dd>20,000
</dd>
<dt>Total:</dt>
<dd>361,000
</dd>
<dt>Mean:</dt>
<dd>72,000
</dd>
</dl>
<p>Oceans</p>
<p><br /></p></td>
</tr>
</tbody>
</table>

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/Tables)

