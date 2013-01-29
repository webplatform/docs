{{Page_Title|Introduction to content security policy}}
{{Flags
|High-level issues=Needs Flags
}}
{{Byline
|Name=Mike West
|Published=June 15, 2012
}}
{{Summary_Section|Provides an overview of Content Security Policy (CSP)}}
{{Tutorial
|Content===Introduction==

'''Caution:''' This article discusses APIs that are not yet fully standardized and still in flux. Be cautious when using experimental APIs in your own projects.

The web’s security model is rooted in the [http://en.wikipedia.org/wiki/Same_origin_policy ''same origin policy'']. Code from <code>https://mybank.com</code> should only have access to <code>https://mybank.com</code>’s data, and <code>https://evil.example.com</code> should certainly never be allowed access. Each origin is kept isolated from the rest of the web, giving developers a safe sandbox in which to build and play. In theory, this is perfectly brilliant. In practice, attackers have found clever ways to subvert the system.

[http://en.wikipedia.org/wiki/Cross-site_scripting Cross-site scripting (XSS)] attacks, for example, bypass the same origin policy by tricking a site into delivering malicious code along with the intended content. This is a huge problem, as browsers trust all of the code that shows up on a page as being legitimately part of that page’s security origin. The [http://ha.ckers.org/xss.html XSS Cheat Sheet] is an old but representative cross-section of the methods an attacker might use to violate this trust by injecting malicious code. If an attacker successfully injects ''any'' code at all, it’s pretty much game over: user session data is compromised and information that should be kept secret is exfiltrated to The Bad Guys™. We’d obviously like to prevent that if possible.

This tutorial highlights one promising new defense that can significantly reduce the risk and impact of XSS attacks in modern browsers: Content Security Policy (CSP).

==Source Whitelists==

The core issue exploited by XSS attacks is the browser’s inability to distinguish between script that’s intended to be part of your application, and script that’s been maliciously injected by a third-party. For example, the Google +1 button at the top of this article loads and executes code from <code>https://apis.google.com/js/plusone.js</code> in the context of this page’s origin. We trust that code, but we can’t expect the browser to figure out on it’s own that code from <code>apis.google.com</code> is awesome, while code from <code>apis.evil.example.com</code> probably isn’t. The browser happily downloads and executes any code a page requests, regardless of source.

Instead of blindly trusting ''everything'' that a server delivers, CSP defines the <code>Content-Security-Policy</code> HTTP header that allows you to create a whitelist of sources of trusted content, and instructs the browser to only execute or render resources from those sources. Even if an attacker can find a hole through which to inject script, the script won’t match the whitelist, and therefore won’t be executed.

Since we trust <code>apis.google.com</code> to deliver valid code, and we trust ourselves to do the same, let’s define a policy that only allows script to execute when it comes from one of those two sources:

 <code>Content-Security-Policy: script-src 'self' https://apis.google.com
 </code>

Simple, right? As you probably guessed, '''<code>script-src</code>''' is a directive that controls a set of script-related privileges for a specific page. We’ve specified <code>'self'</code> as one valid source of script, and <code>https://apis.google.com</code> as another. The browser will dutifully download and execute JavaScript from <code>apis.google.com</code> over HTTPS, as well as from the current page’s origin.

With this policy defined, the browser will simply throw an error instead of loading script from any other source. When a clever attacker does manage to inject code into your site, she’ll run headlong into an error message, rather than the success she was expecting:

[[Image:csp-error.png.pagespeed.ce.8abh9RZ6bz.png|Console error: "Refused to load the script 'http://evil.example.com/evil.js' because it violates the following Content Security Policy directive: "script-src 'self' https://apis.google.com"."]]

===Policy applies to a wide variety of resources===

While script resources are the most obvious security risks, CSP provides a rich set of policy directives that enable fairly granular control over the resources that a page is allowed to load. You’ve already seen <code>script-src</code>, so the concept should be clear. Let’s quickly walk through the rest of the resource directives:

* '''<code>connect-src</code>''' limits the origins to which you can connect (via XHR, WebSockets, and EventSource).
* '''<code>font-src</code>''' specifies the origins that can serve web fonts. Google’s Web Fonts could be enabled via <code>font-src https://themes.googleusercontent.com</code>
* '''<code>frame-src</code>''' lists the origins that can be embedded as frames. For example: <code>frame-src https://youtube.com</code> would enable embedding YouTube videos, but no other origins.
* '''<code>img-src</code>''' defines the origins from which images can be loaded.
* '''<code>media-src</code>''' restricts the origins allowed to deliver video and audio.
* '''<code>object-src</code>''' allows control over Flash and other plugins.
* '''<code>style-src</code>''' is <code>script-src</code>’s counterpart for stylesheets.

By default, directives are wide open. If you don’t set a specific policy for a directive, let’s say <code>font-src</code>, then that directive behaves by default as though you’d specified <code><nowiki>*</nowiki></code> as the valid source (e.g. you could load fonts from everywhere, without restriction).

You can override this default behavior by specifying a '''<code>default-src</code>''' directive. This directive, as you might suspect, will define the defaults for any directive you leave unspecified. If <code>default-src</code> is set to <code>https://example.com</code>, and you fail to specify a <code>font-src</code> directive, then you can load fonts from <code>https://example.com</code>, and nowhere else. We specified only <code>script-src</code> in our earlier examples, which means that images, fonts, and so on can be loaded from any origin.

You can use as many or as few of these directives as makes sense for your specific application, simply listing each in the HTTP header, separating directives with semicolons. You’ll want to make sure that you list ''all'' required resources of a specific type in a ''single'' directive. If wrote something like <code>script-src https://host1.com; script-src https://host2.com</code> the second directive would simply be ignored. <code>script-src https://host1.com https://host2.com</code> would correctly specify both origins as valid.

If, for example, you have an application that loads all of it’s resources from a content delivery network (say, <code>https://cdn.example.net</code>), and know that you don’t need framed content or any plugins at all, then your policy might look like the following:

 <code>Content-Security-Policy: default-src https://cdn.example.net; frame-src 'none'; object-src 'none'
 </code>

===Implementation Details===

Before moving further, it’s important to note that the canonical header I’ve used in the examples is <code>Content-Security-Policy</code>, but current browsers have implemented the feature behind a prefix: Firefox uses <code>X-Content-Security-Policy</code>, and WebKit-based browsers (Safari and Chrome) use <code>X-WebKit-CSP</code>. The implementations are quite similar, however, and are converging rapidly on the standard. This article will continue to use <code>Content-Security-Policy</code>, as browsers will migrate to that header, but the prefixes are essential for the moment.

Regardless of the header you use, policy is defined on a page-by-page basis: you’ll need to send the HTTP header along with every response that you’d like to ensure is protected. This provides a lot of flexibility, as you can fine-tune the policy for specific pages based on their specific needs. Perhaps one set of pages in your site has a +1 button, while others don’t: you could allow the button code to be loaded only when necessary.

The source list in each directive is fairly flexible. You can specify sources by scheme (<code>data:</code>, <code>https:</code>), or ranging in specificity from hostname-only (<code>example.com</code>, which matches any origin on that host: any scheme, any port) to a fully qualified URI (<code>https://example.com:443</code>, which matches only HTTPS, only <code>example.com</code>, and only port 443). Wildcards are accepted, but only as a scheme, a port, or in the leftmost position of the hostname: <code><nowiki>*://*.example.com:*</nowiki></code> would match all subdomains of <code>example.com</code> (but ''not'' <code>example.com</code> itself), using any scheme, on any port.

Four keywords are also accepted in the source list:

* '''<code>'none'</code>''', as you might expect, matches nothing.
* '''<code>'self'</code>''' matches the current origin, but not its subdomains.
* '''<code>'unsafe-inline'</code>''' allows inline JavaScript and CSS (we’ll touch on this in more detail in a bit).
* '''<code>'unsafe-eval'</code>''' allows text-to-JavaScript mechanisms like <code>eval</code> (we’ll get to this too).

These keywords require single-quotes. <code>script-src 'self'</code> authorizes the execution of JavaScript from the current host. <code>script-src self</code> allows JavaScript from a server named “<code>self</code>” (and ''not'' from the current host), which probably isn’t what you meant.

===Sandboxing===

There’s one more directive worth talking about: '''<code>sandbox</code>'''. It’s a bit different than the others we’ve looked at, as is places restrictions on actions the page can take, rather than on resources that the page can load. If the <code>sandbox</code> directive is present, the page will be treated as though it was loaded inside of an <code>iframe</code> with a <code>sandbox</code> attribute. This can have a wide range of effects on the page: forcing the page into a unique origin, and preventing form submission, among others. It’s a bit beyond the scope of this article, but you can find full details on valid sandboxing attributes in the [http://www.whatwg.org/specs/web-apps/current-work/multipage/origin-0.html#sandboxing-flag-set “sandboxing flag set” section of the HTML5 spec].

==Inline Code Considered Harmful==

It should be clear that CSP is based on whitelisting origins, as that’s an unambiguous way of instructing the browser to treat specific sets of resources as acceptable and to reject the rest. Origin-based whitelisting doesn’t, however, solve the biggest threat posed by XSS attacks: inline script injection. If an attacker can inject a script tag that directly contains some malicious payload (<code><script>sendMyDataToEvilDotCom();</script></code>), the browser has no mechanism by which to distinguish it from a legitimate inline script tag. CSP solves this problem by banning inline script entirely: [https://www.youtube.com/watch?v=aCbfMkh940Q it’s the only way to be sure].

This ban includes not only scripts embedded directly in <code>script</code> tags, but also inline event handlers and <code>javascript:</code> URLs. You’ll need to move the content of <code>script</code> tags into an external file, and replace <code>javascript:</code> URLs and <code><a ... onclick="[JAVASCRIPT]"></code> with appropriate <code>addEventListener</code> calls. For example, you might rewrite the following from:

 <code><script>
   function doAmazingThings() {
     alert('YOU AM AMAZING!');
   }
 </script>
 <button onclick='doAmazingThings();'>Am I amazing?</button>
 </code>

to something more like:

 <code><!-- amazing.html -->
 <script src='amazing.js'></script>
 <button id='amazing'>Am I amazing?</button>
 </code>

 <code>// amazing.js
 function doAmazingThings() {
   alert('YOU AM AMAZING!');
 }
 document.addEventListener('DOMContentReady', function () {
   document.getElementById('amazing')
           .addEventListener('click', doAmazingThings);
 });
 </code>

The rewritten code has a number of advantages above and beyond working well with CSP; it’s already best practice, regardless of your use of CSP. Inline JavaScript mixes structure and behavior in exactly the way you shouldn’t. External resources are easier for browsers to cache, more understandable for developers, and conducive to compilation and minification. You’ll write better code if you do the work to move code into external resources.

Inline style is treated in the same way: both the <code>style</code> attribute and <code>style</code> tags should be consolidated into external stylesheets to protect against a variety of [http://scarybeastsecurity.blogspot.com/2009/12/generic-cross-browser-cross-domain.html surprisingly clever] data exfiltration methods that CSS enables.

If you really, absolutely must have inline script and style, you can enable it by adding <code>'unsafe-inline'</code> as an allowed source in a <code>script-src</code> or <code>style-src</code> directive. But please don’t. Banning inline script is the biggest security win CSP provides, and banning inline style likewise hardens your application. It’s a little bit of effort up front to ensure that things work correctly after moving all the code out-of-line, but that’s a tradeoff that’s well worth making.

==Eval Too==

Even when an attacker can’t inject script directly, she might be able to trick your application into converting otherwise inert text into executable JavaScript and executing it on her behalf. <code>eval()</code>, <code>new Function()</code>, <code>setTimeout([string], ...)</code>, <code>and setInterval([string], ...)</code> are all vectors through which injected text might end up executing something unexpectedly malicious. CSP’s default response to this risk is, unsurprisingly, to block all of these vectors completely.

This has a more than few impacts on the way you build applications:

* Parse JSON via the built-in <code>JSON.parse</code>, rather than relying on <code>eval</code>. Native JSON operations are available in [http://caniuse.com/#feat=json every browser since IE8], and they’re completely safe.
* Rewrite any <code>setTimeout</code> or <code>setInterval</code> calls you’re currently making with inline functions rather than strings. For example: <code>setTimeout("document.querySelector('a').style.display = 'none';", 10);
 </code>would be better written as: <code>setTimeout(function () {
   document.querySelector('a').style.display = 'none';
 }, 10);
 </code>
* Avoid inline templating at runtime: Many templating libraries use <code>new Function()</code> liberally to speed up template generation at runtime. It’s a nifty application of dynamic programming, but comes at the risk of evaluating malicious text. Some frameworks support CSP out of the box, falling back to a robust parser in the absence of <code>eval</code><nowiki>; </nowiki>[http://docs.angularjs.org/api/angular.module.ng.$compileProvider.directive.ngCsp AngularJS’s ng-csp directive] is a good example of this.

You’re even better off, however, if your templating language of choice offers precompilation ([http://handlebarsjs.com/precompilation.html Handlebars does], for instance). Precompiling your templates can make the user experience even faster than the fastest runtime implementation, and it’s safer too. Win, win! If eval and its text-to-JavaScript brethren are completely essential to your application, you can enable them by adding <code>'unsafe-eval'</code> as an allowed source in a <code>script-src</code> directive. But, again, please don’t. Banning the ability to execute strings makes it much more difficult for an attacker to execute unauthorized code on your site.

==Reporting==

CSP’s ability to block untrusted resources client-side is a huge win for your users, but it would be quite helpful indeed to get some sort of notification sent back to the server so that you can identify and squash any bugs that allow malicious injection in the first place. To this end, you can instruct the browser to <code>POST</code> JSON-formatted violation reports to a location specified in a '''<code>report-uri</code>''' directive.

 <code>Content-Security-Policy: default-src 'self'; ...; report-uri /my_amazing_csp_report_parser;
 </code>

Those reports will look something like the following:

 <code>{
   "csp-report": {
     "document-uri": "http://example.org/page.html",
     "referrer": "http://evil.example.com/",
     "blocked-uri": "http://evil.example.com/evil.js",
     "violated-directive": "script-src 'self' https://apis.google.com",
     "original-policy": "script-src 'self' https://apis.google.com; report-uri http://example.org/my_amazing_csp_report_parser"
   }
 }
 </code>

It contains a good chunk of information that will help you track down the specific cause of the violation, including the page on which the violation occurred ('''<code>document-uri</code>'''), that page’s referrer (referrer, note that the key is ''not'' misspelled), the resource that violated the page’s policy ('''<code>blocked-uri</code>'''), the specific directive it violated ('''<code>violated-directive</code>'''), and the page’s complete policy ('''<code>original-policy</code>''').

===Report-Only===

If you’re just starting out with CSP, it makes sense to evaluate the current state of your application before rolling out a draconian policy to your users. As a stepping stone to a complete deployment, you can ask the browser to monitor a policy, reporting violations, but not enforcing the restrictions. Instead of sending a <code>Content-Security-Policy</code> header, send a <code>Content-Security-Policy-Report-Only</code> header.

 <code>Content-Security-Policy-Report-Only: default-src 'self'; ...; report-uri /my_amazing_csp_report_parser;
 </code>

The policy specified in report-only mode won’t block restricted resources, but it will send violation reports to the location you specify. You can even send ''both'' headers, enforcing one policy while monitoring another. This is a great way to evaluate the effect of changes to your application’s CSP: turn on reporting for a new policy, monitor the violation reports and fix any bugs that turn up, then start enforcing the new policy once you’re satisfied with its effect.

==Real World Usage==

CSP is quite usable in Chrome 16+ and Firefox 4+, and it’s expected to gain at least limited support in IE 10. Safari’s current implementation is lacking, but WebKit nightlies work just as well as Chrome, so there’s hope for the next iteration of Safari. Massive sites like Twitter have deployed the header ([http://engineering.twitter.com/2011/03/improving-browser-security-with-csp.html Twitter’s case study] is worth a read), and the standard is very much ready for you to start playing around on your own sites.

The first step towards crafting a policy for your application is to evaluate the resources you’re actually loading. Once you think you have a handle on how things are put together in your app, set up a policy based on those requirements. Let’s walk through a few common use-cases, and determine how we’d best be able to support them within the protective confines of CSP:

===Use Case #1: Social media widgets===

* Google’s [http://www.google.com/intl/en/webmasters/+1/button/index.html +1 button] includes script from <code>https://apis.google.com</code>, and embeds an <code>iframe</code> from <code>https://plusone.google.com</code>. You’ll need a policy that includes both these origins in order to embed the button. A minimal policy would be <code>script-src https://apis.google.com; frame-src https://plusone.google.com</code>. You’ll also need to ensure that the snippet of JavaScript that Google provides is pulled out into an external JavaScript file.
* Facebook’s [http://developers.facebook.com/docs/reference/plugins/like/ Like button] has a number of implementation options. I’d recommend sticking with the <code>iframe</code> version, as it’s safely sandboxed from the rest of your site. That would require a <code>frame-src https://facebook.com</code> directive to function properly. Note that, by default, the <code>iframe</code> code Facebook provides loads a relative URL, <code>//facebook.com</code>. Please change that to explicitly specify HTTPS: <code>https://facebook.com</code>. There’s no reason to use HTTP if you don’t have to.
* Twitter’s [https://twitter.com/about/resources/buttons Tweet button] relies on access to a script and frame, both hosted at <code>https://platform.twitter.com</code> (Twitter likewise provides a relative URL by default: please edit the code to specify HTTPS when copy/pasting it locally). You’ll be all set with <code>script-src https://platform.twitter.com; frame-src https://platform.twitter.com</code>, as long as you move the JavaScript snippet Twitter provides out into an external JavaScript file.
* Other platforms will have similar requirements, and can be addressed similarly. I’d suggest just setting a <code>default-src</code> of <code>'none'</code>, and watching your console to determine which resources you’ll need to enable to make the widgets work.

Including multiple widgets is straightforward: simply combine the policy directives, remembering to merge all resources of a single type into a single directive. If you wanted all three, the policy would look like:

 <code>script-src https://apis.google.com https://platform.twitter.com; frame-src https://plusone.google.com https://facebook.com https://platform.twitter.com
 </code>

===Use Case #2: Lockdown===

Assume for a moment that you run a banking site, and want to make very sure that only those resources you’ve written yourself can be loaded. In this scenario, start with a default policy that blocks absolutely everything (<code>default-src 'none'</code>), and build up from there.

Let’s say the bank loads all images, style, and script from a CDN at <code>https://cdn.mybank.net</code>, and connects via XHR to <code>https://api.mybank.com/</code> to pull various bits of data down. Frames are used, but only for pages local to the site (no third-party origins). There’s no Flash on the site, no fonts, no nothing. The most restrictive CSP header that we could send in this scenario is:

 <code>Content-Security-Policy: default-src 'none'; script-src https://cdn.mybank.net; style-src https://cdn.mybank.net; img-src https://cdn.mybank.net; connect-src https://api.mybank.com; frame-src 'self'
 </code>

===Use Case #3: SSL Only===

A wedding-ring discussion forum admin wants to ensure that all resources are only loaded via secure channels, but doesn’t really write much code; rewriting large chunks of the third-party forum software that’s filled to the brim with inline script and style is beyond his abilities. The following policy would be effective:

 <code>Content-Security-Policy: default-src https:; script-src https: 'unsafe-inline'; style-src https: 'unsafe-inline'
 </code>

Even though <code>https:</code> was specified in <code>default-src</code>, the script and style directives don’t automatically inherit that source. Each directive overwrites the default completely for that specific type of resource.

==The Future==

The W3C’s [http://www.w3.org/2011/webappsec/ Web Application Security Working Group] is working through the details of the Content Security Policy specification, and a 1.0 version containing the functionality outlined in this article is fairly close to [http://lists.w3.org/Archives/Public/public-webappsec/2012Jun/0011.html moving to Last Call]. The group isn’t sitting around patting themselves on the back, however: CSP 1.1 is being actively discussed on the [http://lists.w3.org/Archives/Public/public-webappsec/ public-webappsec@ mailing list], and browser vendors are [https://lists.webkit.org/pipermail/webkit-dev/2012-May/020559.html hard at work] solidifying and improving their implementations.

CSP 1.1 has a few interesting bits on the drawing board, a few are worth highlighting here:

* '''Policy injection via <code>meta</code> tags:''' CSP’s preferred delivery mechanism is an HTTP header. It can be very useful, however, to set a policy on a page directly in the markup, or via script. There’s some healthy debate about whether or not setting policy from within the same document to which the policy should apply, but it appears to have a solid enough use-case to make it into the next iteration. The [https://dvcs.w3.org/hg/content-security-policy/raw-file/tip/csp-specification.dev.html#html-meta-element--experimenta <code>meta</code> element portion of the spec] is far enough along that WebKit has already implemented the feature, so you can play around with it now in Chrome: throw <code><meta http-equiv="X-WebKit-CSP" content="[POLICY GOES HERE]"></code> in the head of your document, and you’re good to go.You can even inject a policy at runtime by adding the <code>meta</code> tag via script. A good first step towards a fully locked-down application is to inject an appropriate policy after your application has loaded all the resources it needs, and “booted up”. This gives you a mostly secure site (there’s still significant risk of attack during this vulnerable phase), but allows you to reap some of the advantage of CSP while migrating to the HTTP header.
* '''DOM API:''' If this feature makes it into the next iteration of CSP, you’ll have the ability to query a page’s current policy via JavaScript, which will enable you to make runtime decisions about implementations, and gracefully settle on something that will work for the environment in which your code finds itself. If <code>eval()</code> is available, for example, your code might implement some feature differently. This will be particularly useful for framework authors; the API spec is still very much in flux, and you’ll find the most up-to-date iteration in the [https://dvcs.w3.org/hg/content-security-policy/raw-file/tip/csp-specification.dev.html#script-interfaces “Script Interfaces” section of the draft spec].
* '''New directives:''' A variety of new directives are being discussed, including [https://dvcs.w3.org/hg/content-security-policy/raw-file/tip/csp-specification.dev.html#script-nonce--experimental '''<code>script-nonce</code>'''], which would enable inline script only for explicitly specified script elements; [https://dvcs.w3.org/hg/content-security-policy/raw-file/tip/csp-specification.dev.html#plugin-types--experimental '''<code>plugin-types</code>'''], which would limit the <code>MIME</code> types of content for which plugins could be loaded; [https://dvcs.w3.org/hg/content-security-policy/raw-file/tip/csp-specification.dev.html#form-action--experimental '''<code>form-action</code>'''], which would allow form submission to only specific origins; and a few others that are [https://dvcs.w3.org/hg/content-security-policy/raw-file/tip/csp-specification.dev.html#frame-options--experimental currently less completely specified].

If you’re interested in the discussion around these upcoming features, [http://lists.w3.org/Archives/Public/public-webappsec/ skim the mailing list archives], or join in yourself.
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_version=25
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Unknown
|Firefox_version=
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_version=25
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}
{{See_Also_Section}}
{{Topics|Security}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}