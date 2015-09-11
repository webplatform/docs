---
title: blockquote
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/blockquote)'
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
lang: ja
notes:
  - 'Add Category, Parent, Children and Compatibility information.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLQuoteElement](/dom/HTMLQuoteElement)'
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
summary: 'blockquote要素は拡張された引用を表します。'
tags:
  - Markup
  - Elements
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/footer/ja
    - html/elements/cite/ja
    - html/attributes/cite/ja
uri: html/elements/blockquote/ja

---
## <span>Summary</span>

blockquote要素は拡張された引用を表します。

## <span>Overview Table</span>

[DOM Interface](/dom/interface)
:   [HTMLQuoteElement](/dom/HTMLQuoteElement)

### <span>導入</span>

**blockquote**要素は別のソースから引用したコンテンツであることを示します。追加で[**footer**](/w/index.php?title=html/elements/footer/ja&action=edit&redlink=1)や[**cite**](/w/index.php?title=html/elements/cite/ja&action=edit&redlink=1)要素で引用元を記載したり、注釈や省略のような変更なども一緒に示すことがあります。

**blockquote**要素の中に出典元や変更を記載したい場合、一つだけなら、[**cite**属性](/w/index.php?title=html/attributes/cite/ja&action=edit&redlink=1)に記載することができます。

<dl>
<dd>
注: ブログのコメントのような複数人から投稿されたコンテンツでページが構成されている場合、同じページ上の他の人が書いたコメントを'出典元'とする事ができます。

</dd>
</dl>
cite属性を記載する際は正しいURLを設定しなければいけません。引用元のリンクを対応させるには、属性の値が、「要素と関連する」と解釈される値でなくてはいけません。ユーザエージェントは引用元リンクを辿ることを許可しますが、主に読み手に不要な私的な利用（引用サイトの利用統計を収集するサーバサイドスクリプト等）のために使われます。

cite属性は要素の引用コンテンツの帰属を反映しなければいけません。

## <span>HTML属性</span>

-   `cite` = 有効なURL（前後にスペースがある場合、取り除かれて扱われます。）
    引用元のアドレスを指定します。

## <span>Examples</span>

``` html
<!-- この例は引用をインデントさせて目立たせるためにblockquote要素を使用しています。: -->
<p>彼は
<blockquote cite="http://www.example.com">"やあ、皆さん!"</blockquote>と言いました。
```

**blockquote**要素は別のソースから引用したコンテンツであることを示します。追加で**footer**や**cite**要素で引用元を記載したり、注釈や省略のような変更なども一緒に示すことがあります。例えば、英語では慣例的に省略を示す場合、角括弧を使用します。"フレッドはクラッカーを食べた。そして彼はリンゴと魚が好きだと言った。"という文章を考えましょう。これは以下のように引用されます。

``` html
<blockquote>
 <p>[フレッド]は[...]魚が好きだといった。</p>
</blockquote>
```

**blockquote**の中で、引用されたテキストと注釈とを明確に区別するために引用符が使われます。

``` html
<!-- 例えば、著者が文中で注釈を入れた場合です。 -->
<figure>
 <blockquote>
 "かの怪物、習慣というものは、感覚を食い尽くし、
  悪魔のように振舞うが、"<abbr title="et cetera">などなど</abbr>（ここはFirst Folioの文章ではありません）
 "なんという堕落だろう！
  結婚のとき手に手をとって、
  高潔な愛をもって誓ったこのわしを無みし、
  はるかに品位の劣る悪党に身を任せるとは。"
 </blockquote>
 <footer>
 — <cite class="title">シェイクスピアマニュアル</cite> 著：<cite class="author">フレデリク・ガード・フレーイー</cite>,
 19ページ (in Google Books)
 </footer>
 </figure>
<!-- 注: 上記の例では、引用元はfigure要素内のfooter要素に含まれており、引用とともに引用についての情報を関連付けています。今回のケースでは、キャプションではなく、引用元を含んでいるため、figcaption要素は使っていません。 -->
```

引用の帰属は**blockquote**要素に記述しても良いですが、**cite**要素か**footer**要素に記述すべきです

``` html
<!-- 例えば、ここでは引用したテキストのあとのfooterに帰属を記載し、帰属と引用物の関係を明確にしています。 -->
<blockquote>
 <p>我々は無神論者である、ということを私は強く主張する。 私の信ずる神は
 あなたの信ずる神よりもひとつ少ないというだけだ。あなたが他の神々を拒絶する理由を理解すれば、
 なぜ私があなた方を拒絶するか理解できるだろう。</p>
 <footer>— <cite>ステファン・ロバート</cite></footer>
 </blockquote>
```

``` html
<!--  ここでは引用したテキストの最終行の<cite>要素に帰属を記述しています。著者のリンクも含まれていることに注意してください。 -->
<blockquote>
 人々は、その産物から自分自身を認識する。
 自動車やhi-fi装置、乱平面住宅、台所用品などに自身の魂を見出す。
 — <cite><a href="https://ja.wikipedia.org/wiki/ヘルベルト・マルクーゼ">ヘルベルト・マルクーゼ</a></cite>
 </blockquote>
```

