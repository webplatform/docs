---
title: audio
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/HTML/Element/audio)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/7282145'
lang: ja
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLAudioElement](/dom/HTMLAudioElement)'
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: '&lt;audio&gt;は音楽ファイルを再生したり、最低限のメディアプレイヤーのインターフェイスを表示するのに使用します。'
tags:
  - Markup
  - Elements
  - Audio
  - HTML
  - Media
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/audio/af
    - html/elements/audio/ar
    - html/elements/audio/ast
    - html/elements/audio/az
    - html/elements/audio/bcc
    - html/elements/audio/bg
    - html/elements/audio/br
    - html/elements/audio/ca
    - html/elements/audio/cs
    - html/elements/audio/da
    - html/elements/audio/de
    - html/elements/audio/diq
    - html/elements/audio/el
    - html/elements/audio/eo
    - html/elements/audio/es
    - html/elements/audio/fa
    - html/elements/audio/fi
    - html/elements/audio/fr
    - html/elements/audio/gl
    - html/elements/audio/gu
    - html/elements/audio/he
    - html/elements/audio/hu
    - html/elements/audio/hy
    - html/elements/audio/id
    - html/elements/audio/it
    - html/elements/audio/ka
    - html/elements/audio/kk
    - html/elements/audio/km
    - html/elements/audio/ko
    - html/elements/audio/ksh
    - html/elements/audio/kw
    - html/elements/audio/mk
    - html/elements/audio/ml
    - html/elements/audio/mr
    - html/elements/audio/ms
    - html/elements/audio/nl
    - html/elements/audio/no
    - html/elements/audio/oc
    - html/elements/audio/pl
    - html/elements/audio/pt
    - html/elements/audio/pt-br
    - html/elements/audio/ro
    - html/elements/audio/ru
    - html/elements/audio/si
    - html/elements/audio/sk
    - html/elements/audio/sl
    - html/elements/audio/sq
    - html/elements/audio/sr
    - html/elements/audio/sv
    - html/elements/audio/ta
    - html/elements/audio/th
    - html/elements/audio/tr
    - html/elements/audio/uk
    - html/elements/audio/vi
    - html/elements/audio/yue
    - html/elements/audio/zh
    - html/elements/audio/zh-hans
    - html/elements/audio/zh-hant
    - html/elements/audio/zh-tw
uri: html/elements/audio/ja

---
## Summary

&lt;audio&gt;は音楽ファイルを再生したり、最低限のメディアプレイヤーのインターフェイスを表示するのに使用します。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLAudioElement](/dom/HTMLAudioElement)

より詳細な説明は[HTMLAudioElement](/dom/HTMLAudioElement)を参照してください。

## HTML属性

-   `autoplay` = "autoplay"、"" (空文字)、もしくは指定なし
    ブラウザ上でオーディオストリームを自動で再生します。
-   `preload` = "none"、"metadata" 、"auto"、"" (空文字)、もしくは指定なし
    ブラウザがオーディオストリームまたはメタデータを予めダウンロードするかどうかを指定します。
    -   "none": ユーザが動画を必要としていない、もしくは不要なトラフィックを最小限にしたいと予想される場合に指定します。
    -   "metadata": ユーザが動画を必要としていない、もしくは不要なトラフィックを最小限にしたいと予想される場合に指定します。
    -   "auto": オーディオストリーム全体を予めダウンロードするのが望ましい場合に指定します。空文字を指定した場合も"auto"を指定した場合と同様です。
-   `controls` = "controls"、"" (空文字)、もしくは指定なし
    オーディオストリームの再生をコントロールするインターフェイスを表示するかどうかを指定します。
-   `loop` = "loop"、"" (空文字)、もしくは指定なし
    オーディオストリームが最後まで再生された場合、最初まで戻るかどうかを指定します。
-   `mediagroup` = 文字列
    複数の動画や音楽をグループ化し、リンクさせることができます。
-   `src` = URL（前後のスペースは取り除かれます。）オーディオストリームのURLを指定します。

## アクセシビリティ

製作者は、情報とインターフェイスがいろいろなユーザに見やすくわかりやすいように作成する必要があります ([WCAG 2.0 - 原則 1: 知覚可能](http://waic.jp/docs/WCAG20/Overview.html#perceivable))。テキストのキャプション等の、タイムベースメディア（音楽や動画）に対する代替手法についても含まれています。[ガイダンス 1.2](http://waic.jp/docs/WCAG20/Overview.html#media-equiv).

## フォーマットとコーデック

一部のコーデックについて、すべてのブラウザでサポートされているわけではありません。しかしOgg/VorbisとMP4/AACはほとんどのブラウザでサポートされています。詳細は[対応音声コーデック(Wikipedia)](https://ja.wikipedia.org/wiki/HTML5%E3%82%AA%E3%83%BC%E3%83%87%E3%82%A3%E3%82%AA#.E5.AF.BE.E5.BF.9C.E9.9F.B3.E5.A3.B0.E3.82.B3.E3.83.BC.E3.83.87.E3.83.83.E3.82.AF)を参照してください。

## Examples

この例はウェブページでmp3を再生するサンプルです。

``` html
<audio controls src="http://freedownloads.last.fm/download/533190714/she%2Bso%2Bfly.mp3" type="audio/mp3">
</audio>
```

[View live example](http://code.webplatform.org/gist/7282145)

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/embedded-content.html#the-audio-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/embedded-content-0.html#the-audio-element)
:   W3C Recommendation

## See also

### Other articles

-   [HTML5 and Xiph codecs](http://wiki.xiph.org/Html5)
