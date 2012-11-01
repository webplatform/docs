{{Page_Title}}
{{Flags
|High-level issues=Stub
|Content=Incomplete
}}
{{Summary_Section|The Extensible Markup Language (XML) is a subset of SGML Its goal is to enable generic SGML to be served, received, and processed on the Web in the way that is now possible with HTML. XML has been designed for ease of implementation and for interoperability with both SGML and HTML.}}
{{Basic Page}}
== Introduction ==
Extensible Markup Language, abbreviated XML, describes a class of data objects called XML documents and partially describes the behavior of computer programs which process them. The World Wide Web Consortium maintains the XML standard. 

== XML specifications ==
The first draft of XML was released in November 1996, the current specification (1.0 fifth edition)
is consultable at this address:
http://www.w3.org/TR/2008/REC-xml-20081126/


== The goals of XML ==
The goals of XML, as specified by W3C, are:
<ol>
  <li>XML shall be straightforwardly usable over the Internet</li>
  <li>XML shall support a wide variety of applications</li>
  <li>XML shall be compatible with SGML</li>
  <li>It shall be easy to write programs which process XML documents</li>
  <li>The number of optional features in XML is to be kept to the absolute
minimum, ideally zero</li>
  <li>XML documents should be human-legible and reasonably clear</li>
  <li>The XML design should be prepared quickly</li>
  <li>The XML design should be formal and concise</li>
  <li>XML documents shall be easy to create</li>
  <li>Terseness in XML markup is of minimal importance</li>
</ol>

== Markup, Extensibility ==
Markup is all that has a special meaning, that must be well characterised:
bold text, underlined text are examples of markup.
An XML document is composed of markups and text: markups represent the logical structure of the document, text is the content of the document, the data.
In XML all that is included between angled brackets (“&lt;” and “&gt;”), is considered markup, and is called tag, for example:
&lt;name&gt; is a tag.
XML is a metalanguage: Unlike HTML, which is a predefined language, it does not have predefined tags but allows the definition of new tags and new languages (there is an HTML version in XML). 
It is extensible.
HTML is also a markup language, it was initially defined in SGML. The set of HTML rules are contained in a document (generally included in the browser) called DTD HTML (Document Type Definition).
While the predefined tags of HTML are used to specify the visual aspects of the document, in XML they are used to structure the document, to define the content and to describe the data.


== The components of XML ==
One of the most common problems today is the exchange of documents: each program stores its data in one or more proprietary formats difficult to exchange with other programs.
XML has been studied to allow and facilitate data exchange between different kinds of applications, for example databases and word processors. The interest aroused by the new language is such that many software producers now intend to adopt the XML format or are already using it in theirs programmes.
For a document to be easy to interpret there must be three distinct parts:
<ul>
 <li>the content;</li>
 <li>the specification of the elements, the structure (DTD or Schema);</li>
 <li>the specification of the visual aspects, the style (Stylesheet).</li>
/ul>

Why is it so important to maintain these three components distinct ?
If we have to look for information in a book, we consult the index, when this is available, otherwise we check the chapters to see whether the information contained is inherent, we then scan the paragraphs, finally we look at the
content.
A particular indication such as an indentation or the use of a different character
helps us to understand where a chapter or a paragraph begins: the style
should help us, to understand when reading the relation of the structure with
the content.
Without this distinction, an author concentrating on the visual properties risks
loosing sight of the content of his/her document.
With this distinction effort can be shared: the author, who has no need to
know informatics elements, can concentrate on the content of his document
entrusting the visual aspect to the graphic. In addition, it is more simple to
write applications that must elaborate data. Once the content is separated
from the style, it is easier to integrate data from different sources and different
stylesheet can be applied if needed.
If the language is modified and we want others know this or we want to use it
as an exchange format, we need an open solution not a proprietary one. This
means that the meaning of the extensions made must be declared, with a
public DTD.



