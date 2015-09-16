---
title: Manipulating CSS with JavaScript
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/CSS/Getting_Started/JavaScript)'
readiness: 'Ready to Use'
summary: 'In this article we look at the basics of how to manipulate CSS styles using JavaScript.'
tags:
  - Tutorials
  - CSS
  - DOM
  - JavaScript
uri: 'tutorials/manipulating css with javascript'

---
## Summary

In this article we look at the basics of how to manipulate CSS styles using JavaScript.

### Information: JavaScript

JavaScript is a *programming language*. JavaScript is widely used to provide interactivity in web sites and applications. JavaScript can interact with stylesheets, allowing you to write programs that change a document's style dynamically.

 There are three ways to do this:

-   By working with the document's list of stylesheets—for example: adding, removing or modifying a stylesheet.
-   By working with the rules in a stylesheet—for example: adding, removing or modifying a rule.
-   By working with an individual element in the DOM—modifying its style independently of the document's stylesheets

### Action: A JavaScript demonstration

1.  Make a new HTML document, `doc5.html`. Copy and paste the content from here, making sure that you scroll to get all of it:

    ``` html
    <!DOCTYPE html>
    <html>

    <head>
    <title>Mozilla CSS Getting Started - JavaScript demonstration</title>
    <link rel="stylesheet" type="text/css" href="style5.css" />
    <script type="text/javascript" src="script5.js"></script>
    </head>

    <body>
    <h1>JavaScript sample</h1>

    <div id="square"></div>

    <button type="button" id="clickMe">Click Me</button>

    </body>
    </html>
    ```

2.  Make a new CSS file, `style5.css`. Copy and paste the content from here:

    ``` css
    #square {
      width: 20em;
      height: 20em;
      border: 2px inset gray;
      margin-bottom: 1em;
    }

    button {
      padding: .5em 2em;
    }​
    ```

3.  Make a new text file, `script5.js`. Copy and paste the content from here:

    ``` js
    // JavaScript demonstration

    var square = document.getElementById("square"),
        clickMe = document.getElementById('clickMe'); //Keeping it unobstrusive
    function doDemo () {

      var button = this;
      square.style.backgroundColor = "#fa4";
      button.setAttribute("disabled", "true");
      setTimeout(clearDemo, 2000, button);
    }

    function clearDemo (button) {
      var square = document.getElementById("square");
      square.style.backgroundColor = "transparent";
      button.removeAttribute("disabled");
    }

    clickMe.onclick = doDemo; //Onclick call. Pass no arguments.​​​​​
    ```

4.  Open the document in your browser and press the button.

 What this code does, is that it changes the background color of the `#square` to `#ffaa44`. Here's a [JSFiddle](http://jsfiddle.net/namanyayg/Angmu/1/) so you can see it working live.

 Notes on what is happening in the above example:

-   The HTML document links the stylesheet as usual, and it also links the script.
-   The script works with individual elements in the DOM. It modifies the square's style directly. It modifies the button's style indirectly by changing an attribute.
-   In JavaScript, `document.getElementById("square")` is similar in function to to the CSS selector `#square` and in a similar way, `document.getElementById('clickMe')` is similar to `#clickMe`.
-   In JavaScript, `backgroundColor` corresponds to the CSS property `background-color`. JavaScript does not allow hyphens in names, so "camelCase" is used instead.
-   Your browser has a built-in CSS rule for `button` that changes the button's appearance when it is disabled.

## See also

## Exercise question

Change the script so that the square jumps to the right by 20 em when its color changes, and jumps back afterwards.
