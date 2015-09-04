---
title: ja
tags:
  - Guides
  - HTML
summary: 'この文書では、HTMLでテキストコンテンツをマークアップする時に一番よく使用する要素について扱います。'
uri: 'guides/html text/ja'
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'guides/html text/af'
    - 'guides/html text/ar'
    - 'guides/html text/ast'
    - 'guides/html text/az'
    - 'guides/html text/bcc'
    - 'guides/html text/bg'
    - 'guides/html text/br'
    - 'guides/html text/ca'
    - 'guides/html text/cs'
    - 'guides/html text/da'
    - 'guides/html text/de'
    - 'guides/html text/diq'
    - 'guides/html text/el'
    - 'guides/html text/eo'
    - 'guides/html text/fa'
    - 'guides/html text/fi'
    - 'guides/html text/fr'
    - 'guides/html text/gl'
    - 'guides/html text/gu'
    - 'guides/html text/he'
    - 'guides/html text/hu'
    - 'guides/html text/hy'
    - 'guides/html text/id'
    - 'guides/html text/it'
    - 'guides/html text/ka'
    - 'guides/html text/kk'
    - 'guides/html text/km'
    - 'guides/html text/ko'
    - 'guides/html text/ksh'
    - 'guides/html text/kw'
    - 'guides/html text/mk'
    - 'guides/html text/ml'
    - 'guides/html text/mr'
    - 'guides/html text/ms'
    - 'guides/html text/nl'
    - 'guides/html text/no'
    - 'guides/html text/oc'
    - 'guides/html text/pl'
    - 'guides/html text/pt'
    - 'guides/html text/pt-br'
    - 'guides/html text/ro'
    - 'guides/html text/ru'
    - 'guides/html text/si'
    - 'guides/html text/sk'
    - 'guides/html text/sl'
    - 'guides/html text/sq'
    - 'guides/html text/sr'
    - 'guides/html text/sv'
    - 'guides/html text/ta'
    - 'guides/html text/th'
    - 'guides/html text/tr'
    - 'guides/html text/uk'
    - 'guides/html text/vi'
    - 'guides/html text/yue'
    - 'guides/html text/zh'
    - 'guides/html text/zh-hans'
    - 'guides/html text/zh-hant'
    - 'guides/html text/zh-tw'

---
# HTMLのテキスト

## Summary

この文書では、HTMLでテキストコンテンツをマークアップする時に一番よく使用する要素について扱います。

**言語:**
:   **[English](/guides/html_text)**  • <span lang="es">[español](/guides/html_text/es)</span> • <span lang="ja">**日本語**</span>

## はじめに

この文章では、HTMLの基本を使って、ドキュメントの本文にあるコンテンツをマークアップさせます。

まず最初に、見出しや段落といった一般的な構造要素を見てから、長い引用やコードの埋め込み方を見ていきます。その後、短い引用と強調といったインラインのコンテンツを見て、最後に見栄えを整えるのに使用していた古いマークアップを簡単に調べます。

## スペース — 新たなる未知へ

テキストについて説明する前に、テキストの間にあるスペースについて話す必要があります。 HTMLドキュメントには、テキストを区切る「ホワイト・スペース」と呼ばれている、印刷されない文字があります。普通のスペース文字(キーボードのスペースバー)は一番なじみ深いですが、他にもタブやキャリッジリターン(もしくは改行)のような文字もあります。

HTMLでは、これらの文字が複数続いていると、ほぼ間違いなく1つのスペース文字として扱われます。このソースコードを考えてみてください。

``` {.html}
<h3>In   the
                beginning</h3>
```

 webブラウザがこれを解釈すると、下記と同じになります。

``` {.html}
<h3>In the beginning</h3>
```

`<pre>` 要素が使われた時だけは、当てはまりません。この件に関しては、後ほど議論します。

