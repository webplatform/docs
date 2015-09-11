---
title: HTMLのリスト
lang: ja
summary: この文書では、HTMLの3つのタイプのリストを紹介し、その基本的な特徴を調べます。
tags:
  - Guides
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'guides/html lists/af'
    - 'guides/html lists/ar'
    - 'guides/html lists/ast'
    - 'guides/html lists/az'
    - 'guides/html lists/bcc'
    - 'guides/html lists/bg'
    - 'guides/html lists/br'
    - 'guides/html lists/ca'
    - 'guides/html lists/cs'
    - 'guides/html lists/da'
    - 'guides/html lists/de'
    - 'guides/html lists/diq'
    - 'guides/html lists/el'
    - 'guides/html lists/eo'
    - 'guides/html lists/es'
    - 'guides/html lists/fa'
    - 'guides/html lists/fi'
    - 'guides/html lists/fr'
    - 'guides/html lists/gl'
    - 'guides/html lists/gu'
    - 'guides/html lists/he'
    - 'guides/html lists/hu'
    - 'guides/html lists/hy'
    - 'guides/html lists/id'
    - 'guides/html lists/it'
    - 'guides/html lists/ka'
    - 'guides/html lists/kk'
    - 'guides/html lists/km'
    - 'guides/html lists/ko'
    - 'guides/html lists/ksh'
    - 'guides/html lists/kw'
    - 'guides/html lists/mk'
    - 'guides/html lists/ml'
    - 'guides/html lists/mr'
    - 'guides/html lists/ms'
    - 'guides/html lists/nl'
    - 'guides/html lists/no'
    - 'guides/html lists/oc'
    - 'guides/html lists/pl'
    - 'guides/html lists/pt'
    - 'guides/html lists/pt-br'
    - 'guides/html lists/ro'
    - 'guides/html lists/ru'
    - 'guides/html lists/si'
    - 'guides/html lists/sk'
    - 'guides/html lists/sl'
    - 'guides/html lists/sq'
    - 'guides/html lists/sr'
    - 'guides/html lists/sv'
    - 'guides/html lists/ta'
    - 'guides/html lists/th'
    - 'guides/html lists/tr'
    - 'guides/html lists/uk'
    - 'guides/html lists/vi'
    - 'guides/html lists/yue'
    - 'guides/html lists/zh'
    - 'guides/html lists/zh-hans'
    - 'guides/html lists/zh-hant'
    - 'guides/html lists/zh-tw'
uri: 'guides/html lists/ja'

---
## <span>Summary</span>

この文書では、HTMLの3つのタイプのリストを紹介し、その基本的な特徴を調べます。

<table class="nmbox languages" style>
<tr>
<th class="mbox-image" style>
**言語:**

</th>
<td class="mbox-text">
**[English](/guides/html_lists)**  • <span lang="ja">**日本語**</span>

</td>
</tr>
</table>
## <span>はじめに</span>

リストは、関連する個々の情報を集めるのに使われ、相互の関連がはっきりして読みやすくなります。最近のweb開発において、リストはとても役立つ要素であり、一般的なコンテンツと同様、ナビゲーションによく使われます。

リストは構造的な点で優れています。というのは、構造が整えられて分かりやすくなり、ドキュメントのメンテナンスも容易になるからです。 また便利な点として、CSSスタイルと連携できる専用の要素を用意していることも挙げられます。最後に、意味的に正しいリストによって、webサイトを訪れた人が読み取りやすくなります。加えて、ページがアップデートを必要とした時、メンテナンスがやさしくなります。

## <span>3つのタイプのリスト</span>

HTMLには、3つのタイプのリストがあります。

-   **順序なしリスト** — 任意の順序で関連した項目を集めるのに使用
-   **順序ありリスト** — 特定の順序で関連した項目を集めるのに使用
-   **説明リスト** — 項目と定義のような、名前と値を組み合わせて表示するのに使用

リストの各タイプは、webページの中で独自の目的と意味を持っています。

### <span>順序なしリスト</span>

*順序なし* (ビュレット)リストは、順序に関係なく項目を並べる時に使います。買い物リストがその例です。

-   milk
-   bread
-   butter
-   coffee beans

その項目はリストの一部ですが、どんな順序にでも並べられ、それでも意味があるリストになるでしょう。

-   bread
-   coffee beans
-   milk
-   butter

CSSを使うと、ビュレットを既定のスタイルの1つに変更したり、自分で用意した画像を使ったり、ビュレットなしでリストを表示したりできます — このやり方は [Styling lists and links](/guides/Styling_lists_and_links) という文書で見るつもりです。

#### <span>順序なしリストをマークアップする</span>

順序なしリストは、1つの `<ul></ul>` タグが、複数の `<li></li>` タグを囲む形で使います。

``` html
<ul>
  <li>bread</li>
  <li>coffee beans</li>
  <li>milk</li>
  <li>butter</li>
</ul>
```