== An example of an XML document ==
According to the design goals of XML, it should be human legible. It must be
readable by any text reader, such as Unix vi or Windows Notepad. It should
not be in binary format (even if P. Hoschka, W3C member, during the
inauguration of the W3C office in Italy talked about the possibility of a binary
XML), and should be reasonably clear. The following example, library.xml,
shows how an XML document can be written:
Figure 2 - library.xml
<pre>
&lt;?xml version=”1.0” encoding=”UTF-8”?&gt;
&lt;library&gt;
  &lt;book code=”R414”&gt;
    &lt;title&gt;2001: A Space Odissey&lt;/title&gt;
    &lt;author&gt;
      &lt;first_name&gt;Arthur Charles&lt;/first_name&gt;
      &lt;last_name&gt;Clarke&lt;/last_name&gt;
    &lt;/author&gt;
    &lt;publisher&gt;Polaris Production&lt;/publisher&gt;
    &lt;keyword&gt;romance&lt;/keyword &gt;
    &lt;keyword&gt;science-fiction&lt;/keyword &gt;
  &lt;/book&gt;
&lt;/library&gt;
</pre>



The document begins with a prologue that contains a declaration of conformity
to version 1.0 of the XML standard and to the UTF-8 encoding standard:
&lt;?xml version=”1.0” encoding=”UTF-8”?&gt;

Elements are used to declare the associated content and are written in the form:
<pre>&lt;element_type_name attribute_name=”attribute_value”&gt;element content&lt;/element_type_name&gt;</pre>

The content of an element can be of the following types: character data, parsed character data (character data that can be evaluated by parsers, programs capable of reading and interpreting XML documents), processing instructions (information to give to programs) or other nested elements.
An element can have attributes, used to better specify the content.
Each open tag must have a corresponding final tag; when the element is empty, like the case of BR in HTML, instead of &lt;BR&gt;&lt;/BR&gt; the use of the concise form &lt;BR/&gt; is permissible.
XML is case sensitive, so a &lt;name&gt; tag is different from &lt;Name&gt; and from
&lt;NAME&gt;.
Some characters and sequences of characters are reserved and cannot be used
in the names of the tags (%, xml, ...).
XML supports Unicode (Unicode WorldWide Character Standard), a standard
code system that supports characters of the diverse languages of the world,
both modern and also historical languages. With Unicode, browsers should
automatically render the right character even if a document contains words
written in several code sets.

== DTD - Document Type Definition ==
The DTD contains the definition rules of tags; it denotes the elements and their
order inside the XML document. Unlike SGML, its use is not compulsory, but is
suggested in order to verify the validity and congruence of the document.
Other than defining the elements, it defines the syntax and the relations
among elements.
The structure of an XML document is seen as a tree in which elements
represent the nodes. The following figure (Fig. 3), represents the structure of a
hypothetical library:
library

Figure 1 – the three components of a document
<em>(insert picture)</em>


The unique element that contains all the others is called the root element.
The DTD can be internal or external to the XML document. By convention its
name corresponds to that of the root element (in our example "library").
The following figure (Figure 4) shows an XML DTD, library.dtd, representing
the previous defined structure:

