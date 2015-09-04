---
title: anipulating css with javascript
tags:
  - Tutorials
  - JavaScript
readiness: 'Almost Ready'
notes:
  - 'Needs to be moved to tutorials section'
summary: 'This article shows how to use JavaScript to modify the CSS applied to an HTML page, and create new styles.'
uri: 'manipulating css with javascript'

---
# manipulating css with javascript

## Summary

This article shows how to use JavaScript to modify the CSS applied to an HTML page, and create new styles.

## Introduction

At this point in the JavaScript section of the [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum), you’ve already covered the real basics of JavaScript usage, looked at how to target elements using the DOM, and seen how to manipulate them once you’ve successfully targeted them.

In this article we will look at how to dynamically update the styling applied to your elements by manipulating your CSS at runtime using JavaScript. It uses the same kind of technique that we’ve already seen, but there are a few special considerations to keep in mind when *working with the CSS DOM*.

## Accessing style sheets

The browser provides an interface to interact with style sheets — in your JavaScript code you can access a list of your style sheets by using `document.styleSheets`. `document.styleSheets` will return a list of all of the style sheets applied to a page, including external style sheets referenced with a `link` element and internal style sheets residing inside `style` elements. If your `style` elements have `id` attributes, you can reference them quickly with `document.getElementById(element_id)`.

You can also add new style sheets to the page — you can use the `document.createElement` function to create a new `style` element. This is useful when you want to give site visitors the option of changing your site styles dynamically, using some button controls perhaps. Here is a quick example of how you could create a new style sheet:

    var sheet = document.createElement('style')
    sheet.innerHTML = "div {border: 2px solid black; background-color: blue;}";
    document.body.appendChild(sheet);

Removing a style sheet is also very simple. First you must obtain the style sheet you wish to remove. You can do this by using `document.getElementById`, as shown in the small example below. To remove a style sheet you can use the DOM function `parent.removeChild(element)`, where `element` is the style sheet object you wish to remove and `parent` is the parent node of our style sheet. As shown in the example below, to remove the style sheet (`sheetToBeRemoved`) you first get the style sheet's parent — `var sheetParent = sheetToBeRemoved.parentNode` — then you call `removeChild` with an argument of `sheetToBeRemoved` - `sheetParent.removeChild(sheetToBeRemoved)`

    var sheetToBeRemoved = document.getElementById('styleSheetId');
    var sheetParent = sheetToBeRemoved.parentNode;
    sheetParent.removeChild(sheetToBeRemoved);