### <span>順序ありリスト</span>

*順序あり* (番号付き)リストは、特定の順序で並んだ項目のリストを表示するのに使われます。調理の説明がその例です。

1.  Gather ingredients
2.  Mix ingredients together
3.  Place ingredients in a baking dish
4.  Bake in oven for an hour
5.  Remove from oven
6.  Allow to stand for ten minutes
7.  Serve

リストのアイテムを違う順番に移動すると、もはや情報は意味を持たなくなります。

1.  Gather ingredients
2.  Bake in oven for an hour
3.  Serve
4.  Remove from oven
5.  Place ingredients in a baking dish
6.  Allow to stand for ten minutes
7.  Mix ingredients together

順序ありリストは、順序の付け方を選択して表示できます。たいていのブラウザのデフォルトは10進数字ですが、他に利用できるものもあります。

-   文字
    -   アスキー文字 小文字 (a, b, c…)
    -   アスキー文字 大文字 (A, B, C…).
    -   古典ギリシャ文字 小文字 (έ, ή, ί…)
-   数字
    -   10進数字 (1, 2, 3…)
    -   ゼロを先頭に付けた10進数字 (01, 02, 03…)
    -   ローマ数字 小文字 (i, ii, iii…)
    -   ローマ数字 大文字 (I, II, III…)
    -   伝統的なグルジア数字 (an, ban, gan…)
    -   伝統的なアルメニア数字 (mek, yerku, yerek…)

順序なしリストと同様、CSSを使って順序ありリストのスタイルを変更できます。 さらに詳しい情報は、[Styling lists and links](/guides/Styling_lists_and_links) を見てください。

#### <span>順序ありリストをマークアップする</span>

順序ありリストは、1つの `<ol></ol>` タグが、複数の `<li></li>` タグを囲む形で使います。

``` html
<ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol>
```

#### <span>順序ありリストを1以外の番号で開始する</span>

順序ありリストを使う際によく必要となるのは、リストを1(もしくはiや I等)以外の番号ではじめることです。`start` 属性を使って実現します。この属性には数値を指定します(CSSを使ってリストのカウンターをアルファベットやローマ字にしていても)。項目リストが1つあって、そのリストに注釈や別の関連情報を割り込ませる必要があるとすると、これは役に立ちます。

``` html
<ol>
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
</ol>
```

 これは下記の結果になります。

1.  Gather ingredients
2.  Mix ingredients together
3.  Place ingredients in a baking dish

Before you place the ingredients in the baking dish, preheat the oven to 180 degrees centigrade/350 degrees fahrenheit in readiness for the next step.

1.  Bake in oven for an hour
2.  Remove from oven
3.  Allow to stand for ten minutes
4.  Serve

