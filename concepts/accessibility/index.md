---
title: 'Web accessibility basics'
notes:
  - "Consider merging with http://docs.webplatform.org/wiki/concepts/accessibility/accessibility_basics\nThere should be an explanation of what ARIA *is* which is not clear from this page nor the link.  Even to a professional web developer.  Wikpedia article (WAI-ARIA) was much clearer and better written as an introduction.\n\nShould be overhauled: there are entire books and careers dedicated to Accessibility: what are the web programming techniques? How to make documents accessible? What disabilities are there and how does that affect e-accessibility? There are also a ton of resources out there that aid accessibility, either through audits or through web navigation."
readiness: 'Ready to Use'
summary: 'Accessibility is making the Web work for people with a diverse range of abilities. Accessibility is essential for developers and organizations that want to create high quality websites and web tools, and not exclude people from using their products and services. Accessibility is vital to enable people with disabilities to participate equally on the Web. It is a legal requirement in some cases, and a best practice in all cases.'
tags:
  - Basic
  - Pages
  - Accessibility
  - ARIA
  - Design
  - UI
  - Usability
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/af
    - concepts/ar
    - concepts/ast
    - concepts/az
    - concepts/bcc
    - concepts/bg
    - concepts/br
    - concepts/ca
    - concepts/cs
    - concepts/da
    - concepts/de
    - concepts/diq
    - concepts/el
    - concepts/eo
    - concepts/fa
    - concepts/fi
    - concepts/fr
    - concepts/gl
    - concepts/gu
    - concepts/he
    - concepts/hu
    - concepts/hy
    - concepts/id
    - concepts/it
    - concepts/ja
    - concepts/ka
    - concepts/kk
    - concepts/km
    - concepts/ko
    - concepts/ksh
    - concepts/kw
    - concepts/mk
    - concepts/ml
    - concepts/mr
    - concepts/ms
    - concepts/nl
    - concepts/no
    - concepts/oc
    - concepts/pl
    - concepts/pt
    - concepts/pt-br
    - concepts/ro
    - concepts/ru
    - concepts/si
    - concepts/sk
    - concepts/sl
    - concepts/sq
    - concepts/sr
    - concepts/sv
    - concepts/ta
    - concepts/th
    - concepts/tr
    - concepts/uk
    - concepts/vi
    - concepts/yue
    - concepts/zh
    - concepts/zh-hans
    - concepts/zh-hant
    - concepts/zh-tw
translations:
  es:
    text: español
    href: /concepts/es
uri: concepts/accessibility

---
## Summary

Accessibility is making the Web work for people with a diverse range of abilities. Accessibility is essential for developers and organizations that want to create high quality websites and web tools, and not exclude people from using their products and services. Accessibility is vital to enable people with disabilities to participate equally on the Web. It is a legal requirement in some cases, and a best practice in all cases.

This page provides an overview of web accessibility and links to resources for more information. We suggest that you read through this whole page first, then go back and follow the links to learn more.

## The Web is for all people

The Web is fundamentally designed to work for all people, whatever their hardware, software, language, culture, location, or physical or mental ability.

When the Web meets this goal, it is accessible to people with a diverse range of hearing, movement, sight, and cognitive ability. Thus the impact of disability is radically changed on the Web because the Web removes barriers to communication and interaction that many people face in the physical world.

However, when websites, web technologies, or web tools are badly designed, they can create barriers that exclude people from using the Web. For example, an inaccessible website could:

-   prevent people who are deaf from getting information from a podcast or video
-   prevent people with cognitive impairments from reading the content because of moving, blinking, or flickering images
-   prevent people with physical impairments from completing a transaction because they cannot use a mouse.

### What is web accessibility?

