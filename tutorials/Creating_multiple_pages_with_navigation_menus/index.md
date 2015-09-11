---
title: Creating multiple pages with navigation menus
tags:
  - Tutorials
  - WSC
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'HTML links - lets build a web'
uri: 'tutorials/Creating multiple pages with navigation menus'

---
## <span>Introduction</span>

In this article we’ll talk about web site navigation and menus. You’ll learn about different types of menus and how to create them in HTML. We’ll also touch on the subject of menu usability and accessibility. We won’t go into styling menus yet, but this article will lay the foundations. There are [code examples to download](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/menu_examples.zip) to go along with this article — we will refer to these throughout the tutorial.

## <span>the HTML5 `<nav>` menu</span>

HTML5 defines a `<nav>` menu, which is to be used to contain the primary navigation of a web site, be it a list of links or a form element such as a search box. This is a good idea, as previous to this we would contain the navigation block inside something like `<div id="navigation">`. Yes, you can identify this for styling purposes pretty well, but it is a `<div>`, and therefore semantically anonymous. `<nav>` gives us a consistent way to unambiguously define with the primary navigation is, which is good for things like search engine optimization, and for visually impaired users using a screen reader, who will be able to find the navigation much more easier if it is clearly signposted (this does depend on the screen reader they are using supporting the `<nav>` element, so it might be a little way off yet). So, a navigation block would look something like this:

    <nav>
      <ul>
        <li><a href="#">Navigation</a></li>
        <li><a href="#">Menu</a></li>
        <li><a href="#">Links</a></li>
      </ul>
    </nav>

Bear in mind that `<nav>` should only be used for the main user navigation of a web page, not for advertising links down the bottom of the page, or for a secondary navigation relating to a small part of the page.

## <span>Your main HTML menu tools — links, anchors and lists</span>

There are several different types of menu and navigation idioms to consider in HTML, all connected closely with `<link>` and `<a>` (anchor) elements. In a nutshell:

-   `<link>` elements describe relationships across several documents. You can for example tell a user agent that the current document is part of a larger set that spans several documents, including a table of contents, and define the relationships between the documents.
-   Anchors (aka `<a>` elements) allow you to either link to another document, resource or document section, or to a certain section of the current document. These don’t get automatically followed by the user agent; instead they’ll be activated by your visitors by whatever mean available to them (mouse, keyboard, voice recognition, etc.)

