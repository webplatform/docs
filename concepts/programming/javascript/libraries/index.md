{{Page_Title|JavaScript libraries}}
{{Flags
|High-level issues=Stub, Missing Relevant Sections
|Content=Not Neutral, Examples Best Practices
|Checked_Out=No
}}
{{Summary_Section|Introduction to JavaScript libraries}}
{{Basic Page}}
{{Special:PrefixIndex/js/libraries/}}

== Overview ==
JavaScript is arguably the most widely used computer language in the world. The use cases where JavaScript has shown to be replacing traditional platforms are ever increasing. As the scope of the usage grows, it becomes extremely important that a method of distribution of code is used, to not only bring simplicity in further development but also allow reuse of code by the masses. JavaScript libraries solve this problem really well, and there are dozens if not hundreds of libraries available that cater to various use cases.

These various libraries provide pre-written JavaScript code which makes common or complex tasks easy to do. JavaScript libraries often target specific tasks such as DOM manipulation, framework setup and AJAX handling.

== Benefits ==
* '''Uniform interface for cross-browser compatible code''' - While modern browsers are becoming increasingly similar in their implementations of the language features and DOM, numerous minor differences still exist. The problem becomes substantial when compatibility with older browsers is required. Quite a few JavaScript libraries try to reduce the boilerplate code that developers have to write to address this issue. They provide a uniform API for development, which all compatibility handling throw browser and feature detection is handled in the background.

* '''Higher levels of abstraction''' - Quite often it is the case that development requires implementations of features that are quite popular in the industry. Auto-completion, AJAX handling, graphics and user interface elements are some examples of areas where libraries can be a big boon. Most efforts can then be focused on customization.

* '''Frameworks''' - While the language itself is quite powerful and yet extremely easy to use, developing and maintaining large code bases can become challenging. There are various frameworks available as JavaScript libraries that implement designs like MVC for writing the code in a more structured fashion.

== Getting started ==

The most commonly used libraries have rich communities and forums where you can get help on getting started with that particular library. JavaScript libraries are often downloaded from the library developer site. Many library developers provide both a development and production versions of their libraries. The development versions contain non-minified code which often include comments and hints whereas the production versions often are minified and compressed for to be used upon live site use.

Optionally, many libraries are available from content delivery networks such as [https://developers.google.com/speed/libraries Google Hosted Libraries], [http://cdnjs.com/ cdnjs] and [http://www.asp.net/ajaxlibrary/cdn.ashx Microsoft Ajax Content Delivery Network].

=== Usage ===

To include a library in your application you simply add a <code>&lt;script&gt;</code> element to your <code>&lt;head&gt;</code> element with the <code>src</code> attribute referencing the URL or path to the library's source. Below, you see two examples on how to load the jQuery library, one from Google Hosted Libraries and one from a local path.

==== Examples ====

From CDN (Google Hosted Libraries):
<syntaxhighlight lang="html5">
<script src="//ajax.googleapis.com/ajax/libs/jquery/1.8.3/jquery.min.js"></script>
</syntaxhighlight>

From a local path:
<syntaxhighlight lang="html5">
<script src="js/lib/jquery.min.js"></script>
</syntaxhighlight>

== Common libraries ==

This list showcases JavaScript libraries. They're sorted alphabetically. If you don't see yours, please add it to the list.

{|
! align="left"| Library
! aligh="left"| Type
! Description
|-
|[http://ajile.net ajile]
| Modules
|ajile is an open-source client-side module that provides JavaScript with an API for runtime namespacing, dependency management and on-demand loading and insertion of cross-domain, local, and inline JavaScript.
|-
|[http://angularjs.org AngularJS]
| Framework
|AngularJS is a tool set for building the framework most suited to your application development. It is fully extensible and works well with other libraries. Every feature can be modified or replaced to suit your unique development workflow and feature needs.
|-
|[http://backbonejs.org/ Backbone]
| Framework
|Backbone.js gives structure to web applications by providing models with key-value binding and custom events, collections with a rich API of enumerable functions, views with declarative event handling, and connects it all to your existing API over a RESTful JSON interface.
|-
|[http://fabricjs.com FabricJS]
| Graphics
|Fabric is a powerful graphics library that makes working with HTML5 canvas a breeze. It provides a missing object model for canvas, as well as an SVG parser, layer of interactivity, event system, and a whole suite of other indispensable tools (text abstractions, gradients and patterns, image filters, flipping, clipping, animation, free drawing, canvas serialization, and more).
|-
|[http://createjs.com/EaselJS EaselJS]
| Graphics
|EaselJS provides straight forward solutions for working with rich graphics and interactivity with HTML5 Canvas. It provides an API that is familiar to Flash developers, but embraces JavaScript sensibilities. It consists of a full, hierarchical display list, a core interaction model, and helper classes to make working with Canvas much easier.
|-
|[http://emberjs.com EmberJS]
| Framework
|Ember is a JavaScript framework for creating ambitious web applications that eliminates boilerplate and provides a standard application architecture.
|-
|[http://sencha.com/products/extjs/ Ext JS]
| Framework
|Ext JS is a JavaScript framework for creating business application interfaces, it provides an MVC-style application architecture, a set of standard UI widgets such as grids and trees, a theming and templating system, a charting and drawing library and other utilities for creating rich data-oriented applications.
|-
|[http://jquery.com jQuery]
| Tools and Utilites
|jQuery is a fast and concise JavaScript Library that simplifies HTML document traversing, event handling, animating, and Ajax interactions for rapid web development. jQuery is designed to change the way that you write JavaScript.
|-
|[http://meteor.com/ Meteor]
| Complete Stack
|Meteor is a full-stack web application development environment. It runs on Node.js and functionalities can be extended by modules called Meteorites. 
|-
|[http://prototypejs.org/ Prototype]
| Framework & Utilities
|Prototype is a JavaScript Framework that aims to ease development of dynamic web applications. Featuring a unique, easy-to-use tool kit for class-driven development and the nicest Ajax library around, Prototype is quickly becoming the code base of choice for web application developers everywhere.
|-
|[http://sproutcore.com/ SproutCore]
| Framework
|SproutCore is an open-source JavaScript framework. Its goal is to allow developers to create web applications with advanced capabilities and a user experience comparable to that of desktop applications.
|-
|[http://underscorejs.org/ Underscore]
| Framework
|Underscore is a utility-belt library for JavaScript that provides a lot of the functional programming support that you would expect in Prototype.js (or Ruby), but without extending any of the built-in JavaScript objects. It's the tie to go along with jQuery's tux, and Backbone.js's suspenders.
|-
| [http://raphaeljs.com/ Raphaël]
| Vector Graphics
| Raphaël is a small JavaScript library that should simplify development work with vector graphics on the web. If someone wants to create their own specific chart or image crop and rotate widget, for example, they can achieve it simply and easily with this library.
|-
|[http://yuilibrary.com/ YUI Library]
| JS/CSS Framework
|YUI is a free, open source JavaScript and CSS library for building richly interactive web applications. The YUI Project is a two-way open-source project managed by the YUI engineering team at Yahoo!.
|}
{{Notes_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}