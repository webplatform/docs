{{Page_Title|HTML lists}}
{{Flags
|State=Almost Ready
|Editorial notes=Need to remove compatibility table
|Checked_Out=No
}}
{{Byline
|Name=
|URL=
|Published=
}}
{{Summary_Section|This article introduces the three different list types in HTML and explores their basic features.}}
{{Guide
|Content=== Introduction ==
 
Lists are used to group together related pieces of information, so they are clearly associated with each other and easy to read. In modern web development lists are workhorse elements, frequently used for navigation as well as general content.
 
Lists are good from a structural point of view as they help create a well-structured, more accessible, easy-to-maintain document. They are also useful because they provide specialized elements to which you can attach CSS styles. Finally, semantically correct lists help visitors read your web site, and they simplify maintenance when your pages need to be updated.

== The three list types ==
 
There are three list types in HTML:
 
* '''unordered list''' — used to group a set of related items in no particular order
* '''ordered list''' — used to group a set of related items in a specific order
* '''description list''' — used to display name/value pairs such as terms and definitions
 
Each list type has a specific purpose and meaning in a web page.
 
=== Unordered lists ===
 
''Unordered'' (bulleted) lists are used when a set of items can be placed in any order. An example is a shopping list:
 
* milk
* bread
* butter
* coffee beans
 
Although the items are all part of one list, you could put the items in any order and the list would still make sense:
 
* bread
* coffee beans
* milk
* butter
 
You can use CSS to change the bullet to one of several default styles, use your own image, or even display the list without bullets — 
we'll look at how to do that in the [[guides/Styling lists and links|Styling lists and links]] article.

==== Unordered list markup ====
 
Unordered lists use one set of <code>&lt;ul&gt;&lt;/ul&gt;</code> tags wrapped around one or more sets of <code>&lt;li&gt;&lt;/li&gt;</code> tags:
 
<syntaxhighlight lang="html5"><ul>
  <li>bread</li>
  <li>coffee beans</li>
  <li>milk</li>
  <li>butter</li>
</ul></syntaxhighlight>

=== Ordered lists ===
 
''Ordered'' (numbered) lists are used to display a list of items that should be in a specific order. An example would be cooking instructions:
 
# Gather ingredients
# Mix ingredients together
# Place ingredients in a baking dish
# Bake in oven for an hour
# Remove from oven
# Allow to stand for ten minutes
# Serve
 
If the list items were moved around into a different order, the information would no longer make sense:
 
# Gather ingredients
# Bake in oven for an hour
# Serve
# Remove from oven
# Place ingredients in a baking dish
# Allow to stand for ten minutes
# Mix ingredients together
 
Ordered lists can be displayed with several sequencing options. The default in most browsers is decimal numbers, but there are others available:
 
* Letters
** Lowercase ascii letters (a, b, c…)
** Uppercase ascii letters (A, B, C…).
** Lowercase classical Greek: (έ, ή, ί…)
* Numbers
** Decimal numbers (1, 2, 3…)
** Decimal numbers with leading zeros (01, 02, 03…)
** Lowercase Roman numerals (i, ii, iii…)
** Uppercase Roman numerals (I, II, III…)
** Traditional Georgian numbering (an, ban, gan…)
** Traditional Armenian numbering (mek, yerku, yerek…)
 
As with unordered lists, you can use CSS to change the style of your ordered lists.
See [[guides/Styling lists and links|Styling lists and links]] for more information.
 
==== Ordered list markup ====
 
Ordered lists use one set of <code>&lt;ol&gt;&lt;/ol&gt;</code> tags wrapped around one or more sets of <code>&lt;li&gt;&lt;/li&gt;</code> tags:

<syntaxhighlight lang="html5"><ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol>
</syntaxhighlight>
 
==== Beginning ordered lists with numbers other than 1 ====
 
A common requirement in ordered list usage is to get them to start with a number other than 1 (or i, or I, etc.). This is done using the <code>start</code> attribute, which takes a numeric value (even if you're using CSS to change the list counters to be alphabetic or Roman). This is useful if you have a single list of items, but need to break the list up with some kind of note or other related information. For example, we could do this with the previous example:

<syntaxhighlight lang="html5"><ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
</ol>

<p>Before you place the ingredients in the baking dish, preheat the oven to 180 degrees centigrade/350 degrees fahrenheit in readiness for the next step</p>

<ol start="4">
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol></syntaxhighlight>
 
This gives the following result:
 
<ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
</ol>

<p>Before you place the ingredients in the baking dish, preheat the oven to 180 degrees centigrade/350 degrees fahrenheit in readiness for the next step</p>

<ol start="4">
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol>
 
Note that this attribute was deprecated in HTML 4, so it will prevent your page from validating if you are using an HTML4 strict doctype. If you want to make use of such functionality in an HTML4 strict page, and it absolutely has to validate, you can do it using [http://dev.opera.com/articles/view/automatic-numbering-with-css-counters/ CSS Counters] instead. Fortunately, however, the <code>start</code> attribute has been reinstated in HTML5.

=== Description lists === 
 
''Description lists'' (previously called ''definition lists'', but renamed in HTML5) associate specific names and values within a list. Examples might be items in an ingredient list and their descriptions, article authors and brief bios, or competition winners and the years in which they won. You can have as many name-value groups as you like, but there must be at least one name and at least one value in each pair. 

Description lists are flexible: you can associate more than one value with a single name, or vice versa. For example, the term "coffee" can have several meanings, and you could show them one after the other:

<pre>coffee
  
  a beverage made from roasted, ground coffee beans 
  a cup of coffee
  a social gathering at which coffee is consumed
  a medium to dark brown colour</pre>

Or, you can associate more than one name with the same value. This is useful to show variations of a term, all of which have the same meaning:

<pre>soda
pop
fizzy drink
cola

  a sweet, carbonated beverage</pre>
   
==== Description list markup ====

Description lists use one set of <code>&lt;dl&gt;&lt;/dl&gt;</code> tags wrapped around one or more groups of <code>&lt;dt&gt;&lt;/dt&gt;</code> (name) and <code>&lt;dd&gt;&lt;/dd&gt;</code> (value) tags. You must pair at least one <code>&lt;dt&gt;&lt;/dt&gt;</code> with at least one <code>&lt;dd&gt;&lt;/dd&gt;</code>, and the <code>&lt;dt&gt;&lt;/dt&gt;</code> should always come first in the source order.
 
A simple description list of single names with single values would look like this:

<syntaxhighlight lang="html5"><dl>
  <dt>Name</dt>
  <dd>Value</dd>
  <dt>Name</dt>
  <dd>Value</dd>
  <dt>Name</dt>
  <dd>Value</dd>
</dl></syntaxhighlight>
 
This is rendered as follows:

<pre>Name
  Value
Name
  Value
Name
  Value</pre>

In the following example, we associate more than one value with a name, and vice versa:
 
<syntaxhighlight lang="html5"><dl>
  <dt>Name1</dt>
  <dd>Value that applies to Name1</dd>
  <dt>Name2</dt>
  <dt>Name3</dt>
  <dd>Value that applies to both Name2 and Name3</dd>
  <dt>Name4</dt>
  <dd>One value that applies to Name4</dd>
  <dd>Another value that applies to Name4</dd>
</dl></syntaxhighlight>
 
That code would render like this:

<pre>Name1
  Value that applies to Name1
Name2
Name3
  Value that applies to both Name2 and Name3
Name4
  One value that applies to Name4
  Another value that applies to Name4</pre>
  
== Choosing among list types ==
 
When trying to decide what type of list to use, ask yourself two simple questions:

<ol>
  <li>Am I defining terms or associating other name/value pairs?
    <ul>
      <li>If yes, use a description list.</li>
      <li>If no, don't use a description list.</li>
    </ul>
  </li>
  <li>Is the order of the list items important?
    <ul>
      <li>If yes, use an ordered list.</li>
      <li>If no, use an unordered list.</li>
    </ul>
  </li>
</ol> 

== HTML list advantages ==
 
* Flexibility: If you have to change the order of the list items in an ordered list, you simply move around the list item elements;
when the browser renders the list, it will be properly ordered.
* Styling: Using an HTML list allows you to style the list properly using CSS. The list item tags <code>&lt;li&gt;</code> are different
from the other tags in your document, so you can specifically target CSS rules to them.
* Semantics: HTML lists give the content the proper semantic structure. This has important benefits, such as allowing screen readers to tell users with visual impairments that they are reading a list, rather than just reading out a confusing jumble of text and numbers.
 
To put it another way: '''don't code list items using regular text tags'''. Using text instead of a list makes more work for you and can create problems for your document's readers. So if your document needs a list, you should use the correct HTML list format.
 
== Nesting lists ==
 
An individual list item can contain another entire list, called a ''nested list''. It is useful for things like tables of contents
that contain sub-sections:

<pre>1. Chapter One
    a. Section One
    b. Section Two
    c. Section Three
2. Chapter Two
3. Chapter Three
 
To reflect that in the code, the nested list is contained inside that list item. The code for the list above looks like this:
 
<syntaxhighlight lang="html5"><ol>
  <li>Chapter One
    <ol style="list-style-type: lower-alpha;">
      <li>Section One</li>
      <li>Section Two </li>
      <li>Section Three </li>
    </ol>
  </li>
  <li>Chapter Two</li>
  <li>Chapter Three  </li>
</ol></syntaxhighlight>

Note that we have used the <code>list-style-type: lower-alpha</code> CSS property to sequence the nested list with lower-case letters
instead of decimal numbers.

Nested lists are quite useful, and often form the basis for navigation menus, as they are a good way to define the hierarchical structure of the web site.
 
Theoretically you can nest as many lists as you like, although in practice it can become confusing to nest lists too deeply. For very large lists, you may be better off splitting the content up into several lists with headings instead, or even splitting it up into separate pages.
A good rule of thumb is, don't nest lists deeper than three levels.

==Conclusion==

(Let's see if everything works before writing the conclusion.)

}}
{{Notes_Section
|Usage=
|Notes=
|Import_Notes=
}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=
|External_links=* [http://www.alistapart.com/articles/taminglists/ A List Apart: Taming Lists]
* [http://www.w3.org/TR/REC-CSS2/generate.html#lists W3C CSS2: list-style-type definition]
|Manual_sections==== Exercise questions ===
 
* What are the three types of HTML list?
* When would you use each type of list? How would you choose between them?
* How do you nest lists?
* Why should you use CSS rather than HTML to style your lists?
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}