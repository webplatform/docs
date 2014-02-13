= HTML의 기초 =
{{Languages}}

== 소개 ==
 
이 문서는 요소의 역할 및 문자 참조를 포함한 HTML의 목적이나 구조를 정리 한 것입니다. 개별 기능은 이후 기사에서 자세히 설명하고 있습니다.
 
== What is HTML ==
 
대부분의 소프트웨어는 전용 파일 형식을 읽고 씁니다. 예를 들어, Microsoft Word는 "doc"파일을 지원하며 Microsoft Excel은 "xls"에 해당합니다. 이러한 파일에는 문서 내용 외에 다음 열었을 때의 복구 절차를 쓰는 정보 "메타 데이터"라는 문서에 대한 정보가 포함되어 있습니다. 메타 데이터는 문서의 작성자 나 마지막 수정일 신구 버전을 왕래하는 변경 내용이 포함되어 있습니다.
 
[[html|HTML (“HyperText Markup Language”)]]는 Web 문서의 내용을 기술하는 언어입니다. HTML 구문에서는 "요소 (elements)"라는 구조를 사용합니다. 요소는 문서의 텍스트를 묶 사용자 에이전트에 그 부분이 어떤 행동을 취하면 좋은가를 전하는 것입니다.
 
기에서는 「Web 브라우저」라는 말을 대신해 "사용자 에이전트"라는 기술 용어를 사용하고 있습니다. 사용자 에이전트는 사용자를 대신하여 Web 페이지에 액세스하는 소프트웨어 전반을 가리키는 말입니다. 데스크톱 브라우저 (Internet Explorer, Opera, Firefox Safari 등) 및 기타 장치 용 브라우저 (Wii 인터넷 채널과 Opera Mini, iPhone WebKit으로 대표되는 모바일 브라우저)는 물론 사용자 에이전트입니다.

그러나 여기서 중요한 것은 브라우저 만 사용자 에이전트가 아니라는 것입니다. 예를 들어, Google이나 Yahoo!가 자사의 검색 엔진을 위해 사용하는 Web 자동 인덱스 프로그램도 사용자 에이전트가됩니다 (그러나이 경우 사람이 직접 프로그램을 작동하는 것은 아닙니다).

 
== HTML은 어떤 것? ==
 
HTML은 문서의 내용과 그 의미를 일반 텍스트로 나타내는 형식입니다. 예를 들어, 다음과 같은 것입니다.


<syntaxhighlight lang="html5"><p id="example">This is a paragraph.</p></syntaxhighlight>
 
The “<code>&lt;p&gt;</code>” part is a marker (which we refer to as a “tag”) that means
“what follows should be considered as a paragraph”.  Because it is at the start of the content it is affecting, this particular tag is an "opening tag". The
“<code>&lt;/p&gt;</code>” is a tag to indicate where the end of the paragraph is (which we refer to as a “closing tag”). "요소"는 시작 태그에서 시작 태그에서 종료 태그 사이에있는 내용과 종료 태그까지를 포함한 부분을 말합니다. 시작 태그에있는 id = "example" 는 속성이라고합니다. 이에 대해서는 나중에 설명합니다. 많은 사람들이 부분에 대한 설명에서 "태그"라는 말을 사용하고 있습니다 (앞서 언급했듯이, 이것은 엄밀하게는 올바르지 않습니다.)
 
대부분의 브라우저에는 "소스"또는 "소스보기"기능이 탑재되어 있으며, 대부분의 경우 "보기"메뉴에서 선택할 수 있습니다. 만약 당신이 사용하는 브라우저가 소스보기 기능을 제공하는 경우에 선택하여 페이지의 HTML 소스를 잠시 바라 봅시다.

== HTML 문서 구성 ==
 
일반적인 HTML 문서의 구성 예:
 
<syntaxhighlight lang="html5"><!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Example page</title>
  </head>
  <body>
    <h1>Hello world</h1>
  </body>
