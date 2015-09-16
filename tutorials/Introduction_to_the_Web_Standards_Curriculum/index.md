---
title: 'Introduction to the Web Standards Curriculum'
tags:
  - Tutorials
  - WSC
uri: 'tutorials/Introduction to the Web Standards Curriculum'

---
## Introduction

All the authors who have contributed to this course are passionate about the Web, and big believers in open web standards. We all wanted to do our bit to help make the Web a better place, and I think this comes back to the issue of education, whether that’s teaching people how to collaborate and have more respect for one another, or teaching them how to make their web sites more cross-browser compatible and be accessible and usable by a diverse audience (for example people with disabilities, on slow connections, on mobile devices, etc.) Web standards are key to all of this, so we decided to put our time and energy into something that would help increase the adoption of web standards on the Web today and in the future.

Welcome to Web Standards Curriculum, a course designed to give anyone a solid grounding in web design/development, no matter who they are — it is completely free to use, accessible, and assumes no previous knowledge. We are mainly aiming this at universities, as web standards teaching is lacking in many web-related university courses, but you should be able to get value from the course regardless of your age or position in life, as long as you have an interest in building web sites/applications the right way.

## Why web standards?

Let's go briefly through the main reasons why it is such a good idea to adopt web standards in your web development work (these are expanded on in later articles). Using web standards and associated best practices confers the following benefits:

