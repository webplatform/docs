---
title: ja
tags:
  0: Basic
  1: Pages
  2: Concept
  4: Accessibility
  5: ARIA
  6: Design
  7: UI
  8: Usability
summary: 'アクセシビリティは、能力が様々な人々がWebを活用できるようにすることです。アクセシビリティは、質の高いwebサイトやツールを望み、自分たちの製品やサービスから人々を締め出したくない開発者や組織にとって、とても重要なことです。アクセシビリティは、障害を持った人々でも等しくWebに参加できるようにするのに不可欠です。法的必要条件になっている場合もありますが、どんな場合でも推奨事項です。'
uri: concepts/accessibility/ja
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/accessibility/af
    - concepts/accessibility/ar
    - concepts/accessibility/ast
    - concepts/accessibility/az
    - concepts/accessibility/bcc
    - concepts/accessibility/bg
    - concepts/accessibility/br
    - concepts/accessibility/ca
    - concepts/accessibility/cs
    - concepts/accessibility/da
    - concepts/accessibility/de
    - concepts/accessibility/diq
    - concepts/accessibility/el
    - concepts/accessibility/eo
    - concepts/accessibility/fa
    - concepts/accessibility/fi
    - concepts/accessibility/fr
    - concepts/accessibility/gl
    - concepts/accessibility/gu
    - concepts/accessibility/he
    - concepts/accessibility/hu
    - concepts/accessibility/hy
    - concepts/accessibility/id
    - concepts/accessibility/it
    - concepts/accessibility/ka
    - concepts/accessibility/kk
    - concepts/accessibility/km
    - concepts/accessibility/ko
    - concepts/accessibility/ksh
    - concepts/accessibility/kw
    - concepts/accessibility/mk
    - concepts/accessibility/ml
    - concepts/accessibility/mr
    - concepts/accessibility/ms
    - concepts/accessibility/nl
    - concepts/accessibility/no
    - concepts/accessibility/oc
    - concepts/accessibility/pl
    - concepts/accessibility/pt
    - concepts/accessibility/pt-br
    - concepts/accessibility/ro
    - concepts/accessibility/ru
    - concepts/accessibility/si
    - concepts/accessibility/sk
    - concepts/accessibility/sl
    - concepts/accessibility/sq
    - concepts/accessibility/sr
    - concepts/accessibility/sv
    - concepts/accessibility/ta
    - concepts/accessibility/th
    - concepts/accessibility/tr
    - concepts/accessibility/uk
    - concepts/accessibility/vi
    - concepts/accessibility/yue
    - concepts/accessibility/zh
    - concepts/accessibility/zh-hans
    - concepts/accessibility/zh-hant
    - concepts/accessibility/zh-tw

---
# アクセシビリティ

## Summary

アクセシビリティは、能力が様々な人々がWebを活用できるようにすることです。アクセシビリティは、質の高いwebサイトやツールを望み、自分たちの製品やサービスから人々を締め出したくない開発者や組織にとって、とても重要なことです。アクセシビリティは、障害を持った人々でも等しくWebに参加できるようにするのに不可欠です。法的必要条件になっている場合もありますが、どんな場合でも推奨事項です。

**言語:**
:   **[English](/concepts/accessibility)**  • <span lang="es">[español](/concepts/accessibility/es)</span> • <span lang="ja">**日本語**</span>

このページではwebアクセシビリティを概説します。さらに情報を得るためにリーソスへのリンクも示します。まずこのページを通読してから、元に戻ってさらに知るためにリンク先を参照することをお勧めします。

## Webは皆のもの

本来Webは、すべての人々が利用できるようにデザインされます。ハードウェアやソフトウェア、言語、文化、地域、身体・精神の能力がどうであれです。

Webがこの目標を達成した時、聴覚や運動、視覚、認知能力に差がある人々がWebが身近なものになります。つまり、Webでの障害による影響は根本的に変化し、Webは多くの人々が現実世界で直面しているコミュニケーションと意思疎通の障壁を取り去ることになります。

しかし、webサイトやwebテクノロジー、webツールがひどい設計なら、障壁を作ることになり、Webの利用から人々を排除することになります。例えば、アクセスしづらいwebサイトには下記のようなものがあげられます。

-   聴覚障碍者が、ポッドキャストやビデオから情報を得られない
-   認知障害者が、画像が動いたり、点滅したり、ちらついたりするため、コンテンツを読めない
-   身体障害者が、マウスを使えないために取引を完了できない

### webアクセシビリティとは?

