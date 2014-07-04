{{Page_Title|Part 9: Browser testing}}
{{Flags
|State=Almost Ready
|Editorial notes=Give more examples on ways to test in browser, not only automated commercial tools, but maybe talk about linting, etc.
|Checked_Out=No
}}
{{Summary_Section|To learn how web browsers react, it is quite useful to have automated tools. But modern browsers are now doing a very good job at behaving the same. Unless you are digging right away with technologies that are still in early adoption, you do not need browser testing tools.}}
{{Basic Page}}
{{Beginners submenu}}

== Tools ==

There are many ways to test your web pages. It can be by installing multiple web browsers, have a set of computers and devices, maintain a set of Virtual Machines with the various versions you want to support or even use a service provider that will take snapshots for you.

If you are just starting, a web browser is more than enough. 

'''Also''': It is known and accepted that  "[http://dowebsitesneedtolookexactlythesameineverybrowser.com/ Websites do not ''need'' to look exactly the same in every browsers]". The previous link is a good example of the idea —try it in an old browser to see. There are many techniques possible to have older browser to support features by detecting if they exist  (called "feature sniffing" with [http://modernizr.com Modernizr] for example), and conditionally add library that will add support (we call them "Polyfils" or "shims"). The essential to remember here is that web technology changes quickly and we cannot expect old web browsers to support more recent features. Its as if we would ask a black and white television to be in colors. But all that is beyond the scope of testing your site!

=== In a Virtual Machine ===

If you want to test various versions of old web browsers but you do not see how you can have more than one version of a given web browser, you should consider using Virtual Machines ("VMs").

A VM is like a big file that you can load inside a software as if it was a computer. In fact, that software is emulating hardware and acts as if it was a separate physical machine. We call this "Virtualization". It therefore runs a computer ''inside'' another computer. People creating software and services "in the cloud" are heavily relying on similar technologies.

For example, if you have only a recent computer and you want to see how it will look like in Internet Explorer provided in Windows Vista, you can have a VM that runs Vista and Internet Explorer 7 along with Mozilla Firefox 3.

For this, you can get what we call a "Desktop Virtualization" software, there are a few on the market. Oracle [https://www.virtualbox.org/ VirtualBox] and VMWare has both free versions that can make anybody run VMs.

Once you have a Virtualization software, you will need to use or create your own VMs. While creating a VM is outside of the scope of this article, you can download from Microsoft —for free— one of their testing VMs. Take a look at [http://modern.ie modern.ie].

With this in hand, you can test on various version of the web browsers you want to support, without cluttering your own computer.

'''About Modern.ie VMs'': Note that those VMs are made only to test and cannot be used as a main work environment. The VM will eventually ask you delete the VM (e.g. after 30 days). A trick that you can do is to keep a copy of the downloaded archive and extract it again.

=== Mobile devices ===

Many of us, web developers, keep a set of old computers and smartphones only for that. Those comes in handy when we are building features and want to see if it works well, or if our polyfill actually works.

=== Automated browser testing ===

As for automated browser testing, its is only useful if you work on bigger projects and goes beyond the scope of this section. 

There are  a few automated browser testing services. They do not require you to install anything and they give you screenshots of the pages you are providing them on various browser versions, including the mobile ones.  

Here is a list of browser testing:
* [http://www.browserstack.com/ BrowserStack] (commercial)
* [http://browsershots.org/ Browsershots] (Screenshots only)
* [http://crossbrowsertesting.com/ CrossBrowserTesting] (commercial)
* [https://saucelabs.com/ SauceLabs] (free and commercial plans). 

For more information, check those [[concepts/cross_browser_techniques|articles on cross-browser debugging]].
{{Notes_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}