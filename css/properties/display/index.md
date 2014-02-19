{{Page_Title}}
{{Languages}}
{{Flags
|High-level issues=Needs Review
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|This property specifies the type of rendering box used for an element. It is a shorthand property for many other display properties.}}
{{CSS Property
|Initial value=inline
|Applies to=All elements.
|Inherited=No
|Media=visual
|Computed value=See individual properties.
|Animatable=No
|CSS percentages=See individual properties.
|Values={{CSS Property Value
|Data Type=inline
|Description=Generates one or more inline element boxes.
}}{{CSS Property Value
|Data Type=block
|Description=Generates a block element box.
}}{{CSS Property Value
|Data Type=list-item
|Description=Generates a principal block box and a marker box.
}}{{CSS Property Value
|Data Type=inline-list-item
|Description=Generates an inline principal block box and a marker box.
}}{{CSS Property Value
|Data Type=inline-block
|Description=Generates a block element box that flows with surrounding content as if it were a single inline box--and behaves like a replaced element.
}}{{CSS Property Value
|Data Type=flex
|Description=Generates a block element for laying out content in the flexbox model. This is a flexbox model value in CSS3. See [[css/properties/flex|flex]].
}}{{CSS Property Value
|Data Type=inline-flex
|Description=Generates an inline element for laying out content in the flexbox model. This is a flexbox model value in CSS3. See [[css/properties/flex|flex]].
}}{{CSS Property Value
|Data Type=grid
|Description=Generates a block element for laying out content in the grid model. This is a grid box model value (an experimental tag in CSS 3.0). See [[css/properties/grid|grid]].
}}{{CSS Property Value
|Data Type=inline-grid
|Description=Generates an inline element for laying out content in the grid model. This is a grid box model value (an experimental tag in CSS 3.0). See [[css/properties/grid|grid]].
}}{{CSS Property Value
|Data Type=none
|Description=Causes an element to not appear in the formatting structure and have no effect on layout. Descendant elements and their content are likewise removed from the formatting structure. (This behavior cannot be overridden by setting the ''display'' property on the descendants.) '''Note:''' A display value of "none" does not create an invisible box; it creates no box at all. To render an element box's dimensions, yet have its contents be invisible, use the ''visibility'' property; see [[css/properties/visibility|visibility]].
}}{{CSS Property Value
|Data Type=inherit
|Description=Causes an element to use the specified or computed value of that property on its parent element.
}}{{CSS Property Value
|Data Type=table, inline-table, table-row-group, table-column, table-column-group, table-header-group, table-footer-group, table-row, table-cell, table-caption
|Description=These values cause an element to behave like a table element, subject to certain restrictions. See the [http://www.w3.org/TR/CSS2/tables.html W3C tables specification].
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Change a <code>span</code> element from its initial display <code>inline</code> to display as block-level element.
|Code=&lt;span&gt;Some example text&lt;/span&gt;
&lt;style&gt;
  span {
    display: block;
  }
&lt;/style&gt;
}}{{Single Example
|Language=HTML
|Description=Do not display an element by using <code>display: none;</code>.
|Code=&lt;div&gt;Some example text&lt;/div&gt;
&lt;style&gt;
  div {
    display: none;
  }
&lt;/style&gt;
}}{{Single Example
|Language=CSS
|Description=Specify the rendering type as block or inline to define how the element will display. Set the element to inherit the rendering values of its parent container:
|Code=p.block {
    /* Sets the element to display in a box model rendering type. */
    display:block;
}

p.inline {
    /* Sets the element to display inline inside the current element. */
    display:inline;
}

p.inherit {
    /* Sets the display value to inherit its parent container's display values. */
    display:inherit;
}
}}{{Single Example
|Language=CSS
|Description=Mobile-adapt a table, suppressing column headers and re-inserting text next to vertically stacked cells:
|Code=@media (max-width:400px) {
    /* stack cells vertically... */
    table, tr, td, th, tbody { display: block }
    /* ...but hide column headers */
    thead { display: none }
    /* insert column header text next to content */
    td::before { font-weight: bold }
    td:nth-of-type(1)::before { content: "Column 1: " }
    td:nth-of-type(2)::before { content: "Column 2: " }
    td:nth-of-type(3)::before { content: "Column 3: " }
    td:nth-of-type(4)::before { content: "Column 4: " }
}
}}{{Single Example
|Language=CSS
|Description=Stack generously sized links in mobile interface to extend the touch zone to the full width of the screen:
|Code=@media (max-width:400px) {
    a[href] {
        display: block;
        padding: 12px;
        border-radius: 12px;
        margin: 6px;
        text-decoration: none;
        color: #000;
        background-color: #fff;
        background-image: url(/img/nav_icon.png);
        background-position: 90% center;
    }
}
}}
}}
{{Notes_Section
|Notes='''Computed value and relationship between [[css/properties/display|display]], [[css/properties/position|position]], and [[css/properties/float|float]]'''
* If 'display' has the value 'none', then 'position' and 'float' do not apply. In this case, the element generates no box.
* Otherwise, if 'position' has the value 'absolute' or 'fixed', the box is absolutely positioned, the computed value of 'float' is 'none', and display is set according to the table below. The position of the box will be determined by the 'top', 'right', 'bottom' and 'left' properties and the box's containing block.
* Otherwise, if 'float' has a value other than 'none', the box is floated and 'display' is set according to the table below.
* Otherwise, if the element is the root element, 'display' is set according to the table below, except that it is undefined in CSS 2.1 whether a specified value of 'list-item' becomes a computed value of 'block' or 'list-item'.
* Otherwise, the remaining 'display' property values apply as specified.

{{{!}}
! Specified value !! Computed value
{{!}}-
{{!}} inline-table {{!}}{{!}} table
{{!}}-
{{!}} inline, run-in, table-row-group, table-column, <br />table-column-group, table-header-group,<br /> table-footer-group, table-row, table-cell, <br />table-caption, inline-block {{!}}{{!}} block
{{!}}-
{{!}} others {{!}}{{!}} same as specified
{{!}}}

'''Table-designated elements'''<br />
The Cascading Style Sheets (CSS) table display model does not require explicit elements to correspond with the HTML tags. For example, an element styled as <code>display: table-cell</code> does not need to be contained within a block that is styled <code>display: table-row</code> to be styled correctly. Implicit table elements are created as necessary in an attempt to make the document valid. Contrast this behavior to the traditional HTML table model, where table elements are implicitly closed early to avoid unexpected nesting.
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Display Module Level 3
|URL=http://dev.w3.org/csswg/css-display-3/
|Status=Editor's Draft
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/visuren.html#display-prop
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MSDN
|MDN_link=
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference
|HTML5Rocks_link=
}}