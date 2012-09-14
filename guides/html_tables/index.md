{{Flags}}
{{Summary_Section|In this article we will cover how to use HTML tables correctly.}}
{{Guide
|Content=== Introduction ==
 
“Ack!” — how do you use web standards to organize reams of data? The very idea of tons of nested elements needed to get all the data into nice little rows and boxes ought to put your brain into “Ack!” mode, but there is a solution — tables to the rescue!
 
In web design tables are a good way to organize data into a tabular form. In other words, think of tables, charts, and other information graphics that help you to see and process a great deal of information in a summary that allows you to compare and contrast different pieces of data. You see them all the time on websites, whether they are giving a summary or comparison of political election results, sports statistics, price comparisons, size charts, or other data.
 
Back in the Jurassic Age of the Internet before CSS was popularised as a method of separating the presentation from structure of the HTML, tables were used as a way to lay out web pages — to create columns, boxes, and generally arrange the content. This is the wrong way to go about it; tables for layout resulted in bloated, messy pages with tons of nested tables — larger file sizes, hard to maintain, hard to modify after the fact. You’ll still see sites like this on the Web, but rest assured that these days you should just use tables for what they are designed for — tabular data — and use CSS to control layout.

== The most basic table ==
 
Let's start with the semantic HTML code required to render a basic table — this particular example compares recent volcanic eruptions in the Pacific region of North America:

<pre>&lt;table&gt;
    &lt;tr&gt;
        &lt;td&gt;Volcano Name&lt;/td&gt;
        &lt;td&gt;Location&lt;/td&gt;
        &lt;td&gt;Last Major Eruption&lt;/td&gt;
        &lt;td&gt;Type of Eruption&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;Mt. Lassen&lt;/td&gt;
        &lt;td&gt;California&lt;/td&gt;
        &lt;td&gt;1914-17&lt;/td&gt;
        &lt;td&gt;Explosive Eruption&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;Mt. Hood&lt;/td&gt;
        &lt;td&gt;Oregon&lt;/td&gt;
        &lt;td&gt;1790s&lt;/td&gt;
        &lt;td&gt;Pyroclastic flows and Mudflows&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;Mt .St. Helens&lt;/td&gt;
        &lt;td&gt;Washington&lt;/td&gt;
        &lt;td&gt;1980&lt;/td&gt;
        &lt;td&gt;Explosive Eruption&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;</pre>
 
This code renders roughly like so:
                         
{{{!}} border="1"
{{!}}-
{{!}}Volcano Name
{{!}}Location
{{!}}Last Major Eruption
{{!}}Type of Eruption
{{!}}-
{{!}}Mt. Lassen
{{!}}California
{{!}}1914-17
{{!}}Explosive Eruption
{{!}}-
{{!}}Mt. Hood
{{!}}Oregon
{{!}}1790s
{{!}}Pyroclastic flows and Mudflows
{{!}}-
{{!}}Mt .St. Helens
{{!}}Washington
{{!}}1980
{{!}}Explosive Eruption
{{!}}}

Let’s start by breaking down the HTML markup used in the above code:
 
* <code>&lt;table&gt;&lt;/table&gt;</code>:  The <code>&lt;table&gt;</code> wrapper element is necessary to indicate to the browser that you wish to arrange the content in a tabular fashion.
* <code>&lt;tr&gt;&lt;/tr&gt;</code>:  The <code>&lt;tr&gt;</code> element establishes a table row. This allows the browser to organize any content between the <code>&lt;tr&gt;</code> and <code>&lt;/tr&gt;</code> tags in a horizontal fashion, or all in a row.
* <code>&lt;td&gt;&lt;/td&gt;</code>: The <code>&lt;td&gt;</code> element defines the table cell or each individual space for content within the row. Only use as many <code>&lt;td&gt;</code> table cells as needed for actual data. Don’t use empty <code>&lt;td&gt;</code> cells for white space or padding — you use CSS to create any white space or padding needed, as this is not only a good way to separate presentation from structure; keeping the HTML clean and simple also makes the table easier to understand for people with visual impairments who are using screen readers to read the table contents out to them.
 
Note that the basic elements must be nested as follows:
 
<pre>&lt;table&gt;
    &lt;tr&gt;
        &lt;td&gt;content&lt;/td&gt;
        &lt;td&gt;content&lt;/td&gt;
        &lt;td&gt;content&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;</pre>
 
To order them in another fashion will cause the browser to spit up the equivalent of an internet hair ball and render the table in a very odd fashion, if at all.

== Adding some more features ==
 
Now the basic table is in place, we can add some slightly more complex table features—first, we'll add a caption and Table headers to help improve the data both in terms of semantics and legibility for screen readers. The updated table markup looks like so:

<pre>&lt;table&gt;
    &lt;caption&gt;Recent Major Volcanic Eruptions in the Pacific Northwest&lt;/caption&gt;
    &lt;tr&gt;
        &lt;th&gt;Volcano Name&lt;/th&gt;
        &lt;th&gt;Location&lt;/th&gt;
        &lt;th&gt;Last Major Eruption&lt;/th&gt;
        &lt;th&gt;Type of Eruption&lt;/th&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;Mt. Lassen&lt;/td&gt;
        &lt;td&gt;California&lt;/td&gt;
        &lt;td&gt;1914-17&lt;/td&gt;
        &lt;td&gt;Explosive Eruption&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;Mt. Hood&lt;/td&gt;
        &lt;td&gt;Oregon&lt;/td&gt;
        &lt;td&gt;1790s&lt;/td&gt;
        &lt;td&gt;Pyroclastic flows and Mudflows&lt;/td&gt;
    &lt;/tr&gt;
    &lt;tr&gt;
        &lt;td&gt;Mt. St. Helens&lt;/td&gt;
        &lt;td&gt;Washington&lt;/td&gt;
        &lt;td&gt;1980&lt;/td&gt;
        &lt;td&gt;Explosive Eruption&lt;/td&gt;
    &lt;/tr&gt;
&lt;/table&gt;</pre>
 
This code is rendered as:
                           
{{{!}} border="1"
{{!}}+Recent Major Volcanic Eruptions in the Pacific Northwest
{{!}}-
!Volcano Name
!Location
!Last Major Eruption
!Type of Eruption
{{!}}-
{{!}}Mt. Lassen
{{!}}California
{{!}}1914-17
{{!}}Explosive Eruption
{{!}}-
{{!}}Mt. Hood
{{!}}Oregon
{{!}}1790s
{{!}}Pyroclastic flows and Mudflows
{{!}}-
{{!}}Mt. St. Helens
{{!}}Washington
{{!}}1980
{{!}}Explosive Eruption
{{!}}}

The new elements used here are:
 
* <code>&lt;caption&gt;&lt;/caption&gt;</code>: The <code>&lt;caption&gt;</code> element allows you to give the table data a caption. Most browsers will center the caption and render it the same width as the table by default.
* <code>&lt;th&gt;&lt;/th&gt;</code>: The <code>&lt;th&gt;</code> element delineates the content between the tag as the table head titles for each column.  This is useful not just to help semantically describe what the function of this content is, but it also helps render it more accurately in a variety of browsers and devices.
 
== Structuring the table further ==
 
As a final step in structuring our table, we will define header and body table sections, add a footer and define the scope of row and column headings. We will also add a <code>summary</code> attribute to describe the table contents. The final markup looks like so:
 
<pre>&lt;table summary="a summary of recent major volcanic eruptions in the Pacific Northwest"&gt;
    &lt;caption&gt;Recent Major Volcanic Eruptions in the Pacific Northwest&lt;/caption&gt;
    &lt;thead&gt;
        &lt;tr&gt;
            &lt;th scope="col"&gt;Volcano Name&lt;/th&gt;
            &lt;th scope="col"&gt;Location&lt;/th&gt;
            &lt;th scope="col"&gt;Last Major Eruption&lt;/th&gt;
            &lt;th scope="col"&gt;Type of Eruption&lt;/th&gt;
        &lt;/tr&gt;
    &lt;/thead&gt;
    &lt;tfoot&gt;
        &lt;tr&gt;
            &lt;td colspan="4"&gt;Compiled in 2008 by Ms Jen&lt;/td&gt;
        &lt;/tr&gt;
    &lt;/tfoot&gt;  
    &lt;tbody&gt;
        &lt;tr&gt;
            &lt;th scope="row"&gt;Mt. Lassen&lt;/th&gt;
            &lt;td&gt;California&lt;/td&gt;
            &lt;td&gt;1914-17&lt;/td&gt;
            &lt;td&gt;Explosive Eruption&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;th scope="row"&gt;Mt. Hood&lt;/th&gt;
            &lt;td&gt;Oregon&lt;/td&gt;
            &lt;td&gt;1790s&lt;/td&gt;
            &lt;td&gt;Pyroclastic flows and Mudflows&lt;/td&gt;
        &lt;/tr&gt;
        &lt;tr&gt;
            &lt;th scope="row"&gt;Mt. St. Helens&lt;/th&gt;
            &lt;td&gt;Washington&lt;/td&gt;
            &lt;td&gt;1980&lt;/td&gt;
            &lt;td&gt;Explosive Eruption&lt;/td&gt;
        &lt;/tr&gt;
    &lt;/tbody&gt;
&lt;/table&gt;</pre>
 
This table code looks like so in a browser:

{{{!}} border="1"
{{!}}+Recent Major Volcanic Eruptions in the Pacific Northwest
{{!}}-
!Volcano Name
!Location
!Last Major Eruption
!Type of Eruption
{{!}}-
!Mt. Lassen
{{!}}California
{{!}}1914-17
{{!}}Explosive Eruption
{{!}}-
!Mt. Hood
{{!}}Oregon
{{!}}1790s
{{!}}Pyroclastic flows and Mudflows
{{!}}-
!Mt. St. Helens
{{!}}Washington
{{!}}1980
{{!}}Explosive Eruption
{{{!}} border="1"
{{!}}+Recent Major Volcanic Eruptions in the Pacific Northwest
{{!}}-
!Volcano Name
!Location
!Last Major Eruption
!Type of Eruption
{{!}}-
!Mt. Lassen
{{!}}California
{{!}}1914-17
{{!}}Explosive Eruption
{{!}}-
!Mt. Hood
{{!}}Oregon
{{!}}1790s
{{!}}Pyroclastic flows and Mudflows
{{!}}-
!Mt. St. Helens
{{!}}Washington
{{!}}1980
{{!}}Explosive Eruption
{{!}}+ Compiled in 2008 by Ms Jen
{{!}}}
                                

The new elements/attributes are as follows:
 
* The <code>&lt;thead&gt;</code>, <code>&lt;tbody&gt;</code> and <code>&lt;tfoot&gt;</code> elements: These define the table’s header, body and footer respectively. Unless you are coding a really complex table with many columns and rows of data,  using these may be overkill.  In a complex table however, using them can add useful structure for the developers, and also for browsers and other devices.
* The <code>colspan</code> and <code>rowspan</code> attributes: The <code>colspan</code> attribute creates a table cell that will span more than one column.  In the case of the above footer, we wanted the one table cell to span the whole width of the table, thus we told it that it was to span four columns. Alternately, you can add a table cell <code>rowspan</code> attribute that will allow the table cell to span x amount of rows, for example <code>&lt;td rowspan="3"&gt;</code>.
* The <code>summary</code> attribute: This attribute is used to define a summary of the table contents, for use by screenreaders (you won't see it on the rendered version of the table above.) Note that in the older W3C recommendations, WCAG 1.0 and HTML 4.0, it says you can use the <code>summary</code> attribute as detailed above. In newer drafts of the specs however, the <code>summary</code> attribute is not mentioned.  Whether to still use the <code>summary</code> attribute seems undecided, so for now we at the Web Standards Curriculum have agreed that it is safe to still use it. After all, it doesn’t cause anything to break, and it confers accessibility advantages.
* The <code>scope</code> attribute: You may also have noticed the <code>scope</code> attributes in the <code>th</code> tags, and the fact that we have defined the volcano names as headings too, inside the data rows! The <code>scope</code> attribute can be used in the <code>th</code> element to tell screen readers that the <code>th</code> content is the title for a column or a row.

== CSS to the rescue: a better looking table ==
 
The above listed elements and attributes are all that is necessary to code a good data table. Now the HTML structure is in place, let’s look at some simple CSS to make the table look a bit nicer:

<pre>body {
	background: #ffffff;
	margin: 0;
	padding: 20px;
	line-height: 1.4em;
	font-family: tahoma, arial, sans-serif;
	font-size: 62.5%;
}

table {
	width: 80%;
	margin: 0;
	background: #FFFFFF;
	border: 1px solid #333333;
	border-collapse: collapse;
}

td, th {
	border-bottom: 1px solid #333333;
	padding: 6px 16px;
	text-align: left;
}

th {
	background: #EEEEEE;
}

caption {
	background: #E0E0E0;
	margin: 0;
	border: 1px solid #333333;
	border-bottom: none;
	padding: 6px 16px;
	font-weight: bold;
}</pre>
 
When applied to our final table markup, the table looks as seen in Figure 1. You can also [http://dev.opera.com/articles/view/19-html-tables/table3.html check out the example live here].

[[Image:table300.png|the final table example]] 

Figure 1: The table now looks a lot more visually appealing.

Oooh... Look, much better. You can choose to style the table anyway you want, but the above provides a baseline to work with. You’ll learn a lot more about styling tables with CSS later in the course, but for now I’ll just briefly break down what each section of this CSS is doing:
 
* <code>&lt;body&gt;</code>: In the above CSS, we have added properties to set the margin (to zero in this case), padding to give a little room, background colour (white), font size and family, as well as the line height to also give a little breathing room.  You can [http://dev.opera.com/articles/view/19-html-tables/csstable.zip download the code for this example here] — try altering the property values in the CSS file to see how things change.
* <code>&lt;table&gt;</code>: borders have been added using the CSS <code>border</code> property. To make this work correctly, we also had to set the <code>border-collapse</code> property to <code>collapse</code>, to reset the border values in the table and allow the <code>border-bottom</code> to be a straight rule line across the whole row rather than being broken up at the end of each table cell. A <code>width</code> of 80% was chosen for this example (this makes the table extend across 80% of the screen width).
* <code>&lt;th&gt;</code> and <code>&lt;td&gt;</code>: In the above example CSS, we have set <code>text-align</code> to be <code>left</code>, but you could set it to <code>center</code> or other values if you like. we also gave both the <code>&lt;th&gt;</code> and <code>&lt;td&gt;</code> a bit of padding to open up the rows and allow for greater readability. In the case of the <code>&lt;th&gt;</code> selector above, we set another color as to differentiate the headings from the rest of the table.
* <code>&lt;caption&gt;</code>: In the above example we have given the caption a border (with no bottom border, as the border in the table already provided it), a different background colour and bold type to set the caption apart from the table header row.

== Summary ==
 
In this article we have gone through all you need to know to create effective HTML data tables. That’s a wrap! Let's leave this with some pertinent thoughts:
 
* It is important that tables are correctly coded to be readable by a variety web browsers, mobile, accessible, and other devices.  Table HTML is best kept to a minimum, and you should use CSS to style the tables. You’ll learn a lot more about CSS later on in the course.
* Tables can be accessible to mobile devices and users that use screen reading software by keeping the code clean, using attributes such as <code>scope</code> and <code>summary</code> as well as the <code>&lt;caption&gt;</code> element to help announce clearly and semantically what the respective sections are for. Also important for accessibility is to not use empty table cells for spacing (use CSS for this instead).
}}
{{See_Also_Section
|External_links=* [http://www.w3.org/TR/html401/struct/tables.html W3C HTML 4 Tables Recommendation]
* [http://www.w3.org/TR/CSS21/tables.html W3C CSS 2 tables recommendation]
* [http://www.456bereastreet.com/archive/200410/bring_on_the_tables/ Roger Johansson’s “Bring on the Tables”]
|Manual_sections==== Exercise questions ===
 
* Start by coding a simple table with only the 3 main table elements: <code>table</code>, <code>tr</code>, and <code>td</code>.  Save it and view it in a browser.
* Much like the second example above, add a caption, header, and footer to your table.  How does that change what you see in the browser?
* What can you do to make your table more accessible to screen readers and mobile devices?
* Now create a CSS file.  Try styling the borders, padding, and cell spacing of your table with only CSS and no attributes in your HTML markup.  Add background colour and style the fonts.
}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}