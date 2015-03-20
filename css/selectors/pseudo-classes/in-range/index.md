{{Page_Title|&#58;in-range}}
{{Flags
|State=Not Ready
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The <code>:in-range</code> pseudo selector selects input elements when their value is within a specified range.}}
{{CSS_Selector
|Content=The <code>:in-range</code> CSS pseudo-class matches when an element has its value attribute inside the specified range limitations for this element. It allows the page to give a feedback that the value currently defined using the element is inside the range limits.
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=CSS
|Code=<code>
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
</code>
|LiveURL=http://code.webplatform.org/gist/73a791bbe2cd884f6b2e
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Topic_clusters=Pseudo-Classes, Selectors
}}
{{Topics|CSS}}
{{External_Attribution
|Is_CC-BY-SA=No
}}
{{Compatibility
|feature=pseudo-in-range
|topic=css
}}