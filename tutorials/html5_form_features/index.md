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

=== The &lt;datalist&gt; element and list attribute ===
 
Up until now we have been used to using <code>&lt;select&gt;</code> and <code>&lt;option&gt;</code> elements to create dropdown lists of options for our users to choose from. But what if we wanted to create a list that allowed users to choose from a list of suggested options, as well as being able to type in their own? That used to require fiddly scripting – but now you can simply use the <code>list</code> attribute to connect an ordinary input to a list of options, defined inside a <code>&lt;datalist&gt;</code> element.

<pre>&lt;input type=&quot;text&quot; list=&quot;mydata&quot; … &gt;
&lt;datalist id=&quot;mydata&quot;&gt;
    &lt;option label=&quot;Mr&quot; value=&quot;Mister&quot;&gt;
    &lt;option label=&quot;Mrs&quot; value=&quot;Mistress&quot;&gt;
    &lt;option label=&quot;Ms&quot; value=&quot;Miss&quot;&gt;
&lt;/datalist&gt;</pre>
 
[[Image:html5formfig7.png|Creating an input element with preset options using datalist]]
 
Figure 7: Creating an input element with suggestions using <code>datalist</code>.

=== &lt;input type="tel"&gt;, &lt;input type="email"&gt; and &lt;input type="url"&gt; ===
 
As their names imply, these new input types relate to telephone numbers, email addresses and URLs. Browsers will render these as normal text inputs, but explicitly stating what kind of text we're expecting in these fields plays an important role in client-side form validation. Additionally, on certain mobile devices the browser will switch from its regular text entry on-screen keyboard to the more context-relevant variants. Again, it's conceivable that in the future browsers will take further advantage of these explicitly marked-up inputs to offer additional functionality, such as autocompleting email addresses and telephone numbers based on the user's contacts list or address book.

== New attributes ==
 
In addition to explicit new input types, HTML5 defines a series of new attributes for form controls that help simplify some common tasks and further specify the expected values for certain entry fields.
 
=== placeholder ===
 
A common usability trick in web forms is to have placeholder content in text entry fields – for instance, to give more information about the expected type of information we want the user to enter – which disappears when the form control gets focus. While this used to require some JavaScript (clearing the contents of the form field on focus and resetting it to the default text if the user left the field without entering anything), we can now simply use the <code>placeholder</code> attribute:
 
<pre>&lt;input type=&quot;text&quot;… placeholder=&quot;John Doe&quot;&gt;</pre>
 
[[Image:html5formfig8.png|A text input with placeholder text]]
 
Figure 8: A text input with <code>placeholder</code> text.

=== autofocus ===
 
Another common feature that previously had to rely on scripting is having a form field automatically focused when a page is loaded. This can now be achieved with the <code>autofocus</code> attribute:
 
<pre>&lt;input type="text" autofocus … &gt;</pre>
 
Keep in mind that you shouldn't have more than one <code>autofocus</code> form control on a single page. You should also use this sort of functionality with caution, in situations where a form represents the main area of interest in a page. A search page is a good example – provided that there isn't a lot of content and explanatory text, it makes sense to set the focus automatically to the text input of the search form.
 
=== min and max ===
 
As their name suggests, this pair of attributes allows you to set a lower and upper bound for the values that can be entered into a numerical form field, for example number, range, time or date input types (yes, you can even use it to set upper and lower bounds for dates – for instance, on a travel booking form you could limit the datepicker to only allow the user to select future dates). For <code>range</code> inputs, <code>min</code> and <code>max</code> are actually necessary to define what values are returned when the form is submitted. The code is pretty simple and self-explanatory:
 
<pre>&lt;input type="number" … min="1" max="10"&gt;</pre>
 
=== step ===
 
The <code>step</code> attribute can be used with a numerical input value to dictate how granular the values you can input are. For example, you might want users to enter a particular time, but only in 30 minute increments. In this case, we can use the <code>step</code> attribute, keeping in mind that for <code>time</code> inputs the value of the attribute is in seconds:
 
<pre>&lt;input type=&quot;time&quot; … step=&quot;1800&quot;&gt;</pre>
 
== New output mechanisms ==
 
Beyond the new form controls that users can interact with, HTML5 defines a series of new elements specifically meant to display and visualise information to the user.
 
=== &lt;output&gt; ===
 
We already mentioned the <code>&lt;output&gt;</code> element when talking about the <code>range</code> input type – this element serves as a way to display the result of a calculation, or more generally to provide an explicitly identified output of a script (rather than simply pushing some text into in a random <code>span</code> or <code>div</code>). To make it even more explicit what particular form controls the <code>&lt;output&gt;</code> relates to, we can – in a similar way to <code>&lt;label&gt;</code> – pass a list of <code>ID</code>s in the element's optional <code>for</code> attribute.
 
<pre>&lt;input type=&quot;range&quot; id=&quot;rangeexample&quot; … &gt;
&lt;output onforminput=&quot;value=rangeexample.value&quot; for=&quot;rangeexample&quot;&gt;&lt;/output&gt;</pre>
 
=== &lt;progress&gt; and &lt;meter&gt; ===
 
These two new elements are very similar, both resulting in a gauge/bar being presented to the user. Their distinction is in their intended purpose. As the name suggests, <code>progress</code> is meant to represent a progress bar, to indicate the percentage of completion of a particular task, while meter is a more generic indicator of a scalar measurement or fractional value.
 
[[Image:html5formfig9.png|A progress indicator bar]]
 
Figure 9: A progress indicator bar.


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