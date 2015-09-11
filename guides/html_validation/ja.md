---
title: HTMLの検証
lang: ja
notes:
  - 'まだ体裁が変かも。'
summary: この文書では検証の概要を紹介し、HTMLを検証するW3Cバリデータの使い方を説明します。
tags:
  - Guides
  - HTML
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'guides/html validation/af'
    - 'guides/html validation/ar'
    - 'guides/html validation/ast'
    - 'guides/html validation/az'
    - 'guides/html validation/bcc'
    - 'guides/html validation/bg'
    - 'guides/html validation/br'
    - 'guides/html validation/ca'
    - 'guides/html validation/cs'
    - 'guides/html validation/da'
    - 'guides/html validation/de'
    - 'guides/html validation/diq'
    - 'guides/html validation/el'
    - 'guides/html validation/eo'
    - 'guides/html validation/es'
    - 'guides/html validation/fa'
    - 'guides/html validation/fi'
    - 'guides/html validation/fr'
    - 'guides/html validation/gl'
    - 'guides/html validation/gu'
    - 'guides/html validation/he'
    - 'guides/html validation/hu'
    - 'guides/html validation/hy'
    - 'guides/html validation/id'
    - 'guides/html validation/it'
    - 'guides/html validation/ka'
    - 'guides/html validation/kk'
    - 'guides/html validation/km'
    - 'guides/html validation/ko'
    - 'guides/html validation/ksh'
    - 'guides/html validation/kw'
    - 'guides/html validation/mk'
    - 'guides/html validation/ml'
    - 'guides/html validation/mr'
    - 'guides/html validation/ms'
    - 'guides/html validation/nl'
    - 'guides/html validation/no'
    - 'guides/html validation/oc'
    - 'guides/html validation/pl'
    - 'guides/html validation/pt'
    - 'guides/html validation/pt-br'
    - 'guides/html validation/ro'
    - 'guides/html validation/ru'
    - 'guides/html validation/si'
    - 'guides/html validation/sk'
    - 'guides/html validation/sl'
    - 'guides/html validation/sq'
    - 'guides/html validation/sr'
    - 'guides/html validation/sv'
    - 'guides/html validation/ta'
    - 'guides/html validation/th'
    - 'guides/html validation/tr'
    - 'guides/html validation/uk'
    - 'guides/html validation/vi'
    - 'guides/html validation/yue'
    - 'guides/html validation/zh'
    - 'guides/html validation/zh-hans'
    - 'guides/html validation/zh-hant'
    - 'guides/html validation/zh-tw'
uri: 'guides/html validation/ja'

---
## <span>Summary</span>

この文書では検証の概要を紹介し、HTMLを検証するW3Cバリデータの使い方を説明します。

<table class="nmbox languages" style>
<tr>
<th class="mbox-image" style>
**言語:**

</th>
<td class="mbox-text">
**[English](/guides/html_validation)**  • <span lang="ja">**日本語**</span>

</td>
</tr>
</table>

## <span>はじめに</span>

HTMLを数ページ書き上げ、うまく表示されたようでも、そのページに全く問題がないわけではありません。何が悪いのかを見つける最善の方法はなんでしょうか? また、これらのページ(今後書くことになるページ)が、ブラウザの種類に関わらず、確実に正しくエラー無しで表示される最善の方法は何でしょうか?

答えは、検証(バリデーション)することです! W3Cをはじめ、たくさんのツールが用意されており、サイトのコードを検証できます。利用できる最も一般的なバリデータは、下記の通りです。

