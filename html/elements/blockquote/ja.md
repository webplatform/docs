{{Page_Title|blockquote}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
|Checked_Out=Yes
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Standardization_Status|W3C Candidate Recommendation}}
{{API_Name}}
{{Summary_Section|'''blockquote'''要素は拡張された引用を表します。}}
{{Markup_Element
|DOM_interface=dom/HTMLQuoteElement
|Content====導入===
'''blockquote'''要素は別のソースから引用したコンテンツであることを示します。追加で[[html/elements/footer/ja|'''footer''']]や[[html/elements/cite/ja|'''cite''']]要素で引用元を記載したり、注釈や省略のような変更なども一緒に示すことがあります。

'''blockquote'''要素の中に出典元や変更を記載したい場合、一つだけなら、[[html/attributes/cite/ja|'''cite'''属性]]に記載することができます。

: 注: ブログのコメントのような複数人から投稿されたコンテンツでページが構成されている場合、同じページ上の他の人が書いたコメントを'出典元'とする事ができます。

cite属性を記載する際は正しいURLを設定しなければいけません。引用元のリンクを対応させるには、属性の値が、「要素と関連する」と解釈される値でなくてはいけません。ユーザエージェントは引用元リンクを辿ることを許可しますが、主に読み手に不要な私的な利用（引用サイトの利用統計を収集するサーバサイドスクリプト等）のために使われます。

cite属性は要素の引用コンテンツの帰属を反映しなければいけません。

== HTML属性==

* <code>cite</code> = 有効なURL（前後にスペースがある場合、取り除かれて扱われます。）<br />引用元のアドレスを指定します。
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Code=&lt;!-- この例は引用をインデントさせて目立たせるためにblockquote要素を使用しています。: --&gt;
&lt;p&gt;彼は
&lt;blockquote cite="http://www.example.com"&gt;"やあ、皆さん!"&lt;/blockquote&gt;と言いました。
}}{{Single Example
|Language=HTML
|Description='''blockquote'''要素は別のソースから引用したコンテンツであることを示します。追加で'''footer'''や'''cite'''要素で引用元を記載したり、注釈や省略のような変更なども一緒に示すことがあります。例えば、英語では慣例的に省略を示す場合、角括弧を使用します。"フレッドはクラッカーを食べた。そして彼はリンゴと魚が好きだと言った。"という文章を考えましょう。これは以下のように引用されます。
|Code=&lt;blockquote&gt;
 &lt;p&gt;[フレッド]は[...]魚が好きだといった。&lt;/p&gt;
&lt;/blockquote&gt;
}}{{Single Example
|Language=HTML
|Description='''blockquote'''の中で、引用されたテキストと注釈とを明確に区別するために引用符が使われます。
|Code=&lt;!-- 例えば、著者が文中で注釈を入れた場合です。 --&gt;
&lt;figure&gt;
 &lt;blockquote&gt;
 "かの怪物、習慣というものは、感覚を食い尽くし、
  悪魔のように振舞うが、"<abbr title="et cetera">などなど</abbr>（ここはFirst Folioの文章ではありません） 
 "なんという堕落だろう！
  結婚のとき手に手をとって、
  高潔な愛をもって誓ったこのわしを無みし、
  はるかに品位の劣る悪党に身を任せるとは。"
 &lt;/blockquote&gt;
 &lt;footer&gt;
 — &lt;cite class="title"&gt;シェイクスピアマニュアル&lt;/cite&gt; 著：&lt;cite class="author"&gt;フレデリク・ガード・フレーイー&lt;/cite&gt;, 
 19ページ (in Google Books)
 &lt;/footer&gt;
 &lt;/figure&gt;
&lt;!-- 注: 上記の例では、引用元はfigure要素内のfooter要素に含まれており、引用とともに引用についての情報を関連付けています。今回のケースでは、キャプションではなく、引用元を含んでいるため、figcaption要素は使っていません。 --&gt;
}}{{Single Example
|Language=HTML
|Description=引用の帰属は'''blockquote'''要素に記述しても良いですが、'''cite'''要素か'''footer'''要素に記述すべきです
|Code=&lt;!-- 例えば、ここでは引用したテキストのあとのfooterに帰属を記載し、帰属と引用物の関係を明確にしています。 --&gt;
&lt;blockquote&gt;
 &lt;p&gt;我々は無神論者である、ということを私は強く主張する。 私の信ずる神は
 あなたの信ずる神よりもひとつ少ないというだけだ。あなたが他の神々を拒絶する理由を理解すれば、
 なぜ私があなた方を拒絶するか理解できるだろう。&lt;/p&gt;
 &lt;footer&gt;— &lt;cite&gt;ステファン・ロバート&lt;/cite&gt;&lt;/footer&gt;
 &lt;/blockquote&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!--  ここでは引用したテキストの最終行の&lt;cite&gt;要素に帰属を記述しています。著者のリンクも含まれていることに注意してください。 --&gt;
&lt;blockquote&gt;
 人々は、その産物から自分自身を認識する。
 自動車やhi-fi装置、乱平面住宅、台所用品などに自身の魂を見出す。
 — &lt;cite&gt;&lt;a href="https://ja.wikipedia.org/wiki/ヘルベルト・マルクーゼ"&gt;ヘルベルト・マルクーゼ&lt;/a&gt;&lt;/cite&gt;
 &lt;/blockquote&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!-- ここでは引用文のあとのフッターで帰属と参照元のメタデータをMicrodata構文で記述しています。（※RDFA Liteでマークアップするのと同義です。） --&gt;
&lt;blockquote&gt;
  &lt;p&gt;... 彼女は”口説く”の代わりに"恋する"という言葉が使われている供述書には一切署名をしなかった。その違いは彼女にとって極めて重要な意味があった。それは彼女の元夫がいつも口説文句をささやいているのに、本心では恋をしたことなど一度もなかった、という離婚理由にある。&lt;/p&gt;
  &lt;footer itemscope itemtype="http://schema.org/Book"&gt;
    &lt;span itemprop="author"&gt;ハインリヒ・ベル&lt;/span&gt;,
    &lt;span itemprop="name"&gt;カタリーナ・ブルームの失われた名誉&lt;/span&gt;, 
    &lt;span itemprop="datePublished"&gt;1974年1月1日&lt;/span&gt;
  &lt;/footer&gt;
&lt;/blockquote&gt;
&lt;!-- 注: 引用元から引用してきた要素をマークアップする方法として正しい方法というものはありません。引用元について記述するために'''blockquote'''の中にフッターやcite要素が含まれる場合、例えばclass属性を使って仕組みを拡張し、メタデータと共に引用元の起源を注釈するという --&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!-- この例では、引用元をcite要素に記述し、class属性を使って注釈しています。 --&gt;
&lt;blockquote&gt;
  &lt;p&gt;私のお気に入りの本は&lt;cite class="from-source"&gt;スウィム・トゥ・バーズ亭にて&lt;/cite&gt;です。&lt;/p&gt;
  &lt;footer&gt;- &lt;cite&gt;Mike[tm]Smith&lt;/cite&gt;&lt;/footer&gt;
&lt;/blockquote&gt;
}}{{Single Example
|Language=HTML
|Description=以下の例は上記と異なる方法で帰属を記しています。
|Code=&lt;!-- ここではfigure要素とキャプションをつなぐためにblockquote要素を使用しています。 --&gt;
&lt;figure&gt;
 &lt;blockquote&gt;
  &lt;p&gt;真実とは時に不可解なものだ。真実がすべきことをすることもあるだろう。直感に反することもあるだろう。心の奥底にある偏見と矛盾することもあるだろう。真実だと思い込んでいることと一致しないこともあるだろう。しかし、私達の選択によって何が真実かが決まるわけではない。我々のもつ理論よって真実にたどり着くことは絶対にない。真実に極限まで近づくだけである。そして発見するのは新たな、そして広大な、未発見の可能性の海である。巧みにデザインされた実験が鍵である。&lt;/p&gt;
 &lt;/blockquote&gt;
 &lt;figcaption&gt;&lt;cite&gt;カール・セーガン&lt;/cite&gt;&lt;cite&gt;懐疑的な尋問者&lt;/cite&gt; 19巻1号(1995年1-2月)より"&lt;cite&gt;神秘と懐疑論&lt;/cite&gt;"&lt;/figcaption&gt;
&lt;/figure&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!-- 次の例は引用文と一緒に引用元を記しています。--&gt;
&lt;p&gt;次の作品はふさわしく&lt;cite&gt;ソネット130&lt;/cite&gt;と名付けられました。:&lt;/p&gt;
&lt;blockquote cite="http://quotes.example.org/s/sonnet130.html"&gt;
  &lt;p&gt;我が恋人の目に太陽の輝きはない、&lt;br&gt;
  彼女の唇より珊瑚のほうがずっと赤い、&lt;br&gt;
  ...
}}{{Single Example
|Language=HTML
|Code=&lt;!-- この例ではあるユーザがフォーラムの投稿に返信する際の例です。article要素は投稿ごとに使われ、スレッドをマークアップしています。 --&gt;
&lt;article&gt;
 &lt;h1&gt;&lt;a href="http://bacon.example.com/?blog=109431"&gt;Bacon on a crowbar&lt;/a&gt;&lt;/h1&gt;
 &lt;article&gt;
  &lt;header&gt;&lt;strong&gt;t3yw&lt;/strong&gt; 12 points 1 hour ago&lt;/header&gt;
  &lt;p&gt;I bet a narwhal would love that.&lt;/p&gt;
  &lt;footer&gt;&lt;a href="?pid=29578"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
  &lt;article&gt;
   &lt;header&gt;&lt;strong&gt;greg&lt;/strong&gt; 8 points 1 hour ago&lt;/header&gt;
   &lt;blockquote&gt;&lt;p&gt;I bet a narwhal would love that.&lt;/p&gt;&lt;/blockquote&gt;
   &lt;p&gt;Dude narwhals don't eat bacon.&lt;/p&gt;
   &lt;footer&gt;&lt;a href="?pid=29579"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
   &lt;article&gt;
    &lt;header&gt;&lt;strong&gt;t3yw&lt;/strong&gt; 15 points 1 hour ago&lt;/header&gt;
    &lt;blockquote&gt;
     &lt;blockquote&gt;&lt;p&gt;I bet a narwhal would love that.&lt;/p&gt;&lt;/blockquote&gt;
     &lt;p&gt;Dude narwhals don't eat bacon.&lt;/p&gt;
    &lt;/blockquote&gt;
    &lt;p&gt;Next thing you'll be saying they don't get capes and wizard
    hats either!&lt;/p&gt;
    &lt;footer&gt;&lt;a href="?pid=29580"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
    &lt;article&gt;
     &lt;article&gt;
      &lt;header&gt;&lt;strong&gt;boing&lt;/strong&gt; -5 points 1 hour ago&lt;/header&gt;
      &lt;p&gt;narwhals are worse than ceiling cat&lt;/p&gt;
      &lt;footer&gt;&lt;a href="?pid=29581"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
     &lt;/article&gt;
    &lt;/article&gt;
   &lt;/article&gt;
  &lt;/article&gt;
  &lt;article&gt;
   &lt;header&gt;&lt;strong&gt;fred&lt;/strong&gt; 1 points 23 minutes ago&lt;/header&gt;
   &lt;blockquote&gt;&lt;p&gt;I bet a narwhal would love that.&lt;/p&gt;&lt;/blockquote&gt;
   &lt;p&gt;I bet they'd love to peel a banana too.&lt;/p&gt;
   &lt;footer&gt;&lt;a href="?pid=29582"&gt;permalink&lt;/a&gt;&lt;/footer&gt;
  &lt;/article&gt;
 &lt;/article&gt;
&lt;/article&gt;
}}{{Single Example
|Language=HTML
|Code=&lt;!-- この例ではp要素をblockquote要素に入れずにごく短い引用文を記述しています。 --&gt;
&lt;p&gt;彼は以下のように”レッスン”を始めた。&lt;/p&gt;
&lt;blockquote&gt;メリットを得られるように譲歩することはもちろん、
相手側が非を認めることを前提としないこと&lt;/blockquote&gt;
&lt;p&gt;彼は似たような言葉を続けたあと、以下のように締めくくった。&lt;/p&gt;
&lt;blockquote&gt;最後に、どこかで交渉が崩壊する脅威に対して準備し、
可能性を盾に脅されないこと。&lt;/blockquote&gt;
&lt;p&gt;今回はこれらの点について議論していこう...
}}
}}
{{Notes_Section
|Notes====備考===
*後のセクションで、会話の表し方の例が示されるかもしれませんが、'''cite'''と'''blockquote'''はそのような目的にはふさわしくありません。
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/grouping-content.html#the-blockquote-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/grouping-content.html#the-blockquote-element
|Status=W3C Recommendation
}}{{Related Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/struct/text.html#edef-BLOCKQUOTE
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_sections====Related pages (internal)===
*<code>[[html/elements/q|q]]</code>
*<code>[[html/elements/cite|cite]]</code>
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/blockquote
|MSDN_link=http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Unknown
|Chrome_version=
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_version=1.0
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Unknown
|Internet_explorer_version=
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Unknown
|Opera_version=
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Unknown
|Safari_version=
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Unknown
|Android_version=
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Unknown
|Chrome_mobile_version=
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Yes
|Firefox_mobile_version=1.0
|Firefox_mobile_prefixed_supported=Unknown
|Firefox_mobile_prefixed_version=
|IE_mobile_supported=Unknown
|IE_mobile_version=
|IE_mobile_prefixed_supported=Unknown
|IE_mobile_prefixed_version=
|Opera_mobile_supported=Unknown
|Opera_mobile_version=
|Opera_mobile_prefixed_supported=Unknown
|Opera_mobile_prefixed_version=
|Opera_mini_supported=Unknown
|Opera_mini_version=
|Opera_mini_prefixed_supported=Unknown
|Opera_mini_prefixed_version=
|Safari_mobile_supported=Unknown
|Safari_mobile_version=
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows=
}}