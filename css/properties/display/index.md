{{Page_Title|display}}
{{Flags
|Content=Compatibility Incomplete
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|Specifies the type of rendering box used for an element. In HTML, default display property values are based on behaviors listed in the HTML specifications or from the browser or user's default style sheet. The default value in XML is inline.

In addition to specifying one of the many different display box types, setting the display value to none lets you turn off (hide) the display of an element. A display element set to none ensures all descendant elements are also hidden. In these situations, the document renders as though the element does not exist in the document tree.
}}
{{CSS Property
|Initial value=inline
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=As specified, except for root element, floated elements, and absolutely positioned elements
|Animatable=No
|CSS object model property=display
|CSS percentages=???
|Values={{CSS Property Value
|Data Type=display-value
|Description=A keyword that defines the rendering type to apply to the element. Possible values are '''none''', '''inline''', '''block''', '''list-item''', '''inline-block''', '''inline-table''', '''table''', '''table-caption''', '''table-cell''', '''table-column''', '''table-column-group''', '''table-footer-group''', '''table-header-group''', '''table-row''', '''table-row-group''', '''flex''', '''inline-flex''', '''grid''', '''inline-grid''', and '''run-in'''.
}}{{CSS Property Value
|Data Type=inherit
|Description=By default, the CSS display property is not inherited ("Inherited: no"). However, when the inherited property has been specified on an element ("Inherited: Yes"), the element uses the computed value of that property on its parent element. Only the root element of the document gets the initial value given in the property's summary.
}}{{CSS Property Value
|Data Type=inline
|Description=An element set to inline generates one or more inline element boxes.
}}{{CSS Property Value
|Data Type=none
|Description=Turns off the display of an element (it has no effect on layout); all descendant elements also have their display turned off. The document is rendered as though the element did not exist. To render an element box's dimensions, yet have its contents be invisible, set the visibility property to hidden. This is a basic value in CSS 1.
}}{{CSS Property Value
|Data Type=list-item
|Description=Generates a block box for the content and a separate list-item. This is a basic value in CSS 1.
}}{{CSS Property Value
|Data Type=inline-block
|Description=The element generates a block element box that flows with surrounding content as if it were a single inline box--and behaves like a replaced element. This is a basic value in CSS 2.1.
}}{{CSS Property Value
|Data Type=inline-table
|Description=The inline-table value does not have a direct mapping in HTML. It behaves like a &#60;table&#62; HTML element, but as an inline box, rather than a block-level box. Inside the table box is a block-level context. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=table
|Description=Behaves like the &#60;table&#62; HTML element. It defines a block-level box. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=table-caption
|Description=Behaves like the &#60;caption&#62; HTML element. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=table-cell
|Description=Behaves like the &#60;td&#62; HTML element. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=table-column
|Description=Behaves like the &#60;col&#62; HTML element. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=table-column-group
|Description=Behaves like the &#60;colgroup&#62; HTML element. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=table-footer-group
|Description=Behaves like the &#60;tfoot&#62; HTML element. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=table-header-group
|Description=Behaves like the corresponding &#60;thead&#62; HTML element. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=table-row
|Description=Behaves like the &#60;tr&#62; HTML element. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=table-row-group
|Description=Behaves like the &#60;tbody&#62; HTML element. This is a table model value in CSS 2.1.
}}{{CSS Property Value
|Data Type=flex
|Description=Behaves like an block element for laying out content in the flexbox model. This is a flexbox model value in CSS3.
}}{{CSS Property Value
|Data Type=inline-flex
|Description=Behaves like an inline element for laying out content in the flexbox model. This is a flexbox model value in CSS3.
}}{{CSS Property Value
|Data Type=grid
|Description=Behaves like a block element for laying out content in the grid model.
Note: At the time of this writing, most modern browsers do not support this property. This is a grid box model value (an experimental tag in CSS 3.0).
}}{{CSS Property Value
|Data Type=inline-grid
|Description=Behaves like an inline element for laying out content in the grid model. This is a grid box model value (an experimental tag in CSS 3.0).
}}{{CSS Property Value
|Data Type=run-in
|Description=The behavior depends on the following conditions:

* If the run-in box contains a block box, same as block.
* If a block box follows the run-in box, the run-in box becomes the first inline box of the block box.
* If a inline box follows, the run-in box becomes a block box. .
}}{{CSS Property Value
|Data Type=block
|Description=Generates a block element box. This is a basic value in CSS 1.
}}{{CSS Property Value
|Data Type=ruby
|Description=Specifies that an element defines a '''ruby''' structure. This and the following values are from the [http://go.microsoft.com/fwlink/p/?linkid{{=}}203763 CSS3 Ruby Module]. This value only applies to the supported ruby elements, '''rt''' and '''ruby'''.
}}{{CSS Property Value
|Data Type=ruby-base
|Description=Specifies that an element defines a ruby base.  This value only applies to the supported ruby elements, '''rt''' and '''ruby'''.
}}{{CSS Property Value
|Data Type=ruby-text
|Description=Specifies that an element defines a '''ruby text'''.  This value only applies to the supported ruby elements, '''rt''' and '''ruby'''.
}}{{CSS Property Value
|Data Type=ruby-base-container
|Description=Specifies a container for one or more ruby base elements.  This value only applies to the supported ruby elements, '''rt''' and '''ruby'''.
}}{{CSS Property Value
|Data Type=ruby-text-container
|Description=Specifies a container for one or more ruby text elements.  This value only applies to the supported ruby elements, '''rt''' and '''ruby'''.
}}{{CSS Property Value
|Data Type=-ms-flexbox
|Description=Internet Explorer 10. Specifies a block-level flexible box ("flexbox") container. For more information on flexbox containers, see [[css/flexbox|Flexible Box ("Flexbox") Layout]].
}}{{CSS Property Value
|Data Type=-ms-inline-flexbox
|Description=Internet Explorer 10. Specifies an inline-level flexible box ("flexbox") container. For more information on flexbox containers, see [[css/flexbox|Flexible Box ("Flexbox") Layout]].
}}{{CSS Property Value
|Data Type=-ms-grid
|Description=Internet Explorer 10. Specifies a block-level Grid element. For more information on grid layout, see Grid Layout.
}}{{CSS Property Value
|Data Type=-ms-inline-grid
|Description=Internet Explorer 10. Specifies an inline-level Grid element. For more information on grid layout, see Grid Layout.
}}
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Change a <code>span</code>-element from its initial display <code>inline</code> to display as block-level element.
|Code=&lt;span&gt;Some example text&lt;/span&gt;
&lt;style&gt;
  span {
    display: block;
  }
&lt;/style&gt;
}}{{Single Example
|Language=HTML
|Description='''Second example'''

Do not display an element by using <code>display: none;</code>.
|Code=&lt;div&gt;Some example text&lt;/div&gt;
&lt;style&gt;
  div {
    display: none;
  }
&lt;/style&gt;
}}{{Single Example
|Language=HTML
|Description='''Third example'''

Specify the rendering type as block or inline to define how the element will display. Set the element to inherit the rendering values of its parent container:
|Code=p.block 
{
display:block; //Sets the element to display in a box model rendering type.
}

p.inline 
{
display:inline; //Sets the element to display inline inside the current element.
}

p.inherit 
{
display:inherit; //Sets the display value to inherit its parent container's display values.
}
}}
}}
{{Notes_Section
|Usage='''Basic values in CSS 1'''

*none
*inline
*block
*list-item

'''Extended values in CSS 2.1'''

*inline-block

'''Table model values in CSS 2.1'''

*inline-table
*table
*table-caption
*table-cell
*table-column
*table-column-group
*table-footer-group
*table-header-group
*table-row
*table-row-group

'''Flexbox model values in CSS3'''

*flex
*inline-flex

'''Grid box model values (experimental in CSS3)'''

*grid
*inline-grid

'''Experimental values'''

*run-in
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS Basic Box Model
|URL=http://dev.w3.org/csswg/css3-box/#display
|Status=Working Draft
}}{{Related Specification
|Name=CSS Grid Layout
|URL=http://dev.w3.org/csswg/css3-grid-layout/#grid-declaration
|Status=Working Draft
}}{{Related Specification
|Name=CSS Flexible Box Layout Module
|URL=http://dev.w3.org/csswg/css3-flexbox/#flex-containers
|Status=Candidate Recommendation
}}{{Related Specification
|Name=CSS Level 2 (Revision 1)
|URL=http://www.w3.org/TR/CSS2/visuren.html#display-prop
|Status=Recommendation
}}{{Related Specification
|Name=CSS Level 1
|URL=http://www.w3.org/TR/CSS1/#display
|Status=Recommendation
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Feature=none, inline and block
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=4.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0 (85)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=inline-block
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.0 (1.9)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=5.5 (to 7.0) natural inline elements only
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0 (85)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=list-item
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 (1.0)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=6.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0 (85)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=run-in
|Chrome_supported=Yes
|Chrome_version=1.0 Not before inline-elements
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0 (85) Not before inline-elements
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=inline-table
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=3.0 (1.9)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0 (85)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=table, table-cell, table-column, table-colgroup, table-header-group, table-row-group, table-footer-group, table-row, and table-caption
|Chrome_supported=Yes
|Chrome_version=1.0
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0 (1.0)
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=8.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=7.0
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_version=1.0 (85)
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=flex
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21.0
|Firefox_supported=Yes
|Firefox_version=18.0 (behind a preference),  20.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=inline-flex
|Chrome_supported=No
|Chrome_version=
|Chrome_prefixed_supported=Yes
|Chrome_prefixed_version=21.0
|Firefox_supported=Yes
|Firefox_version=18.0 (behind a preference),  20.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=No
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_version=12.10
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=No
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=grid
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}{{Compatibility Table Desktop Row
|Feature=inline-grid
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=No
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_version=10.0
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_version=2.1+
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Yes
|Blackberry_version=7.0+
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Yes
|Opera_mobile_version=5.0+
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Yes
|Opera_mini_version=5.0+
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Yes
|Safari_mobile_version=3.2+
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Firefox
|Note=Supports only single-line flexbox. To activate flexbox support, for Firefox 18 and 19, the user has to change the about:config preference "layout.css.flexbox.enabled" to true.
}}{{Compatibility Notes Row
|Browser=Internet Explorer 
|Version=7 and earlier
|Note=Does not support inline-block and table display.
}}{{Compatibility Notes Row
|Browser=Internet Explorer 
|Version=7 and earlier
|Note=Only supports the display value on elements with the display set to inline.
}}{{Compatibility Notes Row
|Browser=Firefox
|Version=16+
|Note=Supports inline-block and table display.
}}{{Compatibility Notes Row
|Browser=Internet Explorer
|Version=All
|Note=Does not support flex or inline-flex.
}}{{Compatibility Notes Row
|Browser=Safari
|Version=All
|Note=Does not support flex or inline-flex.
}}{{Compatibility Notes Row
|Browser=iOS Safari mobile
|Version=3.2+
|Note=Supports inline-block and table display.
}}
}}
{{See_Also_Section
|Topic_clusters=CSS Font, Fonts, Text
|External_links=* Quirksmode: [http://www.quirksmode.org/css/display.html The display property]
* W3 Schools: [http://www.w3schools.com/cssref/pr_class_display.asp CSS display property]
* Mozilla Developer Network: [https://developer.mozilla.org/en-US/docs/CSS/display CSS Reference: The display property]
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Notes_Section
|Notes====Remarks===
To render an element box's dimensions, yet have its contents be invisible, see the [[css/properties/visibility|visibility]] property.

All visible HTML '''div''' object is a block element, and a '''span''' object is an inline element. Block elements typically start a new line and can contain other block elements and inline elements. Inline elements do not typically start a new line and can contain other inline elements or data. Changing the values for the '''display''' property affects the layout of the surrounding content by:
*Adding a new line after the element with the value '''block'''.
*Removing a line from the element with the value '''inline'''.
*Hiding the data for the element with the value '''none'''.

In contrast to the [[css/properties/visibility|visibility]] property, <code>display: none</code> reserves no space for the object on the screen.
The <code>table-header-group</code> and <code>table-footer-group</code> values can be used to specify that the contents of the <code>thead</code> and <code>tfoot</code> elements are displayed on every page for a table that spans multiple pages.

You can use <code>inline-block</code> to give an object a layout without specifying the object's height or width.

The Cascading Style Sheets (CSS) table display model does not require explicit elements to correspond with the HTML tags. For example, an element styled as <code>display: table-cell</code> does not need to be contained within a block that is styled <code>display: table-row</code> to be styled correctly. Implicit table elements are created as necessary in an attempt to make the document valid. Contrast this behavior to the traditional HTML table model, where table elements are implicitly closed early to avoid unexpected nesting.

===Rendering for floating or absolute positioned elements===
{{{!}}
! Specified value !! Computed value
{{!}}-
{{!}} inline-table {{!}}{{!}} table
{{!}}-
{{!}} inline, run-in, table-row-group, table-column, table-column-group, table-header-group, table-footer-group, table-row, table-cell, table-caption, inline-block {{!}}{{!}} block
{{!}}-
{{!}} others {{!}}{{!}} same as specified
{{!}}}
}}