-   [Validator.nu](http://html5.validator.nu/): HTML5やARIA、SVG 1.1、MathML 2.0を検証できる新しいスタイルのバリデータ。ドキュメント全体をチェックし、マークアップがドキュメントタイプに合致していないところを指摘してくれます(つまりエラーがある箇所)。HTML5を使用しているなら、こちらを強くおすすめします。
-   [The W3C MarkUp Validator](http://validator.w3.org/): チェックしたいドキュメントが(X)HTMLのドキュメントタイプなら、こちらを。適切にマークアップをチェックしてくれます。HTML4やXHTML1.xのドキュメントタイプならば、こちらをおすすめします。HTML5も検証しますが、議論の余地はあるものの、validator.nuの方が最新の情報が得られます。
-   [The W3C Link Checker](http://validator.w3.org/checklink): ドキュメントをチェックし、リンク全てが切れていないかテストします(例えば、`<href>` の値が実際に存在しているリソースを指し示しているか)。
-   [The W3C CSS Validator](http://jigsaw.w3.org/css-validator/): CSS(もしくはHTML/CSS)ドキュメントをチェックし、CSSが仕様にのっとっているか検証します。

このドキュメントでは2番目のバリデータの使い方を扱い、マークアップの検証を実際に行い、バリデータがよく示す結果を説明します。

## <span>エラー</span>

— マークアップ言語を含む —コンピュータ・プログラミングにおいて、コードのエラーには大別して2つのタイプがあります。

-   シンタックスエラー — このエラーは、コンピュータが実行できなかったり、プログラムを正しくコンパイルできなかったりして、間違いを伴うのが一般的です(例えば、ブレースやパーレンがない)。
-   論理エラー — このエラーは、コードはシンタックス上は正しくても、意図した通りに動かない場合に起こります。

ほとんどのプログラミング言語では、最初のタイプのエラーを見落とすことはありません。そのコードは、コンパイルで蹴られるか、エラーが訂正されなければ実行できません。また、コンパイラはプログラマーにエラーとその行番号を警告するのが普通です。 このおかげで、論理エラーよりもシンタックスエラーの方が、発見して修正するのが簡単です。論理エラーは、「どうして思うように動かないんだ?」という頭を抱える状況になることが通例なので。検証は、ご推察通り、シンタックスエラーしか見つけられません。

HTMLは、手続き型プログラミング言語というよりも宣言型マークアップ言語ですが、シンタックスエラーは起こり得ます。 しかし、webページでのシンタックスエラーで、ブラウザがページを表示しないということはまずありません。webブラウザにおけるこの独特の寛容さが、webが急速に採用され、拡大していった最大の理由の1つです。タグを閉じるのを忘れてしまっても、普通はページが表示されるでしょう。

初めてのwebブラウザは、[WorldWideWeb](http://www.w3.org/People/Berners-Lee/WorldWideWeb.html) (Tim Berners-Lee氏作成)です。このブラウザはエディターでもあり、作成者がHTMLを学ぶことなくwebページを作成できました。このエディターが作るHTMLは正しくありませんでしたが、現在でもブラウザ全てに当てはまる重要な定型を確立しました。— それは、ユーザーがコンテンツにアクセスできることが、より重要であるとしたことです。エラーを理解できなかったり、エラーを訂正する立場でなかったりする人々に対して、エラーを示すことよりもです —

## <span>検証とは?</span>

webブラウザは、webページにある正しくないコードを受け付け、作成者の意図をできるだけ活かすようにレンダリングしますが、HTMLが正しく書かれているか否かをチェックできます。実際にそうしてみるのは下記を見れば分かるように、よい考えです。私たちはこれをHTMLを「検証する」とします。

検証プログラムは、webページにあるHTMLコードを[doctype](/guides/doctypes_and_markup_styles)に付随するルールと比較し、もしルールが守られていないなら、どこが守られていないのかを教えてくれます。

## <span>なぜ検証する?</span>

webページがブラウザでよさそうに見えれば、検証しなくても問題ないと思っているweb開発者がいます(「美は機能に宿る」とよく言われています)。彼らは検証を理想的な目標とみなしていて、白黒はっきりした問題とはみなしていません。

この考え方には一理あります。HTML4の仕様は完全ではありませんし、— [順序付きリストを１より大きい数値ではじめる](http://www.w3.org/wiki/HTML_lists#Beginning_ordered_lists_with_numbers_other_than_1) — のように、間違いとは言えなくても、HTMLとしては正しくないものもあります。HTML5では、仕様上の問題が相当な数修正されています。この問題もそうです。それでも、望み通りにページをレンダリングするために、検証を打ち切らなければいけない状況になるかもしれません。格言にもある通り、「ルールを学べば、それらを正しく破る方法が分かる」です。

自分がHTMLを書いた時、それを検証することを納得するに足る理由は2つあります。

-   完璧な人はいないし、コードもまた同じです。間違いは誰でも犯します。その間違いを取り除けば、webページの質はもっと向上します(つまり、より確実に動作する)。
-   ブラウザが変わるのは、まぎれもない事実です。今後は、ブラウザが正しくないコードをパースする時、許容幅が広がるのではなく、狭まる可能性があります。

検証は、バグが「変わっていて気付けない」かつ直し難い形で現れる時に対する、早期警戒システムです。 ブラウザが正しくないHTMLに出くわすと、意図することは何なのか、目星をつけなければいけません。— 別のブラウザは、違う答えを見つけ出すかもしれません。

## <span>ブラウザが異なれば、正しくないHTMLの解釈も変わる</span>

正しいHTMLが、ブラウザの作り手とあなたとの唯一の取り決め事です。HTMLの仕様には、どのようにドキュメントを書くべきで、そのドキュメントをどのように解釈すべきかが、書いてあります。最近になって、正しいコードを書いていれば、メジャーなブラウザなら同じ方法でコードを解釈するはず、というところまで、ブラウザの標準準拠がたどり着きました。これは、少なくともHTMLの場合にほぼ間違いなくあてはまりますが、他の標準については、サポートの色々な面で事情が多少異なります。

しかし、ブラウザに正しくないコードを渡した時、何が起こるでしょう? 答えは、ブラウザのエラー処理が働いて、コードを何とか対処します。「このコードは正しくありません。なので、このコードをエンドユーザーにどう表示したらいいですか?」と言う感じです。

これは素晴らしいことではないでしょうか? ページにあるエラーをいくつかそのままにしておくと、ブラウザはギャップを埋めてくれるでしょう! ただ、ブラウザ毎に違うことをします。下記のコードを考えてください。

``` html
<p><strong>このテキストはボールドのはず</p>
<p>このテキストはボールドになる? レンダリングした時、HTMLはどう見える?</p>

<p><a href="#"></strong>このテキストはリンクのはず</p>
<p>このテキストはリンクになる? レンダリングした時、HTMLはどう見える?</p>
```

 エラーの内容は、(1)「strong」要素が誤って重複し、ブロック要素に渡ってネストされている、(2)「anchor」要素が閉じていない、です。

-   Operaは、後続の要素を「bold」要素の子供とします。
-   Firefoxは、段落間に「bold」要素を余分に追加します。その要素はマークアップには示されていません。
-   Internet Explorerは、リンクを作る「anchor」要素の外側に「このテキストはリンクのはず」というテキストを置きます。

この例のオリジナルバージョンは、Hallvord Steen氏の文書 [Same DOM errors, different browser interpretations](http://blog.teamtreehouse.com/same-dom-errors-different-browser-interpretations) で見られます。 — HTMLのエラーの処理についてより深く知りたいなら、これを読んでください。デバッグツールについても情報があります。

ブラウザ毎に異なる処理に欠陥があるわけではありません。いずれも、正しくないコードとのギャップを埋めようとしているからです。要するに「可能な限り、ページにある正しくないマークアップを回避する」です。

注意すべきなのは、HTML5がこの問題をある程度まで修正している点です。HTMLの歴史の中で初めて、ブラウザが正しくないマークアップをどのように扱うべきか、ということを定義しました。しかし、この文書を書いている時点では、このHTML5のエラー処理がブラウザに広まっているわけではありませんので、まだこれに頼れません。

## <span>ページの検証方法</span>

これまで、HTMLを検証する背景となる理論を探ってきましたので、次はやさしい話をしましょう。— 実際の検証についてです。そう、これは完璧に正確ではありません。URLをバリデータに入力し、ページが正しい否かを見るのは難しくありません。悪いところを何とかして、エラーを修正することが簡単でないこともあります。それは、エラーメッセージが時として謎めいているからです。それでは例をいくつか見ていきましょう。

このセクションで見ていく例は下記にあります。自由にお気に入りのエディターにコピー&ペーストしてください。

``` html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en">
  <head>
    <title>Validating your HTML</title>
  </head>
  <body>
    <h2>The tale of Herbet Gruel</h2>
    <p>Welcome to my story. I am a slight whisp of a man, slender and fragile, features wrinkled and worn, eyes sunken into their sockets like rabbits cowering in their burrows. The <em>years have not been kind to me</em>, but yet I hold no regrets, as I have overcome all that sought to ail me, and have been allowed to bide my time, making mischief as I travel to and fro, 'cross the unyielding landscape of the <a href="http://outer-rim-rocks.co.uk" colspan="3">outer rim</a>.</p>

    <h3>Buster</h3>
    <p>Buster is my guardian angel. Before that, he was my dog. Before that, who knows? I lost my dog many moons ago while out hunting geese in the undergrowth. A shot rang out from my rifle, and I called for Buster to collect the goose I had felled. He ran off towards where the bird had landed, but never returned. I never found his body, but I comfort myself with the thought that he did not die; rather he transcended to a higher place, and now watches over me, to ensure my well-being.

    <h3>My possessions</h3>
    <p>A travelling man needs very little to accompany him on the road:</p>
    <ul>
      <li>My hat full of memories</li>
      <li>My trusty walking cane</li>
      <li>A purse that did contain gold at one time</li>
      <li>A diary, from the year 1874<li>
      <li>An empty glasses case</li>
      <li>A newspaper, for when I need to look busy</li>
    </ul>
  </body>
```

 この簡単なページには、見出しが3つと段落が3つ、ハイパーリンクが1つ、箇条書きリストが1つあります。検証に対するルールセットとして、XHTML 1.0のstrictなドキュメントタイプを使用しています(XHTML 1.0のstrictの方が、HTML5ドキュメントタイプよりもエラーを返す可能性が高いため使用)。ドキュメントにはいくつかエラーがありますが、W3C HTMLバリデータを使って見つけだします。

### <span>W3C HTMLバリデータ</span>

[W3C online validator](http://validator.w3.org/) を新しいタブかウィンドウで開いてください。そうすれば、例を読み進めていきながら、バリデータとこの文書を行き来できます(Operaブラウザから直接W3Cバリデータでページを検証することもできます。右クリックして、「検証」オプションを選択します)。 <sup>[[1]](#cite_note-1)</sup>

トップ画面で、3つのタブが利用できるのに気付くでしょう。

-   URIによって検証する：インターネットで有効なページのアドレスを入力して検証できる
-   ファイルをアップロードして検証する：ローカルのHTMLファイルをアップロードして検証できる
-   直接入力して検証する：HTMLをウィンドウに直接貼り付けて検証できる

どの方法を使っても同じ結果が出るはずです。例のページをテストする一番簡単な方法は、この上の例のコードをすべてコピーし、3番目のタブに貼り付ける方法です。そうすると、Figure 1で見られる結果が返ってくるはずです。

![The results of validating the sample document is 11 errors](/assets/public/2/2b/html_validation_errors.png)

*Figure 1: サンプルのドキュメントを検証した結果 — 11個のエラー!*

これは厄介だと思われるかもしれませんが、そのドキュメントには11個もエラーは「ありません」と強調しておきます! 失望してはいけません — バリデータは、実際よりも多くのエラーを報告します。これは、カスケードしていると予測されるページのトップにおいてよく起こるエラーで、この後にさらに閉じていない要素や正しくないネストがあるかのように、後のエラーをバリデータが報告します。エラーメッセージが意味するところを、よく考えなければいけません。マークアップから疑いようのないエラーを洗い出し、トップから作業していきましょう。下記のTable 1には、ページを検証するために修正したエラーがすべて載っています。それとともに、何が悪いのかを解くプロセスと問題を解決するのに使った修正も載せてあります。

|エラーメッセージ|解決プロセス|修正したこと|
|:---------------|:-----------|:-----------|
|Line 8, Column 461: there is no attribute "colspan"|`colspan` 要素は存在し、それが正しいHTMLであることは分かっています。ではなぜ無いとしたのでしょう? 使うべきでない要素のところに、使ってしまったのでしょうか? 予想通り、間違っていました。— `<a>` 要素 のところです! 。|`colspan` 要素を `<a>` 要素から取り除きました。|
|Line 13, Column 7: document type does not allow element "h3" here; missing one of "object", "applet", "map", "iframe", "button", "ins", "del" start-tag. `<h3>My possessions</h3>`|これも、一見するとおかしく思えます。— the `<h3>` 要素は適切に閉じており、このコンテキストでの使用が認められています。このエラーメッセージは、すぐ近くに閉じていない要素が存在する、ということを理解しておいてください。|問題になっている見出しの上の行に、`<p>`タグを追加しました。|
|Line 19, Column 40: document type does not allow element "li" here; missing one of "ul", "ol", "menu", "dir" start-tag. `<li>A diary, from the year 1874<li>`|このエラーはかなり簡単です — エラーが示す行を見れば、`<li>` タグの閉じのスラッシュ (`/`)がないことが分かるでしょう。|問題になっている行に、閉じのスラッシュを追加しました。|
|Line 23, Column 9: end tag for "html" omitted, but OMITTAG NO was specified. `</body>`|これも簡単に修正できます。`<html>` タグがないという意味です。エラーメッセージの原因は、恐らく要素をうっかり閉じ忘れたことによるものです。|抜けている`</html>` 要素を追加しました。|

4つのエラーを修正すると残り7つはなくなり、望み通りバリデータは成功した旨のメッセージを表示します。Figure 2がそれです。

![A success message to say that all my errors have been fixed](/assets/public/2/2a/validatehtml2.gif)

「Figure 2: エラーがすべて修正されたことを伝える成功のメッセージ」

下記が訂正されたバージョンのコードです。お気に入りのエディターに自由にコピー＆ペーストしてください。

``` html
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en">
  <head>
    <title>Validating your HTML</title>
  </head>
  <body>
    <h2>The tale of Herbet Gruel</h2>
    <p>Welcome to my story. I am a slight whisp of a man, slender and fragile, features wrinkled and worn, eyes sunken into their sockets like rabbits cowering in their burrows. The <em>years have not been kind to me</em>, but yet I hold no regrets, as I have overcome all that sought to ail me, and have been allowed to bide my time, making mischief as I travel to and fro, 'cross the unyielding landscape of the <a href="http://outer-rim-rocks.co.uk">outer rim</a>.</p>

    <h3>Buster</h3>
    <p>Buster is my guardian angel. Before that, he was my dog. Before that, who knows? I lost my dog many moons ago while out hunting geese in the undergrowth. A shot rang out from my rifle, and I called for Buster to collect the goose I had felled. He ran off towards where the bird had landed, but never returned. I never found his body, but I comfort myself with the thought that he did not die; rather he transcended to a higher place, and now watches over me, to ensure my well-being.</p>

    <h3>My possessions</h3>
    <p>A travelling man needs very little to accompany him on the road:</p>
    <ul>
      <li>My hat full of memories</li>
      <li>My trusty walking cane</li>
      <li>A purse that did contain gold at one time</li>
      <li>A diary, from the year 1874</li>
      <li>An empty glasses case</li>
      <li>A newspaper, for when I need to look busy</li>
    </ul>
  </body>
</html>
```

## <span>結論</span>

ここでできることは、これくらいです。自分とコードについて、気を抜かず十分考えていてください。そして、検証は自分のページのドキュメントタイプが何であるか、によることをお忘れなく。

## <span>See also</span>

### <span>External resources</span>

-   [Opera Dragonfly](http://www.opera.com/dragonfly/) (built into Opera)
-   [General validation bookmarklet](https://www.squarefree.com/bookmarklets/validation.html)
-   [The Firefox web developer toolbar extension](http://chrispederick.com/work/web-developer/)
-   [The IE developer toolbar](http://www.microsoft.com/downloads/details.aspx?FamilyID=e59c3964-672d-4511-bb3e-2d5e1db91038&displaylang=en)
-   [Safari tidy](http://zappatic.net/safaritidy/)
-   [HTML tidy](http://tidy.sourceforge.net/)

### <span>練習問題</span>

-   正しくないHTMLをブラウザがパースすると何が起こりますか?
-   これについての問題は何ですか?
-   HTML 4のStrictなドキュメントタイプで検証済のドキュメントにあるフレームセットを使うと、エラーは発生しますか?

1.  <span class="mw-cite-backlink">[↑](#cite_ref-1)</span> <span class="reference-text">【訳注】現在のOpera(Ver 30.0.1835.59)では、組み込みの開発者用ツールで検証するようになっています。拡張機能(W3C Markup Validation Service)を追加すると、W3Cバリデータを利用できるようになります。</span>
