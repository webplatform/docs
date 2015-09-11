---
title: JavaScript functions
readiness: 'Ready to Use'
summary: 'This article discusses JavaScript functions, or how we create reusable pockets of code that we can call over and over again as we need.'
tags:
  - Tutorials
  - JavaScript
uri: 'tutorials/javascript functions'

---
## <span>Summary</span>

This article discusses JavaScript functions, or how we create reusable pockets of code that we can call over and over again as we need.

## <span>Introduction</span>

In this part of the [Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum), we will discuss functions. Functions lie at the core of practically everything *useful* that you will do with JavaScript. Broadly speaking, they offer the ability to break a program into logical chunks, each implementing a specific piece of functionality. They are a central feature of the language, and a good chunk of JavaScript’s attractiveness is due to the particular ways in which it enables you to use and create functions. If you have done some programming before in languages like PHP or Java, you will feel right at home with functions in JavaScript; if not, do not worry. Functions are *critical*, but they are not hard to wrap your head around. This article explains why you will want to understand functions, then dives into their syntax and shows you how to create and use them.

Note that the [functions examples are available for download](http://dev.opera.com/articles/view/javascript-functions/functions_code.zip), as well as being linked to at appropriate places in the article below.

## <span>What and why</span>

You certainly do not want to reach for your specifications to refresh your memory each time you need to perform a specific calculation; it is much better to simply code the calculation’s steps **once**, bundle that up as a `calculateSomething` function, and then point to that implementation next time you need to perform the same activity. This simple act of bundling up a set of commands means that you can concentrate on the *activities* that your code implements instead of the intimate details of those activities’ internal steps. You can think of the functions you write as a layer sitting on top of JavaScript’s built-in core; you are creating *new commands* that are more expressive and more understandable in the context of your particular application.

With that in mind, the “why?” of functions has a very straightforward answer: they are the basic building blocks that allow you to structure your code to enhance understanding of its purpose, and to reuse the functions you have written to avoid writing the same bits of code in multiple places. Your program will be easier to write and test if you break it into small pieces, each with a defined task.

Moreover, breaking your code up into well thought-out functions makes maintaining your code much easier. Imagine, for example, that the rules for daylight savings time are changed again next year. If you have done that calculation eighty-five times throughout your project, you *will* introduce new bugs when you update the code in each of those locations; it is repetitive, manual, and failure-prone. On the other hand, changing a single `calculateDaylightSavings` function allows you to cascade that single change down through the rest of your program with a single fix, much the same as the CSS cascade of style down through the page. In this way, functions make maintenance much less error-prone, and easier to implement successfully.

## <span>A function’s syntax</span>

Defining your own function is a simple task. As an example, let’s build a [function that generates a random background color for an element](http://dev.opera.com/articles/view/javascript-functions/functions_1.html) on a page:

``` js
function setElementBackground() {
  var red = Math.floor(Math.random() * 256);
  var green = Math.floor(Math.random() * 256);
  var blue = Math.floor(Math.random() * 256);

  var obj = document.getElementById('element_to_change');
  if ( obj ) {
    obj.style.background = 'rgb(' + red + ',' + green + ',' + blue + ')';
  }
}
```

 Without worrying too much about the code executed by the function, let us focus on four important features of the function’s syntax:

1.  A function declaration always begins with the keyword `function`, which makes sense.
2.  The next bit is the function’s name, in this case `setElementBackground` (I generally use [camelCase](http://en.wikipedia.org/wiki/CamelCase) for function names). The name of the function is important, as it is the bit you have to remember in order to use and reuse the code. Make sure it is an accurate description of what the function does; `setElementBackground` is a **much** better, more descriptive function name than something like `coloursAreNice` or `crazySetter`.
3.  Directly after the function’s name come a pair of parentheses. Inside these come the functions **argument list**, which enables you to make your functions more generic, and thus more reusable—you can apply them to more situations more easily. This is a powerful concept, but optional, so it will be discussed in more detail in the next section.
4.  Finally comes a pair of curly-brackets containing some code: these signify a **block** of code in JavaScript. Everything inside this block will be executed when the function is called, in order, just like any other bit of JavaScript code you have written.

### <span>Using the function</span>

Now we have defined the function, to call it somewhere in your code you would simply write:

``` js
setElementBackground();
```

 That is all there is to it! You no longer have to concern yourself with the difficult internal details of `setElementBackground`; you have already written the code, so now you are able to use it with ease wherever you like, and reap the (random) rewards of reuse.

Now, the function above is completely self-contained. It performs some activity, then exits; it neither needs input from the code that called it, nor does it give any information back to its caller about what happened. JavaScript, of course, allows us to write code that is a bit more talkative and flexible than that, so let us have a look at how we deal with information input to and output from functions.

### <span>Arguments</span>

Passing information into a function in order to influence its behavior is a great way to make it more flexible and useful in a variety of situations. For example, I have hard-coded the `id` of the element whose background is changed inside `setElementBackground`; it would be nice to be able to specify different elements on the page whenever I call the function so that I could *reuse* this function for different elements, instead of duplicating all that code. **Arguments** are the solution.

Earlier, I noted that the function’s definition contains a set of parentheses directly after the function’s name. This is the function’s **argument list**. To accept input from the caller, just specify a comma-separated list of variables that your function would like to receive. You can specify as many or as few as you like, and the names you use in the argument list can be referenced inside the function’s body just like with any other variable. The updated `setElementBackground` function looks like so ([check out the first example improvement](http://dev.opera.com/articles/view/javascript-functions/functions_2.html) live):

``` js
function setElementBackground( elementID ) {
  var red = Math.floor(Math.random() * 256);
  var green = Math.floor(Math.random() * 256);
  var blue = Math.floor(Math.random() * 256);

  var obj = document.getElementById( elementID );
  if ( obj ) {
    obj.style.background = 'rgb(' + red + ',' + green + ',' + blue + ')';
  }
}
```

 Calling this function with an element ID passed in as an argument is straightforward:

``` js
setElementBackground( 'element_to_change' );
```

 If you accidentally call the function without passing in an argument, it takes the value `undefined`. You can test for this inside your function body to provide a bit of defense against unintentional misuse:

``` js
if ( typeof elementID === "undefined") {
  // This will evaluate to `true` if the `elementID`
  // variable wasn't provided by the caller.
  // You can then write some code inside this
  //if statement to stop the code from erroring.
}
```

 The confusing, but nice, bit about function arguments is that the names of variables in the argument list have *nothing* to do with the name of variables passed into the function. If `elementID` is defined as the function’s argument, JavaScript creates a variable *inside* the function named `elementID` that has no effect on any variables outside the function — you can have another function outside the function of the same name, and its value would not be altered as a result of any statements inside the function. For example:

``` js
var elementID = "No change!";
setElementBackground( 'element_to_change' );
alert( elementID ); // Alerts "No change!";
```

 This has a very important side effect. JavaScript creates a new variable inside the function, meaning that any changes it makes to its internal argument has *no effect* on any variable passed in. This concept (called **scope**) will be discussed further in the [Objects](http://dev.opera.com/articles/view/objects-in-javascript/) and [JavaScript best practices](http://www.w3.org/wiki/JavaScript_best_practices) articles, but for now, here is a quick example. This is a `substring` function accepting a string and a starting point:

``` js
function substring( obj, start ) {
  obj = obj.substring(start);
}

var myString = "This is a string!";
substring(myString, 8);
alert(myString); // Alerts "This is a string!"
```

 Even though the `obj` variable is reassigned inside the function to the result of the built-in `substring` method, `myString` is not affected at all; only the *copy* of `myString` sitting inside `substring` was changed. The external variable has no idea at all that anything has happened.

This raises the question of communication: if changing arguments’ values has no effect outside the function, how do you pass information back from a function to its caller? Let's look at this now.

### <span>Return values</span>

It is very common for a function to do some calculation, and give the result of that work back to its caller to be used elsewhere. It might be useful, for example, for our `setElementBackground` function to *return* an array of the color values for use elsewhere. That is a simple matter of using the `return` keyword JavaScript provides, as shown here:

``` js
function setElementBackground( elementID ) {
  var red = Math.floor(Math.random() * 256);
  var green = Math.floor(Math.random() * 256);
  var blue = Math.floor(Math.random() * 256);

  var obj = document.getElementById( elementID );
  if ( obj ) {
    obj.style.background = 'rgb(' + red + ',' + green + ',' + blue + ')';
  }

  return [ red, green, blue ];
}
```

[Check out the second example improvement](http://dev.opera.com/articles/view/javascript-functions/functions_3.html) in action.

That simple addition means that you can now call the function in such a way as to capture its result in a variable:

``` js
var my_result = setElementBackground('element_to_change');
```

 Even if your function does not need to return a value, or has no real value to return, it is good practice to indicate success or failure by returning `true` or `false`, respectively. With that in mind, I will change `setElementBackground` to return `false` if the `elementID` that was passed in does not actually exist:

``` js
function setElementBackground( elementID ) {
  var red = Math.floor(Math.random() * 256);
  var green = Math.floor(Math.random() * 256);
  var blue = Math.floor(Math.random() * 256);

  var obj = document.getElementById( elementID );
  if ( obj ) {
    obj.style.background = 'rgb(' + red + ',' + green + ',' + blue + ')';
    return [ red, green, blue ];
  } else {
    return false;
  }
}
```

[Check out the third example improvement](http://dev.opera.com/articles/view/javascript-functions/functions_4.html) in action.

This allows you to check that the code executed properly by testing its return value, for example:

``` js
if ( !setElementBackground('element_does_not_exist') ) {
  alert("Something went wrong!  `element_does_not_exist` doesn't exist!");
}
```

 Additionally, please note that the `return` keyword actually ends execution of your function right when it is called, *returning* execution to the place at which your function was called. Code sitting below the call to `return` is not executed — it’s simply ignored.

## <span>Summary</span>

With that, you now know pretty much everything you need to in order to begin sprinkling your code full of functions. They are a foundation of good JavaScript code and your programs will be better organized, clearer, more readable, and easier to comprehend if you take the opportunity to wrap code up in well-named functions for reuse.

### <span>Exercise questions</span>

-   What are functions? Why are they useful?
-   How do you define a function?
-   How do you pass information into a function? Why would you want to? Conversely, how can you get information out of a function?
-   Wouldn’t it be nice if you could pass a color array into \`setElementBackground\`? Try modifying the code to accept another argument, and use that variable inside the function to override the random background colour.
