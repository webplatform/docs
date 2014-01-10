{{Page_Title}}
{{Flags
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|Registers a new, custom element and returns the element's constructor.}}
{{API_Object_Method
|Parameters={{Method Parameter
|Name=type
|Data type=String
|Description=The custom element's tag name. The name must contain a dash (-). So for example, <x-foo>, <foo-element>, and <my-foo-element> are valid names, while <tabs> and <foo_bar> are not.
|Optional=No
}}{{Method Parameter
|Name=options
|Data type=Object
|Description=The object describing the element's prototype, public properties and methods.
|Optional=Yes
}}
|Method_applies_to=dom/Document
|Example_object_name=document
|Return_value_name=XFoo
|Javascript_data_type=Object
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=JavaScript
|Description=Register's the custom element and adds it to the DOM.
|Code=var XFoo = document.register('x-foo');
document.body.appendChild(new XFoo());
}}{{Single Example
|Language=JavaScript
|Description=Registers the custom element and defines the element's prototype.
|Code=var XFoo = document.register('x-foo', {
  prototype: Object.create(HTMLElement.prototype, {
    bar: {
      get: function() { return 5; }
    },
    foo: {
      value: function() {
        alert('foo() called');
      }
    }
  })
});
}}
}}
{{Notes_Section
|Notes=The custom element name must not be one of the following existing hyphen-containing element names:
* annotation-xml
* color-profile
* font-face
* font-face-src
* font-face-uri
* font-face-format
* font-face-name
* missing-glyph
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=Custom Elements
|URL=https://dvcs.w3.org/hg/webcomponents/raw-file/tip/spec/custom/index.html
}}
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Web Components
|External_links=* [http://www.html5rocks.com/en/tutorials/webcomponents/customelements/ Custom Elements] on [http://www.html5rocks.com HTML5Rocks!]
}}
{{Topics|API, DOM}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=HTML5Rocks
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=http://www.html5rocks.com/en/tutorials/webcomponents/customelements/
}}