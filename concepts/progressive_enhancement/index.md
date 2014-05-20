{{Page_Title|Progressive Enhancement}}
{{Flags
|Checked_Out=No
|Editorial notes=Needs topics like "concept" or "methodology"..
}}
{{API_Name}}
{{Summary_Section|Progressive enhancement is a powerful development philosophy for creating universally accessible sites and web apps. It does require some learning, experience and discipline, but the return of investment is high.}}
{{Concept_Page
|Content=Part of the appeal of PE is the strength of the end result. PE forces you to initially plan out your project as a functional system using only the most basic of Web technologies. This means that you know you’ll always have a strong foundation to fall back on. 
You start by establishing a basic level of user experience that all browsers will be able to provide when rendering your web site, but you also build in more advanced functionality that will automatically be available to browsers that can use it.

==The Layers of Progressive Enhancement==

In practical terms, it’s easiest to break the concept of PE into different layers, each one building on the previous to improve the experience of interacting with the website.

* '''Markup''' The first layer is clean, semantic HTML. This allows text-based, speech-based, antiquated and robotic user-agents to navigate the content of your website properly.
* '''Styling''' The second layer is CSS. This allows visual-based user-agents to display or alter the visual representation of your website’s content.
* '''Behavior''' The third layer is JavaScript. This allows user-agents that are capable of using it to provide your users with enhanced usability.

There is another concept called  [[concepts/graceful_degradation|'''Graceful Degradation''']] (GD), you should . GD is similar, but it is an older concept ''(predecessor of progressive enhancement)'' that does things the other way round.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Description=RGBa is not supported in all Browsers, so we have to declare a fallback color.  Not declaring a fallback means no color will be applied in browsers that don't support it.
|Code=div {
   background: red; /* The Fallback */
   background: rgba(200, 54, 54, 0.5); 
}
|LiveURL=http://css-tricks.com/rgba-browser-support/
}}{{Single Example
|Language=JavaScript
|Description=requestAnimationFrame provides a native API for running any type of animation in the browser. How to use it the progressive enhanced way?
''Avoid browser-specific code and use feature detection (not browser detection)''
|Code=// Crossbrowser animation
var requestAnimation = (function() {
    return window.requestAnimationFrame ||
    window.webkitRequestAnimationFrame ||
    window.mozRequestAnimationFrame ||
    function(callback, element) {
        window.setTimeout(callback, 1000 / 60);
    };
}());
|LiveURL=http://www.html5rocks.com/en/tutorials/speed/animations/
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|External_links=*[http://sixrevisions.com/web-development/progressive-enhancement/ Overview and Best Practices]
*[http://www.smashingmagazine.com/2009/04/22/progressive-enhancement-what-it-is-and-how-to-use-it/ What It Is, And How To Use It?]
}}
{{Topics|Compatibility, CSS, Design, HTML, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
}}