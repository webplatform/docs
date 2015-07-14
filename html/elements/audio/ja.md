{{Page_Title|audio}}
{{Flags
|State=Ready to Use
|Checked_Out=No
|High-level issues=Needs Topics, Missing Relevant Sections, Data Not Semantic, Unreviewed Import
|Content=Incomplete, Not Neutral, Cleanup, Compatibility Incomplete, Examples Best Practices
}}
{{Languages}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|'''<audio>'''は音楽ファイルを再生したり、最低限のメディアプレイヤーのインターフェイスを表示するのに使用します。}}
{{Markup_Element
|DOM_interface=dom/HTMLAudioElement
|Content=より詳細な説明は[[dom/HTMLAudioElement|HTMLAudioElement]]を参照してください。


== HTML属性==

* <code>autoplay</code> = "autoplay"、"" (空文字)、もしくは指定なし<br />ブラウザ上でオーディオストリームを自動で再生します。
* <code>preload</code> = "none"、"metadata" 、"auto"、"" (空文字)、もしくは指定なし<br />ブラウザがオーディオストリームまたはメタデータを予めダウンロードするかどうかを指定します。
** "none": ユーザが動画を必要としていない、もしくは不要なトラフィックを最小限にしたいと予想される場合に指定します。
** "metadata": ユーザが動画を必要としていない、もしくは不要なトラフィックを最小限にしたいと予想される場合に指定します。
** "auto": オーディオストリーム全体を予めダウンロードするのが望ましい場合に指定します。空文字を指定した場合も"auto"を指定した場合と同様です。
* <code>controls</code> = "controls"、"" (空文字)、もしくは指定なし<br />オーディオストリームの再生をコントロールするインターフェイスを表示するかどうかを指定します。
* <code>loop</code> = "loop"、"" (空文字)、もしくは指定なし<br />オーディオストリームが最後まで再生された場合、最初まで戻るかどうかを指定します。
* <code>mediagroup</code> = 文字列<br />複数の動画や音楽をグループ化し、リンクさせることができます。
* <code>src</code> = URL（前後のスペースは取り除かれます。）オーディオストリームのURLを指定します。



== アクセシビリティ==

製作者は、情報とインターフェイスがいろいろなユーザに見やすくわかりやすいように作成する必要があります ([http://waic.jp/docs/WCAG20/Overview.html#perceivable WCAG 2.0 - 原則 1: 知覚可能])。テキストのキャプション等の、タイムベースメディア（音楽や動画）に対する代替手法についても含まれています。[http://waic.jp/docs/WCAG20/Overview.html#media-equiv ガイダンス 1.2].


== フォーマットとコーデック ==

一部のコーデックについて、すべてのブラウザでサポートされているわけではありません。しかしOgg/VorbisとMP4/AACはほとんどのブラウザでサポートされています。詳細は[https://ja.wikipedia.org/wiki/HTML5%E3%82%AA%E3%83%BC%E3%83%87%E3%82%A3%E3%82%AA#.E5.AF.BE.E5.BF.9C.E9.9F.B3.E5.A3.B0.E3.82.B3.E3.83.BC.E3.83.87.E3.83.83.E3.82.AF 対応音声コーデック(Wikipedia)]を参照してください。
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=この例はウェブページでmp3を再生するサンプルです。
|Code=<audio controls src="http://freedownloads.last.fm/download/533190714/she%2Bso%2Bfly.mp3" type="audio/mp3">
</audio>
|LiveURL=http://code.webplatform.org/gist/7282145
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/embedded-content.html#the-audio-element
|Status=W3C Working Draft
}}{{Related Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/embedded-content-0.html#the-audio-element
|Status=W3C Recommendation
}}
}}
{{See_Also_Section
|Manual_links=* [http://wiki.xiph.org/Html5 HTML5 and Xiph codecs]
}}
{{Topics|Audio, HTML, Media}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=https://developer.mozilla.org/en-US/docs/HTML/Element/audio
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
}}