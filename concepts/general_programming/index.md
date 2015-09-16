---
title: General Programming Concepts
notes:
  - "This article may need to be a topic all its own. However it started, it seems now to be an attempt to provide the reader a compressed version of a four-year software development degree. I have tried to provide a syllabus, but there may be plenty more to add.\nTo explain, I have tried to break down the subjects by level of required background knowledge and essentially develop a syllabus. The first level of the bulleted list is intended to be the link to the concept page and the second level outlines the intended content of the associated concept page.\n\nAs the first-level pages are written to cover the second-level topics, remove the second level topics that have been covered."
readiness: 'In Progress'
summary: 'These articles introduce you to computers, computer programming, computer networking, and programming for the Web specifically.'
tags:
  - Basic
  - Pages
  - CSS
  - HTML
  - JavaScript
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'concepts/general programming/How does a computer run applications'
uri: 'concepts/general programming'

---
## Summary

These articles introduce you to computers, computer programming, computer networking, and programming for the Web specifically.

## Computer Organization and Architecture

-   [What is in a computer?](/concepts/general_programming/What_is_in_a_Computer)
-   [How does a computer work?](/concepts/general_programming/How_does_a_computer_work)
-   [How does a computer run applications?](/w/index.php?title=concepts/general_programming/How_does_a_computer_run_applications&action=edit&redlink=1)
    -   Machine code [[1]](http://en.wikipedia.org/wiki/Machine_code)
    -   Registers, instruction address, heap, stack
    -   Introduce assembler language

## Programming Languages

-   What is the purpose of a programming language?
    -   Easier to read and use than Assembler
-   How are programming languages categorized?
    -   1GL, 2GL, 3GL, etc.
    -   Families (languages derived from, inspired by, or related to other languages)
-   What programming language should I use?
    -   Different languages for different purposes
    -   Different languages for different people

## Networking and the Internet

-   What is the Internet?
-   What is a protocol?
-   What protocols do websites rely on?
    -   ARP, TCP, IP (v4 and v6), HTTP, FTP, SSL
-   What is Http?
-   [What is NAT?](/concepts/general_programming/NAT)

## Basic Programming Concepts

-   How do I store information?
    -   Introduce scalar variables
    -   Assignment operator
-   How do I do arithmetic?
    -   Math operators (add, subtract, multiply, divide, modulo)
    -   Logic operators (bit-wise and, or, xor, not, maybe shifts)
-   How do I make decisions?
    -   if...else if...else
    -   switch...case
-   How do I repeat instructions?
    -   do...while loops
    -   while loops
    -   for loops
-   How do I group instructions?
    -   Introduce functions

## Basic Development Concepts

-   Where should I start?
    -   Design
    -   Pseudo-code
-   What is the "application life cycle"?
    -   Iterative cycle
    -   Design, prototype, development, maintenance
    -   Stress the amount of time and effort spent on maintenance
-   How do I get from start to finish?
    -   Bottom-up design
    -   Top-down design

## Basic Web Development Concepts

-   What do I need to write a website?
    -   Minimum: simple text editor, FTP client (Windows Explorer, ftp command-line)
    -   Freeware and shareware solutions: WYSIWYG editors, Eclipse, Notepad++, GUI FTP clients
    -   Commercial solutions
-   How do I get started with HTML?
    -   What is HTML and what is a simple example?
    -   Stick to basic formatting: p, br, hr, h1...h6, ol, ul, em, strong, a
-   How do I get started with CSS?
    -   What is CSS and what is a simple example?
    -   Stick to basic selectors and properties (tag names only, background-color, color, font-family, font-style, font-weight, text-decoration).
    -   Maybe introduce span tag.
-   How do I get started with JavaScript?
    -   What is JavaScript and what is a simple example?
    -   Keep examples simple: Hello world, simple arithmetic and string operations

## Intermediate Programming Concepts

-   Do I really need to understand math and physics?
    -   How does algebra help? Finding different ways to do the same math.
    -   Unit conversions (em, ex, pt, px, in) and proportions/ratios (screen size, etc.)
    -   Specific applications need trigonometry and physics.
    -   Theory uses differential and integral calculus, multi-variable calculus, series mathematics, sometimes higher mathematics.
-   How do I group information?
    -   Structs, arrays
    -   Basic patterns: queues, stacks, linked lists
-   What is object-oriented programming?
    -   Introduction to objects and inheritance
    -   Private and public
-   How do I put instructions and information together?
    -   Objects
    -   States
    -   Methods
    -   Why should I use getters and setters? (Value validation and access.)
-   What is different between server-side and client-side programming?

## Intermediate Development Concepts

-   How do I reduce my workload?
    -   Design tools: flow charts, pseudo-code, prototypes.
-   How do I reduce my future workload?
    -   Design with maintenance in mind.
    -   Readable code.
    -   Look forward, plan for expansion and integration.
    -   Black-box mentality: good or bad?
-   How can I work as part of a team?
    -   Coding conventions.
    -   Documentation and documentation conventions. (Introduce JavaDoc?)

## Intermediate Web Development Concepts

-   How do I progress with HTML?
    -   More tags: table (caption, thead, tbody, tfoot, tr, th, td), div, dl/dt/dd, form (fieldset, input, button, etc.), abbr, acronym.
    -   Encourage documentation.
    -   Use div for layout, table for tabular data.
    -   Attributes: id, alt, title.
-   How do I progress with CSS?
    -   Expand selectors: class, id, descendant, child selectors.
    -   CSS 2.0.
    -   CSS files.
    -   Encourage documentation.
-   How do I progress with JavaScript?
    -   Script files
    -   O.O.P. with JavaScript.
    -   If not already done, introduce JavaDoc.
-   How do I reach the most people?
    -   Designing an accessible website.
    -   Setting compatibility standards.
-   How do I get started with server-side programming languages?
    -   What are the benefits of a server-side programming language?
    -   Examples of server-side programming languages: ASP, ColdFusion, JSP, PHP, etc.
-   What are SOAP and AJAX?
    -   Introduction to SOAP and AJAX (and other similar technologies or protocols).
    -   How are they used?

## Media, Multimedia and Plugins

-   How do I go beyond text on my website?
    -   Add images to your website.
    -   Basic layout (float img and div).
-   How do I make a site that works well?
    -   Basic design concepts.
    -   Basic UX.
    -   Include links to UX references (Nn/g, etc.).
-   What are plugins and how should I use them?
    -   Any additional software (beyond the browser) is a plugin (PDF, Flash video, audio players).
    -   Accessibility requirements.
    -   When to use them and when to avoid them.

## Introduction to Databases

-   What is a database?
    -   Introduction to databases, tables, fields, and relationships.
-   What is SQL?
    -   Introduction to SQL.
    -   Basic CRUD statements.
-   What is normalization?
    -   Define 1NF, 2NF, 3NF, 4NF, etc.
    -   Recommend 3NF?
-   How should my database reflect my application (or vice versa)?
    -   Define tables as they relate to O.O.P.
    -   Introduce views and stored procedures.

## Advanced Programming Concepts

-   What are design patterns and how do I use them?
    -   Introduce some common design patterns (singleton, factory, template, etc.).
    -   Include links to design pattern reference pages or useful books.
-   What are frameworks and how do I use them?
    -   Introduce different frameworks, such as MVC and specific examples.
-   What are state machines and how do I use them?
    -   Introduce FSMs.
    -   Examples of how FSMs can be used to parse text.
    -   Examples of how FSMs can be used to handle business logic.
-   What is application integration and how does it help me?
    -   Define application integration.
    -   Examples of importing, exporting, and non-proprietary file formats.

## Advanced Development Concepts

-   What is requirement gathering?
-   What is quality assurance and how to I make it easier?
    -   Introduce unit-testing.
-   What is usability testing?
    -   Best practices.
    -   Include links to reference pages or useful books.

## Advanced Web Development Concepts

-   How do I progress with SQL?
    -   Introduce JOIN, UNION, triggers, constraints.
    -   Writing faster queries (benchmarking).
    -   Writing more efficient queries. When to use SQL and when to use server-side code.
-   Is there more to CSS?
    -   CSS 3.0.
    -   Compatibility concerns.
-   What is Web 2.0?
    -   Introduce social networking.
    -   Introduce browser-based MMORPGs.
    -   Introduce other web applications (banking solutions, shopping carts, etc.)
-   What is a CMS?
    -   Blogs, webcomics.
    -   Include example sites, particularly web development blogs.
    -   Include examples of software (WordPress, Plogue, Drupal, etc.)
-   What is jQuery and how do I use it?
    -   Benefits of jQuery.
    -   jQuery libraries and plugins.
-   How do I use AJAX?
    -   What are the benefits?
    -   Using a JavaScript framework (like jQuery) with AJAX.
    -   What are the shortfalls? Accessibility.
-   What is responsive web design?
    -   Introduce RWD and mobile-first design.
    -   Include links to reference pages.

### Original Links

-   [Variables in JavaScript](/concepts/programming/variables_in_javascript)
-   [Style Guides](/concepts/programming/style_guides)
-   [How do computers work?](/concepts/programming/how_do_computers_work)
