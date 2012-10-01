{{Page_Title}}
{{Flags}}
{{Byline}}
{{Summary_Section|In this tutorial we will take you through how to create different types of basic navigation menu using HTML lists and links.}}
{{Tutorial
|Content=== Introduction ==

HTML5 includes many new features to make web forms a lot easier to write, and a lot more powerful and consistent across the Web. This article gives a brief overview of some of the new form controls and functionalities that have been introduced.

== Why did we need new form features? ==
 
Let's face it – HTML forms have always been a pain. They are not much fun to mark up and they can be fiddly to style – especially if you want them to be consistent cross-browser and fit in with the overall look and feel of your site. And they can be frustrating for your end users to fill out, even if you create them with care and consideration to make them as usable and accessible as possible. Creating a good form is more about damage limitation than pleasurable user experiences.
 
Back when HTML 4.01 became a stable recommendation, the web was a mostly static place. Yes, there was the odd comment form or guest book script, but generally web sites were there for visitors to simply read. Since then, the web has evolved. For many people, the browser has already become a window into a world of complex, web-based applications that try to bring an almost desktop-like experience.
 
[[Image:html5formfig1.png|Some complicated non-native form controls, faked with JavaScript]]
 
Figure 1: Some complicated non-native form controls, faked with JavaScript.
 
To fill the need for the more sophisticated controls required for such applications, developers have been taking advantage of JavaScript libraries and frameworks (such as jQueryUI or YUI). These solutions have certainly matured over the years, but essentially they're a workaround to compensate for the limited form controls available in HTML. They “fake” the more complex widgets (such as date pickers and sliders) by layering additional (not always semantic) markup and a slew of JavaScript on top of pages.
 
HTML5 aims to standardise some of the most common rich form controls, making them render natively in the browser and obviating the need for these script-heavy workarounds.

== Introducing our example ==
 
To illustrate some of the new features, this article comes with a [[http://devfiles.myopera.com/articles/4582/html5-forms-example.html basic HTML5 forms example]]. It's not meant to represent a "real" form (as you'd be hard-pressed to find a situation where you need all the new features in a single form), but it should give you an idea of how the various new aspects look and behave.
 
Note: the look and feel of the new form controls and validation messages differs from brower to browser, so styling your forms to look reasonably consistent across browsers will still need careful consideration.

== New form controls ==
 
As forms are the main tool for data input in Web applications, and the data we want to collect has become more complex, it has been necessary to create an input element with more capabilities, to collect this data with more semantics and better definition, and allow for easier, more effective error management and validation.
 
=== &lt;input type="number"&gt; ===
 
The first new input type we'll discuss is <code>type="number"</code>:
 
<pre>&lt;input type="number" … &gt;</pre>
 
This creates a special kind of input field for number entry – in most supporting browsers this appears as a text entry field with a spinner control, which allows you to increment and decrement its value.
 
[[Image:html5formfig2.png|A number input type]]
 
Figure 2: A <code>number</code> input type.

=== &lt;input type="range"&gt; ===
 
Creating a slider control to allow you to choose between a range of values used to be a complicated, semantically dubious proposition, but with HTML5 it is easy — you just use the <code>range</code> input type:
 
<pre>&lt;input type="range" … &gt;</pre>
 
[[Image:html5formfig3.png|A range input type]]
 
Figure 3: A <code>range</code> input type.
 
Note that, by default, this input does not generally show the currently selected value, or even the range of values it covers. Authors will need to provide these through other means – for instance, to display the current value, we could use an <code>&lt;output&gt;</code> element together with some JavaScript to update its display whenever the user has interacted with the form:
 
<pre>&lt;output onforminput="value=weight.value"&gt;&lt;/output&gt;</pre>

=== &lt;input type="date"&gt; and other date/time controls ===
 
HTML5 has a number of different input types for creating complicated date/time pickers, for example the kind of date picker you see featured on pretty much every flight/train booking site out there. These used to be created using unsemantic kludges, so it is great that we now have standardized easy ways to do this. For example:
 
<pre>&lt;input type="date" … &gt;
&lt;input type="time" … &gt;</pre>
 
Respectively, these create a fully functioning date picker, and a text input containing a separator for hours, minutes and seconds (depending on the <code>step</code> attribute specified) that only allows you to input a time value.
 
[[Image:html5formfig4.png|date and time input types]]
 
Figure 4: <code>date</code> and <code>time</code> input types.
 
But it doesn't end here — there are a number of other related input types available:
 
* <code>datetime</code>: combines the functionality of two we have looked at above, allowing you to choose a date and a time.
* <code>month</code>: allows you to choose a month, stored internally as a number between 1-12, although different browsers may provide you with more elaborate choosing mechanisms, like a scrolling list of the month names.
* <code>week</code>: allows you to choose a week, stored internally in the format 2010-W37 (week 37 of the year 2010), and chosen using a similar datepicker to the ones we have seen already.

=== &lt;input type="color"&gt; ===
 
This input type brings up a color picker. Opera's implementation allows the user to pick from a selection of colors, enter hexadecimal values directly in a text field, or to invoke the OS's native color picker.

[[Image:html5formfig5.png|a color input, and the native color pickers on Windows and OS X]]

Figure 5: a <code>color</code> input, and the native color pickers on Windows and OS X.

=== <input type="search"> ===
 
The <code>search</code> input type is arguably nothing more than a differently-styled text input. Browsers are meant to style these inputs the same way as any OS-specific search functionality. Beyond this purely aesthetic consideration, though, it's still important to note that marking up search fields explicitly opens up the possibility for browsers, assistive technologies or automated crawlers to do something clever with these inputs in the future – for instance, a browser could conceivably offer the user a choice to automatically create a custom search for a specific site.
 
[[Image:html5formfig6.png|A search input as it appears in Opera on OS X]]
 
Figure 6: A <code>search</code> input as it appears in Opera on OS X.
}}
{{Compatibility_Section
|Not_required=Yes
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_sections==== Exercise Questions ===
 
* Why is it a good idea to mark up menus as lists?
* When you design a navigation menu, what do you need to plan for in the future?
* What are the benefits of using <code>&lt;select&gt;</code> elements for menus, and what are the problems?
* What do you define with <code>&lt;area&gt;</code> elements, and what is the <code>nohref</code> attribute of an area element for (this is not in here, you'd need to do some online research)
* What are the benefits of skip links?
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}