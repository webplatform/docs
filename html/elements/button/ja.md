---
title: button
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[\<button\> on MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button) Article]'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/b08191a8d5915621a5e1'
  - 'http://gist.github.com/ceb6531b1b86fb0b21d0'
  - 'http://gist.github.com/c579515bcd4378bfd634'
lang: ja
notes:
  - 'Add Category, Parent, Children and Compatibility information.'
overview_table:
  '[DOM Interface](/dom/interface)': '[HTMLButtonElement](/dom/HTMLButtonElement)'
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
summary: 'button要素はクリック可能なボタンを表示します。'
tags:
  - Markup
  - Elements
  - HTML
  - UI
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - html/elements/form/ja
    - dom/MouseEvent/click/ja
    - html/elements/input/ja
    - css/properties/background-image/ja
uri: html/elements/button/ja

---
## Summary

button要素はクリック可能なボタンを表示します。

## Overview Table

[DOM Interface](/dom/interface)
:   [HTMLButtonElement](/dom/HTMLButtonElement)

button要素ではボタンの中にテキストや画像を設置することができます。button要素がdisableでなければ、ボタンを押すことができます。

 デフォルトではボタンをクリックすることで、[**form**](/w/index.php?title=html/elements/form/ja&action=edit&redlink=1)のデータをサブミットします。type属性を変更することでボタンがクリックされた際の挙動を変更できます。

### 属性(HTML 4)

name
:   ボタンの名前です。これによってformをサブミットしたボタンを識別することができます。
type
:   ボタンのタイプを指定します。type属性を記述しない場合、`submit`となります。使用できるtypeは以下の3つです。

    -   `submit`: 紐付いたフォームのデータをサーバに送ります。これがデフォルト値となります。
    -   `reset`: 紐付いたフォームをリセットします。フィールドに初期値をセットします。
    -   `button`: これを指定すると、デフォルトでは何もしません。JavaScriptの[**click**](/w/index.php?title=dom/MouseEvent/click/ja&action=edit&redlink=1)イベントを設定すると非常に便利です。

value
:   ボタンの初期値です。
disabled
:   このBooleanの属性は、ユーザにボタンを操作できなくするためのものです。特にこの属性を指定しない場合、button要素は親要素の設定を継承します。例えば、**fieldset**の中の要素にdisabled属性を設定したものがなければ、ボタンは有効となります。disabledを指定したボタンはクリックすることができません。

### 追加属性(HTML 5勧告候補)

autofocus
:   この属性を"true"にすると、ユーザが別の入力をしない限り、ページをロードしたあとすぐにボタンがフォーカスされます。 ドキュメント内のform関連要素の中で1つだけがこの属性を指定できます。
form
:   ボタンに紐づくformを指定します。属性の値はformのid属性と一致していなければいけません。**button**要素をサブミットできるformデータを持ったフォームの子要素としていれば、この属性を指定せずに使用することができます。この属性によって**form**要素の子要素としてだけでなく、button要素をドキュメント内のどこにでも配置することができます。
formaction
:   formからの情報を処理するプログラムのURIを指定します。紐付いたformのaction属性を上書きます。
formmethod
:   formデータをサブミットするHTTP メソッドを指定します。`post`または`get`を指定できます。指定した場合、紐付いたformのmethod属性を上書きます。利用可能な値は以下のとおりです。
    -   `post`: formのbodyに含まれるデータをサーバに送信します。
    -   `get`: form属性のURIにセパレータとして”?”をつけてフォームのデータを追記し、作成されたURIをサーバに送信します。formが動的でなく、ASCII文字のみで構成されていればこのメソッドを使用できます。

