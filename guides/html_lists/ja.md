{{Page_Title|HTMLのリスト}}
{{Flags
|State=Unreviewed
|Checked_Out=No
}}
{{Byline}}
{{Summary_Section|この文書では、HTMLの3つのタイプのリストを紹介し、その基本的な特徴を調べます。}}
{{Guide
|Content={{Languages}}
== はじめに ==

リストは、関連する個々の情報を集めるのに使われ、相互の関連がはっきりして読みやすくなります。最近のweb開発において、リストはとても役立つ要素であり、一般的なコンテンツと同様、ナビゲーションによく使われます。

リストは構造的な点で優れています。というのは、構造が整えられて分かりやすくなり、ドキュメントのメンテナンスも容易になるからです。
また便利な点として、CSSスタイルと連携できる専用の要素を用意していることも挙げられます。最後に、意味的に正しいリストによって、webサイトを訪れた人が読み取りやすくなります。加えて、ページがアップデートを必要とした時、メンテナンスがやさしくなります。

== 3つのタイプのリスト ==

HTMLには、3つのタイプのリストがあります。

* '''順序なしリスト''' — 任意の順序で関連した項目を集めるのに使用
* '''順序ありリスト''' — 特定の順序で関連した項目を集めるのに使用
* '''説明リスト''' — 項目と定義のような、名前と値を組み合わせて表示するのに使用

リストの各タイプは、webページの中で独自の目的と意味を持っています。

=== 順序なしリスト ===

''順序なし'' (ビュレット)リストは、順序に関係なく項目を並べる時に使います。買い物リストがその例です。

* milk
* bread
* butter
* coffee beans

その項目はリストの一部ですが、どんな順序にでも並べられ、それでも意味があるリストになるでしょう。

* bread
* coffee beans
* milk
* butter

CSSを使うと、ビュレットを既定のスタイルの1つに変更したり、自分で用意した画像を使ったり、ビュレットなしでリストを表示したりできます — このやり方は [[guides/Styling lists and links|Styling lists and links]] という文書で見るつもりです。

==== 順序なしリストをマークアップする ====

順序なしリストは、1つの <code>&lt;ul&gt;&lt;/ul&gt;</code> タグが、複数の <code>&lt;li&gt;&lt;/li&gt;</code> タグを囲む形で使います。

<syntaxhighlight lang="html5"><ul>
  <li>bread</li>
  <li>coffee beans</li>
  <li>milk</li>
  <li>butter</li>
</ul></syntaxhighlight>

=== 順序ありリスト ===

''順序あり'' (番号付き)リストは、特定の順序で並んだ項目のリストを表示するのに使われます。調理の説明がその例です。

# Gather ingredients
# Mix ingredients together
# Place ingredients in a baking dish
# Bake in oven for an hour
# Remove from oven
# Allow to stand for ten minutes
# Serve

リストのアイテムを違う順番に移動すると、もはや情報は意味を持たなくなります。

# Gather ingredients
# Bake in oven for an hour
# Serve
# Remove from oven
# Place ingredients in a baking dish
# Allow to stand for ten minutes
# Mix ingredients together

順序ありリストは、順序の付け方を選択して表示できます。たいていのブラウザのデフォルトは10進数字ですが、他に利用できるものもあります。

* 文字
** アスキー文字 小文字 (a, b, c…)
** アスキー文字 大文字 (A, B, C…).
** 古典ギリシャ文字 小文字 (έ, ή, ί…)
* 数字
** 10進数字 (1, 2, 3…)
** ゼロを先頭に付けた10進数字 (01, 02, 03…)
** ローマ数字 小文字 (i, ii, iii…)
** ローマ数字 大文字 (I, II, III…)
** 伝統的なグルジア数字 (an, ban, gan…)
** 伝統的なアルメニア数字 (mek, yerku, yerek…)

順序なしリストと同様、CSSを使って順序ありリストのスタイルを変更できます。
さらに詳しい情報は、[[guides/Styling lists and links|Styling lists and links]] を見てください。

==== 順序ありリストをマークアップする ====

順序ありリストは、1つの  <code>&lt;ol&gt;&lt;/ol&gt;</code> タグが、複数の  <code>&lt;li&gt;&lt;/li&gt;</code> タグを囲む形で使います。

<syntaxhighlight lang="html5"><ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol>
</syntaxhighlight>

==== 順序ありリストを1以外の番号で開始する ====

順序ありリストを使う際によく必要となるのは、リストを1(もしくはiや I等)以外の番号ではじめることです。<code>start</code>  属性を使って実現します。この属性には数値を指定します(CSSを使ってリストのカウンターをアルファベットやローマ字にしていても)。項目リストが1つあって、そのリストに注釈や別の関連情報を割り込ませる必要があるとすると、これは役に立ちます。

<syntaxhighlight lang="html5"><ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
</ol>

<p>Before you place the ingredients in the baking dish, preheat the oven to
180 degrees centigrade/350 degrees fahrenheit in readiness for the next step.</p>

<ol start="4">
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol></syntaxhighlight>

これは下記の結果になります。

<ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
</ol>

<p>Before you place the ingredients in the baking dish, preheat the oven to 180 degrees centigrade/350 degrees fahrenheit in readiness for the next step.</p>

<ol start="4">
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol>

注意したいのは、この属性はHTML 4では非推奨だったことです。したがって、ページでHTML 4の strict 型を使っていると検証が通らないでしょう。HTML 4の strict 型なページでそのような機能を使って完璧に正しくしたいのなら、代わりに [http://dev.opera.com/articles/view/automatic-numbering-with-css-counters/ CSS Counters] を使って実装してください。しかし幸いにも、 <code>start</code> 属性は、HTML5で非推奨ではなくなりました。

=== 説明リスト===

''説明リスト''(以前は ''定義リスト'' と言われていましたが、HTML5で変わりました)は、リスト内で特定の名前と値を関連付けます。
例として、材料リストと説明や記事の著者と略歴、競技会の勝者と勝利した年が挙げられるかもしれません。好きなだけ名前と値のグループを作成できますが、少なくとも1つの名前と値のペアが存在する必要があります。

説明リストは融通が利きます。1つの名前に複数の値を関連付けられますし、その逆も可能です。例えば「coffee」という項目にいくつも意味を持たせられ、次々と表示できます。

<pre>coffee

  a beverage made from roasted, ground coffee beans
  a cup of coffee
  a social gathering at which coffee is consumed
  a medium to dark brown colour</pre>

もしくは、1つの値に複数の名前を関連付けることもできます。これは項目全てが同じ意味を持つといった、項目のバリエーションを表すのに便利です。

<pre>soda
pop
fizzy drink
cola

  a sweet, carbonated beverage</pre>

==== 説明リストをマークアップする ====

説明リストは、1つの <code>&lt;dl&gt;&lt;/dl&gt;</code> タグが複数の <code>&lt;dt&gt;&lt;/dt&gt;</code> (名前)と <code>&lt;dd&gt;&lt;/dd&gt;</code> (値)タグを囲む形で使います。少なくても1つの<code>&lt;dt&gt;&lt;/dt&gt;</code> と<code>&lt;dd&gt;&lt;/dd&gt;</code> のペアが必要です。<code>&lt;dt&gt;&lt;/dt&gt;</code> は、ソース上の順番で必ず最初にくるようにしてください。

名前1つに値が1つの単純な説明リストは、このようになります。

<syntaxhighlight lang="html5"><dl>
  <dt>Name</dt>
  <dd>Value</dd>
  <dt>Name</dt>
  <dd>Value</dd>
  <dt>Name</dt>
  <dd>Value</dd>
</dl></syntaxhighlight>

これは次のようにレンダリングされます。

<pre>Name
  Value
Name
  Value
Name
  Value</pre>

下記の例では、名前1つに複数の値のものと複数の名前に値が1つもの両方を関連付けしています。

<syntaxhighlight lang="html5"><dl>
  <dt>Name1</dt>
  <dd>Value that applies to Name1</dd>
  <dt>Name2</dt>
  <dt>Name3</dt>
  <dd>Value that applies to both Name2 and Name3</dd>
  <dt>Name4</dt>
  <dd>One value that applies to Name4</dd>
  <dd>Another value that applies to Name4</dd>
</dl></syntaxhighlight>

このコードは、このようにレンダリングされます。

<pre>Name1
  Value that applies to Name1
Name2
Name3
  Value that applies to both Name2 and Name3
Name4
  One value that applies to Name4
  Another value that applies to Name4</pre>

==  リストのタイプを選ぶ ==

どのタイプのリストにするのかを決めようとする時には、簡単な2つの質問を自問してください。

<ol>
  <li>項目を定義するか? もしくは他の名前と値の組み合わせを関連付けするか?
    <ul>
      <li>Yesなら、説明リストを使用</li>
      <li>Noなら、説明リストは不使用</li>
    </ul>
  </li>
  <li>リストの項目の順序は重要か?
    <ul>
      <li>Yesなら、順序ありリストを使用</li>
      <li>Noなら、順序なしリストを使用</li>
    </ul>
  </li>
</ol>

== HTMLのリストの長所 ==

* 柔軟さ：順序ありリストでリストの項目の順序を変更しなければならなくなっても、リストの項目要素を移動させるだけです。ブラウザがそのリストをレンダリングすると、正しく並ぶでしょう。
* スタイル：HTMLのリストを使えば、CSSを利用してリストをきっちり整えられます。リストの項目の <code>&lt;li&gt;</code> タグは、ドキュメントにある他のタグと違っていて、CSSのルールを細かく適用できます。
* 意味付け：HTMLのリストは、コンテンツに正しい意味的な構造をもたらします。これは重要なメリットで、スクリーンリーダーによって視覚障害があるユーザーが、リストを読めるようになります。テキストと数字がごちゃまぜで、ややこしくなったものから読み取ることがなくなります。

別の言い方をすれば、'''普通のテキストタグを使って、リストの項目を記述するな''' です。リストのかわりにテキストを使うと、手間が余計にかかる上、ドキュメントの読者も困難な状況になります。したがって、ドキュメントにリストが必要なら、HTMLのリスト形式を正しく使う必要があります。

==リストをネスト(入れ子に)する ==

個々のリストの項目には、 別のリスト全体を入れることができます。いわゆる ''ネストされたリスト(入れ子のリスト)'' です。
サブセクションがあるコンテンツの見出しのようなものに役に立ちます。

<pre>1. Chapter One
    a. Section One
    b. Section Two
    c. Section Three
2. Chapter Two
3. Chapter Three</pre>

コードで示すと、最初のリストの項目の内側にネストされたリスト全体を入れることになります。コードはこのようになります。

<syntaxhighlight lang="html5"><ol>
  <li>Chapter One
    <ol style="list-style-type: lower-alpha;">
      <li>Section One</li>
      <li>Section Two </li>
      <li>Section Three </li>
    </ol>
  </li>
  <li>Chapter Two</li>
  <li>Chapter Three  </li>
</ol></syntaxhighlight>

注意して欲しいのは、CSSのプロパティの <code>list-style-type: lower-alpha</code> を使って、ネストされたリストを10進数字の代わりに小文字を並べている点です。

ネストされたリストはとても便利で、ナビゲーションメニューの基礎となっており、webサイトの階層的な構造を規定するための手っ取り早い方法になっています。またとても融通が利き、順序あり・順序なしリストどちらでも、順序あり・順序なしリストの項目を内側にネストできます。順序ありリストの内側に順序なしリストをネストさせた例が、上記の「リストのタイプを選ぶ 」にあります。

理屈の上では、好きなレベルだけリストをネストすることができますが、実際はあまりに深くネストしてしまうと混乱をきたします。とても大きなリストなら、コンテンツを分割し見出しを付けてリストを分けるか、さらにページに分割するかした方がもっと良くなるでしょう。
経験則では、3レベル以上に深くしないことです。

== 結論 ==

この文書では、HTMLのリストの様々なタイプがどのように使われ、コーディングされるかを見てきました。基本的なリストのオプションも調べました。
HTMLのリストの体裁や振る舞い修正する具体的な情報がさらに必要なら、[[guides/Styling lists and links|Styling lists and links]] を見てください。
}}
{{Notes_Section}}
{{Compatibility_Section
|Not_required=Yes
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|External_links=* [http://www.alistapart.com/articles/taminglists/ A List Apart: Taming Lists]
* [http://www.w3.org/TR/REC-CSS2/generate.html#lists W3C CSS2: list-style-type definition]
|Manual_sections==== 練習問題 ===
 
* 3つのタイプのHTMLリストとは何か?
* どのような時にそれぞれのリストを使うか? どうやって選ぶのか?
* どうやってリストをネストするのか?
* リストを整形するのに、なぜHTMLよりもCSSを使うのか?
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
}}