The [accessing style sheets example](http://dev.opera.com/articles/view/dynamic-style-css-javascript/accessingstylesheets.html) demonstrates both accessing all styles sheets and adding and removing a new style sheet to the page.

## Style Sheet Properties

The `stylesheet` object is available through JavaScript, and allows you to access information about a style sheet referenced from the current web page, such as if it is disabled, its location, and the list of CSS rules it contains. For a full list of the properties of the `stylesheet` object (and many things besides), check out the [W3C Document Object Model Style Sheets documentation](http://www.w3.org/TR/DOM-Level-2-Style/stylesheets.html).

Let’s consider a (currently) theoretical example — say we have a website where we show a series of technical articles. We want to spotlight some of these articles in a nice animated carousel, but what about users that don’t have JavaScript enabled for whatever reason? Thinking back to our [unobtrusive JavaScript knowledge](http://www.w3.org/wiki/The_principles_of_unobtrusive_JavaScript), we want the website functionality to still work for these users, but we might want to style the site differently for those users so that their user experience is still pleasant, even without the carousel.

What you want is a style sheet that gets enabled only if JavaScript is enabled. You are in luck — the DOM style sheet interface gives us access to the `disabled` attribute, which allows us to turn style sheets on or off.

Most of the properties of the `stylesheet` object are read only, but some, such as `disabled`, aren’t.

You can also use the style sheet properties to help differentiate between multiple style sheets on the page. The `src` property can help you identify external style sheets, but it won’t help you to reference internal style elements. A better way, which allows you to reference both internal and external style sheets individually, is to use the `title` property. If you iterate through `document.styleSheets` you can differentiate between the different style sheets you have included on the page. The following example shows how you can accomplish this iteration:

    function getStyleSheet(unique_title) {
      for(var i=0; i<document.styleSheets.length; i++) {
        var sheet = document.styleSheets[i];
        if(sheet.title == unique_title) {
          return sheet;
        }
      }
    }

For each `stylesheet` object retrieved from the `styleSheets` array you can access its `title` property to check if it has the title our code is looking for. You can see a functional example of this in the [adding and removing rules example](http://dev.opera.com/articles/view/dynamic-style-css-javascript/addingandremovingrules.html), which I will discuss in the next section.

Switching between different style sheets based on user preference is a fairly common web site feature — using what we have discussed so far, you can set up multiple style sheets and enable only the ones that the current site visitor would want to view. Let’s look at a real example — initially the text is styled, but when we set the `disabled` attribute to `true`, our defined CSS gets disabled. You can easily turn the CSS back on by setting `disabled` to `false`. Check out my [style sheet properties example](http://dev.opera.com/articles/view/dynamic-style-css-javascript/stylesheetproperties.html) for a practical look at how to use this.

## Adding and Removing Rules

Remember the theoretical showcase site we discussed above? Let’s say this site has a list of articles; some are about CSS, some are about HTML, and some are about JavaScript. On our webpage we show all the articles at once, but our user only wants to see the CSS articles. How might we do this? Because all the articles are already being shown, we don’t want to do another round trip to the server to get to a page containing just the CSS articles — that is a waste of time.

To solve this issue, we can use JavaScript to either iterate through all the articles and only make the CSS articles visible (I’ll discuss how to do this later), or add a rule to one of our style sheets that will make only the CSS articles visible. Using CSS will actually be faster than traversing over all the elements.

Our `stylesheet` object has two functions to help us with this problem. First is the `insertRule` function, which looks like this:

    stylesheet.insertRule(rule,index)

`rule` is a string containing the rule we would like to add to the style sheet. `index` specifies where within the style sheet’s rule list the rule should be placed. Here is how it might look.

    stylesheet.insertRule(".have-border { border: 1px solid black;}", 0);

I’ve created an example to demonstrate how the `insertRule` function is used. In this example is a list of all the rules in a style sheet. When the button is pressed it adds a rule with an index of 2 to make the text red by adding the property `color: red` to the `p { ... }` rule. Take a look at the [adding and removing rules example](http://dev.opera.com/articles/view/dynamic-style-css-javascript/addingandremovingrules.html).

If you want to delete this rule, you can call the function `stylesheet.deleteRule(index)`, where `index` is the index of the rule you want to be removed.

In our article showcase example, we can create a rule that turns the display to `none` for all the HTML and JavaScript articles — check out the [carousel example](http://dev.opera.com/articles/view/dynamic-style-css-javascript/carousel.html) to see this in action.

Note: IE does not implement rules according to the standard. Instead of the attribute `cssRules` it uses `rules`. IE also uses `removeRule` instead of `deleteRule` and `addRule(selector, rule, index)` instead of `insertRule`.

## Changing Element Styles

At this point you should understand how to edit style sheets connected to the page and create and modify the CSS rules within them. What if you want to change a specific element inside the DOM? Using the DOM API you can access the specific elements of your page. Looking back at our [carousel example](http://dev.opera.com/articles/view/dynamic-style-css-javascript/carousel.html), functionality is defined so that when you click on an article, that article becomes highlighted while the main article text gets displayed below.

Through the DOM, you have access to a `style` object that describes the style of an element. This `style` object is defined as a *CSSStyleDeclaration*; you can see a detailed explanation of this at the [W3C documentation of the CSSStyleDeclaration interface](http://www.w3.org/TR/DOM-Level-2-Style/css.html#CSS-CSSStyleDeclaration). The `style` object doesn’t quite work the same as some of the other properties defined in your HTML element. Unlike `element.href` or `element.id`, which return strings, `element.style` returns an object. This means you cannot set the style by assigning a string to `element.style`.

The `style` object has attributes that correspond to the different CSS properties we set. For example, `style.color` returns the colour that element has set on it. By calling `element.style.color = "red";` you can apply the style change dynamically. Below is a function that turns an element’s colour to red when you pass it the element’s `id`.

    function colorElementRed(id) {
      var el = document.getElementById(id);
      el.style.color = "red";
    }

You could also use `setAttribute(key, value)` to set a style on an element. For example, you could set the colour of an element to red by calling `element.setAttribute('style', 'color: red');` on the element, but be wary as this *will* erase any changes you have made to the `style` object.

When you set the style of an element in this manner it is the same as if you were assigning it as a declaration in a `style` attribute of the `html` element. The style will only be applied if the importance and specificity of the rule is greater than the other rules applied to the element (specificity is explained in the article about [the inheritance and cascade of CSS](http://www.w3.org/wiki/Inheritance_and_cascade).

Some of you may be wondering what happens when the CSS property being set has a hyphen. The syntax has to be different here, because for example if you write `element.style.font-size`, JavaScript will try to subtract `size` from the `element.style.font` notation, which is not what you want to happen. To stop this problem from occurring, all the CSS properties are written out in **CamelCase**. As shown below, you should write `element.style.fontSize` to access the element’s font size. For example:

    function changeElement(id) {
      var el = document.getElementById(id);
      el.style.color = "red";
      el.style.fontSize = "15px";
      el.style.backgroundColor = "#FFFFFF";
    }

Remember those stylesheet objects? Well, `styleSheet.cssRules` will return a list of `style` objects representing all the CSS rules contained in the style sheet. You can use these `style` objects just like the `style` objects for the other elements. In this case, rather than changing one specific element on our page, changes here will change all elements that the CSS rules apply to.

In the example below, the function to make the text bigger uses the `style` object and the function to make it smaller uses `setAttribute`. If you set the text to red and then call `setAttribute` with the smaller text button, you will notice that our change gets overwritten. Check out the [changing element styles example](http://dev.opera.com/articles/view/dynamic-style-css-javascript/changingelementstyles.html) live.

## Element Class Names

Another way to alter the style of an element is by changing its `class` attribute. `class` is a reserved word in JavaScript, so in order to access the element’s class, you use `element.className`. You can append strings to `className` if you want to add a class to an element, or you could just overwrite `className` and assign it a whole new class. Check out the [element class names example](http://dev.opera.com/articles/view/dynamic-style-css-javascript/elementclassnames.html).

## See also

### Exercise Questions

-   What is the difference between `setAttribute` and setting the style through the *CSSStyleDeclaration* object?
-   List two ways that you could cause all images to have a green border when a user clicks a button.
-   Will changing the *CSSStyleDeclaration* object of an element always change the element’s style? Why?
-   List two ways to access a specific style sheet.

