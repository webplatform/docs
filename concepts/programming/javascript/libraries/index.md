{{Page_Title|JavaScript libraries}}
{{Flags
|High-level issues=Stub, Missing Relevant Sections
|Content=Not Neutral, Examples Best Practices
|Editorial notes=Meteor description is not in line with the other library descriptions.
}}
{{Summary_Section|Introduction to JavaScript libraries}}
{{Basic Page}}
{{Special:PrefixIndex/js/libraries/}}

== Overview ==
Javascript is arguably the most widely used computer language in the world. The use cases where Javascript has shown to be replacing traditional platforms are ever increasing. As the scope of the usage grows, it becomes extremely important that a method of distribution of code is used, to not only bring simplicity in further development but also allow reuse of code by the masses. JS Libraries solve this problem really well, and there are dozens if not hundreds of libraries available that cater to various use cases.

These various libraries provide pre-written JavaScript code which makes common or complex tasks easy to do. JavaScript libraries often target specific tasks such as DOM manipulation, framework setup and AJAX handling.

== Benefits ==
* '''Uniform interface for cross-browser compatible code''' - While modern browsers are becoming increasingly similar in their implementations of the language features and DOM, numerous minor differences still exist. The problem becomes substantial when compatibility with older browsers is required. Quite a few JS Libraries try to reduce the boilerplate code that developers have to write to address this issue. They provide a uniform API for development, which all compatibility handling throw browser and feature detection is handled in the background.

* '''Higher Levels of Abstraction''' - Quite often it is the case that development requires implementations of features that are quite popular in the industry. Autocomplete, AJAX handling, graphics and UI elements are some examples of areas where libraries are be a big boon. Most efforts can hence be focussed on customization.

* '''Frameworks''' - While the language itself is quite powerful and yet extremely easy to use, developing and maintaining large codebases can become challenging. There are various frameworks available as JS libraries that implement designs like MVC for writing the code in a more structured fashion.

== Getting started ==

The most commonly used libraries have rich communities and forums where you can get help on getting started with that particular library. JavaScript libraries are often downloaded from the library developer site. Many library developers provide both a development and production versions of their libraries. The development versions contain non-minified code which often include comments and hints whereas the production versions often are minified and compressed for to be used upon live site use.

Optionally, many libraries are available from CDN's such as [https://developers.google.com/speed/libraries/ Google Hosted Libraries], [http://cdnjs.com/ cdnjs] and [http://www.asp.net/ajaxlibrary/cdn.ashx Microsoft Ajax Content Delivery Network].

=== Usage ===

To include a library in your application you simply add a <code>&lt;script&gt;</code> tag to your <code>&lt;head&gt;</code> tag with the <code>src</code> attribute to the URL or path to the library source. Below you see two examples on how to load the jQuery library, one from Google Hosted Libraries and one from a local path.

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
|[http://angularjs.org AngularJS]
| Framework
|AngularJS is a toolset for building the framework most suited to your application development. It is fully extensible and works well with other libraries. Every feature can be modified or replaced to suit your unique development workflow and feature needs.
|-
|[http://backbonejs.org/ Backbone]
| Framework
|Backbone.js gives structure to web applications by providing models with key-value binding and custom events, collections with a rich API of enumerable functions, views with declarative event handling, and connects it all to your existing API over a RESTful JSON interface.
|-
|[http://createjs.com/EaselJS EaselJS]
| Graphics
|EaselJS provides straight forward solutions for working with rich graphics and interactivity with HTML5 Canvas. It provides an API that is familiar to Flash developers, but embraces Javascript sensibilities. It consists of a full, hierarchical display list, a core interaction model, and helper classes to make working with Canvas much easier.
|-
|[http://emberjs.org EmberJS]
| Framework
|Ember is a JavaScript framework for creating ambitious web applications that eliminates boilerplate and provides a standard application architecture.
|-
|[http://jquery.com jQuery]
| Tools and Utilites
|jQuery is a fast and concise JavaScript Library that simplifies HTML document traversing, event handling, animating, and Ajax interactions for rapid web development. jQuery is designed to change the way that you write JavaScript.
|-
|[http://meteor.com/ Meteor]
| Complete Stack
|Meteor is an open-source platform for building top-quality web apps in a fraction of the time, whether you're an expert developer or just getting started.
|-
|[http://prototypejs.org/ Prototype]
| Framework & Utilities
|Prototype is a JavaScript Framework that aims to ease development of dynamic web applications. Featuring a unique, easy-to-use toolkit for class-driven development and the nicest Ajax library around, Prototype is quickly becoming the codebase of choice for web application developers everywhere.
|-
|[http://underscorejs.org/ Underscore]
| Framework
|Underscore is a utility-belt library for JavaScript that provides a lot of the functional programming support that you would expect in Prototype.js (or Ruby), but without extending any of the built-in JavaScript objects. It's the tie to go along with jQuery's tux, and Backbone.js's suspenders.
|}
{{Notes_Section}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}