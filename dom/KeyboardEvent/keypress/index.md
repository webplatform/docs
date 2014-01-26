{{Page_Title}}
{{Flags
|High-level issues=Missing Relevant Sections
|Content=Incomplete, Compatibility Incomplete
|Checked_Out=No
}}
{{Standardization_Status|Deprecated}}
{{API_Name}}
{{Summary_Section}}
{{Event
|Event_applies_to=dom/KeyboardEvent
|Synchronous=Yes
|Bubbles=Yes
|Target=dom/Element, dom/Document
|Cancelable=Yes
|Default_action=Varies: launch text composition system; blur and focus events; DOMActivate event; other event
|Content=This event used to be used to detect when a key value was inserted into the DOM. Developers should use beforeInput, keyup, or keydown events depending on the task instead of this event.
|Default Action=Varies: launch text composition system; blur and focus events; DOMActivate event; other event
|Interface=dom/KeyboardEvent
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Code=&lt;!doctype html&gt;
&lt;html&gt;
&lt;head&gt;
    &lt;meta charset=&quot;utf-8&quot;&gt;
    &lt;title&gt;Keypress event demonstration&lt;/title&gt;
    &lt;style&gt;
        // this styling only exists so things look better on code.webplatform.org
        form {
            padding-top: 30px;
        }
    &lt;/style&gt;
&lt;/head&gt;
&lt;body&gt;
    &lt;form&gt;
        &lt;label for=&quot;keypress&quot;&gt;Keypress&lt;/label&gt;
        &lt;input name=&quot;keypress&quot;/&gt;
    &lt;/form&gt;
    &lt;div id=&quot;target&quot;&gt;
        &lt;p&gt;The last key code you entered for keypress is: &lt;span id=&quot;keypressEcho&quot;&gt;&lt;/span&gt;&lt;/p&gt;
    &lt;/div&gt;

    &lt;script&gt;
    // Getting the target elements from the DOM that we would like to mess with.
    var keypressInput = document.getElementsByName('keypress')[0];
    var keypressTarget = document.getElementById('keypressEcho');

    // This is going to run the function whenever a keypress event occurs on the Input element.
    keypressInput.addEventListener('keypress', function(e) {
        //Change the text of the target element to be the number of the key pressed. (number is based on the ASCII key standard.)
        keypressTarget.textContent = e.which;
        // Log the key event as well.
        console.log(e.which);
    });
    &lt;/script&gt;
&lt;/body&gt;
&lt;/html&gt;
|LiveURL=http://code.webplatform.org/gist/8631904
}}
}}
{{Notes_Section
|Usage====Related event order===
# keydown
# beforeInput
# keypress
# input
# keyup
}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Manual_links=*<code>[[dom/KeyboardEvent/keydown|onkeydown]]</code>
*<code>[[dom/KeyboardEvent/keyup|onkeyup]]</code>
|External_links=*[http://www.w3.org/TR/DOM-Level-3-Events/#event-type-keypress DOM Level 3 Events]
}}
{{Topics|DOM, DOMEvents}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}