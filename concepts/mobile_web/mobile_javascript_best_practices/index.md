{{Flags}}
{{API_Name}}
{{Summary_Section}}
{{Concept_Page
|Content=When optimising JavaScript, it is important to first understand
the big picture and the major stack components affecting the performance.
Equally important is to understand what can and cannot be optimised
in JavaScript without touching the browser code base. A good starting
point for this study is to first take a look at the [[JavaScript Performance Stack (John Resig's blog)]] depicted below.

  [[Image:GUID-CB38A361-981A-423E-90A2-AAE8D512A981_d0e4581_href.png]] Figure 1. Performance stack 
* Pick your battles. First optimise those parts that give you the biggest improvements.
* The most performance-intensive operations tend to be reflowing the layout and repainting. When developing with JavaScript, you cannot optimise the browser layout or painting algorithms but you can still affect the performance of these operations by not triggering them unnecessarily. A real-life example of Internet Explorer 8 reveals that layout and rendering tasks are the most time-consuming on this browser — see [[Yahoo UI blog webcast of Douglas Crockford, "Ajax Performance"]] at about –20:00 on the video counter)
 
In the table below you can find examples of common reasons for
slow JavaScript performance that can easily be addressed and will
instantly improve web application performance.

                    
{| border="1"
|+Table 1. Reasons
for poor JavaScript performance
|-
|Document Object Model (DOM) Access
|Interaction with the DOM is usually slower than normal JavaScript
code so should be avoided where possible. For instance, dynamically
creating HTML with strings and setting the innerHTML is usually faster
than creating HTML with DOM methods.
|-
|eval method
|Whenever possible, avoid the eval method as
significant overhead is involved in script evaluation.
|-
|with statements
|Using with statements creates additional scope
objects that slow variable access and create ambiguities.
|-
|for-in loops
|Unfortunately, most JavaScript environments have a slow implementation
of for-in loops. Opt to traverse arrays instead,
using the for (var i=0; i&lt;array.length; i++) instead
of for-in loops.
|}  
== Using jQuery Mobile ==

The [[jQuery Mobile]] touch-optimized web framework
for smartphones &amp; tablets supports Symbian including S60 5th Edition
and Symbian^3. This framework provides a unified user interface system
across popular mobile device platforms, built on jQuery and the jQuery
UI. For the complete list of supported platforms, see [[jQuery Mobile Graded Browser Support]]. jQuery Mobile's lightweight code has
a flexible, easily themeable design.
}}
{{Examples_Section
|Not_required=No
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