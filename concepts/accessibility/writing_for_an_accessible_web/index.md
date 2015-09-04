---
title: writing for an accessible web
tags:
  - Concept
  - Pages
  - Accessibility
summary: "\nDo you have a cool idea for a website that you want to share with everyone? Excellent! People with disabilities tend to feel left out of websites, so try following these tips to share your website with them, too.\n"
uri: 'concepts/accessibility/writing for an accessible web'

---
# Writing for an Accessible Web

## Summary

Do you have a cool idea for a website that you want to share with everyone? Excellent! People with disabilities tend to feel left out of websites, so try following these tips to share your website with them, too.

With several browsers available and a continuing history of incompatibility between them, many website designers have been satisfied to produce robust websites that work in a certain selection of those browsers. Sometimes, website designers will choose a single browser and design the site to work with that one; sometimes, the designer will choose a selection of browsers (usually what the designer already has installed). With the amount of effort trying to design a website to work well in the browser or browsers the designer has selected, it feels like making the site accessible to people with disabilities is the straw that broke the camel's back.

Fortunately, making a website accessible to people with disabilities doesn't have to be difficult. Some basic principles apply and many of these principles make a site accessible and usable for people without disabilities, too.

## Who is my audience?

There is a whole spectrum of people who may visit your website, regardless of what brought them there. This includes a wide range of "typical" people, people who have not been diagnosed with a disability, as well as people with [audio](/concepts/accessibility/definitions/audio_impairment), [cognitive](/concepts/accessibility/definitions/cognitive_impairment), [mobility](/concepts/accessibility/definitions/mobility_impairment), and [visual](/concepts/accessibility/definitions/visual_impairment) impairments. Many of the affordances made for people with disabilities actually underline sound web design and make a site easier to use for people without disabilities.

## How do I reach my audience?

