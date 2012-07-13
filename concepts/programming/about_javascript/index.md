<p>JavaScript is a cross-platform, object-based scripting language. This guide explains everything you need to know about using JavaScript.</p>
<h2>New features in JavaScript versions</h2>
<pre class="script" style="font-size: 16px;">/* Note: To add a link to new JavaScript version description
add version number to versionList variable below. The page linked to
must reside in /en/JavaScript/New_in_JavaScript/N, where N is version number. */

var versionList = ["1.5", "1.6", "1.7", "1.8", "1.8.1", "1.8.5"];
var s = "";
&lt;ul&gt;
  foreach (var i in versionList){
    let s = "/en/JavaScript/New_in_JavaScript/" .. i;
&nbsp;   &lt;li&gt;web.link(s, wiki.getPage(s).title)&lt;/li&gt;;
  }
&lt;/ul&gt;;</pre>
<h2>What you should already know</h2>
<p>This guide assumes you have the following basic background:</p>
<ul>
	<li>A general understanding of the Internet and the World Wide Web (WWW).</li>
	<li>Good working knowledge of HyperText Markup Language (<a href="mks://localhost/en/HTML" title="en/HTML">HTML</a>).</li>
</ul>
<p>Some programming experience with a language such as C or Visual Basic is useful, but not required.</p>
<h2>JavaScript versions</h2>
<table class="standard-table">
	<caption style="text-align: left;">Table 1 JavaScript and Navigator versions</caption>
	<thead>
		<tr>
			<th scope="col">JavaScript version</th>
			<th scope="col">Navigator version</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>JavaScript 1.0</td>
			<td>Navigator 2.0</td>
		</tr>
		<tr>
			<td>JavaScript 1.1</td>
			<td>Navigator 3.0</td>
		</tr>
		<tr>
			<td>JavaScript 1.2</td>
			<td>Navigator 4.0-4.05</td>
		</tr>
		<tr>
			<td>JavaScript 1.3</td>
			<td>Navigator 4.06-4.7x</td>
		</tr>
		<tr>
			<td>JavaScript 1.4</td>
			<td></td>
		</tr>
		<tr>
			<td>JavaScript 1.5</td>
			<td>Navigator 6.0<br />
				Mozilla (open source browser)</td>
		</tr>
		<tr>
			<td>JavaScript 1.6</td>
			<td><a href="mks://localhost/en/Firefox_1.5_for_developers" title="en/Firefox_1.5_for_developers">Firefox 1.5</a>, other Mozilla 1.8-based products</td>
		</tr>
		<tr>
			<td>JavaScript 1.7</td>
			<td><a href="mks://localhost/en/Firefox_2_for_developers" title="en/Firefox_2_for_developers">Firefox 2</a>, other Mozilla 1.8.1-based products</td>
		</tr>
		<tr>
			<td>JavaScript 1.8</td>
			<td><a href="mks://localhost/en/Firefox_3_for_developers" title="en/Firefox_3_for_developers">Firefox 3</a>, other Gecko 1.9-based products</td>
		</tr>
	</tbody>
</table>
<p>Each version of the Netscape Enterprise Server also supports a different version of JavaScript. To help you write scripts that are compatible with multiple versions of the Enterprise Server, this manual uses an abbreviation to indicate the server version in which each feature was implemented.</p>
<table class="standard-table">
	<caption style="text-align: left;">Table 2 Abbreviations of Netscape Enterprise Server versions</caption>
	<thead>
		<tr>
			<th scope="col">Abbreviation</th>
			<th scope="col">Enterprise Server version</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td>NES 2.0</td>
			<td>Netscape Enterprise Server 2.0</td>
		</tr>
		<tr>
			<td>NES 3.0</td>
			<td>Netscape Enterprise Server 3.0</td>
		</tr>
	</tbody>
</table>
<h2>Where to find JavaScript information</h2>
<p>JavaScript documentation includes the following books:</p>
<ul>
	<li><a href="mks://localhost/en/JavaScript/Guide" title="en/Core_JavaScript_1.5_Guide">JavaScript Guide</a> (this guide) provides information about JavaScript language and its objects.</li>
	<li><a href="mks://localhost/en/JavaScript/Reference" title="en/JavaScript/Reference">JavaScript Reference</a> provides reference material for JavaScript language.</li>
