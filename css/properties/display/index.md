{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status}}
{{API_Name}}
{{Summary_Section|The display CSS property specifies the type of rendering box used for an element. In HTML, default display property values are taken from behaviors described in the HTML specifications or from the browser/user default stylesheet. The default value in XML is inline.

In addition to the many different display box types, the value none lets you turn off the display of an element; when you use none, all descendant elements also have their display turned off. The document is rendered as though the element doesn't exist in the document tree.
}}
{{CSS Property
|Initial value=inline
|Applies to=All elements
|Inherited=No
|Media=visual
|Computed value=specified value; except for floats, root elements and positioned elements
|Animatable=No
|CSS percentages=N/A
|Values={{CSS Property Value
|Data Type=block
|Description=Object is rendered as a block element.
}}{{CSS Property Value
|Data Type=inline
|Description=Default. Object is rendered as an inline element sized by the dimensions of the content.
}}{{CSS Property Value
|Data Type=list-item
|Description=Internet Explorer 6 and later.  Object is rendered as a block element, and a list-item marker is added.
}}{{CSS Property Value
|Data Type=none
|Description=Element is not rendered. The element (it has no effect on layout); all child elements also have their display turned off. The document is rendered as though the element did not exist.
}}{{CSS Property Value
|Data Type=table-header-group
|Description=Object is rendered as '''tHead'''. Table header is always displayed before all other rows and row groups, and after any top captions. The header is displayed on each document spanned by a table.
}}{{CSS Property Value
|Data Type=table-footer-group
|Description=Object is rendered as '''tFoot'''. Table footer is always displayed after all other rows and row groups, and before any bottom captions. The footer is displayed on each document spanned by a table.
}}{{CSS Property Value
|Data Type=inline-block
|Description=Object is rendered inline, but the contents of the object are rendered as a block element.  Adjacent inline elements are rendered on the same line, space permitting.
}}{{CSS Property Value
|Data Type=table
|Description=Object is rendered as [[html/elements/table|'''table''']].
}}{{CSS Property Value
|Data Type=inline-table
|Description=Object is rendered as [[html/elements/table|'''table''']] within an <code>inline-block</code>.
}}{{CSS Property Value
|Data Type=table-row
|Description=Object is rendered as '''tr'''.
}}{{CSS Property Value
|Data Type=table-row-group
|Description=Object is rendered as '''tBody'''. Table body is always displayed after <code>table-header-group</code> objects and before <code>table-footer-group</code> objects.
}}{{CSS Property Value
|Data Type=table-column
|Description=Object is rendered as '''col'''.
}}{{CSS Property Value
|Data Type=table-column-group
|Description=Object is rendered as '''colGroup'''.
}}{{CSS Property Value
|Data Type=table-cell
|Description=Object is rendered as cell ('''td''') or header cell ('''th'''), depending on location within the table.
}}{{CSS Property Value
|Data Type=table-caption
|Description=Object is rendered as '''caption'''.
}}{{CSS Property Value
|Data Type=run-in
|Description=If the <code>run-in</code> box contains a <code>block</code> element, object is rendered as a block. If not, and the following sibling is a <code>block</code> (which is neither floating nor absolutely positioned), object is rendered as the first <code>inline-block</code> of the sibling. Otherwise, same as <code>block</code>.
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
|Description=Internet Explorer 10. Specifies a block-level flexible box ("flexbox") container. For more information on flexbox containers, see [[css/flexbox|Flexible Box ("Flexbox") Layout]].
}}{{CSS Property Value
|Data Type=-ms-inline-flexbox
|Description=Internet Explorer 10. Specifies an inline-level flexible box ("flexbox") container. For more information on flexbox containers, see [[css/flexbox|Flexible Box ("Flexbox") Layout]].
}}{{CSS Property Value
|Data Type=-ms-grid
|Description=Internet Explorer 10. Specifies a block-level Grid element. For more information on grid layout, see Grid Layout.
}}{{CSS Property Value
|Data Type=-ms-inline-grid
|Description=Internet Explorer 10. Specifies an inline-level Grid element. For more information on grid layout, see Grid Layout.
}}{{CSS Property Value
|Data Type=flex
|Description=<code>display: flex</code> is a flex container. It is used for [[css/flexbox|flex-box model layout]].
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
}}
}}
{{Notes_Section
|Notes====Remarks===
To render an element box's dimensions, yet have its contents be invisible, see the [[css/properties/visibility|"visibility"]] visibility property.

All visible HTML '''div''' object is a block element, and a '''span''' object is an inline element. Block elements typically start a new line and can contain other block elements and inline elements. Inline elements do not typically start a new line and can contain other inline elements or data. Changing the values for the '''display''' property affects the layout of the surrounding content by:
*Adding a new line after the element with the value '''block'''.
*Removing a line from the element with the value '''inline'''.
*Hiding the data for the element with the value '''none'''.

In contrast to the [[css/properties/visibility|'''visibility''']] property, '''display''':'''none''' reserves no space for the object on the screen.
The '''table-header-group''' and '''table-footer-group''' values can be used to specify that the contents of the '''tHead''' and '''tFoot''' objects are displayed on every page for a table that spans multiple pages.
In Microsoft Internet Explorer 4.0, the '''block''', '''inline''', and '''list-item''' values are not supported explicitly, but do render the element.
The '''block''' and '''inline''' values are supported explicitly as of Microsoft Internet Explorer 5.
In Microsoft Internet Explorer 5.5 and earlier, the default value of this property for '''li''' elements is '''block'''.
The '''inline-block''' value is supported  starting with Internet Explorer 5.5. You can use this value to give an object a layout without specifying the object's height or width.
Starting with Internet Explorer 8, the <code>table</code> display styles allow elements to closely parallel the visual layout of a table. The Cascading Style Sheets (CSS) table display model does not require explicit elements to correspond with the HTML tags. For example, an element styled as '''display:table-cell''' does not need to be contained within a block that is styled '''display:table-row''' to be styled correctly. Implicit table elements are created as necessary in an attempt to make the document valid. Contrast this behavior to the traditional HTML table model, where table elements are implicitly closed early to avoid unexpected nesting.
In Windows Internet Explorer 7 and earlier, the default value of this property for [[html/elements/table|'''table''']], '''tr''', '''td''', '''col''', and '''colGroup''' elements is <code>block</code>.
|Import_Notes====Syntax===
<code>'''display: '''inline '''{{!}}''' block '''{{!}}''' list-item '''{{!}}''' run-in '''{{!}}''' inline-block '''{{!}}''' table '''{{!}}''' inline-table '''{{!}}''' table-row-group '''{{!}}''' table-header-group '''{{!}}''' table-footer-group '''{{!}}''' table-row '''{{!}}''' table-column-group '''{{!}}''' table-column '''{{!}}''' table-cell '''{{!}}''' table-caption '''{{!}}''' -ms-flexbox '''{{!}}''' -ms-inline-flexbox '''{{!}}''' -ms-grid '''{{!}}''' -ms-inline-grid '''{{!}}''' none</code>

===Rendering for floating or absolute positioned elements===
{{{!}}
! Specified value !! Computed value
{{!}}-
{{!}} inline-table {{!}}{{!}} table
{{!}}-
{{!}} inline, run-in, table-row-group, table-column, table-column-group, table-header-group, table-footer-group, table-row, table-cell, table-caption, inline-block {{!}}{{!}} block
{{!}}-
{{!}} others {{!}}{{!}} same as specified
{{!}}}
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=CSS basic box model, Section 4.1.
|URL=http://www.w3.org/TR/css3-box/#the-lsquo
|Status=Working Draft
}}{{Related Specification
|Name=CSS 2.1, Visual formatting model, Section 9.2.4
|URL=http://www.w3.org/TR/CSS21/visuren.html#display-prop
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
{{See_Also_Section
|Topic_clusters=Box Model, Generated and Replaced Content
|Manual_sections====Related pages (MSDN)===
*<code>[[css/cssom/CSSStyleDeclaration/CSSStyleDeclaration|CSSStyleDeclaration]]</code>
*<code>[[css/cssom/currentStyle|currentStyle]]</code>
*<code>[[dom/defaultSelected|defaults]]</code>
*<code>[[css/cssom/style|style]]</code>
*<code>CSS Enhancements in Internet Explorer 6</code>
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/CSS/display
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}