If you haven’t read the [links](http://www.w3.org/wiki/HTML_links_-_lets_build_a_web) and [lists](http://www.w3.org/wiki/HTML_lists) articles earlier in the course, you should do, as they a required prerequisites for understanding this one.

Anchors/links do not just become menus on their own — you need to structure and style them to let both the browser and your users know that their function is as a navigation menu, not just a set of random links. If the order of the pages is not important you can use an unordered list as in this [unordered list menu example](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/unordered.html).

If the order in which the visitors go through all the documents is important then you need to use an ordered list. If for example you have a multi-document online course where one tutorial builds on top of the last one, you could use an ordered list like in this [ordered list example](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/ordered.html).

Using `<nav>` and lists to create menus is great for several reasons:

-   It is easy to differentiate the primary navigation lists/links from other lists and links on the page because they are the ones inside the `<nav>`. Not only will this make finding it easier for screen reader users, as mentioned above, but it makes targeting it with CSS and JavaScript easier too.
-   Lists can be nested, which means you can easily create several levels of navigation hierarchy.
-   Even without any styling applied to the list, the browser rendering of the HTML makes sense and it is easy to grasp for a visitor that these links belong together and make up one logical unit.

You nest lists by embedding the nested list inside the `<li>` element, not after it. you can see a [correct and an incorrect example here](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/nesting.html).

Notice that browsers display both examples in the same way. Browser display should never be an indicator for the quality of your code. An invalid HTML construct like the wrong example shown on the above example page will be hard to style, add behaviour to with JavaScript or convert to another format. The structure of nested ULs should always be `<ul><li><ul><li></li></ul></li></ul>` and never `<ul><li></li><ul><li></li></ul></ul>`.

## <span>The need for flexibility</span>

The menu of a site is unlikely to stay the same for very long — sites tend to grow organically as functionality is added and the user base grows, so you should create menus with scope for menu items to be added and removed as the site progresses, and for menus to be translated into different languages (so links will change in length). Also, you may well find yourself working on sites where the HTML for menus is created dynamically using server-side languages rather than with static HTML. This does not however mean that knowing HTML will become obsolete; it will actually become more important as this knowledge will still be needed to create HTML templates for the server-side script to populate.

## <span>Different types of menu</span>

There are several types of menus you will be called upon to create in HTML, as you work on different web sites. Most of these can be created with lists, although sometimes interface restrictions force you to use something different (more on that later). The list-based menus you will be likely to create are as follows:

-   In-page navigation: For example a table of contents for a single page, with links pointing to the different sections on the page.
-   Site navigation: A navigation bar for your whole web site (or a subsection of it), with links pointing to different pages on the same site.
-   Content-contextual navigation: A list of links that point to pages closely related to the subject of the page you’re currently on, either on the same site, or different ones.
-   Sitemaps: Large lists of links that point to all the different pages of a web site, grouped into related sublists to make them easier to make sense of.
-   Pagination: Links pointing to other pages that make up further sections or parts of a whole, along with the current page, for example part 1, part 2, and part 3 of an article.

### <span>In-page navigation (table of contents)</span>

We've already covered this to a certain degree in the tutorial about links, but here’s a more in-depth description of what in-page navigation means and what you need to make it work.

In the [example related to this in-page navigation section](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/inpagenavigation.html), we have used a list of links that point to anchors further down the page. Each menu link looks like so:

    <nav>
        <ol>
          <li><a href="#intro">Introduction</a></li>

      ...

The `href` attribute points to the corresponding anchor further down the page via the anchor's `id` attribute value, preceded by a hash symbol (\#). So the anchor looks like this:

    <h2 id="intro">Introduction</h2>

Each section of the page also has a “back to menu” link that works in the same way, but points back to the menu instead.

Technically, this is all you need to make this kind of navigation work, however, there is an annoying bug in Internet Explorer that forces you do to a bit more.

You can try this bug out yourself:

1.  Open the document in Internet Explorer 6 or 7
2.  Do not use a mouse; instead use the keyboard to navigate the document. You can hit the tab key to jump from link to link and the enter key to activate a link — in this case to jump to the section it points to.
3.  Seemingly all is well when you do that — the browser scrolls down to where you wanted to go.
4.  If you hit the tab key again the right behaviour for a browser is to take you to (give focus to) the first link inside the section you chose. Internet Explorer, however, will take you back to the start of the menu at the top of the page!

The way around this is terribly confusing and deals with a special property of Internet Explorer called `<hasLayout>`. You can trigger this in several ways, all of which are explained in [Ingo Chao’s excellent article "On having layout"](http://www.satzansatz.de/cssd/onhavinglayout.html). The easiest way is to [wrap the anchor in an element and then set that element's width using CSS](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/inpagenavigationmsiefix.html). In this case we used `<section>` elements and then set their width to 100% using CSS. This is what IE needs — the anchor to be inside an element with `<hasLayout>`.

Having to do this is annoying, but it also helps you if you want to style the sections differently - you can't add styling to a whole section unless you wrap it in an appropriate block level element.

Note that keyboard navigation around links in Opera is slightly different—try looking at the above example in Opera, then hold down Shift and use the arrow keys to navigate around links (it also works on form elements). This is called spatial navigation.

### <span>Site navigation</span>

Site navigation is most probably the most common menu type you’ll need to create. It is the menu of the whole site (or a subset of it), showing both the options visitors can choose from and the hierarchy of the site. Lists are perfect for this purpose, as you’ll see from this [site navigation example](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/home.html).

    <nav>
      <ul>
        <li><strong>Home</strong></li>
        <li><a href="about.html">About Us</a></li>
        <li><a href="clients.html">Our Clients</a></li>
        <li><a href="products.html">Our Products</a></li>
        <li><a href="services.html">Our Services</a></li>
        <li><a href="contact.html">Contact Us</a></li>
      </ul>
    </nav>

There aren’t many surprises here, at least not from a pure HTML point of view — try navigating to the different pages in the example to see what happens. Later on in the course we’ll talk about styling these kind of menus with CSS and adding behaviour via JavaScript. One important thing to consider is how to highlight the current document in the menu, to give the user a sense of being in a particular place, and that they are moving location (even though in reality they aren’t, unless of course they are using a mobile device to browse the Web!). In this case we are just removing the link to the current page, in each case - this makes sense, as you don't need to link to the same document you are on, and it makes it clear where you are in the menu. We’ll look more at "you are here" in the next section.

#### <span>Providing visitors with a “You are here” feeling</span>

One golden rule of web development and navigation is that the current document should never link to itself but instead be obviously different to the other entries in the menu. This is important as it gives the visitors something to hold on to and tells them where they are on their journey through your site. There are edge cases like web applications, permalinks in blogs and so called “one page” web sites but in 99% of cases a link to the document you are already looking at is redundant and confusing to the visitor.

In [HTML links - lets build a web](/w/index.php?title=HTML_links_-_lets_build_a_web&action=edit&redlink=1), we stated that a link is an agreement and a liability: you offer visitors a way to reach more information that they need, but you need to be careful — you’ll lose credibility and trust if that link doesn’t give the users what they want, and/or results in unexpected behaviour. If you offer for example a link that points to the current document, activating it will reload the document. As a user this is something you don’t expect — what purpose did clicking this link have? This results in users getting confused.

This is the reason why the current page should never be linked to from the menu. You could remove it altogether, or even better highlight it as well (eg. by surrounding it with a `<strong>` element) — this gives users a visual clue and also tells blind visitors that this is extra important — this [current page highlight example](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/about.html) illustrates this.

#### <span>How many options should you give users at one time?</span>

Another issue to consider is how many options you want to give visitors. A lot of menus you see on the web try to make sure that every page in the site can be accessed from one single menu. This is where scripting and CSS trickery comes in — you can make the menu more manageable by hiding certain parts until users select certain areas (rollover menus, as they are sometimes called). This is clever from a technical point of view, but there are several issues with this approach:

-   Not all visitors will be able to use the clever trick as intended; keyboard users for example will have to tab through all links on the page just to reach the one they are looking for.
-   You'll need to add a lot of HTML to each document of your site to achieve this, and a lot of it can be redundant on many pages. If we drill down three levels in a menu to reach the document we want to read, we don’t need to see options leading us to 4, 5, and 6 levels deep.
-   You can overwhelm visitors if you present them with too many options at once — humans don’t like making decisions. Think about how long it can take you to pick a meal from a lengthy restaurant menu.
-   If there is not much content on a page but a lot of links, search engines will assume that there is not much valid information on this page and not give the page much attention, so it is harder to find when searching the Web.

All in all, it is up to you how many items you put into a menu — different designs will call for different choices — but if in doubt, you should try cutting your menus down to only the links to the main sections of the site. You can always provide further submenus where appropriate.

### <span>Contextual menus</span>

Contextual menus are links that build on the content of the current document and offer more information related to the current page you are on. A classic example is the “related articles” links you tend to get at the bottom of news articles, as shown in Figure 1.

![Screenshot of a contexual menu, in this case related news items](/assets/public/1/16/menus-fi.png)

Figure 1: An example of a contextual menu — a news article offering related news items at the bottom.

This is a slightly different thing to context menus in software user interfaces, which offer different options depending on where they are accessed (like the right-click or Ctrl + click menus you find in desktop applications that offer specific options depending on where your mouse pointer is at the time).

Contextual menus on web sites are a great way to promote content on other parts of the site; in terms of HTML they are just another list of links.

### <span>Sitemaps</span>

Sitemaps are what you might expect — maps of all the different pages (or the main sections if you are talking about really huge sites) of your site. They allow your site’s visitors to get a glimpse of the overall structure of your site, and go anywhere they need to fast — even if the page they need is deep within your page hierarchy.

Both sitemaps and site searches are a great way of offering visitors a fallback option when they are lost or to offer quick access for those who are in a hurry.

From an HTML point of view they could either be one massive nested list full of links or — in the case of very large sites — section headings with nested links of section-specific hierarchies or even search forms for each of the sections.

### <span>Pagination</span>

Pagination is necessary when you have to offer a way to navigate through large documents split into separate pages. You’ll find pagination in large image archives or search result pages (like Google or Yahoo search), for example

Pagination is different from other types of navigation because it does normally link back to the same document — but results in more options or further information being displayed. Some examples of pagination are shown in Figure 2:

![Different types of pagination menus](/assets/public/0/00/menus-fj.png)

Figure 2: Pagination menus allow visitors to go through large sets of data without losing track of where they are.

The HTML is nothing ground-breaking — once again you offer a list of links with the current link (indicating which chunk of data is shown and how far down in your pagination you are) being highlighted (eg. with a `<strong>` element) and not linked.

The main difference to site navigation is that there is a lot of programming logic going on with pagination. Depending on where you are in the whole data set you need to show or hide the previous, next, first and last links. If you have really massive amounts of information to navigate through you will also want to offer links to landmarks like 0-100 results, 101-200 results, etc. This is why you are not very likely to hard-code menus like these in HTML but instead create them on the server-side. This does not change the rules however — the current chunk should not link to itself and you shouldn’t offer links that lead nowhere.

## <span>When lists are not enough — image maps and forms</span>

In 99% of cases an ordered or unordered list is a sufficient HTML construct for menus, especially as the logical order and nesting also allows for styling with CSS very nicely. There are however some situations that may require different design techniques.

### <span>Setting hotspots with image maps</span>

One technique is client side image maps. Image maps turn an image into a menu by turning sections of the images into interactive areas that you can link to different documents. The [imagemap example](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/imagemap.html) associated with this section turns an image into a clickable menu. Try it out by following the link above and clicking the different sections of the triangle in the image shown in Figure 3.

![Screenshot of an image with hotspots](/assets/public/f/f8/menus-fk.png)

Figure 3: By defining a map with area elements you can turn parts of an image into interactive elements.

You can turn any image into a menu by defining a map with different areas (also called hotspots). You give the map a `name` attribute and connect the image and the map using the `usemap` attribute on the `<img>` element. The code in our example looks like this:

    <nav>
      <img src="skillset.gif" alt="A web developer's skillset - web standards, browser bugs and user impact" usemap="#skillset_Map">
      <map name="skillset_Map">
        <area shape="poly" alt="W3C Guidelines" coords="90,70,113,112,67,112,90,70" href="w3c.html">
        <area shape="poly" alt="Browser Bugs" coords="61,120,115,120,137,157,40,157,62,120" href="browser.html">
        <area shape="poly" alt="User Impact" coords="35,166,142,166,171,216,6,216,35,166" href="userimpact.html">
      </map>
    </nav>

Note that this works exactly like in-page links, which means that you need to precede the value of the `usemap` attribute with a hash.

Each area has several attributes:

-   `href` defines the URL the area should link to (which could also be a target in the same document).
-   `alt` defines alternative text that can be displayed if the image is not viewable for whatever reason.
-   `shape` defines the shape of the area. This can be `rect` for rectangles, `circle` for circles or `poly` for irregular shapes defined using polygons.
-   `coords` defines the coordinates in the image that should become hotspots — these values are measured from the top left corner of the image, and can be measured in pixels or percentages. For rectangular areas you only need to define the top left and the bottom right corner; for circles you need to define the center of the circle and the radius; for polygons you need to provide a comma-delimited list of all the corner points.

Image maps are not much fun to define and type in as HTML, which is why image manipulation tools like Adobe Image Ready or Fireworks offer an option to create them visually (they generate the HTML for you).

### <span>Saving screen space and preventing link overload with forms</span>

Another technique you can employ is to using a form control for navigation — for example, you could use a `<select>` element for the navigation, with the different pages as options inside the `<select>` element. Your visitors can choose an option then submit the form to jump to different pages. You can find a [form menu example here](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/selectnavigation.html): note that it won't actually work, as it is not wired up to any script to make it work.

The most obvious benefit of using this type of menu is that you can offer a lot of options without using up a lot of space on the screen, as browsers render the menu as one line — see Figure 4.

![Screenshot of a menu created with a select box, open and closed](/assets/public/b/ba/menus-fl.png)

Figure 4: Select menus take up only one line on the screen.

You can go further with this, grouping the different menu options using the `<optgroup>` element, as shown in this [optgroup example](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/selectnavigationoptgroup.html).

This will show a menu with non-selectable options (these are the group names) as shown in Figure 5:

![Screenshot of a menu created with a select boxincluding option groups](/assets/public/3/38/menus-fm.png)

Figure 5: Select menus can get option groups that allow you to tell visitors which options belong together.

This technique has the benefit of using up hardly any space but it also means that you need to have a server-side script to send the visitors to the pages they have chosen. You can also use JavaScript to make the links work, but you cannot rely on JavaScript being available — you need to make sure your users can still make use of the menu with JavaScript disabled.

Another, less obvious benefit is that you don’t offer too many links in the same document. This means that you don’t overwhelm users of assistive technologies (who often tend to be presented with the links in one big list). It also means that search engines don’t consider the links on your page worthless as the link to text ratio makes the document appear to be a sitemap. However, many assistive technologies can produce a map of your pages' links; if your important links are all in a select menu, there is a chance that a visitor might never chance upon them. It is therefore a good idea to offer anchor links to the main destination pages and `<select>` element menus to offer more options. Visitors will be able to use them, but machines like search engine robots don’t need to know they exist.

## <span>Where to put the menu, and offering options to skip it</span>

One last thing to mention about HTML menus is that the placement of the menu plays a large role. Consider visitors that have no scrolling mechanism or might not be able to see so rely on keyboard navigation to find their way around your site. The first thing they'll encounter when they load the document is its location and the title; next the document gets read top to bottom, stopping at each link to ask the visitor if they wanted to follow this link or not. Other options are to get a list of all the links or to jump from heading to heading.

If the menu is at the top of document, it will be the first thing the user will meet. Having to skip through 15 or 20 links before they get to any content could get really annoying. There are two workarounds available. First, you could put the menu after the main content of the document (you can still place it at the top the screen using CSS if you wish). Second, you could offer a skip link. Skip links are simply links placed before the main menu that link to the start of the content, allowing the visitor to skip over the menu and get to the content immediately if they wish. You can add another “go to menu” link at the end of the document to make it easy to get back up to the top. Check out the [skiplinks example for more of an insight](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/skiplinks.html).

Skip links are not only useful for these kind of disabilities but make life a lot easier when you navigate a site on a mobile device with a small screen.

## <span>Summary</span>

In this tutorial we have covered the different types of menu you are likely to have to write in HTML.

## <span>Exercise Questions</span>

-   Why is it a good idea to mark up menus as lists?
-   When you design a navigation menu, what do you need to plan for in the future?
-   What are the benefits of using `<select>` elements for menus, and what are the problems?
-   What do you define with `<area>` elements, and what is the `nohref` attribute of an area element for (this is not in here, you'd need to do some online research)
-   What are the benefits of skip links?

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [23: Creating multiple pages with navigation menus](http://dev.opera.com/articles/view/23-creating-multiple-pages-with-navigat/), written by Christian Heilmann. Like the original, it is published under the [Creative Commons Attribution, Non Commercial - Share Alike 2.5](http://creativecommons.org/licenses/by-nc-sa/2.5/) license.