One of the first things to remember when designing a website that is intended to be accessible is that your site should not rely on JavaScript to operate. Since JavaScript is a core technology for AJAX (it's the J in AJAX), your site should not rely on AJAX, either. Does this mean your site cannot use JavaScript or AJAX? No! It means that your site should be just as usable without JavaScript and AJAX as it is with those technologies. It may not be as flashy, but people should be able to perform the same tasks with JavaScript turned off as they could with everything enabled and working.

Because the Web is predominantly a visual medium, [visual impairments](/concepts/accessibility/definitions/visual_impairment) seem to require more accommodations than any other type of impairment. While [cognitive impairments](/concepts/accessibility/definitions/cognitive_impairment) and the accommodations afforded them may also seem daunting, many of these accommodations are actually part of good usability design.

## Remember

Disabilities are not mutually exclusive. Someone with a cognitive impairment may also have audio, mobility, and visual impairments.

## What do I need to do?

Here are some guidelines (yes, there are a lot of them) to follow when building websites.

### JavaScript & Plugins

-   Provide a `noscript` version of your website.
    -   This version should be as functional as the JavaScript-enabled version of your website. You will lose visitors (and not just people with disabilities) if your `noscript` version is entirely non-functional (*i.e.*, "You must enable JavaScript to view this page.").
    -   Screen readers can have trouble processing changes to the content of a page and some browsers do not support JavaScript.
    -   Changing content can also be perceived as "noise" and interfere with a person's ability to understand the content of your website.
-   If a hyperlink fires a JavaScript function (*e.g.*, `href="javascript:doSomething()"`), use the text of the hyperlink or the `alt` tag of the image in the hyperlink to describe what the function does.
    -   A screen reader can understandably have difficulty trying to read the name of a JavaScript function. Just as the text of a hyperlink would ease the understanding of a typical browser, so the text of the hyperlink or `alt` text of the image ease the understanding of someone using a screen reader.
-   Avoid making functionality dependent on events other than onLoad, onUnload, and onClick.
    -   Besides inconsistent implementation of certain events (*e.g.*, onChange), screen readers may never fire certain events. Events such as onMouseOver and onMouseOut may not be fired by someone who uses a screen reader or touch screen.
    -   If you decide to attach handlers to other events, make sure that the functionality is available through accessible means (*e.g.*, hyperlinks).
-   Link to accessible sites for any plugins that are required to render your website properly.
    -   If you have anything other than plain text or simple web pages on your site, chances are that plugins are required to render your website properly. Don't make the browser search for an accessible site where the plugins are available; find the sites and provide the links yourself.

### Images

-   Provide text alternatives for any content images (*e.g.*, the `alt` attribute of the `img` tag) that are not simply placeholders. Set the `alt` attribute to an empty string for a placeholder image.
    -   Screen readers will use the `alt` text in an attempt to describe the import of your images.
-   When providing a text alternative for an image with text in it, make sure the image text is reflected exactly in the text alternative, particularly if the image is used as a button or link. **Example**: A green button with the text "Start" could use "Green Start button" as its `alt` text.
    -   Screen readers cannot read the text in the image itself. If written or spoken instructions refer to the text of the image, the person using a screen reader should be able to identify that image through the `alt` text.
-   Whenever possible, use client-side image maps.
    -   A server-side image map hides the destination from the user and prevents a screen reader from seeing what areas of the image are active and where each area would direct the user.
-   Provide textual alternatives to all image maps, particularly server-side image maps.
    -   Navigation should not rely on the ability to click on certain points in an image map. If necessary due to the number of links, you can provide this alternative on another page so long as it is clear how to get to that page.
    -   Every area in an image map should have `alt` text to assist someone using a screen reader.
-   Avoid flickering images.
    -   People who suffer from epileptic seizures can be sensitive to flickering lights. If your website presents a flickering image, it may cause a seizure for someone prone to have them.

### Navigation

-   Provide text to explain the function of any frames in your website.
    -   Screen readers will use the `alt` text for a `frame` tag to describe the function of that frame.
-   If you have navigation links, provide a link to skip to the main content of your website.
    -   Someone using a screen reader and already familiar with the navigation of your website can use this link to skip to the content without having to listen to the list of navigation links again.
-   *See the guidelines under "Images" regarding image maps.*

### Tables

-   Provide a summary and caption for any tables on your website.
    -   This will help someone using a screen reader get a quick grasp of the layout and content of your tables, much like a person without a visual disability will scan over a table to determine its layout and import before delving into the details of the content.
-   Define row and column headers.
    -   Use the `scope` attribute for `th` elements to indicate when the header applies to a column, row, column group, or row group. This helps a screen reader associate the header with the appropriate data cells.
    -   Use the `id` attribute for `th` elements and `headers` attribute for `td` elements to associated data cells with the appropriate header cells. This also helps a screen reader associate the appropriate headers with their associated data cells.

### Forms

-   Break forms into semantically related input groups using the `fieldset` tag.
    -   Provide a caption for the `fieldset` that will make the form easier to understand. Some screen readers will read the `fieldset` caption with each form element contained therein. Used properly, fieldsets also break form elements into semantically related groups, aiding people with or without cognitive and visual disabilities.
-   Active form elements must be explicitly labeled.
    -   Someone using a screen reader may not understand what to provide in a form element without having a label to describe it.
    -   Labels provide another landing point for the cursor, making it easier for someone to select the form element. This helps everyone, not just people with mobility or visual impairments.
    -   Use explicit labels for form elements. Some screen readers are unable to handle implicit labels properly. Explicit labels include the associated form element's `id` attribute as the label's `for` attribute and wrap only the text identifying the form element, not the form element itself. Implicit labels do not necessarily include the `for` attribute, but wrap the form element itself.
-   If describing the purpose of an element might take too much space for a label, use the `title` attribute for that description.
    -   Screen readers may not support or otherwise have difficulty if the value of the element is originally used to describe its purpose. The `title` text will appear as a tooltip for most browsers.

### Media

-   Provide captioning for multimedia elements (*e.g.*, videos with audio) and transcripts for audio media (*e.g.*, podcasts).
    -   A multimedia presentation should include captioning, allowing someone with an audio impairment (or muted sound) to understand the video without hearing the audio.
    -   A transcript is sufficient for audio-only presentations.

### Colors & Styles

-   Color may be used to convey information, but do not rely on color alone.
    -   Color cannot translate well to some people with a visual impairment, like color blindness. Make sure that whatever information the color conveys (*e.g.*, valid or invalid) is also conveyed in another way (boldface, italics, descriptive context).
-   Stylesheets may be used to organize information, but do not rely on stylesheets alone.
    -   Someone with a visual impairment may need to override the stylesheets of websites they visit with a personal stylesheet (*e.g.*, high-contrast) in order to read the content. Make sure your website is understandable when any stylesheets are disabled.

### General

-   If it is otherwise impossible or terribly intrusive to provide textual alternatives inline with non-textual elements, provide a text-only version of your website.
    -   It can be difficult to make a site "cool" and accessible at the same time, to be all things to all people at all times. If you decide to provide a text-only version, make sure that it is always current with the version that has dynamic or non-textual elements.
-   If your website is time-sensitive, *e.g.*, it logs the user out after a certain period of inactivity, give the user an opportunity to request more time.
    -   While you might think 15 minutes is plenty of time for someone to fill out a form, people for whom your site is in a non-native language or people with disabilities may need more time to complete it. This helps people who do not have disabilities, too. Make sure that someone can request more time without losing the work already completed.

## Section 508 and Beyond

If you follow the guidelines above, you will go a long ways in making your site accessible and compliant with Section 508 Standards for Electronic and Information Technology. The following guidelines are inteneded to make your site accessible by people with cognitive impairments, but can make your website easier to use by anybody.

### Use of Language

-   Use simple sentence structures.
    -   It doesn't take a cognitive impairment to have difficulty with complex sentences or complex structures.
-   Use simple language where possible.
    -   Informal writing guidelines suggest that non-technical writing should be readable at the fifth-grade level. Where possible or expedient, avoid using language a grade-school child would have trouble understanding.
-   Define abbreviations, acronyms and jargon.
    -   Make sure that you define abbreviations, acronyms and jargon in plain text (not exclusively a tooltip or `title` text) with the first use.
    -   HTML 4.0 added the `abbr` and `acronym` tags. Whenever you use an abbreviation, acronym or jargon, wrap the term in an `abbr` or `acronym` tag, whichever is appropriate, and include the definition as the `title` attribute. When the user hovers a mouse over the term, the definition will appear as a tooltip. (Some browsers will display the term specially because of the tag; you can set up a style definition to accomplish the same thing.) When a screen reader encounters the item, the definition will be read with it.
-   Keep paragraphs short.
    -   Long blocks of text will make even accomplished readers want to stop reading. If you keep your paragraphs short, even people interested in a bit of light reading will get more out of your content.
-   Summarize your paragraphs.
    -   Include a summary of the paragraph as either the first or last sentence. Use the rest of the paragraph to back up the statement of the summary.
-   Write clearly and unambiguously.
    -   Unless you intend for your writing to have dual meaning, be unambiguous. The only exception to this rule is when unambiguous writing would result in a lengthy explanation that reduces the clarity of an otherwise simple sentence.
    -   Some people with cognitive impairments have trouble with fuzzy logic. Some sites offer security questions for which the user provides identifying answers. Make sure some absolute, time-independent, unambiguous questions are available for items like this.
        -   "Where did you go to high school?" can be ambiguous: the user may have attended multiple high schools. "Which high school did you graduate from?" is not as ambiguous. "What school did you go to for sixth grade?" will have a larger audience.
        -   "What is your grandmother's maiden name?" can be ambiguous: most people have two grandmothers. "What is your maternal grandmother's maiden name?" is not as ambiguous.

### Memory and Decision Making

-   Use whitespace.
    -   Maybe your paragraphs are short, but if they are all jumbled together, they still look foreboding.
    -   Whitespace also allows people to group things together and break apart a page into manageable pieces.
-   Don't make me think.
    -   If your website isn't intended to be a problem-solving game, don't make it one. Keep your navigation clear and simple. It doesn't take someone with a cognitive impairment to give up on a site because they can't make it work. (It sometimes takes a cognitive impairment like autism to stay on a challenging page long enough to figure out how to make it work.)
-   Break tasks down into incremental pieces.
    -   Write your instructions to be detailed, yet skimmable. Write high-level instructions for experts. Break them down incrementally until a novice can follow your instructions.
-   Jog your user's memory.
    -   If the user gave you information, give it back to the user when it is needed.
    -   If the user needs to look something up for future use, provide space to store it so it can be presented when needed.
-   Track your user's progress.
    -   If the user is going through a lengthy process on your website, let the user know what has been done and what is left.
    -   Provide affordances for the user so information isn't lost. If possible, automatically save information along the way. Let the user know that information entered will not be lost if something happens.
-   Keep the selection of choices small and provide defaults where possible.
    -   Some people, whether due to a cognitive impairment or simple fatigue, are unable to concentrate enough to make a rational decision. If possible, provide default behavior and selections that will neither hinder nor frustrate the user.
    -   Some people, whether due to a cognitive impairment or simple fatigue, are unable to decide between more than a certain number of choices.
    -   Try to guide the user through the selection process and make sure all the possible choices and choice combinations are valid and any invalid choices or choice combinations are unavailable.
    -   If possible, break complex decisions into simpler decisions.

### Usability

-   Use form elements as intended.
    -   Users become confused when familiar actions have unexpected results.
    -   Drop-down boxes should be used to make a single choice on a form. They were not intended for navigation.
    -   Radio buttons were intended to make a choice from mutually exclusive options. They were not intended for navigation.
    -   Radio buttons perform a function similar to drop-down boxes, but take up more space. Use radio buttons when the space makes them easier to use and understand; use drop-down boxes when radio buttons would take up too much space.
    -   Check boxes were intended to make choices from potential combinations. They were not intended to be used when radio buttons are more appropriate.
    -   Buttons were intended to perform actions against forms (*e.g.*, submit, set defaults, reset). They were not intended for browsing or choice selections.
-   Make matches and searches case-insensitive when possible and appropriate.
    -   Children, elders, people with cognitive impairments, and people with mobility impairments can have trouble with capitalization. Passwords would be one of a very few exceptions.

## See also

### External resources

[http://www.access-board.gov/sec508/guide/](http://www.access-board.gov/sec508/guide/)

