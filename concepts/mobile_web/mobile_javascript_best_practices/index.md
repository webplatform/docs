{{Page_Title}}
{{Flags}}
{{API_Name}}
{{Summary_Section}}
{{Concept_Page
|Content=When optimising JavaScript, it is important to first understand the big picture and the major stack components affecting the performance. Equally important is to understand what can and cannot be optimised in JavaScript without touching the browser code base. A good starting point for this study is to first take a look at the JavaScript Performance Stack [http://ejohn.org/blog/javascript-performance-stack/ (John Resig's blog)] depicted below.

[[File:Performance stack.png]]
Figure 1. Performance stack

- Pick your battles. First optimise those parts that give you the biggest improvements.

- The most performance-intensive operations tend to be reflowing the layout and repainting. When developing with JavaScript, you cannot optimise the browser layout or painting algorithms but you can still affect the performance of these operations by not triggering them unnecessarily. A real-life example of Internet Explorer 8 reveals that layout and rendering tasks are the most time-consuming on this browser — see [http://yuiblog.com/blog/2008/12/23/video-crockford-performance/ Yahoo UI blog webcast of Douglas Crockford, "Ajax Performance"] at about –20:00 on the video counter)

In the table below you can find examples of common reasons for slow JavaScript performance that can easily be addressed and will instantly improve web application performance.

{{{!}}
! Document Object Model (DOM) Access
! Interaction with the DOM is usually slower than normal JavaScript code so should be avoided where possible. For instance, dynamically creating HTML with strings and setting the innerHTML is usually faster than creating HTML with DOM methods.
{{!}}-
{{!}} <code>eval</code> method
{{!}} Whenever possible, avoid the <code>eval</code> method as significant overhead is involved in script evaluation.
{{!}}-
{{!}} <code>with</code> statements
{{!}} Using <code>with</code> statements creates additional scope objects that slow variable access and create ambiguities.
{{!}}-
{{!}} <code>for-in</code> loops
{{!}} Unfortunately, most JavaScript environments have a slow implementation of <code>for-in</code> loops. Opt to traverse arrays instead, using the <code>for (var i=0; i<array.length; i++)</code> instead of for-in loops.
{{!}}}

==Using jQuery Mobile==

The jQuery Mobile touch-optimized web framework for smartphones & tablets supports Symbian including S60 5th Edition and Symbian^3. This framework provides a unified user interface system across popular mobile device platforms, built on jQuery and the jQuery UI. For the complete list of supported platforms, see [http://jquerymobile.com/gbs/ jQuery Mobile Graded Browser Support]. jQuery Mobile's lightweight code has a flexible, easily themeable design.

Note: This material was originally published as part of the Nokia Developer Web Development Library, available as [http://www.developer.nokia.com/Resources/Library/Web/#!nokia-browsers/common-elements-of-nokia-browsers/mobile-javascript-best-practices.html Mobile JavaScript best practices]
}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section}}
{{Topics|Mobile}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}