注意したいのは、この属性はHTML 4では非推奨だったことです。したがって、ページでHTML 4の strict 型を使っていると検証が通らないでしょう。HTML 4の strict 型なページでそのような機能を使って完璧に正しくしたいのなら、代わりに [CSS Counters](http://dev.opera.com/articles/view/automatic-numbering-with-css-counters/) を使って実装してください。しかし幸いにも、 `start` 属性は、HTML5で非推奨ではなくなりました。

### <span>説明リスト</span>

*説明リスト*(以前は *定義リスト* と言われていましたが、HTML5で変わりました)は、リスト内で特定の名前と値を関連付けます。 例として、材料リストと説明や記事の著者と略歴、競技会の勝者と勝利した年が挙げられるかもしれません。好きなだけ名前と値のグループを作成できますが、少なくとも1つの名前と値のペアが存在する必要があります。

説明リストは融通が利きます。1つの名前に複数の値を関連付けられますし、その逆も可能です。例えば「coffee」という項目にいくつも意味を持たせられ、次々と表示できます。

    coffee

      a beverage made from roasted, ground coffee beans
      a cup of coffee
      a social gathering at which coffee is consumed
      a medium to dark brown colour

もしくは、1つの値に複数の名前を関連付けることもできます。これは項目全てが同じ意味を持つといった、項目のバリエーションを表すのに便利です。

    soda
    pop
    fizzy drink
    cola

      a sweet, carbonated beverage

#### <span>説明リストをマークアップする</span>

説明リストは、1つの `<dl></dl>` タグが複数の `<dt></dt>` (名前)と `<dd></dd>` (値)タグを囲む形で使います。少なくても1つの`<dt></dt>` と`<dd></dd>` のペアが必要です。`<dt></dt>` は、ソース上の順番で必ず最初にくるようにしてください。

名前1つに値が1つの単純な説明リストは、このようになります。

``` html
<dl>
  <dt>Name</dt>
  <dd>Value</dd>
  <dt>Name</dt>
  <dd>Value</dd>
  <dt>Name</dt>
  <dd>Value</dd>
</dl>
```

 これは次のようにレンダリングされます。

    Name
      Value
    Name
      Value
    Name
      Value

下記の例では、名前1つに複数の値のものと複数の名前に値が1つもの両方を関連付けしています。

``` html
<dl>
  <dt>Name1</dt>
  <dd>Value that applies to Name1</dd>
  <dt>Name2</dt>
  <dt>Name3</dt>
  <dd>Value that applies to both Name2 and Name3</dd>
  <dt>Name4</dt>
  <dd>One value that applies to Name4</dd>
  <dd>Another value that applies to Name4</dd>
</dl>
```

 このコードは、このようにレンダリングされます。

    Name1
      Value that applies to Name1
    Name2
    Name3
      Value that applies to both Name2 and Name3
    Name4
      One value that applies to Name4
      Another value that applies to Name4

## <span>リストのタイプを選ぶ</span>

どのタイプのリストにするのかを決めようとする時には、簡単な2つの質問を自問してください。

1.  項目を定義するか? もしくは他の名前と値の組み合わせを関連付けするか?
    -   Yesなら、説明リストを使用
    -   Noなら、説明リストは不使用

2.  リストの項目の順序は重要か?
    -   Yesなら、順序ありリストを使用
    -   Noなら、順序なしリストを使用

## <span>HTMLのリストの長所</span>

-   柔軟さ：順序ありリストでリストの項目の順序を変更しなければならなくなっても、リストの項目要素を移動させるだけです。ブラウザがそのリストをレンダリングすると、正しく並ぶでしょう。
-   スタイル：HTMLのリストを使えば、CSSを利用してリストをきっちり整えられます。リストの項目の `<li>` タグは、ドキュメントにある他のタグと違っていて、CSSのルールを細かく適用できます。
-   意味付け：HTMLのリストは、コンテンツに正しい意味的な構造をもたらします。これは重要なメリットで、スクリーンリーダーによって視覚障害があるユーザーが、リストを読めるようになります。テキストと数字がごちゃまぜで、ややこしくなったものから読み取ることがなくなります。

別の言い方をすれば、**普通のテキストタグを使って、リストの項目を記述するな** です。リストのかわりにテキストを使うと、手間が余計にかかる上、ドキュメントの読者も困難な状況になります。したがって、ドキュメントにリストが必要なら、HTMLのリスト形式を正しく使う必要があります。

## <span>リストをネスト(入れ子に)する</span>

個々のリストの項目には、 別のリスト全体を入れることができます。いわゆる *ネストされたリスト(入れ子のリスト)* です。 サブセクションがあるコンテンツの見出しのようなものに役に立ちます。

    1. Chapter One
        a. Section One
        b. Section Two
        c. Section Three
    2. Chapter Two
    3. Chapter Three

コードで示すと、最初のリストの項目の内側にネストされたリスト全体を入れることになります。コードはこのようになります。

``` html
<ol>
  <li>Chapter One
    <ol style="list-style-type: lower-alpha;">
      <li>Section One</li>
      <li>Section Two </li>
      <li>Section Three </li>
    </ol>
  </li>
  <li>Chapter Two</li>
  <li>Chapter Three  </li>
</ol>
```

 注意して欲しいのは、CSSのプロパティの `list-style-type: lower-alpha` を使って、ネストされたリストを10進数字の代わりに小文字を並べている点です。

ネストされたリストはとても便利で、ナビゲーションメニューの基礎となっており、webサイトの階層的な構造を規定するための手っ取り早い方法になっています。またとても融通が利き、順序あり・順序なしリストどちらでも、順序あり・順序なしリストの項目を内側にネストできます。順序ありリストの内側に順序なしリストをネストさせた例が、上記の「リストのタイプを選ぶ 」にあります。

理屈の上では、好きなレベルだけリストをネストすることができますが、実際はあまりに深くネストしてしまうと混乱をきたします。とても大きなリストなら、コンテンツを分割し見出しを付けてリストを分けるか、さらにページに分割するかした方がもっと良くなるでしょう。 経験則では、3レベル以上に深くしないことです。

## <span>結論</span>

この文書では、HTMLのリストの様々なタイプがどのように使われ、コーディングされるかを見てきました。基本的なリストのオプションも調べました。 HTMLのリストの体裁や振る舞い修正する具体的な情報がさらに必要なら、[Styling lists and links](/guides/Styling_lists_and_links) を見てください。

## <span>See also</span>

### <span>External resources</span>

-   [A List Apart: Taming Lists](http://www.alistapart.com/articles/taminglists/)
-   [W3C CSS2: list-style-type definition](http://www.w3.org/TR/REC-CSS2/generate.html#lists)

### <span>練習問題</span>

-   3つのタイプのHTMLリストとは何か?
-   どのような時にそれぞれのリストを使うか? どうやって選ぶのか?
-   どうやってリストをネストするのか?
-   リストを整形するのに、なぜHTMLよりもCSSを使うのか?