</html></syntaxhighlight>

위 코드는 웹 브라우저에서 아래처럼 출력됩니다.

[[File:HTMLrender.png]]
 
HTML 문서는 "문서 유형"또는 "DOCTYPE 선언」라는 것으로부터 시작됩니다 (자세한 내용은 Choosing the right doctype for your HTML documents 를 참조하십시오). DOCTYPE 선언은 주로 "표준 모드"라는 것으로 HTML을 잘 렌더링하는 데 도움이 됩니다. 또한 검사기는 모든 HTML 버전 코드를 확인하는 방법을 알 수 있습니다. 현재 이 의미를 몰라도 걱정하지 마십시오. 이봐 설명하고 있습니다. 이 예제에서는 HTML5의 DOCTYPE 선언을 볼 수 있습니다.
 
DOCTYPE 선언 다음에 있는 것이, <code>html</code> 요소의 여는 태그입니다. 이 문서 전체를 둘러싸 요소입니다. 그래서 <code>html</code> 요소의 종료 태그는 문서의 마지막에 등장합니다. <code>html</code> 요소는 항상 <code>lang</code> 속성을 가져야 합니다. 이것은 페이지의 기본 언어를 지정합니다. 예를 들어, <code>en</code> 은 "영어"을 의미하고, <code>fr</code> 은 "프랑스어"을 의미합니다. 언어 코드를 찾기 위해 Richard Ishida의 [http://rishida.net/utils/subtags/ | Language Subtag Lookup tool] 등의 도구도 사용할 수 있습니다.

<code>html 요소 중 일부는 <code>head</code> 요소가 있습니다. 이것은 문서에 대한 정보 (메타 데이터)를 저장하는 부분입니다. <code>head 요소에 대해서는 다음 기사 에서 자세히 설명합니다. <code>head</code> 요소 안에있는 <code>title</code> 요소가 윈도우에 표시되는 타이틀 (이 경우 "샘플 페이지")을 지정하는 요소입니다. <code>head</code> 요소에는 항상 페이지의 문자 코드를 식별하는 <code>charset</code> 속성을 가진 <code>meta 요소를 포함해야합니다. 가능한 UTF-8을 사용하는 것이 좋습니다. more about character encodings 참조하십시오.
 
After the <code>[[html/elements/head|head]]</code> element there is a <code>[[html/elements/body|body]]</code> element, which is the
wrapper to contain the actual content of the page—in this case, only a level-one header (<code>[[html/elements/hn|h1]]</code>) element, which contains the text “Hello world.”

And that’s our document in full.
 
Elements often contain other elements. The body of
the document will invariably end up involving many nested elements.
Structural elements such as <code>article</code>, <code>header</code> and <code>div</code> create the overall structure of the document, and will
contain subdivisions. These will contain headings, paragraphs, lists
and so on. Paragraphs can contain elements that make links to other
documents, quotes, emphasis and so on. You will find out more about
these elements in later articles.

== The syntax of HTML elements ==
 
A basic element in HTML consists of two
markers around a block of text, and in almost every case elements can contain
sub-elements (such as <code>html</code> containing <code>head</code> and <code>body</code> in the
example above). There are some exceptions to the rule: some elements do not contain text or sub-elements, for example <code>img</code>. You'll learn more about these later on.
 
Elements can also have attributes, which can modify the behaviour
of the element and introduce extra meaning. Let's have a look at another example.
 
<syntaxhighlight lang="html5"><header>
  <h1>The Basics of 
    <abbr title="Hypertext Markup Language">HTML</abbr>
  </h1>
</header></syntaxhighlight>

This looks like so when rendered:

[[File:htmlrender2.png]]
 
In this example a <code>header</code> element (used to mark up header sections of documents) contains an <code>h1</code>
element (first, or most important level header), which in turn
contains some text. Part of that text is wrapped in an <code>abbr</code> element
(used to specify the expansion of abbreviations), which has a <code>title</code> attribute, the value of which is set to <code>Hypertext Markup
Language</code>.
 
Many attributes in HTML are common to all elements, though some are
specific to a given element or elements. They are always of the form
<code>keyword="value"</code>. The value is often surrounded by single or double quotes: this is not necessary in HTML5, except when the attribute value has multiple words, in which case you need to use quotes to make it clear that it is a single attribute value, and not several attributes. Saying all this, I would however recommend that you stick to quoting values for now, as it is good practice and can make the code easier to read. In addition, some HTML flavours you may work with in the future DO require quoting of attributes, for example XHTML 1.0, and it doesn't hurt to do so in flavours that don't.
 
[http://www.w3.org/TR/html401/index/attributes.html Attributes and their possible values are mostly defined by the HTML specifications]—you cannot make up your own attributes without making the HTML invalid, as this can confuse user agents and cause problems interpreting the web page correctly. The only real exceptions are the <code>id</code> and <code>class</code> attributes—their values are entirely under your control, as they are for defining custom meanings .
 
An element within another element is referred to as being a “child”
of that element. So in the above example, <code>abbr</code> is a child of the
<code>h1</code>, which is itself a child of the <code>header</code>. Conversely, the <code>header</code> element
would be referred to as a “parent” of the <code>h1</code> element. This parent/child concept is important, as it forms the basis of CSS and is heavily
used in JavaScript.

== Block level and inline elements ==
 
There are two general categories of elements in HTML, which
correspond to the types of content and structure those elements
represent—block level elements and inline elements.

Block level means a higher level element, normally informing the
structure of the document. It may help to think of block level
elements being those that start on a new line, breaking away
from what went before. Some common block level elements include
paragraphs, list items, headings and tables.

Inline elements are those that are contained within block level
structural elements and surround only small parts of the document’s content,
not entire paragrahs and groupings of content. An inline element will not cause a new line to
appear in the document: they are the kind of elements that would
appear in a paragraph of text. Some common inline elements include
hypertext links, highlighted words or phrases and short quotations.

Note: HTML5 redefines the element categories in HTML: see [http://www.whatwg.org/specs/web-apps/current-work/complete/section-index.html#element-content-categories Element content categories]. While these definitions are more accurate and less ambiguous than the ones that went before, they are a lot more complicated to understand than "block" and "inline". We will therefore stick with these throughout this course.

== Character references ==
 
One last item to mention in an HTML document is how to include
special characters. In HTML the characters <code>&lt;</code>, <code>&gt;</code> and <code>&amp;</code> are special.
They start and end parts of the HTML document, rather than
representing the characters less-than, greater-than and ampersand. For this reason, they must always be used in escaped form in content.

Other than for these characters, you should try to avoid using character references unless you are dealing with an invisible or ambiguous character. If you use the UTF-8 character encoding you can represent any character (other than the three mentioned above) without escaping.
 
One of the earliest mistakes a web author can make is to use an
ampersand in a document and then have something unexpected appear.
For example, writing “Imperial units measure weight in stones&amp;pounds” could actually end up appearing as “…stones£s” in some browsers.
 
This is because the literal string “&amp;pound;” is actually a character
reference in HTML. A character reference is a way of including a
character into a document that is difficult or impossible to enter
using a keyboard, or in a particular document encoding.
 
The ampersand (&amp;) introduces the reference and the semi-colon (;) ends
it. However, many user agents can be quite forgiving of HTML mistakes
such as leaving out the semi-colon, and treat “&amp;pound” as a character
reference. References can either be numbers (numeric references) or
shorthand words (entity references).
 
An actual ampersand has to be entered into a document as "&amp;amp;",
which is the character entity reference, or as "&amp;#38;" which is
the numeric reference. Web Platform Docs includes a [[html/entities#HTML_Entities_Table | Table of Common HTML Entities]] for reference.

For more information about working with character escapes see [http://www.w3.org/International/questions/qa-escapes Using character escapes in markup and CSS].