1.  **Efficiency of code**: A lot of best practice web standards usage is all about reusing code — writing code once, and then reusing it wherever it is needed.
2.  **Ease of maintenance**: This follows closely on from the last point — if you can write code only once, and then apply it wherever needed, then if you need to change something at a later date you can just make the change in one place and it propagates throughout the entire web site, rather than having to specify that change everywhere that it is needed!
3.  **Accessibility**: The next two points are closely related — one of the big ideals of the Web is *making web sites accessible to everyone, no matter who they are, regardless of circumstance*. This includes making web sites usable by people with impairments such as blindness/visual impairment and mobility impairment (ie, people who have restricted movement). By using web standards and best practices, you’ll be able to make your web sites more accessible to this significant group of the web audience with little or no extra effort.
4.  **Device compatibility**: This means ensuring that your web sites will work not only across different platforms — ie Windows, Mac, Linux — but also alternative browsing devices, including mobile phones, TVs, tablets and games consoles. Using web standards and best practices, you significantly increase the likelihood of your web sites working across such devices. There are more web-capable mobile phones in the world than desktop computers, so can you or your clients afford to miss out on this market?
5.  **Web crawlers/search engines**: By this, we are talking about what is termed *search engine optimization* — the practice of making your web sites as visible as possible to the so–called web crawlers that crawl the web and index web sites, giving you better search rankings on sites such as Google. There is a science to this (see SEO articles such as [Intelligent site structure for better SEO!](http://dev.opera.com/articles/view/intelligent-site-structure-for-better-se/) and [Semantic HTML and Search Engine Optimization](http://dev.opera.com/articles/view/semantic-html-and-search-engine-optimiza/)) but yet again, just by using web standards you will make your site a lot more visible on Google, Yahoo!, etc., which is good for business.

Even with all these advantages however, most sites on the Web still do not follow web standards, and many web developers working today still use bad, outdated practices. "Why?", you ask. There are a number of reasons for this — people will cite lack of education, company policy, not needing to learn standards because they are getting paid anyway, it’s too hard to learn, standards support in web browsers… Let’s look at each one of these in more detail, and then look at the counter arguments, to try to get rid of any excuse for not adopting/learning standards.

1.  **Lack of education**: This is one of the main reasons this course was created. A lot of universities don’t teach web standards very well in their web–related courses, and a lot of curricula tend to contain outdated practices, and are hard to change due to bureaucracy. Books and training courses tend to be expensive. But wait! Now we’ve provided a course for educators to base their curricula on that’s free!
2.  **Company policy**: There is no doubt that some companies/institutions still have really old and outdated web sites. They may have policies that force their employees to use outdated browsers, but it is getting better, and now that there is a free course available to easily show how to make changes, things should improve further. Upgrading a web site to modern standards encourages companies to upgrade the browsers that they use, as sites will look better in modern browsers. Companies should encourage their customers to upgrade as well. There is sound business reasoning — sites that use web standards, as explained above, will yield better search engine results and be more accessible to people with disabilities and users of alternative devices. Can companies afford to ignore this audience?
3.  **"I don’t need to learn them!"**: I know some developers will sit there and say "but I’m using outdated practices and still getting paid — so why do I need to bother with this new stuff?" As explained above, it makes your code more efficient, easier to write, and easier to maintain. And it allows you to write modern code that is accessible and usable on alternative devices — isn’t that exciting? It will also make your skillset more future–proof, and make you capable of earning more. A lot of job ads request web standards knowledge these days.
4.  **"It’s too hard to learn!"**: Rubbish. After reading some of this course, you’ll realize how easy it is to pick up the basics of using web standards, whether you’re new to web development/design, or an existing web person upgrading your skillset.
5.  **Standards support in browsers**: Standards support in browsers used to differ greatly, which made getting web sites to work across different browsers a nightmare. But those days are gone — modern browsers all have decent web standards support, and you can build sites so that they will still work in older browsers, even if they don't support all the latest technologies.

So as you can see, there’s really not any excuse to not adopt web standards in your web development work. At least if you are coming to this course from the point of view of a beginner, you are starting off on the right foot and learning best practices from the start, rather than having to unlearn bad practices.

OK, so we keep talking about these bad practices in hushed tones, like they’re the secret plans to the Death Star or something. We are not going to cover these practices in this course, as we don’t believe we should; we think you should just be sent along the correct path to begin with. You are however probably wondering what they are, so let’s just talk about them briefly.

In the old days, people used to do things like:

-   Laying out their web sites inside giant tables, using the different table cells to position their graphics, text etc (not what tables were intended for, adds superfluous markup to the page).
-   They used to use invisible images called spacer GIFs to fine tune positioning of page elements (not what images are intended for, add superfluous markup and images to the page).
-   They used to write JavaScript that generated menus etc on the fly (no good for people with JavaScript disabled in their browsers, or people with visual impairments using screenreaders, which get confused by such JavaScript) or worked on only one browser (what about people using other browsers?).
-   They used to insert styling information directly into the HTML using `<font>` elements (terrible for maintenance, and adds superfluous markup to the page).

And the list goes on, including many other crimes against web development. The worst thing is that I say "in the old days" above, but the fact is that a lot of people are still doing things like this! Web development is a messy skill at the best of times, but bad practices like these just make it harder. Using web standards and best practices, as outlined in this course, is the best way to go.

## Article structure

The course is composed of several articles; each article focuses on a specific microtopic, including background on the topic, essential theory, practical examples and walkthrough tutorials to follow, and exercise questions to test your knowledge.

## Who should use this course?

This course is aimed at pretty much anyone who wants to learn web standards–based web design from scratch. It is intended to take the reader from nothing more than a basic familiarity with browsing the Web to being competent with HTML, CSS and JavaScript, including cutting edge HTML5/CSS3 features, and having a good degree of knowledge of surrounding concepts such as information architecture, UX, mobile optimization/adaptive design and typography.

It should give you enough knowledge to start thinking about entering the job market with confidence (obviously experience can’t be taught).

Who is it aimed at? It should be usable by anyone who wants to learn web design "the right way":

1.  **University/college students and teachers**: we have mentioned this already — this is an ideal set of articles to either create your own course from and deliver it to students, or use parts of to supplement your own course. To any students already studying some kind of web–related course, you should use this material to supplement your knowledge, and lobby your teachers into considering it as well!
2.  **Pre–college/university age students**: While this course has been mainly written with adults in mind, there is no reason why younger students can’t benefit from it — have a go and see how you get on.
3.  **Existing web designers and developers**: There are a lot of existing web developers and designers out there who either aren’t using web standards and best practices and should brush up their knowledge, or could use an easily accessible reference to look things up in. To the former, we urge you to give this course a chance and see how easy and valuable web standards are to adopt. To the latter, we're sure you will find this course useful in helping others, brushing up on your skills, looking up hard–to–recall facts, and finding ammunition to help convince bosses and clients that things such as accessibility make a lot of sense.
4.  **Educators inside companies**: This is an ideal way to provide inexpensive training to employees.

We are not expecting people to pay to use this course — it is released on a Creative Commons license, so freely available to anyone who wants to make use of it, as long as they give us the proper attribution.

## Acknowledgements

The number of people who have helped with this course are too numerous to mention all by name, but you know who you are. We'd like to give you all our admiration and gratitude.

## Find out more

We are constantly looking to improve this course, and get it adopted by as many people as possible. If you have any suggestions for how the course could be improved, any general comments to share, or want to talk to me about adopting it somewhere, then get in touch. You can ask questions or keep up to date with the latest happenings on the [W3C public evangelist mailing list](http://lists.w3.org/Archives/Public/public-evangelist/), or by e-mailing Chris Mills at cmills [at] opera [dot] com. Feel free also to post queries on the discussion page for each article (the "discussion" link at the top of each page), or make edits if you think you could improve it (the "edit" link at the top of each page). To find out about such contributions, read [Web Education moving forward — Opera WSC goes to the W3C!](http://my.opera.com/ODIN/blog/2011/07/15/web-education-moving-forward-opera-wsc-goes-to-the-w3c)

Note: This material was originally published as part of the Opera Web Standards Curriculum, available as [Introductory material](http://dev.opera.com/articles/view/1-introduction-to-the-web-standards-cur/), written by Chris Mills. Like the original, it is published under the [Creative Commons Attribution, Non Commercial — Share Alike 2.5](http://creativecommons.org/licenses/by-nc-sa/2.5/) license.
