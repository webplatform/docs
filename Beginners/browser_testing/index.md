{{Page_Title|Part 9: Browser testing}}
{{Flags
|State=Almost Ready
|Editorial notes=Give more examples on ways to test in browser, not only automated commercial tools, but maybe talk about linting, etc.
|Checked_Out=No
}}
{{Summary_Section|To learn how web browsers react, it is quite useful to have automated tools. But modern browsers are now doing a very good job at behaving the same. Unless you are digging right away with technologies that are still in early adoption, you do not need browser testing tools.}}
{{Basic Page}}
== Topics ==
The '''[[Beginners]]''' section covers the various aspects of web development separated in 9 parts, you can browser through them using this list.

* [[Beginners/the_beginning|1. The beginning]]
* [[Beginners/crash_course|2. A crash course in web site code]]
* '''[[Beginners/planning|3. Planning]]'''
* [[Beginners/html|4. Structuring our content with HTML]]
* [[Beginners/css|5. Styling our content with CSS]]
* [[Beginners/programming|6. Programming fundamentals]]
* [[Beginners/javascript|7. JavaScript]]
* [[Beginners/advanced|8. Advanced topics]]
* [[Beginners/browser_testing|9. Browser testing]]
* [[Beginners/glossary|Glossary]]

== TODO ==
NOTE: This article is not done yet, we have editorial notes, but no content.

== Tools ==

There are many ways to test your web pages. It can be by installing multiple web browsers, have a set of computers and devices, maintain a set of Virtual Machines with the various versions you want to support or even use a service provider that will take snapshots for you.

If you are just starting, a web browser is more than enough. 

'''Also''': It is known and accepted that  "[http://dowebsitesneedtolookexactlythesameineverybrowser.com/ Websites do not ''need'' to look exactly the same in every browsers]". The previous link is a good example of the idea but that’s outside of the scope.

If you want to test various versions of old web browsers, including Microsoft Internet Explorer, you can use a Virtual Machine ("VM"). In fact, Microsoft has created a set of VMs at [http://modern.ie modern.ie] from which you can load and test your sites on. Those VMs aren’t made to use as a main workspace, but merely to boot and try your pages. You can install older version of web browsers on them too.

Note that the  [http://modern.ie modern.ie VMs] will ask you to delete the VM after 30 days. A trick that you can do is to keep a copy of the downloaded archive and extract it again when appropriate.

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