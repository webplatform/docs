{{Page_Title|Progressive Enhancement}}
{{Flags
|High-level issues=Needs Topics, Needs Review
|Checked_Out=No
|Editorial notes=Needs topics like "concept" or "methodology"..
}}
{{API_Name}}
{{Summary_Section|If you've read this section, you learned the fundamentals of the term Progressive Enhancement, what it is and how to use it?}}
{{Concept_Page
|Content=Progressive enhancement (PE) is a methodology for building web pages that are robust to the ever-changing nature of the web platform. Part of the appeal of PE is the strength of the end result. PE forces you to initially plan out your project as a functional system using only the most basic of Web technologies. This means that you know you’ll always have a strong foundation to fall back on as complexity is introduced to the project.
PE is also good for your users. It gives them the security of knowing they can visit your website using any of the thousands of user-agents available to them and still interact with your content as that agent allows.

You start by establishing a basic level of user experience that all browsers will be able to provide when rendering your web site, but you also build in more advanced functionality that will automatically be available to browsers that can use it.

'''The Layers of Progressive Enhancement'''

In practical terms, it’s easiest to break the concept of PE into different layers, each one building on the previous to improve the experience of interacting with the website.

* The first layer is clean, semantic HTML. This allows text-based, speech-based, antiquated and robotic user-agents to navigate the content of your website properly.
* The second layer is CSS. This allows visual-based user-agents to display or alter the visual representation of your website’s content.
* The third layer is JavaScript. This allows user-agents that are capable of using it to provide your users with enhanced usability.

'''Further reading'''

There is another term you have to hear about that is called [[graceful_degradation|'''Graceful Degradation''']] (GD). GD is similar to PE,  but it does things the other way round.
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
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Graceful degradation
|URL=http://docs.webplatform.org/wiki/concepts/graceful_degradation
}}
}}
{{See_Also_Section}}
{{Topics|Compatibility, CSS, HTML, JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}