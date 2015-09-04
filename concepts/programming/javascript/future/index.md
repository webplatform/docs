---
title: future
tags:
  - Concept
  - Pages
uri: concepts/programming/javascript/future

---
**Note**: Please note that this document is currently under development, if you have anything to add please use the Comments to share.

### Next Release

ECMAScript 6 is the next draft version of the standard, code-named **"Harmony"** or **"ES.next"**. Draft 12 was released November 22, 2012.<sup>[[1]](#cite_note-md-1)</sup>

### Syntax

There has been a wide range of changes in regards to syntax, below are some examples of syntax additions and changes.

#### let

Let and const are new ways to declare variables, firstly `let` is exactly the same as `var` apart from it bounds the declared variable to the inner-most scope. example:

     //Testing var scope
     function scope()
     {
       for(var i = 0; i != 10; i++)
       {
          //(i) is available here
       }
       //(i) is also available here
     }

     //Testing let scope
     function scope()
     {
       for(let i = 0; i != 10; i++)
       {
          //(i) is available here
       }
       //(i) is *not* available here!
     }

This may not seem like a huge change but it's actually a much needed feature. An example of ES3/5 would be:

     for(var i = 0; i < 10; i++)
     {
        setTimeout(function(){
          alert(i);
        }, 20);
     }

The above statement will alert the number 10, ten times. this is because the loop iterations finish before the execution of the time-out, so the value of `i` will be the last possible value in the loop.

Using `let` allows you to scope the variable to the **current** iteration scope, meaning that the example below act's like your creating an anonymous function for every iteration.

     for(let i = 0; i < 10; i++)
     {
        let k = i;
        setTimeout(function(){
          alert(k);
        });
     }

#### const

`const` is similar to `let` and `var` apart from the variable is marked as read-only.

#### for..of

`for(x of y)` loops allow you to iterate over arrays in the same way you iterate over object's key. an example usage would be:

     let array = [0,2,4,8,16,32,64];
     for(num of array)
     {
     }

### Features

TODO: List some of the EMCAScript 6 features such as Syntax, Structures and Library implementations

### Concepts

Describe concepts such as Classes, Private Names, Inheritance and Abstraction.

## References

1.  <span class="mw-cite-backlink">[↑](#cite_ref-md_1-0)</span> <span class="reference-text">ECMAScript 6 Draft 12 <span class="citation web">["harmony:specification\_drafts"](http://wiki.ecmascript.org/doku.php?id=harmony:specification_drafts#current_working_draft). 17-Dec-2004<span class="printonly">. [http://wiki.ecmascript.org/doku.php?id=harmony:specification\_drafts\#current\_working\_draft](http://wiki.ecmascript.org/doku.php?id=harmony:specification_drafts#current_working_draft)</span>.</span><span class="Z3988" title="ctx_ver=Z39.88-2004&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Abook&amp;rft.genre=bookitem&amp;rft.btitle=harmony%3Aspecification_drafts&amp;rft.atitle=&amp;rft.date=17-Dec-2004&amp;rft_id=http%3A%2F%2Fwiki.ecmascript.org%2Fdoku.php%3Fid%3Dharmony%3Aspecification_drafts%23current_working_draft&amp;rfr_id=info:sid/en.wikipedia.org:concepts/programming/javascript/future"><span style="display: none;"> </span></span></span>