Figure 2 - library.dtd
<pre>
&lt;!DOCTYPE library [
&lt;!ELEMENT library (book+)&gt;
&lt;!ELEMENT book (title, author+, publisher, keyword+)&gt;
&lt;!ATTLIST book
code ID #REQUIRED&gt;
&lt;!ELEMENT title (#PCDATA)&gt;
&lt;!ELEMENT author (first_name, last_name)&gt;
&lt;!ELEMENT publisher (#PCDATA)&gt;
&lt;!ELEMENT keyword (#PCDATA)&gt;
&lt;!ELEMENT last_name (#PCDATA)&gt;
&lt;!ELEMENT first_name (#PCDATA)&gt;
]&gt;
</pre>


A DTD can be internal or external to the XML document; generally it is written
in one or more separate documents.
If internal to the XML document, the DTD starts with a DOCTYPE declaration:
&lt;!DOCTYPE root_element [element, attribute, entity, notation]&gt;
otherwise this declaration must be made inside the XML document; the
library.xml file would be written:
<pre>
&lt;?xml version=”1.0”?&gt;
&lt;!DOCTYPE library SYSTEM "library.dtd"&gt;
&lt;library&gt;
...
&lt;/library&gt;
</pre>
After the DOCTYPE declaration we have to declare elements:
<pre>&lt;!ELEMENT element_name (permitted_elements_names)&gt;</pre>

Examining the declaration of the "book" element, we can note that is
composed by the elements "title", "author", "publisher" and "keyword".
These elements are separated by a comma and thus must be present in that
exact order in the library.xml file.
Let us examine the following declaration:
<pre>&lt;!ELEMENT person (first_name|last_name)&gt;
&lt;!ELEMENT person (first_name|last_name|email)*&gt;
</pre>

<pre>
In the first case the "|" character means that the "person" element will be
constituted by the "first_name" or by the "last_name" element; in the second case, in which a "*" character is present, by 0, 1 or more "first_name", "last_name", "email" elements in any order.
We can see that the author element is followed by the "+" character: this
means that there must be one or more “author” elements.
If an element, or a group of elements listed between parentheses, is followed
by the "?" character it can be present none or one times.
&lt;!ELEMENT title (#PCDATA)&gt; means that the title element can be composed
by any character except for markup strings or special characters like ", & or ]
(PCDATA = Parsed Character Data).
Attributes are used generally as specifications of elements, to add information
to elements. In this case, we can consider attributes as metadata, i.e.
information about information. But attributes are also used to have a control
on values; we can oblige data to be a value of a predefined list, like the
enumerated type in the C language.
Attributes are declared in the form:
&lt;!ATTRIBUTE element_name
attribute_name attribute_type default_value&gt;
In our example, each book element will have a univocal code (ID).
Attribute types can be CDATA (character data), ID, or a list of values
(enumerated type) and are declared in this way:
&lt;!ATTLIST element_name
attribute_name attribute_type default_value&gt;
The attribute value is compulsory when the option #REQUIRED is specified (in
our example the code of the book element is compulsory), it can have no
specified code if the option is #IMPLIED, or only the specified value is valid
with the option #FIXED.
In addition to elements and attributes, the DTD can contain entities and
notations.
An XML document can be composed by elements referencing other objects;
these objects are called entities. The following example shows a document
internal entity:
&lt;!ENTITY XML "eXtensible Markup Language"&gt;
In this case, during visualisation, each &XML occurrence will be replaced by
the string “eXtensible Markup Language “.
Entities can be used to represent reserved characters like, for example, “&lt;” or
“&gt;” (&lt;, &gt), but can also be used to reference external objects, such as
other XML documents or images, when the document does not consist of a
unique file. The following example defines an external entity:
&lt;!ENTITY introduction SYSTEM "introduction.txt"&gt;
A document can also contain parametrical entities:
&lt;!ENTITY % [name] "[a_list_of_names]"&gt;
for example:
8
&lt;!ENTITY % headings "H1 | H2 | H3 | H4"&gt;
&lt;!ENTITY BODY (%headings | P | DIV | BR)*&gt;
The notation declaration is useful to identify specific types of external binary
data, like for example files in “gif” format
&lt;!NOTATION GIF87A SYSTEM “GIF”&gt;
In case we need to preserve the space contained in an element, for example in
a poem, we use the xml:space attribute set to “preserve”
&lt;!ELEMENT poem (#PCDATA)&gt;
&lt;!ATTLIST poem
xml:space (default| preserve) “preserve”&gt;
Processing instructions used to pass information to the applications are written
in the form ”&lt;?name PIdata?&gt;” where name, called the Pitarget, is used to
identify the process instruction to the programs.
The DTD is required when we have to define default attribute values, when we
need to handle white spaces and when other programs need to read it to
understand the structure of the document.
</pre>


In order for a document to be considered “well formed”:
<ul>
 <li>it must contain at least one element;</li>
 <li>there must be a unique open and close tag that contains the entire
document; this tag is called the root element;</li>
 <li>all the tags must be nested (unlike HTML &lt;B&gt;&lt;I&gt;text&lt;/B&gt;&lt;/I&gt; is not
allowed);</li>
 <li>all the entities must be declared.</ul>
</ul>
A document is said “valid” when it is associated with a DTD and respects the
rules defined in the DTD.



== Namespaces ==


== The schema ==
{{Notes_Section
|Notes=draft
to be styled
sections to be added
}}
{{Topics|XML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}