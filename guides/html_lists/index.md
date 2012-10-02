{{Page_Title|HTML lists}}
{{Flags}}
{{Byline}}
{{Summary_Section|This article will give a clear understanding of the three different list types in HTML. Using the step-by-step example, you should have created all three and learned how to nest lists inside list items.}}
{{Guide
|Content=== Introduction ==
 
Lists are used to group related pieces of information together, so they are clearly associated with each other and easy to read. In modern web development lists are workhorse elements, frequently used for navigation as well as general content.
 
Lists are good from a structural point of view as they help create a well-structured, more accessible, easy-to-maintain document. They are also useful for a purely practical reason — they give you extra elements to attach CSS styles to, for a whole variety of styling (we'll get on to CSS later in the course.)

Once you know how to use HTML lists properly, you will probably discover that you use them all the time. There is a lot of content on the web that should have been placed into a list, but was just thrown into a generic element with some line break tags. It’s a lazy practice that causes far more problems than it solves — so don’t do it! You should always create semantically correct lists to help people read your websites. It is a better practice for everyone, not least yourself when you need to maintain your sites later on.

== The three list types ==
 
There are three list types in HTML:
 
* '''unordered list''' — used to group a set of related items, in no particular order.
* '''ordered list''' — used to group a set of related items, in a specific order.
* '''description list''' — used to display name/value pairs such as terms and their definitions, or times and events.
 
Each one has a specific purpose and meaning — they are not interchangeable.
 
=== Unordered lists ===
 
Unordered lists, or bulleted lists, are used when a set of items can be placed in any order. An example is a shopping list:
 
* milk
* bread
* butter
* coffee beans
 
These items are all part of one list, however, you could put the items in any order and the list would still make sense:
 
* bread
* coffee beans
* milk
* butter
 
You can use CSS to change the bullet to one of several default styles, use your own image, or even display the list without bullets—we’ll look at how to do that in the [[Styling lists and links]] article.

==== Unordered list markup ====
 
Unordered lists use one set of <code>&lt;ul&gt;&lt;/ul&gt;</code> tags, wrapped around many sets of <code>&lt;li&gt;&lt;/li&gt;</code>:
 
<pre>&lt;ul&gt;
  &lt;li&gt;bread&lt;/li&gt;
  &lt;li&gt;coffee beans&lt;/li&gt;
  &lt;li&gt;milk&lt;/li&gt;
  &lt;li&gt;butter&lt;/li&gt;
&lt;/ul&gt;</pre>

=== Ordered lists ===
 
Ordered lists, or numbered lists, are used to display a list of items that need to be placed in a specific order. An example would be cooking instructions, which must be completed in order for the recipe to work:
 
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
 
Ordered lists can be displayed with one of several numbering or alphabetic systems—that is, letters or numbers. The default in most browsers is decimal numbers, but there are more options:
 
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
 
Again, you can use CSS to change the style of your ordered lists.
 
==== Ordered list markup ====
 
Ordered lists use one set of <code>&lt;ol&gt;&lt;/ol&gt;</code> tags, wrapped around many sets of <code>&lt;li&gt;&lt;/li&gt;</code>:
 
<pre>&lt;ol&gt;
  &lt;li&gt;Gather ingredients&lt;/li&gt;
  &lt;li&gt;Mix ingredients together&lt;/li&gt;
  &lt;li&gt;Place ingredients in a baking dish&lt;/li&gt;
  &lt;li&gt;Bake in oven for an hour&lt;/li&gt;
  &lt;li&gt;Remove from oven&lt;/li&gt;
  &lt;li&gt;Allow to stand for ten minutes&lt;/li&gt;
  &lt;li&gt;Serve&lt;/li&gt;
&lt;/ol&gt;</pre>
 
==== Beginning ordered lists with numbers other than 1 ====
 
It is possible to get an ordered list to start with a number other than 1 (or i, or I, etc.). This is done using the <code>&lt;start&gt;</code> attribute, which takes a numeric value, even if you’re using CSS to change the the list counters to be alphabetic, roman or. This is useful if you have a single list of items, but you want to break the list up with some kind of note, or some other related information. For example, we could do this with the previous example:
 
<pre>&lt;ol&gt;
  &lt;li&gt;Gather ingredients&lt;/li&gt;
  &lt;li&gt;Mix ingredients together&lt;/li&gt;
  &lt;li&gt;Place ingredients in a baking dish&lt;/li&gt;
&lt;/ol&gt;

&lt;p class="note"&gt;Before you place the ingredients in the baking dish, preheat the oven to 180 degrees centigrade/350 degrees fahrenheit in readiness for the next step&lt;/p&gt;

&lt;ol start="4"&gt;
  &lt;li&gt;Bake in oven for an hour&lt;/li&gt;
  &lt;li&gt;Remove from oven&lt;/li&gt;
  &lt;li&gt;Allow to stand for ten minutes&lt;/li&gt;
  &lt;li&gt;Serve&lt;/li&gt;
&lt;/ol&gt;</pre>
 
This gives the following result:
 
<ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
</ol>

<p class="note">Before you place the ingredients in the baking dish, preheat the oven to 180 degrees centigrade/350 degrees fahrenheit in readiness for the next step</p>

<ol start="4">
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol>
 
Note that this attribute was deprecated in HTML 4, so it will make your page not validate if you are using an HTML4 strict doctype. If you want to make use of such functionality in an HTML4 strict page, and it absolutely has to validate, you can do it using [http://dev.opera.com/articles/view/automatic-numbering-with-css-counters/ CSS Counters] instead. <code>&lt;start&gt;</code> has however been reinstated in HTML5, which is a good thing, as it is useful.

=== Description lists === 
 
Description lists associate specific names and their values within a list, for example items in an ingredient list and their descriptions, article metadata such as authors and categories and their values, or competition winners and the years in which they won. Let's explore the ingredient list example a bit more deeply. You could write an ingredients list like so:

<pre>milk
  
A white, liquid dairy product.
  
bread
  
A baked food made of flour or meal.
  
butter
  
A yellow, solid dairy product.
  
coffee beans
  
The seeds of the fruit from certain coffee trees.</pre>

Note: In HTML4, description lists were called definition lists, so if you hear that term mentioned in conversation, then just assume you are talking about a description list. HTML5 has changed the definition of this type of list to the more general "description list" because designers and developers were all too often using description lists to mark up name/value groups that weren't items and descriptions.
  
You can have as many name-value groups as you like, but there must be at least one name and at least one value in each pair. You can associate more than one value with a single name, or vice versa. For example, the term "coffee" can have several meanings, and you could show them one after the other:

<pre>coffee
  
a beverage made from roasted, ground coffee beans
a cup of coffee
a social gathering at which coffee is consumed
a medium to dark brown colour</pre>

Alternatively you can have more than one name with the same value. This is useful to show variations of a term, all of which have the same meaning:

<pre>soda
pop
fizzy drink
cola

a sweet, carbonated beverage.</pre>
   
Description lists are different from the other kinds of list, as they use names and values instead of list items. You wrap a description list in one set of <code>&lt;dl&gt;&lt;/dl&gt;</code> elements, wrapped around groups of <code>&lt;dt&gt;&lt;/dt&gt;</code> (name) and <code>&lt;dd&gt;&lt;/dd&gt;</code> (value) tags. You must pair at least one <code>&lt;dt&gt;&lt;/dt&gt;</code> with at least one <code>&lt;dd&gt;&lt;/dd&gt;</code>; a <code>&lt;dt&gt;&lt;/dt&gt;</code> should always come first in the source order.
 
A simple description list of single names with single values would look like this:

<pre>&lt;dl&gt;
  &lt;dt&gt;Name&lt;/dt&gt;
  &lt;dd&gt;Value&lt;/dd&gt;
  &lt;dt&gt;Name&lt;/dt&gt;
  &lt;dd&gt;Value&lt;/dd&gt;
  &lt;dt&gt;Name&lt;/dt&gt;
  &lt;dd&gt;Value&lt;/dd&gt;
&lt;/dl&gt;
</pre>
 
This is rendered as follows:

<pre>Name
  Value
Name
  Value
Name
  Value</pre>

In this example, we associate more than one value with a name, and vice versa:
 
<pre>&lt;dl&gt;
  &lt;dt&gt;Name&lt;/dt&gt;
  &lt;dd&gt;Value that applies to the preceding name&lt;/dd&gt;
  &lt;dt&gt;Name&lt;/dt&gt;
  &lt;dt&gt;Name&lt;/dt&gt;
  &lt;dd&gt;Value that applies to both of the preceding name&lt;/dd&gt;
  &lt;dt&gt;Name that can have both of the following values&lt;/dt&gt;
  &lt;dd&gt;One value of the name&lt;/dd&gt;
  &lt;dd&gt;Another value of the name&lt;/dd&gt;
&lt;/dl&gt;
</pre>
 
Which would render as follows:

<pre>Name
  Value that applies to the preceding name
Name
Name
  Value that applies to both of the preceding names
Name that can have one of the following values
  One value of the name
  Another value of the name</pre>
  
== Choosing between list types ==
 
When trying to decide what type of list to use, you can usually decide by asking two simple questions:

<ol>
  <li>Am I defining terms or associating other name/value pairs?
    <ul>
      <li>If yes, use a description list.</li>
      <li>If no, don’t use a description list — go on to the next question.</li>
    </ul>
  </li>
  <li>Is the order of the list items important?
    <ul>
      <li>If yes, use an ordered list.</li>
      <li>If no, use an unordered list.</li>
    </ul>
  </li>
</ol> 

== The difference between HTML lists and text ==
 
You may be wondering what the difference is between an HTML list and some text with bullets or numbers written in by hand. Well, there are several advantages to using an HTML list:
 
* If you have to change the order of the list items in an ordered list, you simply move around the list item elements. If you wrote the numbers in manually you would have to go through and change every single item’s number to correct the order — which is tedious to say the least!
* Using an HTML list allows you to style the list properly - you can use CSS to style just the list elements. If you just use a blob of text, you will find it more difficult to style the individual items in any useful manner, as the elements used will be the same as used for every other piece of text.
* Using an HTML list gives the content the proper semantic structure, as well as a "list-ish" visual effect. This has important benefits such as allowing screen readers to tell users with visual impairments they are reading a list, rather than just reading out a confusing jumble of text and numbers.
 
To put it another way: '''text and lists are not the same'''. Using text instead of a list makes more work for you and can create problems for your document’s readers. So if your document needs a list, you should use the correct HTML list.
 
== Nesting lists ==
 
A list item can contain another entire list — this is known as "nesting" a list. It is useful for things like tables of contents, such as the one at the start of this article:

# Chapter One
## Section One
## Section Two
## Section Three
# Chapter Two
# Chapter Three
 
The key to nesting lists is to remember that the nested list should relate to one specific list item. To reflect that in the code, the nested list is contained inside that list item. The code for the list above looks something like this:
 
<pre>&lt;ol&gt;
  &lt;li&gt;Chapter One
    &lt;ol&gt;
      &lt;li&gt;Section One&lt;/li&gt;
      &lt;li&gt;Section Two &lt;/li&gt;
      &lt;li&gt;Section Three &lt;/li&gt;
    &lt;/ol&gt;
  &lt;/li&gt;
  &lt;li&gt;Chapter Two&lt;/li&gt;
  &lt;li&gt;Chapter Three  &lt;/li&gt;
&lt;/ol&gt;</pre>
 
Note how the nested list starts after the <code>&lt;li&gt;</code> and the text of the containing list item (“Chapter One”); then ends before the <code>&lt;/li&gt;</code> of the containing list item. Nested lists often form the basis for website navigation menus, as they are a good way to define the hierarchical structure of the website.
 
Theoretically you can nest as many lists as you like, although in practice it can become confusing to nest lists too deeply. For very large lists, you may be better off splitting the content up into several lists with headings instead, or even splitting it up into separate pages.

== Step by step example ==
 
Let’s run through a step by step example, to put all of this together. Consider the following scenario:
 
You are creating a small website for the HTML Cooking School. On the main page, you are to show a list of categorised recipes, linking through to recipe pages. Each recipe page lists the ingredients required, notes on those ingredients and the preparation method. The three categories are:

* Cakes (including recipes for Plain Sponge, Chocolate Cake and Apple Tea Cake)
* Biscuits (including recipes for ANZAC Biscuits, Jam Drops and Melting Moments)
* Quickbreads (including recipes for Damper and Scones)

The client doesn’t mind what order the categories and recipes are shown; they just want to be sure people know which items are categories and which ones are recipes.
 
Let’s step through the process of creating this site.
 
=== Main page markup ===

<ol> 
<li><p>Create a properly-formed HTML page, including a doctype, <code>&lt;html&gt;</code>, <code>&lt;head&gt;</code> and <code>&lt;body&gt;</code> elements, and save it as ''stepbystep-main.html''. Add a main heading (<code>&lt;h1&gt;</code>) of “HTML Cooking School”, and a subheading (<code>&lt;h2&gt;</code>) of “Recipes”:</p>

<pre>&lt;h1&gt;HTML Cooking School&lt;/h1&gt;
&lt;h2&gt;Recipes&lt;/h2&gt;</pre></li>

<li><p>You have three categories of recipe to represent, and the order is not important — an unordered list is most appropriate for these, so add the following to your page:</p>

<pre>&lt;h2&gt;Recipes&lt;/h2&gt;
   &lt;ul&gt;
   &lt;li&gt;Cakes&lt;/li&gt;
   &lt;li&gt;Biscuits&lt;/li&gt;
   &lt;li&gt;Quickbreads&lt;/li&gt;
 &lt;/ul&gt;</pre>

<p>Indenting the <code>&lt;li&gt;</code> elements makes the code more readable, but it is not required.</p></li>

<li><p>Now you need to add the recipes as sub-items, for example “Plain Sponge”, “Chocolate Cake” and “Apple Tea Cake” are all part of the “Cakes” category. To do this, you need to create a nested list within each item. Since the order is not important, once again unordered lists are appropriate. To make things easier for the tutorial, I’ll get you to link all of the recipes to one single recipe page ([[html links lets build a web]] explains HTML links in depth].):</p>

<pre>&lt;h2&gt;Recipes&lt;/h2&gt;
 &lt;ul&gt;
   &lt;li&gt;Cakes
     &lt;ul&gt;
       &lt;li&gt;&lt;a href="stepbystep-recipe.html"&gt;Plain Sponge&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt;&lt;a href="stepbystep-recipe.html"&gt;Chocolate Cake&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt;&lt;a href="stepbystep-recipe.html"&gt;Apple Tea Cake&lt;/a&gt;&lt;/li&gt;
     &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Biscuits
     &lt;ul&gt;
       &lt;li&gt;&lt;a href="stepbystep-recipe.html"&gt;ANZAC Biscuits&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt;&lt;a href="stepbystep-recipe.html"&gt;Jam Drops&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt;&lt;a href="stepbystep-recipe.html"&gt;Melting Moments&lt;/a&gt;&lt;/li&gt;
     &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Breads/quickbreads
     &lt;ul&gt;
       &lt;li&gt;&lt;a href="stepbystep-recipe.html"&gt;Damper&lt;/a&gt;&lt;/li&gt;
       &lt;li&gt;&lt;a href="stepbystep-recipe.html"&gt;Scones&lt;/a&gt;&lt;/li&gt;
     &lt;/ul&gt;
   &lt;/li&gt;
 &lt;/ul&gt;</pre></li>
 </ol>

<p>The final result should be something similar to Figure 1:</p>

[[Image:mainpage.png|Screenshot of main page]]
 
Figure 1: The finished main page.
 
You can also [http://dev.opera.com/articles/view/16-html-lists/stepbystep-main.html view the live example page here].

=== The recipe page ===
 
For the sake of the example, we will just create the sponge cake recipe page — feel free to create the others yourself, using this one as a template. The HTML Cooking School has supplied the sponge recipe to you in a text file, looking like this:
 
<pre>Simple Sponge Cake
Ingredients
3 eggs
100g castor sugar
85g self-raising flour
 
Notes on ingredients:
  Caster Sugar - Finely granulated white sugar.
  Self-raising flour - A pre-mixed combination of flour and leavening agents (usually salt and baking powder).</code>

Method
  1. Preheat the oven to 190°C.
  2. Grease a 20cm round cake pan.
  3. In a medium bowl, whip together the eggs and castor sugar until fluffy.
  4. Fold in flour.
  5. Pour mixture into the prepared pan.
  6. Bake for 20 minutes in the preheated oven, or until the top of the cake springs back when lightly pressed.
  7. Cool in the pan over a wire rack.</pre>

=== Recipe page markup ===
 
<ol>
<li><p>Create another properly-formed HTML document, and save it as stepbystep-recipe.html. Add the following headings to it:</p>

<pre>&lt;h1&gt;Simple Sponge Cake&lt;/h1&gt;
 &lt;h2&gt;Ingredients&lt;/h2&gt;
 &lt;h3&gt;Notes on ingredients&lt;/h3&gt;
 &lt;h2&gt;Method&lt;/h2&gt;</pre></li>
<li>The ingredients list has several items but the order isn’t important. An unordered list therefore makes sense. Add the following into the <code>&lt;body&gt;</code> of your HTML:

<pre>&lt;h2&gt;Ingredients&lt;/h2&gt;
 &lt;ul&gt;
   &lt;li&gt;3 eggs&lt;/li&gt;
   &lt;li&gt;100g castor sugar&lt;/li&gt;
   &lt;li&gt;85g self-raising flour&lt;/li&gt;
 &lt;/ul&gt;</pre></li>

<li><p>The notes on the ingredients are there to properly define what some of the ingredients are. You need to associate the ingredient — the name — with its value. A description list is right for this purpose. Add the following to your HTML, below the unordered list in the previous step:</p>

<pre>&lt;h3&gt;Notes on ingredients&lt;/h3&gt;
 &lt;dl&gt;
   &lt;dt&gt;Castor Sugar&lt;/dt&gt;
     &lt;dd&gt;Finely granulated white sugar.&lt;/dd&gt;
   &lt;dt&gt;Self-raising flour&lt;/dt&gt;
     &lt;dd&gt;A pre-mixed combination of flour and leavening agents (usually salt and baking powder).&lt;/dd&gt;
 &lt;/dl&gt; </pre></li>
<li><p>The method must obviously follow a single correct order, so it should be an ordered list — add the following to your HTML, below the description list: </p>

<pre>&lt;h2&gt;Method&lt;/h2&gt;
 &lt;ol&gt;
   &lt;li&gt;Preheat the oven to 190°C.&lt;/li&gt;
   &lt;li&gt;Grease a 20cm round cake pan.&lt;/li&gt;
   &lt;li&gt;In a medium bowl, whip together the eggs and castor sugar until fluffy.&lt;/li&gt;
   &lt;li&gt;Fold in flour.&lt;/li&gt;
   &lt;li&gt;Pour mixture into the prepared pan.&lt;/li&gt;
   &lt;li&gt;Bake for 20 minutes in the preheated oven, or until the top of the cake springs back when lightly pressed.&lt;/li&gt;
   &lt;li&gt;Cool in the pan over a wire rack.&lt;/li&gt;
 &lt;/ol&gt;</pre></li>
 </ol>

The page should look something like Figure 2:
 
[[Image:recipepa.png|Screenshot showing the recipe page]]
 
Figure 2: The finished recipe page.
 
You can also [http://dev.opera.com/articles/view/16-html-lists/stepbystep-recipe.html view the live example page here].
 
You’re done!
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
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