formnovalidate
:   ボタンがサブミットボタンであれば、formの値の妥当性を確認するかどうかを指定することができます。formの持つnovalidate属性を上書きます。
formtarget
:   この属性は送信されたフォームを受け取るウィンドウを指定します。以下の中から一つ指定することができます。

    -   `_self`: 自身のフォームにレスポンスを表示します。これがデフォルト値となります。
    -   `_blank`: 名前の無いコンテキストとして新しいウインドウにレスポンスを読み込ませます。
    -   `_parent`: 親コンテキストにレスポンスを読み込ませます。親が存在しない場合、\_selfを指定した時と同じ動作をします。
    -   `_top`: 一番上のコンテキストにレスポンスを読み込ませます。これは現在のコンテキストの一番祖先のコンテキストを指します。親が存在しない場合、\_selfを指定した時と同じ動作をします。

これらの属性は`name`属性を除き、デフォルト値を持っているため、記載せずに利用することができます。

## Examples

この例は`<button>`要素を使って、送信もリセットもしないクリック可能なボタンを表示しています。

``` html
<button name="myButton" type="button">クリックしてね</button>
```

[View live example](http://code.webplatform.org/gist/b08191a8d5915621a5e1)

この例ではフォームを送信するための`<button>`の使い方を紹介します。よくわからない場合は、form要素についてのページを読んで[**form**](/w/index.php?title=html/elements/form/ja&action=edit&redlink=1)の使い方について詳細な情報を学んでください。

``` html
<form action="dataReceiverURI">
  <label for="name">氏名:</label>
  <input id="name" type="text" name="user_name">
  <button name="mySubmitButton">送信</button>
</form>
```

[View live example](http://code.webplatform.org/gist/ceb6531b1b86fb0b21d0)

`<button="reset">`を使ってformをリセットする例を紹介します。よくわからない場合は、form要素についてのページを読んで[**form**](/w/index.php?title=html/elements/form/ja&action=edit&redlink=1)の使い方について詳細な情報を学んでください。

``` html
<form>
  <label for="name">氏名:</label>
  <input id="name" type="text" name="user_name" >
  <button name="myResetButton">リセット</button>
</form>
```

[View live example](http://code.webplatform.org/gist/c579515bcd4378bfd634)

## Usage

     一般的に、button要素はいつでもクリック可能であるべきです。

閉じタグは必須です。

ボタンには簡単な説明文をボタン内に記載するべきです。ボタンの中のテキストが空だとｍユーザはそのボタンがどんな動きをするのかわからなくなってしまいます。

サブミットボタンを装飾するときは\<button\>要素を使うよりもtype属性に`submit`を指定した[**input**](/w/index.php?title=html/elements/input/ja&action=edit&redlink=1)要素のほうが簡単に実装することができます。

## Notes

type属性のデフォルト値は`type`であるため、特に他の`type`を使用する必要がない場合は、`type`を省略することができます。過去のブラウザでは`type`の値がそれぞれ違いました。

Android用のFirefoxではデフォルトで`background-image`がセットされており、すべての**button**にグラデーションがついていました。 これは`background-image: none`を指定することで無効化することができます。

Firefoxは他のブラウザと異なり、デフォルトでbuttonの[disabledの状態がページ読み込みを挟んでも保持されます](http://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing)。 autocomplete属性をoffにするとこの機能を無効にすることができます。[Mozilla Bug \#654072](https://bugzilla.mozilla.org/show_bug.cgi?id=654072)をご覧ください。

### クリックとフォーカス

ブラウザ/OS別　**button**をクリックした際、フォーカスが切り替わるかどうか

buttonをクリックしたときフォーカスされますか？

|デスクトップブラウザ|Windows 8.1|OS X 10.9|
|:-------------------|:----------|:--------|
|Firefox 30.0|Yes|No (even with a [`tabindex`](/html/attributes/tabIndex))|
|Chrome 35|Yes|Yes|
|Safari 7.0.5|N/A|No (even with a [`tabindex`](/html/attributes/tabIndex))|
|Internet Explorer 11|Yes|N/A|
|Presto (Opera 12)|Yes| ???|

**button**をタップしたときフォーカスされますか？

|Mobile Browsers|iOS 7.1.2|Android 4.4.4|
|:--------------|:--------|:------------|
|Safari Mobile|No (even with a [`tabindex`](/html/attributes/tabIndex))|N/A|
|Chrome 35| ???|Yes|

## Related specifications

[HTML 5.1](http://www.w3.org/TR/html51/forms.html#the-button-element)
:   W3C Working Draft

[HTML 5](http://www.w3.org/TR/html5/forms.html#the-button-element)
:   W3C Recommendation

[HTML 4.01](http://www.w3.org/TR/html401/interact/forms.html#edef-BUTTON)
:   W3C Recommendation

## See also

### Related articles

#### Document Structure

-   [button](/html/elements/button)

-   **button**

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [main](/html/elements/main)

-   [nav](/html/elements/nav)

-   [p](/html/elements/p)

-   [section](/html/elements/section)

#### HTML

-   [user-modify](/css/properties/user-modify)

-   [textLength](/dom/HTMLTextAreaElement/textLength)

-   [value](/dom/HTMLTextAreaElement/value)

-   [accept](/html/attributes/accept)

-   [action](/html/attributes/action)

-   [alt](/html/attributes/alt)

-   [autocomplete](/html/attributes/autocomplete)

-   [autofocus](/html/attributes/autofocus)

-   [checked](/html/attributes/checked)

-   [crossorigin](/html/attributes/crossorigin)

-   [form](/html/attributes/form)

-   [formEnctype](/html/attributes/formEnctype)

-   [height](/html/attributes/height)

-   [list](/html/attributes/list)

-   [max (HTMLInputElement)](/html/attributes/max_(HTMLInputElement))

-   [maxLength](/html/attributes/maxLength)

-   [min](/html/attributes/min)

-   [multiple](/html/attributes/multiple)

-   [readonly](/html/attributes/readonly)

-   [size](/html/attributes/size)

-   [standby](/html/attributes/standby)

-   [step](/html/attributes/step)

-   [HTML Elements](/html/elements)

-   [!DOCTYPE](/html/elements/!DOCTYPE)

-   [!DOCTYPE](/html/elements/!DOCTYPE/ja)

-   [acronym](/html/elements/acronym)

-   [b](/html/elements/b)

-   [b](/html/elements/b/ja)

-   [br](/html/elements/br)

-   [br](/html/elements/br/ja)

-   [button](/html/elements/button)

-   **button**

-   [caption](/html/elements/caption)

-   [cite](/html/elements/cite)

-   [code](/html/elements/code)

-   [col](/html/elements/col)

-   [colgroup](/html/elements/colgroup)

-   [datalist](/html/elements/datalist)

-   [del](/html/elements/del)

-   [dfn](/html/elements/dfn)

-   [div](/html/elements/div)

-   [em](/html/elements/em)

-   [EMBED](/html/elements/embed)

-   [fieldset](/html/elements/fieldset)

-   [font](/html/elements/font)

-   [footer](/html/elements/footer)

-   [head](/html/elements/head)

-   [hn](/html/elements/hn)

-   [hr](/html/elements/hr)

-   [html](/html/elements/html)

-   [i](/html/elements/i)

-   [img](/html/elements/img)

-   [input](/html/elements/input)

-   [ins](/html/elements/ins)

-   [kbd](/html/elements/kbd)

-   [legend](/html/elements/legend)

-   [mark](/html/elements/mark)

-   [option](/html/elements/option)

-   [p](/html/elements/p)

-   [samp](/html/elements/samp)

-   [script](/html/elements/script)

-   [span](/html/elements/span)

-   [strong](/html/elements/strong)

-   [table](/html/elements/table)

-   [tbody](/html/elements/tbody)

-   [td](/html/elements/td)

-   [tfoot](/html/elements/tfoot)

-   [th](/html/elements/th)

-   [time](/html/elements/time)

### Other articles

-   [**input type="button"**](/html/elements/input/type/button)
-   [**input type="submit"**](/html/elements/input/type/submit)