</ul>
<p>If you are new to JavaScript, start with the <a href="mks://localhost/en/JavaScript/Guide" title="en/Core_JavaScript_1.5_Guide">JavaScript Guide</a>. Once you have a firm grasp of the fundamentals, you can use the <a href="mks://localhost/en/JavaScript/Reference" title="en/JavaScript/Reference">JavaScript Reference</a> to get more details on individual objects and statements.</p>
<h2>Tips for learning JavaScript</h2>
<p>Getting started with JavaScript is easy: all you need is a modern Web browser. This guide includes some JavaScript features which are only currently available in the latest versions of Firefox (and other Gecko powered browsers), so using the most recent version of Firefox is recommended.</p>
<h3>An interactive interpreter</h3>
<p>An interactive JavaScript prompt is an invaluable aid to learning the language, as it enables you to try things out interactively without having to save a file and refresh a page. The Firefox Error Console, accessible through the Tools menu, provides a simple way to try interactive JavaScript: Just enter a line of code and click the "Evaluate" button.</p>
<p><img alt="Image:ErrorConsole.png" class="internal" src="/@api/deki/files/192/=ErrorConsole.png" /></p>
<h3>Firebug</h3>
<p>A more advanced interactive prompt is available using <a class="external" href="http://www.getfirebug.com/">Firebug</a>, a Firefox extension. Expressions you type are interpreted as objects and linked to other parts of Firebug. For example, you can add 5 plus 5, change the case of a string, get a clickable link to the document, or get a link to an element:</p>
<p><img alt="" class="internal" src="/@api/deki/files/5188/=FirebugCommandLine.PNG" style="width: 728px; height: 281px;" /></p>
<p>Using the arrow on the right bottom corner gives a command editor for multiline scripts.</p>
<p>Firebug also provides an advanced DOM inspector, a JavaScript debugger, a profiling tool and various other utilities. JavaScript code running in a Web page can call, <code>console.log()</code>, a function that prints its arguments to the Firebug console.</p>
<p>Many of the examples in this guide use <code>alert()</code> to show messages as they execute. If you have Firebug installed you can use <code>console.log()</code> in place of <code>alert()</code> when running these examples.</p>
<h2>Document conventions</h2>
<p>JavaScript applications run on many operating systems; the information in this book applies to all versions. File and directory paths are given in Windows format (with backslashes separating directory names). For Unix versions, the directory paths are the same, except that you use slashes instead of backslashes to separate directories.</p>
<p>This guide uses uniform resource locators (URLs) of the following form:</p>
<p><code>http://<em>server</em>.<em>domain</em>/<em>path</em>/<em>file</em>.html</code></p>
<p>In these URLs, <em>server</em> represents the name of the server on which you run your application, such as <code>research1</code> or <code>www</code>; <em>domain</em> represents your Internet domain name, such as <code>netscape.com</code> or <code>uiuc.edu</code>; <em>path</em> represents the directory structure on the server; and <em>file</em><code>.html</code> represents an individual file name. In general, items in italics in URLs are placeholders and items in normal monospace font are literals. If your server has Secure Sockets Layer (SSL) enabled, you would use <code>https</code> instead of <code>http</code> in the URL.</p>
<p>This guide uses the following font conventions:</p>
<ul>
	<li><code>The monospace font</code> is used for sample code and code listings, API and language elements (such as method names and property names), file names, path names, directory names, HTML tags, and any text that must be typed on the screen. (<code><em>Monospace italic font</em></code> is used for placeholders embedded in code.)</li>
	<li><em>Italic type</em> is used for book titles, emphasis, variables and placeholders, and words used in the literal sense.</li>
	<li><strong>Boldface</strong> type is used for glossary terms.</li>
</ul>
<pre class="script" style="font-size: 16px;">autoPreviousNext("JSGChapters");

</pre>
<p></p>
{{MDN_Attribution|copr_date=2012|src_url=https://developer.mozilla.org/en/JavaScript/Guide/About|src_title=About this guide}}