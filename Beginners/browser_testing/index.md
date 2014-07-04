{{Page_Title|Part 9: Browser testing}}
{{Flags
|State=Almost Ready
|Editorial notes=Give more examaples on ways to test in browser, not only automated commercial tools, but maybe talk about linting, etc.
|Checked_Out=No
}}
{{Summary_Section|To learn how web browsers react, it is quite useful to have automated tools. But modern browsers are now doing a very good job at behaving the same. Unless you are digging right away with technologies that are still in early adoption, you do not need browser testing tools.}}
{{Basic Page}}

There are a few services to help you test on multiple browsers. While it is very helpful, if you have more than one web browser available its more enough to start learning.

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