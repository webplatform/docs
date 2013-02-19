=APIs=

==Summary==

APIs, or Application Programming Interfaces, are standard JavaScript objects that perform a variety of tasks. They encapsulate objects, methods, properties, and events that you can use to build applications that will work across different browsers.

== Background ==

APIs came into popularity on the Web a number of years ago, when open standards creators and web property developers realised it was a really good idea to make their data, services and technologies easily query-able and reusable via simple interfaces consisting of custom JavaScript objects. These days you'll find many examples of APIs available and in use all over the Web, for example:

* Web sites/applications as diverse as [https://dev.twitter.com/docs Twitter], [http://www.flickr.com/services/developer/ Flickr], [https://affiliate-program.amazon.com/gp/advertising/api/detail/main.html Amazon], [http://code.google.com/apis/youtube/overview.html YouTube], [http://www.dropbox.com/developers Drop Box] and [http://www.guardian.co.uk/open-platform The Guardian].
* JavaScript libraries such as [http://modernizr.com/ Modernizr], [http://jquery.com/ jQuery] and [http://raphaeljs.com/ Raphaël].

Many libraries include API functionality, so you don't have to use the raw API. For APIs like [[apis/xhr|XHR]] and [[apis/websocket|Web Socket]], you would use the API through a library like jQuery rather than spin up your own HTTP request or build in your own socket layer. That said, though, these APIs are here for your reference.

Note: If you are completely new to web development, you may want to review [[beginners|Web development for beginners]].

== Explore our API docs ==

Some of the more sought-after APIs in use today include the following.

<div class="topic-container">

  <div class="short-topic">
  
    <div class="image icon-api"></div>
    
    <div class="inner">
    <h3>[[apis/canvas|Canvas]]</h3>
    
    <p>The <code><canvas></code> element and the corresponding API are among the most-used tools in web development. This API helps you render two-dimensional pixel-based graphics, and in combination with other APIs, lets your applications perform displays of awesome artistic brilliance.</p>
    </div>
  
  </div>
  
  <div class="short-topic">
  
    <div class="image icon-api"></div>
    
    <div class="inner">
    <h3>[[apis/indexeddb|Indexed DB]]</h3>
    
    <p>Off-line storage is one of the key features of a modern web app, and the Indexed DB,  [[apis/appcache|AppCache]], [[apis/file|File]], and [[apis/filesystem|File System]] APIs provide the interfaces to the browsers storage facilities.</p>
    </div>
  
  </div>
  
  <div class="short-topic">
  
    <div class="image icon-api"></div>
    
    <div class="inner">
    <h3>[[apis/webrtc|Web RTC]]</h3>
    
    <p>Real-Time Communication, until recently only available through installed applications like Skype, is quickly becoming native browser functionality, and is poised to become one of the most disruptive technologies on the internet.</p>
    </div>
  
  </div>

</div>
<div class="clearfixboth"></div>

== List of all APIs ==

{{Concept_Listing
|Query=[[Category:API]][[Category:API_Listings]]
|Use_page_title=No
|List_all_subpages=No
}}

==Contributing to the API documentation==

See the [[WPD:Proposals/api_docs]] for a description of the work being performed to develop the API reference. See [[WPD:Creating_API_pages|Creating API pages]] to learn how to document an API.

==Contributing to the HTML technology==

To contribute to the development of APIs and provide feedback, you need to know where the specification and/or source code is kept. For example, you can find out how to comment on the HTML5 APIs by consulting the [http://www.w3.org/html/ W3C HTML home page], or suggest fixes to Modernizr via the [https://github.com/Modernizr/Modernizr Modernizr Github repo].