``` html
<!-- ここでは引用文のあとのフッターで帰属と参照元のメタデータをMicrodata構文で記述しています。（※RDFA Liteでマークアップするのと同義です。） -->
<blockquote>
  <p>... 彼女は”口説く”の代わりに"恋する"という言葉が使われている供述書には一切署名をしなかった。その違いは彼女にとって極めて重要な意味があった。それは彼女の元夫がいつも口説文句をささやいているのに、本心では恋をしたことなど一度もなかった、という離婚理由にある。</p>
  <footer itemscope itemtype="http://schema.org/Book">
    <span itemprop="author">ハインリヒ・ベル</span>,
    <span itemprop="name">カタリーナ・ブルームの失われた名誉</span>,
    <span itemprop="datePublished">1974年1月1日</span>
  </footer>
</blockquote>
<!-- 注: 引用元から引用してきた要素をマークアップする方法として正しい方法というものはありません。引用元について記述するために'''blockquote'''の中にフッターやcite要素が含まれる場合、例えばclass属性を使って仕組みを拡張し、メタデータと共に引用元の起源を注釈するという -->
```

``` html
<!-- この例では、引用元をcite要素に記述し、class属性を使って注釈しています。 -->
<blockquote>
  <p>私のお気に入りの本は<cite class="from-source">スウィム・トゥ・バーズ亭にて</cite>です。</p>
  <footer>- <cite>Mike[tm]Smith</cite></footer>
</blockquote>
```

以下の例は上記と異なる方法で帰属を記しています。

``` html
<!-- ここではfigure要素とキャプションをつなぐためにblockquote要素を使用しています。 -->
<figure>
 <blockquote>
  <p>真実とは時に不可解なものだ。真実がすべきことをすることもあるだろう。直感に反することもあるだろう。心の奥底にある偏見と矛盾することもあるだろう。真実だと思い込んでいることと一致しないこともあるだろう。しかし、私達の選択によって何が真実かが決まるわけではない。我々のもつ理論よって真実にたどり着くことは絶対にない。真実に極限まで近づくだけである。そして発見するのは新たな、そして広大な、未発見の可能性の海である。巧みにデザインされた実験が鍵である。</p>
 </blockquote>
 <figcaption><cite>カール・セーガン</cite><cite>懐疑的な尋問者</cite> 19巻1号(1995年1-2月)より"<cite>神秘と懐疑論</cite>"</figcaption>
</figure>
```

``` html
<!-- 次の例は引用文と一緒に引用元を記しています。-->
<p>次の作品はふさわしく<cite>ソネット130</cite>と名付けられました。:</p>
<blockquote cite="http://quotes.example.org/s/sonnet130.html">
  <p>我が恋人の目に太陽の輝きはない、<br>
  彼女の唇より珊瑚のほうがずっと赤い、<br>
  ...
```

``` html
<!-- この例ではあるユーザがフォーラムの投稿に返信する際の例です。article要素は投稿ごとに使われ、スレッドをマークアップしています。 -->
<article>
 <h1><a href="http://bacon.example.com/?blog=109431">Bacon on a crowbar</a></h1>
 <article>
  <header><strong>t3yw</strong> 12 points 1 hour ago</header>
  <p>I bet a narwhal would love that.</p>
  <footer><a href="?pid=29578">permalink</a></footer>
  <article>
   <header><strong>greg</strong> 8 points 1 hour ago</header>
   <blockquote><p>I bet a narwhal would love that.</p></blockquote>
   <p>Dude narwhals don't eat bacon.</p>
   <footer><a href="?pid=29579">permalink</a></footer>
   <article>
    <header><strong>t3yw</strong> 15 points 1 hour ago</header>
    <blockquote>
     <blockquote><p>I bet a narwhal would love that.</p></blockquote>
     <p>Dude narwhals don't eat bacon.</p>
    </blockquote>
    <p>Next thing you'll be saying they don't get capes and wizard
    hats either!</p>
    <footer><a href="?pid=29580">permalink</a></footer>
    <article>
     <article>
      <header><strong>boing</strong> -5 points 1 hour ago</header>
      <p>narwhals are worse than ceiling cat</p>
      <footer><a href="?pid=29581">permalink</a></footer>
     </article>
    </article>
   </article>
  </article>
  <article>
   <header><strong>fred</strong> 1 points 23 minutes ago</header>
   <blockquote><p>I bet a narwhal would love that.</p></blockquote>
   <p>I bet they'd love to peel a banana too.</p>
   <footer><a href="?pid=29582">permalink</a></footer>
  </article>
 </article>
</article>
```

``` html
<!-- この例ではp要素をblockquote要素に入れずにごく短い引用文を記述しています。 -->
<p>彼は以下のように”レッスン”を始めた。</p>
<blockquote>メリットを得られるように譲歩することはもちろん、
相手側が非を認めることを前提としないこと</blockquote>
<p>彼は似たような言葉を続けたあと、以下のように締めくくった。</p>
<blockquote>最後に、どこかで交渉が崩壊する脅威に対して準備し、
可能性を盾に脅されないこと。</blockquote>
<p>今回はこれらの点について議論していこう...
```

## <span>Notes</span>

### <span>備考</span>

-   後のセクションで、会話の表し方の例が示されるかもしれませんが、**cite**と**blockquote**はそのような目的にはふさわしくありません。

## <span>Related specifications</span>

[HTML 5.1](http://www.w3.org/TR/html51/grouping-content.html#the-blockquote-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/grouping-content.html#the-blockquote-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/struct/text.html#edef-BLOCKQUOTE)
:   W3C Recommendation

## <span>See also</span>

### <span>Related pages (internal)</span>

-   `q`
-   `cite`