ホワイト・スペースの圧縮は、HTML作成の初心者の混乱の元になります。そういう初心者は、インデントを望み通りにするために、更にスペースを追加してテキストを伸ばそうとするかもしれません。文の間のピリオドの後にスペースを追加したり、段落の間に垂直スペースを挿入したりしてです。 HTMLは、意味を表すための言語であって、形式を表すための言語ではないことを忘れないでください。視覚的なレイアウトは、HTMLのソースで実現するのではなく、CSSを用いて実現するようにしてください。

## ブロック要�

「ブロック要素」は、要素の前後で強制改行するものを指します。 このセクションでは、一般的なブロック要素の文法と使い方について見ていくことにします。

### ページセクションの見出し

webコンテンツの各部で、見出しを適切に設ける必要があります。

HTMLでは、見出しに6つのレベルを定義しています：`<h1>` と `<h2>`、 `<h3>`、`<h4>`、`<h5>`、`<h6>` です(重要なものから順に)。一般的には、`<h1>` がページの最も重要な見出しです。 ページをセクションに分けて構成するためには、`<h2>` を使うことになります。そして、`<h3>`は、サブセクションを設ける時に使用する等々です。

ドキュメントの構成を表現するために、見出しのレベルを利用することは重要です。レベルを飛び越したり、間違って異なるレベルをネストさせてはいけません。見出しのレベルでドキュメントの構成を表せば、スクリーンリーダーやインデックスを作成するボットのような自動化したプロセスが、ドキュメントをより理解できるようになります。さらに詳しい情報は [この文書](http://www.accessibilitytips.com/2008/03/10/avoid-skipping-header-levels/) を見てください。

見出しの正しい構成例は、テンプレートとしてこの文書で利用しています。

``` {.html}
<h1>HTMLでテキストベースのコンテンツをマークアップする</h1>
<h2>はじめに</h2>
<h2>スペース &mdash; 新たなる未知へ</h2>
<h2>ブロック要素</h2>
<h3>ページセクションの見出し</h3>
<h3>段落について全般</h3>
<h3>他の情報源を引用する</h3>
<h3>整形済みテキスト</h3>
<h2>インライン要素</h2>

[等々]
```

### 段落について全般

「段落」は、大部分のドキュメントにおいて最も重要な構成要素です。HTMLでは、段落は `<p>` 要素で表します。例えば、下記のようになります。

``` {.html}
<p>This is a very short paragraph. It only has two sentences.</p>
```

 段落にはいくつでもテキストが入ります。文字1つから数千もの単語まで可能ですが、書き物をする上での慣習的なの感覚から、文はいくつか入れるのが一般的です。 しかし、`<p>` を使い過ぎないでください。コンテンツがリストや見出し、リンクなどの特定のタイプのものなら、目的に合ったふさわしい要素がたくさんあります。

### 他の情報源を引用する

記事やブログの投稿、参考文献といったドキュメントは、別のドキュメントからテキストのセクションを引用することがよくあります。これを「ブロック引用」と言います。 HTMLでは、このたぐいの引用を `<blockquote>` 要素を使ってマークアップします。

技術的には `<blockquote>` 要素に、その他の要素で囲まれていない生のテキストを直接入れられます。しかしそれはよくないパターンで、おそらくそのコードは検証を通りません。 そうはしないで、`<blockquote>` の内に他の要素をネストしてください。別の情報源から引用する時には、同じ種類の要素を使うようにしてください。テキストの段落を引用するなら段落タグを使用し、項目リストを引用するならリストタグを使用する、というように。

必要なら、引用した情報源を `cite` 属性を使って下記のように表示できます。

``` {.html}
<p>HTML 4.01 is the only version of HTML that you should use
when creating a new web page, according to the
specification:</p>
<blockquote cite="http://www.w3.org/TR/html401/">
<p>This document obsoletes previous versions of HTML 4.0,
although W3C will continue to make those specifications and
their DTDs available at the W3C website.</p>
</blockquote>
```

 デフォルトとユーザー定義のスタイルにもよりますが、上記のコンテンツはブラウザでは下記のようにレンダリングされるでしょう。

HTML 4.01 is the only version of HTML that you should use when creating a new web page, according to the specification:

> This document obsoletes previous versions of HTML 4.0, although W3C will continue to make those specifications and their DTDs available at the W3C website.

`cite` 属性は、実のところその場では何もしないことを忘れないでください。しかし、引用そのものとして同じページ位置でその引用の情報源を記録しておくのに便利です。

### 整形済みテキスト

サンプル・コードのように、書式設定やホワイト・スペースを保つ必要があるなら、「整形済み」要素 `<pre>` を使ってマークアップしてください。 下記の例は、Perl プログラミング言語で書かれたコードのスニペットを挙げています。

``` {.html}
<pre><code class="language-perl">
# read in the named file in its entirety
sub slurp {
  my $filename = shift;
  my $file     = new FileHandle $filename;

  if ( defined $file ) {
    local $/;
    return <$file>;
  }
  return undef;
};
</code></pre>
```

 ブラウザでは、そのスニペットはホワイト・スペースを含め、書かれた通りにレンダリングされます。

    <code class="language-perl">
    # read in the named file in its entirety
    sub slurp {
      my $filename = shift;
      my $file     = new FileHandle $filename;

      if ( defined $file ) {
        local $/;
        return <$file>;
      }
      return undef;
    };
    </code>

たいていのwebブラウザでは、整形済みとしてマークされたテキストを、ソースコードで見られるかのようにユーザーに表示します。普通は等幅(モノスペース)フォントを使って、タイプライターやプリンターから出てきたテキストの雰囲気になります。これは固定幅フォントしかなかった古いコンピュータの名残りですが、コードの例等ブラウザが変更を加えること無く表示するのがベストなコンテンツには、とても役に立ちます。

注意：`<code>` 要素は [Lesser-known semantic elements](/tutorials/lesser-known_semantic_elements) で扱っています。

## インライン要�

「インライン要素」は、前後で強制改行しない要素です。 このセクションでは、よく使うインライン要素の文法と使い方を見ていくことにします。

### 短い引用

普通の文や段落に入れる短い引用は、「引用」要素 `<q>` の中に入れます。`<blockquote>` と同様、引用の情報源を示す `cite` 属性を入れられます。

短い引用は、普通は周りに引用符を付けてレンダリングされるはずです。 [HTML specification](http://www.w3.org/TR/html401/struct/text.html#h-9.2.2.1) によると、 引用符がきちんとネストし、引用文字が使用しているドキュメントの言語にふさわしいように、ユーザーエージェントが挿入します。

`lang` 属性と連携して動作する `<q>` の例を挙げます。

``` {.html}
<p>This did not end well for me. Oh well,
<q lang="fr">c'est la vie</q>, as the French say.</p>
```

 ブラウザでは、この段落は下記のようにレンダリングされるでしょう(欧州の引用文字であることに注意)：

This did not end well for me. Oh well, “c'est la vie”, as the French say.

### 強調

HTMLには、強調をする要素が4つあります。強調とは、周りのコンテンツから特定のテキストを目立たせる方法です。 ブラウザでは、テキストをボールドにしたり、イタリックにしたりするのが普通です。 スクリーンリーダーでは、別の音声や別の聴覚効果を用いることになります。

#### \<em\>

強調で文の意味を微妙に変えるには、「強調」要素 `<em>` を使います。このような感じです。

``` {.html}
<p><em>Please</em> remember to unplug the kettle at night.</p>
```

 たいていのブラウザは `<em>` をイタリックのテキストにレンダリングします。

*Please* remember to unplug the kettle at night.

#### \<i\>

`<i>` 要素は、HTML4では「イタリック」にしたい場合に使われましたが、これはよくないやり方です。というのは、意味づけをするというよりも見栄えのための要素だからです。つまり、その要素の意味が何なのかではなく、どのように見えるかを表現しているだけだからです(この種の要素についてのさらに詳しい話は後述します)。しかし、HTML5では、`<i>` の意味を見直しました。そこでは、「他の部分と異なる声や感情、あるいは普通の文章との違いを表すテキストの範囲を示します。例えば、分類学上の名称や専門用語、別の言語の慣用句、心の中で考えたこと、船名、そして印刷で普通イタリックで表現する文章が挙げられます」とあります。

これは少し分かりづらいので、`<i>` が適切なところを例にしてみます。

``` {.html}
<p>As we sailed into port, we spied the <i>Black Pearl</i> moored at the dock.</p>
<p>She really does add that little bit of <i lang="fr">je ne sais quoi</i>.</p>
```

 ブラウザで、望んだ通りにレンダリングされます。

As we sailed into port, we spied the *Black Pearl* moored at the dock.

She really does add that little bit of *je ne sais quoi*.

#### \<strong\>

「重要」要素 `<strong>` はコンテンツで特に重要なところを示します。周りのコンテンツよりも大切であることを示しています。例えば下記のようにです。

``` {.html}
<p>There are twenty different species living inside this enclosure.
<strong>Warning! Do not feed them: they will eat your shoes.</strong></p>
```

 たいていのブラウザは、`<strong>` をボールドのテキストにレンダリングします。

There are twenty different species living inside this enclosure. **Warning! Do not feed them: they will eat your shoes.**

#### \<b\>

`<i>` と同様に、「ボールド」要素 `<b>` は、使用するのがはばかられていました。というのは、コンテンツの意味ではなく見栄えを表現していたからです。そのため、HTML5でこの要素は見直され、現在では「他のテキストと体裁上の違いを表現したもので、意味の重要さを表現したものではありません」となっています。この例のように、プロダクトレビューやドキュメントのアブストラクトの中で、一番目立たせたい単語に使用することを検討してみて下さい。

``` {.html}
<p>In this article, Chris Mills will show you how to combine <b>HTML5</b>, <b>CSS3</b>, <b>coloured card</b>,
and <b>string</b> to create an attractive mobile for your child's bedroom.</p>
```

`<i>` と同様に、予想通りにレンダリングされます。

In this article, Chris Mills will show you how to combine **HTML5**, **CSS3**, **coloured card**, and **string** to create an attractive mobile for your child's bedroom.

#### 強調要素を組み合わせる

強調要素は、異なる種類のものを組み合わせてネストできます。例えば、一文丸々が強調されていて、さらにその中で重要な部分があったとすると、`<strong>` と `<em>` 要素を一緒にして、元よりもいっそう強調できます。

``` {.html}
<p><em>Please note: The kettle <strong>must</strong> be unplugged every evening, otherwise it will explode --
<strong>killing us all!</strong></em></p>
```

 ブラウザはその段落を下記のようにレンダリングするでしょう。

*Please note: The kettle **must** be unplugged every evening, otherwise it will explode -- **killing us all!***

### 細かい文字

「字を細かくする」要素 `<small>` は、元は見栄えを表すもう一つの要素でしたので、HTML4では使用をはばかられていましたが、HTML5で見直されました。普通のテキストよりも小さなフォントにする要素として使われていたものを、HTML5では正式に細かい文字をマークアップするのに使われるようになりました。例えば、法的な制約や免責事項、著作権情報、帰属表示、ライセンス情報などです。 例を挙げます。

``` {.html}
<p><small>This content is released under a
Creative Commons Attribution Share-alike license.</small></p>
```

 ブラウザでは、下記のようにレンダリングされます。

<small>This content is released under a Creative Commons Attribution Share-alike license.</small>

### 時刻が分かる

HTML5で新たに導入された「時刻」要素 `<time>` は、日時をテキスト中にマークアップするやり方です。日時を好きなように表示できますが、コンピュータで読み取れて整合性のとれたISO形式の日付も入れます。例は下記です。

``` {.html}
<p>I was born on the <time datetime="1978-06-27">27<sup>th</sup> June 1978</time>.</p>
```

 開閉タグの間には何でも入れられますので、どんな方法でも書くことができますが、日付を正確にしてコンピュータが読み取れるようにしておいてください。

``` {.html}
<p><time datetime="1978-06-27">June 27 1978 - my birthday</time>.</p>
```

 日付に時刻を追加することもできます。ISO形式の文字列の後に大文字のTを加えてから、24時間形式で時刻を入れます。<sup>[[1]](#cite_note-1)</sup>

``` {.html}
<p><time datetime="1978-06-27T21:00">9pm on my birthday</time>.</p>
```

 もしくは、下記のように望みの時刻をそのまま記述できます。

``` {.html}
<p><time datetime="21:00">9pm</time>.</p>
```

 ただし、現在「August 2011」や「2011」のような、任意の日付は記述できない点に注意してください。

また、時刻の値に続けて秒数(さらにもう一つのコロンの後)やミリ秒数(ピリオドの後)、タイムゾーン・オフセット(ダッシュの後)を追加できます。下記が例です。

``` {.html}
<p><time datetime="1978-06-27T21:00:00.006-08:00">9pm and 6 milliseconds
on my birthday, in Pacific standard time</time>.</p>
```

<sup>[[2]](#cite_note-2)</sup> Finally, you can also add a *publication date* attribute `pubdate` to a `<time>` element, to specify that the datetime value represents when the content was published:

``` {.html}
<p>Published on <time datetime="2011-07-20" pubdate>July 27<sup>th</sup> 2011</time>.</p>
```

## 見栄えのための要素 — 使わないこと

`<i>` や `<b>` 、`<small>` に加えて、HTML4の仕様には、まさに見栄えのための要素が他にもあります。その要素は、コンテンツが何を意味するかではなく、要素中でどのように見えるかについてに特化しています。 これらの要素を使用することは推奨されておらず、HTML5の仕様からはほとんど削除されました。

ここでは手短に説明していきます。ただし注意して欲しいのは、歴史的な関心から説明しているということです — 現在のwebページには決して使用しないでください。こういった効果を実現したいのなら、CSSを使う必要があります。

### \<font face="..." size="..."\>

「font」要素は、デフォルトとは違うフォントを使ってレンダリングすべきテキストを指定します。代わりにCSSを使ってください。

### \<strike\>

「strike」要素は、線でテキストを消し込む指定をします。代わりにCSSを使ってください。

### \<u\>

「u」要素は、テキストに下線を指定します。代わりにCSSではこれは実現できません。というのは、読者のほとんどは下線をハイパーリンクと見なすからです。言うまでもありませんが、下線はハイパーリンクではないので、クリックしても何も起こりません — 読者がイライラするのを除けば。

### \<tt\>

「tt」要素は、テキストを「テレタイプ」もしくは等幅フォントで表示するように指定します。代わりにCSSを使ってこの効果を実現するには、ブロックコンテンツなら `<pre>` 、インラインコンテンツなら`<code>` という意味を表す要素を使います。

### \<big\>

「big」要素は、テキストをより大きなフォントでレンダリングする時に指定します。

## 結論

この文書で、HTMLのテキストをマークアップする基本である、見出しと段落、引用、コード、各種の強調要素を見てきました。これらの考え方をよく理解したなら、このシリーズの他のチュートリアルに進んでください。そこには、リストや画像、リンク、テーブル等があります。

1.  <span class="mw-cite-backlink">[↑](#cite_ref-1)</span> <span class="reference-text">訳注：HTML5の勧告では、日付と時刻の区切りに大文字の「T」に加えて「スペース」が使用できるようになりました。</span>
2.  <span class="mw-cite-backlink">[↑](#cite_ref-2)</span> <span class="reference-text">訳注：下記に説明されている「publication date」属性(記事の公開日時を表す)は、HTML5の勧告では採用されなかったので、翻訳していません。同等の機能をMetadataを使って実装する例が [W3Cの`<time>`要素の解説](http://momdo.github.io/html5/text-level-semantics.html#the-time-element) にありますので、参考になさってください。</span>
