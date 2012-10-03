{{Page_Title|Auditing your web app for speed}}
{{Flags
|High-level issues=Stub
}}
{{Byline
|Name=Seth Ladd
|Published=July 28, 2010
}}
{{Summary_Section|How to audit a web app for speed.}}
{{Tutorial
|Content==Auditing Your Web App For Speed=

==Introduction==

A fast web app is a successful web app. Your job as a developer is not done until you have optimized both the real and perceived performance of your app. Not only is it simply the right thing to do to ensure that your users have an excellent experience, but there are very practical and important business reasons to optimize. Amazon measured a 1% drop in sales for every 100ms of site latency, and Google measured a 20% drop in traffic for every 0.5 second delay ([http://www.scribd.com/doc/4970486/Make-Data-Useful-by-Greg-Linden-Amazoncom citation]). Those are real numbers with real implications for your business and web apps.

Web speed is so important that Google even has an entire effort devoted to [http://code.google.com/speed/ making the web faster]. And if you need yet another reason to optimize your app performance, Google has announced that they are [http://googlewebmastercentral.blogspot.com/2010/04/using-site-speed-in-web-search-ranking.html adding page speed to their ranking algorithm].

There are many published best practices for optimizing the performance of your web app, including two great books ([http://oreilly.com/catalog/9780596529307/ High Performance Web Sites] and [http://oreilly.com/catalog/9780596522308/ Even Faster Web Sites]). Techniques on the server (such as implementing the correct cache control headers) and on the client (such as providing image width and height attributes) are combined into an end-to-end strategy for optimizing performance. With so many tips and tricks, it's sometimes difficult to gauge how they all map to real life and your real web apps.

Luckily, the Chrome Developer Tools (included in every instance of Chrome) provides an excellent tool which inspects your web app and offers customized recommendations to enhance performance and reduce latency. This article covers the Audit Panel, which is similar in scope to the very popular [http://developer.yahoo.com/yslow/ YSlow] tool, and explains how you can use it to speed up your website, decrease latency, and increase user satisfaction.

==Getting Started==

To illustrate how the Audit Panel can recommend web app performance improvements, we'll turn the tool toward our very own [http://www.html5rocks.com/ HTML5Rocks!]. We'll use the Audit Panel to help make our site even faster.

Starting Developer Tools is as easy as using the wrench icon (upper right of the Chrome window) and selecting '''Tools > Developer tools'''.

[[Image:auditspeed01.png|Chrome Developer Tools]]<br/>
''The Developer Tools are accessible from the Wrench menu''

For more information on how to get started with Developer Tools, please see [http://docs.webplatform.org/wiki/tutorials/developertools_chrome1 Introduction to Chrome Developer Tools, Part One].

The Audit Panel is located in the main tools button panel. You'll notice that, once selected, the Audit Panel has not yet run through its analysis of your web app. Running all of the heuristics can be slow, especially for a large web app such as GMail, so the tool is disabled by default.

[[Image:auditspeed02.png|Audit Panel]]<br/>
''The Audit Panel''

Let's dive in by clicking the ''Run'' button, which reloads the web app with the performance heuristics turned on. After the page reloads, you'll see a list of recommendations similar to the screen shot below.

[[Image:auditspeed03b.png|Improvement recommendations]]<br/>
''Recommendations of performance improvements from the Audit Panel''

You'll notice that the Audit Panel classifies the suggestions by severity, with the most severe marked with a red dot, and the medium severity suggestions marked with a yellow dot. This color-coding helps you prioritize the suggestions, focusing on the most important (those providing the biggest gains) first.

The number in parentheses following the suggestion is how many instances the Audit Tool detected. For example, there were 12 instances of "Leverage browser caching". This gives you a sense of how often the suggestion can be applied.

==Speed Strategies==

As mentioned before, there are plenty of well known and heavily tested strategies for optimizing web app performance. We won't be covering them all in depth with this article, but it's easy to find more information and details. Helpful resources for learning more about the specifics of web app optimization include Google's [http://code.google.com/speed/articles/ Let's make the web faster tutorials] and High Scalability's [http://highscalability.com/blog/2009/7/25/latency-is-everywhere-and-it-costs-you-sales-how-to-crush-it.html Latency is Everywhere and It Costs You Sales].

The Audit Panel groups its suggestions into two categories, Network Utilization and Web Page Performance. According to the Audit Panel, to improve Network Utilization we should:

* leverage browser caching
* leverage proxy caching
* minimize cookie size
* serve static content from a cookieless domain
* specify image dimensions

To improve web page performance, we should:

* optimize the order of styles and scripts
* remove unused CSS rules

Let's look at one of the strategies we can focus on to improve performance at HTML5Rocks!.

==Leverage Browser Caching==

Let's first dive into the recommendation to leverage browser caching. What does this mean, specifically? Opening up the option in the UI, we are presented with the following details:

[[Image:auditspeed04b.png|Audit Panel recommendations]]<br/>
''The Audit Panel gives you recommendations for performance improvements''

* The following resources are missing a cache expiration. Resources that do not specify an expiration may not be cached by browsers.
* The following cacheable resources have a short freshness lifetime.
* The following resources are explicitly non-cacheable. Consider making them cacheable if possible.

Caching resources is an excellent way to improve network utilization, which leads to lower bandwidth bills for the developer and faster response times for the user. Unfortunately, the tool doesn't tell you exactly what you need to do, so we need to dive into the recommendations a bit and use our knowledge of web app performance optimizations to apply these suggestions.

===Caching===

Without getting too deep into HTTP caching, we can certainly cover some of the basics. The HTTP protocol includes [http://tools.ietf.org/html/rfc2616#section-13 caching instructions], allowing the server and the client to reduce the amount of data that needs to be transferred over the wire. For example, the server can tell the client to save a resource locally for a certain amount of time, thus eliminating the need to request the resource again. The client can also ask if the server's resource is newer than the one that is stored locally. Ideally, if a resource is static, the server should tell the client to store the resource locally and avoid asking the server for the resource in the future. There are, as you can imagine, an incredible number of details regarding HTTP caching, but the general theme is "reduce the amount of data sent over the wire by storing resources locally on the client".

==Fixing Non-Cacheable Resources==

Let's look at one recommendation in depth, and learn how to connect the Audit recommendation to other tools inside Developer Tools. Specifically, let's look at how to address "the following resources are explicitly non-cacheable."

Because caching is accomplished via the HTTP protocol, we need to look at the HTTP request and response for the http://www.html5rocks.com/ resource. Simply click on the resource to view the original request and its response headers and details.

[[Image:auditspeed05.png|Navigating recommendations]]<br/>
''Navigating the recommendations''

You are then taken to the Resources Panel with the contents of the resources in view. Click the ''Headers'' tab, next to Content, to view the headers used in the request and the response.

[[Image:auditspeed06.png|Viewing header information]]<br/>
''Viewing header information''

We are trying to confirm that the server has told the client "do not cache the home page of html5rocks.com". To do this, we need to look at the Response Headers, as these are the headers and instructions sent by the server.

[[Image:auditspeed07.png|The Cache-Control header]]<br/>
''The <code>Cache-Control</code> header''

Sure enough, the server sent the "Cache-Control: no-cache" header to the client. This, as you would imagine, tells the client to always ask for the resource and to not cache it locally. Specifically, the HTTP specification for [http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.9.1 no-cache] reads:

"If the no-cache directive does not specify a field-name, then a cache MUST NOT use the response to satisfy a subsequent request without successful revalidation with the origin server. This allows an origin server to prevent caching even by caches that have been configured to return stale responses to client requests."

This is exactly why the Audit Panel recommends enabling caching, because otherwise the server and client are sending potentially redundant information.

Now that we have confirmed the root cause of the Audit suggestion, how do we fix it? In this case, the solution involves server side configuration or code. Depending on your setup, you could enable caching through your web server's configuration or through configurations in your web app framework. Specifically, you should include an Expires header and a Cache-Control: private with a max-age parameter for any resource that you want cached.

==Suggestions Are Just That&mdash;Suggestions==

Remember that the Audit Panel is recommending improvements based on generic heuristics. It is applying best practices, learned over many years, to your specific web app. Most of the time, these recommendations are spot on and should be taken to heart.

However, there are a few cases where recommendations may be correct but may not actually lead to any improvement. For example, if your page only has a single large image, the Audit Panel would recommend adding width and height attributes to the &lt;img&gt; tag, so that the rendering engine knows the image dimensions without first having to download and inspect the image. While this is generally great advice, it won't help much if the image is the only element on the page.

Remember to apply these suggestions after you understand them. And don't forget to measure performance before and after the changes, to ensure that there is actually an improvement.

==Summary==

The Audit Panel is an excellent and easy-to-use tool that will quickly show you how to optimize the performance of your web app. Speed is a crucial web app attribute, and many companies have found direct correlations between performance and revenue or activity. Optimizing your app's performance is not just the right thing to do for your users, but it is the right thing to do for your business's bottom line.
}}
{{Compatibility_Section
|Not_required=No
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Version=all
|Note=Developer Tools are currently available only in Chrome, but other WebKit browsers are expected to eventually integrate it.
}}
}}
{{See_Also_Section}}
{{Topics|Performance}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/tutorials/developertools/auditpanel/
}}