Web accessibility means that people with disabilities can use the Web. More specifically, it means that people with disabilities can perceive, understand, navigate, and interact with the Web, and that they can contribute to the Web. For an introduction to **why** - the case for web accessibility, **what** - examples of web accessibility, and **how** to make your website and web tools accessible, see [Writing for an Accessible Web](/concepts/accessibility/writing_for_an_accessible_web) and [Accessibility - W3C](http://www.w3.org/standards/webdesign/accessibility).

Web accessibility encompasses all disabilities that affect access to the Web, including people with auditory, cognitive, neurological, physical, speech, and visual disabilities. Accessibility includes people with impairments due to ageing.

While accessibility focuses on people with disabilities, it also benefits others, such as people using mobile devices and people in limiting situations (e.g., a loud environment where they cannot hear audio). **Accessibility supports social inclusion** for people with disabilities, older people, mobile users, people in rural areas, people with low bandwidth connections, people with low literacy, etc. More information is in [Mobile Web](#Mobile_Web) below, [Older users](#Older_users) below, and [Web Accessibility Benefits People With and Without Disabilities](http://www.w3.org/WAI/bcase/soc.html#groups).

### Web accessibility is essential for equal opportunity

The Web is increasingly an essential resource for many aspects of life: education, employment, government, commerce, health care, recreation, social interaction, and more. The Web is used not only for receiving information, but also for providing information and interacting with society. Therefore, it is essential that the Web be accessible in order to provide equal access and equal opportunity to people with disabilities. Indeed, the United Nations recognizes web accessibility as a basic human right. Learn more from [Web Accessibility is a Social Issue](http://www.w3.org/WAI/bcase/soc#social) in the Social Factors page.

## Understand how people use the Web

Stories about people using the Web help to illustrate the everyday needs of people with disabilities. For example:

-   Ms. Olsen attends middle school, and particularly likes her literature class. She has attention deficit hyperactivity disorder (ADHD) and dyslexia, and the combination leads to substantial difficulty in reading.
-   Ms. Laitinen is the chief accountant at an insurance company that uses web-based documents and forms over a corporate intranet. She is blind and, like many other people who are blind, she does not read braille.
-   Mr. Yunus is 85 years old and started to use the Web several years ago to stay in touch with family and friends, and to read about art history. He has reduced vision, hand tremor, and mild short-term memory loss due to ageing.

More details on how these and others use the Web are in [Stories of Web Users](http://www.w3.org/WAI/intro/people-use-web/stories).

 People have a diverse range of abilities that impact how they use the Web. Some people have temporary impairments, some have age-related impairments, some have disabilities from birth, some develop disabilities from injuries or health conditions, and some have multiple disabilities. Some people's abilities change based on fatigue, inflammation, medication, etc. To learn about the diversity of abilities, and about the types of web accessibility barriers that people commonly encounter from poorly designed websites and web tools, see [Diversity of Web Users](http://www.w3.org/WAI/intro/people-use-web/diversity).

People with disabilities access and navigate the Web in different ways. Sometimes people configure standard software and hardware according to their needs, and sometimes people use specialized software or hardware that help them perform certain tasks. To learn about the techniques and tools that people with disabilities use to interact with the Web, such as browser settings, text-to-speech, voice recognition, see [Diversity in Web Use](http://www.w3.org/WAI/intro/people-use-web/browsing).

## Accessibility requirements

In order for people with disabilities to be able to use the Web, there are certain things that websites and web tools need to do. These accessibility requirements fulfill four underlying principles:

1.  **Perceivable** information and user interface.
    Accessibility requirements include: providing text alternative for images, providing captions or transcripts for video and audio, and providing sufficient color contrast between text and background.
2.  **Operable** user interface and navigation.
    Accessibility requirements include: enabling navigation using only a keyboard, providing meaningful hyperlinks, and allowing enough time for users to complete a task.
3.  **Understandable** information and user interface.
    Accessibility requirements include: making content readable, providing predictable functionality, and helping users avoid and correct mistakes.
4.  **Robust** content and reliable interpretation.
    Accessibility requirements include: maximizing compatibility with current and future tools (web browsers, assistive technologies, etc.).

**To learn more about these web accessibility principles and requirements, see [Accessibility Principles](http://www.w3.org/WAI/intro/people-use-web/principles).**

For a short introduction to three web accessibility issues (alternative text for images, keyboard input, and transcripts), see [What: Examples of Web Accessibility](http://www.w3.org/standards/webdesign/accessibility#examples).

## ARIA

"WAI-ARIA describes how to add semantics and other metadata to HTML content in order to make user interface controls and dynamic content more accessible. For example, with WAI-ARIA it is possible to identify a list of links as a navigation menu and to state whether it is expanded or collapsed." For further information please refer to [WAI-ARIA](http://en.wikipedia.org/wiki/WAI-ARIA)

ARIA provides the ability to specify visual information to [accessability software](http://en.wikipedia.org/wiki/Computer_accessibility). The software can then inform the impaired user about the purpose of elements on the page and what "state" they are in.

For an introduction to Rich Internet Application accessibility challenges and solutions, see [WAI-ARIA 1.0 Primer](http://www.w3.org/TR/wai-aria-primer/).

### Learning Materials

[Introduction to Web Accessibility](https://webaccessibility.withgoogle.com) is an online course from Google that introduces tools and techniques for web developers to easily ensure that websites are more accessible to users who are blind or have low vision.

Learn the fundamentals of using ARIA within HTML5, and inspect the accessibility of websites using Google Chrome Extensions: ChromeVox and Accessibility Developer Tools. This course is a starting point for developers to learn how to build accessibility into websites to help users with visual impairments.

## The components of web accessibility

The accessibility principles apply to the components introduced below. It is essential that the components of web development and interaction work together in order for the Web to be accessible to people with disabilities. The W3C Web Accessibility Initiative (WAI) provides guidelines that cover the accessibility requirements of the technical components.

### Web Content

Content is the information in a web page or web **application**, including: natural information such as text, images, and sounds; code or markup that defines structure, presentation, interaction, etc. Content requirements are covered in Web Content Accessibility Guidelines (**WCAG**).

The **WCAG** documents explain how to make web content (including web applications) more accessible to people with disabilities. To learn more about how WCAG is structured and about the supporting documents that provide practical advice for meeting accessibility requirements, see [the **WCAG Overview**](http://www.w3.org/WAI/intro/wcag.php).

### Tools

The tools that we use to create and use web content can help or hinder web accessibility.

-   **Authoring tools** are software and services that are used to create and edit websites; for example, content management systems (CMS), HTML editors, websites that let users add content (such as social media), and other tools. Tools should support people in making their web content accessible, and the tools should be accessible so that people with disabilities can use them. This is covered in Authoring Tool Accessibility Guidelines, see **[ATAG Overview](http://www.w3.org/WAI/intro/atag.php)**.
-   **Evaluation tools** help check if websites meet standards. (Relevant information is in [Selecting Web Accessibility Evaluation Tools](http://www.w3.org/WAI/eval/selectingtools.html).)
-   **Web browsers**, media players, and other "user agents" that access web content are covered in User Agent Accessibility Guidelines, see **[UAAG Overview](http://www.w3.org/WAI/intro/uaag.php)**.
-   **Assistive technologies** are software or hardware that people with disabilities use to improve interaction with the Web, e.g., screen readers that read aloud web pages, voice recognition software, alternative keyboards, etc. (Introduced in [Tools|Techniques|Diversity in Web Use](http://www.w3.org/WAI/intro/people-use-web/browsing.html).)

### People - web content creators and web users

In addition to web content and tools, people are an important component of web accessibility.

**People who create content** need to understand and implement accessibility. This includes developers, designers, authors, managers, etc., anyone who is involved with developing content (including applications), authoring tools, evaluation tools, browsers and other user agents.

**People who use the Web** have different knowledge, experiences, and skill levels that affect accessibility; for example, how well a person knows how to use assistive technologies or adaptive strategies, and if they can get tools to meet their needs.

For more information on these web content, tools, and people components, see the ["Components of Web Accessibility" Presentation](http://www.w3.org/WAI/presentations/components/Overview.php) or [Essential Components of Web Accessibility](http://www.w3.org/WAI/intro/components.php).

## Business case

In order for organizations to be willing to make the initial investment in accessibility, many need to understand the financial benefits of web accessibility. For an introduction, see ["Web Accessibility is Smart Business" Presentation](http://www.w3.org/WAI/presentations/bcase/Overview.php).

To learn more about the social, technical, financial, and legal and policy factors, see [Developing a Web Accessibility Business Case for Your Organization](http://www.w3.org/WAI/bcase/Overview.html). This set of pages presents different aspects of web accessibility along with guidance on developing a customized business case.

For example, one aspect of the business case is reaching more users, including older users and mobile users.

### Older users

Older web users are an increasing market segment and an important target group for many businesses, governments, and other organizations. Many older people have age-related impairments that can affect how they use the Web, such as declining vision, physical ability, hearing, and cognitive ability. These issues overlap with the accessibility needs of people with disabilities. Thus, websites and tools that are accessible to people with disabilities are more accessible to older users as well. For more information, see [Web Accessibility and Older People: Meeting the Needs of Ageing Web Users](http://www.w3.org/WAI/older-users/Overview.php).

### Mobile Web

With global mobile phone use at an all time high, there has been a surge of interest in developing websites that are accessible from a mobile device. Users of mobile devices and people with disabilities experience similar barriers when interacting with Web content. Websites can more efficiently meet both goals when developers understand the significant overlap between making a website accessible for a mobile device and for people with disabilities. For more information, see [Web Content Accessibility and Mobile Web: Making a Web Site Accessible Both for People with Disabilities and for Mobile Devices](http://www.w3.org/WAI/mobile/).

## Learn more from W3C WAI

The W3C Web Accessibility Initiative (WAI) brings together people from industry, disability organizations, government, and research labs from around the world to develop guidelines and resources to help make the Web accessible to people with disabilities. We encourage you to look around the [WAI website](http://www.w3.org/WAI/) and find more information that is useful to you. See [Finding Your WAI ("way") to New Web Accessibility Resources](http://www.w3.org/WAI/yourWAI).

## References and acknowledgements

Referencing this information: Most of the text on this page comes from other documents, which are linked within each section. For references, please use the source document. (See [Using WAI Material: Permission to Use with Attribution](http://www.w3.org/WAI/about/usingWAImaterial.html).)

## See also

-   [This page originally available at W3C WAI](http://www.w3.org/WAI/EO/wiki/Web_Accessibility_Basics)
-   [Improving accessibility using HTML5 features](http://www.w3.org/WAI/GL/wiki/Techniques/HTML5)
-   [Improving accessibility using ARIA features](http://www.w3.org/WAI/GL/wiki/Techniques/ARIA)
-   [HTML and CSS techniques for passing WCAG conformance criteria](http://www.w3.org/TR/WCAG20-TECHS/)
-   [Making Accessible Windows Store apps using JavaScript and HTML](http://msdn.microsoft.com/en-us/library/windows/apps/hh452681.aspx)
-   [Introduction to Web Accessibility by Google](https://webaccessibility.withgoogle.com)