Webアクセシビリティとは、障害を持った人々がWebを利用できることを意味します。さらに具体的に言うと、障害を持った人々が、気付いて、理解し、操作して、Webとやり取りできることを指します。そして、Webに貢献できるようになるでしょう。**なぜ**：webアクセシビリティが問題になるのか **何が**：webアクセシビリティなのか **どうやって**：webサイトやwebツールを利用しやすくするのか、については、まず　[Writing for an Accessible Web](/concepts/accessibility/writing_for_an_accessible_web) と [Accessibility - W3C](http://www.w3.org/standards/webdesign/accessibility)　を見てください。

Webアクセシビリティは、Webにアクセスするのに差し障りがある障害全てを対象とします。そこには、聴覚や認知、神経、身体、発話、視覚に障害を持った人々が含まれます。アクセシビリティには、老化に伴う障害を持った人々も対象になっています。

アクセシビリティは障害を持った人々に焦点を当てていますが、その他の人々にもメリットがあります。例えばモバイル・デバイスを使う人や制約のある状況にある人(例えば、音声が聞こえないほど騒がしい環境)です。 **アクセシビリティは社会的共生を支援します**。それは障害を持った人々や高齢者、モバイルユーザー、不便な地域に住む人々、狭い帯域で接続している人々、低学歴な人々等のためです。詳しい情報は、 [Mobile Web](#Mobile_Web) 以下、 [Older users](#Older_users) 以下と [Web Accessibility Benefits People With and Without Disabilities](http://www.w3.org/WAI/bcase/soc.html#groups) を見てください。

### Webアクセシビリティは、機会均等に欠かせないもの

Webは、生活の様々な場面でますます不可欠な手段になってきました。教育や雇用、行政、商業、医療、娯楽、社会的交流等々です。Webは情報を得るだけではなく、情報を発信し、社会と交わることにも使われます。したがって、障害を持った人々に対して等しくアクセスする機会を提供するために、Webを利用しやすくすることが最も重要になります。実際に、米国はwebアクセシビリティを基本的人権と認めています。詳細は、 [Web Accessibility is a Social Issue](http://www.w3.org/WAI/bcase/soc#social) を見てください。

## 人々がどのようにWebを使っているのか理解する

Webを使う人々の話は、障害を持った人々が日常必要としていることを説明するのに役立ちます。例えば、

-   Olsenさんは、中学校に通っています。特に文学クラスがお気に入りです。彼女は、注意欠陥多動性障害(ADHD)と失読症を患っており、この障害の組み合わせのせいで、読むことがかなり困難です。
-   Laitinenさんは、保険会社の会計主任です。この会社ではイントラネットでwebベースのドキュメントと帳票を使っています。彼女は目が不自由で、他の目が不自由な多くの人々と同様、点字を読みません。
-   Yunusさんは85歳です。数年前からWebを利用し始め、家族や友人と連絡を取ったり、美術史を読んでいます。視覚が衰え、手の震えがあり、加齢による軽い短期記憶喪失があります。

こうした人々が、どうやってWebを利用しているかについての詳細は、 [Stories of Web Users](http://www.w3.org/WAI/intro/people-use-web/stories) にあります。

Webを使う方法に影響する人々の能力は様々です。一時的な障害の人もいれば、加齢による人、生まれながらの人、怪我や健康状態からくる障害を患った人、複数の障害を持つ人もいます。疲労や炎症、投薬等によって能力が変わる人もいます。能力の多様さや人々がよく出くわすデザインがまずいwebサイトやwebツールによるwebアクセシビリティの障害の種類をさらに学びたいなら、 [Diversity of Web Users](http://www.w3.org/WAI/intro/people-use-web/diversity) を見てください。

障害を持った人々は、色々な手段でWebにアクセスし操作しています。標準のソフトウェアとハードウェアを必要に応じて設定している場合もあれば、特殊なソフトウェアやハードウェアを使って、特定の操作を支援させている場合もあります。ブラウザの設定やテキストの読み上げ、音声認識といった、障害を持った人々がWebとやりとりするテクニックやツールについて学びたいなら、 [Diversity in Web Use](http://www.w3.org/WAI/intro/people-use-web/browsing) を見てください。

## アクセシビリティの要件

障害を持った人々がWebを利用できるようにするために、webサイトとwebツールがしなければいけないことがあります。 これらのアクセシビリティの要件は、4つの基本原則を実現させます。

1.  **知覚** 情報とユーザーインターフェース。
    アクセシビリティの要件には次のものがあります。画像の代わりにテキストを用意すること。ビデオや音声の代わりにキャプションやコピーを用意すること。テキストと背景色のコントラストを十分につけること。
2.  **操作** ユーザーインターフェースとナビゲーション。
    アクセシビリティの要件には次のものがあります。キーボードだけで移動が可能なこと。意味を持ったハイパーリンクを用意すること。操作を完了するのに十分な時間を与えること。
3.  **理解可能**情報とユーザーインターフェース。
    アクセシビリティの要件には次のものがあります。コンテンツを読めるようにすること。 分かりやすい機能を用意すること。ユーザーが間違いを避ける・訂正する支援をすること。
4.  **揺るがない** コンテンツと明確な説明。
    アクセシビリティの要件には次のものがあります。現在から将来にわたって、ツール(webブラウザ、支援テクノロジー等)に互換性を可能な限り持たせること。

**webアクセシビリティの原則や要件についてさらに知りたいなら、 [Accessibility Principles](http://www.w3.org/WAI/intro/people-use-web/principles)を見てください。**

webアクセシビリティの3つの課題(画像の代わりのテキストとキーボード入力、コピー)についての入門,は、 [What: Examples of Web Accessibility](http://www.w3.org/standards/webdesign/accessibility#examples) を見てください。

## ARIA

「WAI-ARIAは、ユーザー・インターフェースの操作と動きのあるコンテンツをより利用しやすくするため、HTMLに意味と他のメタデータを追加する方法について説明しています。例えばWAI-ARIAでは、折り畳まれていてもいなくても、ナビゲーション・メニューとして、リンクのリストが確認できます。」 これ以上の情報については、 [WAI-ARIA](http://en.wikipedia.org/wiki/WAI-ARIA) を参照してください。

ARIAは、 [accessability software](http://en.wikipedia.org/wiki/Computer_accessibility) に対して視覚情報を規定する機能を提供します。そのソフトウェアは、障害のあるユーザーにページのエレメントの目的とエレメントがどんな状態なのかの情報を伝えます。

リッチ・インターネット・アプリケーション・アクセシビリティの課題と解決策についての入門は、 [WAI-ARIA 1.0 Primer](http://www.w3.org/TR/wai-aria-primer/) を見てください。

### 学習教材

[Introduction to Web Accessibility](https://webaccessibility.withgoogle.com) は、Googleのオンラインコースで、web開発者が簡単かつ確実に、盲目もしくは弱視のユーザーがよりwebサイトを利用しやすくなるツールとテクニックについて紹介しています。

HTML5でARIAを使う基本とGoogle Chromeの拡張機能であるChromeVoxとAccessibility Developer Toolsを使ったwebサイトのアクセシビリティの調査を学びます。このコースは、開発者が視覚障害を持ったユーザーを支援するために、webサイトにアクセシビリティを導入する方法を学ぶ出発点になります。

## アクセシビリティの要�

アクセシビリティの原則は、下記に登場する要素に適用されます。障害を持った人々がWebを利用しやすくするために、webの開発と双方向の要素が連携することが欠かせません。W3CのWeb Accessibility Initiative (WAI)はガイドラインを提供し、アクセシビリティが要件としている技術的な要素をカバーしています。

### Webのコンテンツ

コンテンツは、webページやweb**アプリケーション**にある情報です。その情報とは、テキストや画像、音声といった普通の情報や、コードやマークアップといった構造や体裁、双方向性等を定義したものがあります。コンテンツの要件は、Web Content Accessibility Guidelines (**WCAG**)で扱われています。

「WCAG」のドキュメントでは、障害を持った人々がより利用しやすいwebコンテンツ(webアプリケーション含む)を作る方法を解説しています。WCAGがどのように構成されているか、アクセシビリティの要件に沿ったどんな実践的なアドバイスを提供しているドキュメントがあるのか、についてさらに学ぶなら、 [the **WCAG Overview**](http://www.w3.org/WAI/intro/wcag.php) を見てください。

### ツール

私たちがwebコンテンツを作ったり使ったりするツールは、webアクセシビリティを支援する場合もあれば妨げる場合もあります。

-   **オーサリングツール** はwebサイトを作ったり修正したりするソフトウェアとサービスです。例えば、コンテンツ・マネージメント・システム(CMS)やHTMLエディター、コンテンツをユーザーに追加させるwebサイト(ソーシャルメディアのような)等のツールです。ツールは、webコンテンツを作る際に、利用しやすくしなければいけません。この点については、Authoring Tool Accessibility Guidelinesで触れています。 **[ATAG Overview](http://www.w3.org/WAI/intro/atag.php)** を見てください。
-   **評価ツール** は、webサイトが標準に準拠しているかチェックするのを支援するものです（ [Selecting Web Accessibility Evaluation Tools](http://www.w3.org/WAI/eval/selectingtools.html) に関連情報があります）
-   **Webブラウザ**、メディアプレーヤー、その他webコンテンツにアクセスする"ユーザーエージェント"は、User Agent Accessibility Guidelinesで触れています。**[UAAG Overview](http://www.w3.org/WAI/intro/uaag.php)** を見てください。
-   **支援テクノロジー**は、障害を持った人々がWebとやりとりするのを改善するのに使われるソフトウェアとハードウェアです。例えば、web,ページを読み上げるスクリーンリーダーや音声認識ソフトウェア、キーボードの代わりになるもの等

### 人 - webコンテンツの作り手とユーザー

webコンテンツとツールに加えて、人もwebアクセシビリティの重要な要素です。

「コンテンツを作る人」アクセシビリティを理解して実装する必要があります。開発者とデザイナー、著者、マネージャー等がそれに該当し、コンテンツ(アプリケーションを含む)の開発やオーサリングツール、評価ツール、ブラウザ、その他ユーザーエージェントに関わる全ての人も対象です。

「Webを使う人」は、知識や経験がバラバラで、アクセシビリティに影響を与えるスキルレベルも様々です。例えば、どの程度支援技術や適応戦略の利用方法を知っているかとか、必要に合わせてツールを使っているかです。

webコンテンツとツール、人的要素について、これ以上知りたければ、["Components of Web Accessibility" Presentation](http://www.w3.org/WAI/presentations/components/Overview.php) か [Essential Components of Web Accessibility](http://www.w3.org/WAI/intro/components.php) を見てください。

## 投資対効果検討書

組織でアクセシビリティの初期投資をしようとするなら、webアクセシビリティの金銭的な利益を理解する必要があります。 ["Web Accessibility is Smart Business" Presentation](http://www.w3.org/WAI/presentations/bcase/Overview.php) に紹介されています。

社会的、技術的、金銭的、法的、政策的要因についてさらに知りたいなら、 [Developing a Web Accessibility Business Case for Your Organization](http://www.w3.org/WAI/bcase/Overview.html) を見てください。この中では、投資対効果検討書を見直して発展させるガイダンスとともに、webアクセシビリティについて、これまでと違った視点を提供しています。

例えば、投資対効果検討書の一側面として、ユーザーを増やすには、高齢のユーザーとモバイルユーザーを取り込む、というものがあります。

### 高齢のユーザー

高齢のユーザーのマーケット・セグメントは広がっていて、ビジネスや政府、その他の組織の多くで重要なターゲット・グループになっています。高齢な人々の多くは、加齢に関連した障害を持っていて、それがWebの利用の仕方に影響を及ぼしています。その障害とは、視力や身体能力、聴覚、認知能力の低下です。これらの問題は、障害を持った人々が必要としているアクセシビリティと重なっています。つまり、障害を持った人が利用しやすくなるwebサイトとツールは、高齢のユーザーにも同じようにさらに利用しやすくするということです。詳しい情報は、 [Web Accessibility and Older People: Meeting the Needs of Ageing Web Users](http://www.w3.org/WAI/older-users/Overview.php) を見てください。

### モバイルWeb

グローバル・モバイル・フォンは、これまでになく使われています。モバイル・デバイスから利用しやすくなるwebサイトの開発で、関心が高まって来ています。モバイル・デバイスのユーザーと障害を持った人々は、Webコンテンツを扱う際に同じような使いにくさを感じます。開発者がwebサイトを利用しやすくするのに、モバイル・デバイスと障害を持った人々のためにすることに重複する部分がかなりあることを理解した時、Webサイトはより効率的に両者の目的をかなえられるでしょう。さらに詳しい情報は、 [Web Content Accessibility and Mobile Web: Making a Web Site Accessible Both for People with Disabilities and for Mobile Devices](http://www.w3.org/WAI/mobile/) を見て下さい。

## W3C WAIからもっと学ぶ

W3CのWeb Accessibility Initiative (WAI)は、世界各国の産業界や障害者団体、政府、研究所の人々が一緒になって、障害を持った人々がWebを利用しやすくなるように、ガイドラインの作成と支援を進めています。 [WAI website](http://www.w3.org/WAI/) を見渡してみることをおすすめします。そうすれば、さらに役立つ情報が得られるでしょう。 [Finding Your WAI ("way") to New Web Accessibility Resources](http://www.w3.org/WAI/yourWAI) を見て下さい。

## 引用文献と謝辞

このドキュメントの情報の引用について：このページのテキストの大部分は、他のドキュメントを引用しており、セクション内からリンクされています。引用する場合は、オリジナルのドキュメントを使ってください( [Using WAI Material: Permission to Use with Attribution](http://www.w3.org/WAI/about/usingWAImaterial.html) )

## 関連項目

-   [This page originally available at W3C WAI](http://www.w3.org/WAI/EO/wiki/Web_Accessibility_Basics)
-   [Improving accessibility using HTML5 features](http://www.w3.org/WAI/GL/wiki/Techniques/HTML5)
-   [Improving accessibility using ARIA features](http://www.w3.org/WAI/GL/wiki/Techniques/ARIA)
-   [HTML and CSS techniques for passing WCAG conformance criteria](http://www.w3.org/TR/WCAG20-TECHS/)
-   [Making Accessible Windows Store apps using JavaScript and HTML](http://msdn.microsoft.com/en-us/library/windows/apps/hh452681.aspx)
-   [Introduction to Web Accessibility by Google](https://webaccessibility.withgoogle.com)

