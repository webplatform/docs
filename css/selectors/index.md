{{Page_Title|:in-range}}
{{Flags
|State=Ready to Use
|Checked_Out=No
}}
{{Summary_Section|The :in-range pseudo selector selects input elements when their value is within a specified range.}}
{{Basic Page}}
The :in-range CSS pseudo-class matches when an element has its value attribute inside the specified range limitations for this element. It allows the page to give a feedback that the value currently defined using the element is inside the range limits.

This pseudo-class only applies to elements that have a range limitations, such as input elements with min and max attributes. In absence of such a limitation, the element can neither be 'in-range' nor 'out-of-range'.

Use the :out-of-range selector to select all elements with a value that is outside a specified range.

SYNTAX

:in-range {
    css declarations;
}

EXAMPLE

li {
    list-style: none;
    margin-bottom: 1em;
}
input {
    border: 1px solid black;
}
input:in-range {
    background-color: rgba(0, 255, 0, 0.25);
}
input:out-of-range {
    background-color: rgba(255, 0, 0, 0.25);
    border: 2px solid red;
}
input:in-range + label::after {
    content:' OK';
}
input:out-of-range + label::after {
    content:'out of range!';
}


Note: This pseudo-class is not currently supported in Internet Explorer.
{{Notes_Section}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
}}