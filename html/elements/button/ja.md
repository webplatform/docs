{{Page_Title|button}}
{{Flags
|State=In Progress
|Editorial notes=Add Category, Parent, Children and Compatibility information.
|Checked_Out=No
}}
{{Standardization_Status|W3C Recommendation}}
{{API_Name}}
{{Summary_Section|'''button'''要素はクリック可能なボタンを表示します。|The "button" tag is one of many ways to create buttons on an HTML page_ A web developer can also use the "input" tag in conjunction with type="button" or by styling an "a" tag to achieve the same functionality. However, those may be harder and their results may not be as clean.
}}
{{Markup_Element
|DOM_interface=dom/HTMLButtonElement
|Content=button要素ではボタンの中にテキストや画像を設置することができます。button要素がdisableでなければ、ボタンを押すことができます。


デフォルトではボタンをクリックすることで、[[html/elements/form/ja|'''form''']]のデータをサブミットします。type属性を変更することでボタンがクリックされた際の挙動を変更できます。

===属性(HTML 4)===
<dl>
<dt>name</dt>
<dd>ボタンの名前です。これによってformをサブミットしたボタンを識別することができます。</dd>
<dt>type</dt>
<dd>ボタンのタイプを指定します。type属性を記述しない場合、<code>submit</code>となります。使用できるtypeは以下の3つです。
<ul>
<li><code>submit</code>:  紐付いたフォームのデータをサーバに送ります。これがデフォルト値となります。</li>
<li><code>reset</code>: 紐付いたフォームをリセットします。フィールドに初期値をセットします。</li>
<li><code>button</code>: これを指定すると、デフォルトでは何もしません。JavaScriptの[[dom/MouseEvent/click/ja|'''click''']]イベントを設定すると非常に便利です。</li> 
</ul>
</dd>
<dt>value</dt>
<dd>ボタンの初期値です。</dd>
<dt>disabled</dt>
<dd>このBooleanの属性は、ユーザにボタンを操作できなくするためのものです。特にこの属性を指定しない場合、button要素は親要素の設定を継承します。例えば、'''fieldset'''の中の要素にdisabled属性を設定したものがなければ、ボタンは有効となります。disabledを指定したボタンはクリックすることができません。</dd>
</dl>

===追加属性(HTML 5勧告候補)===
<dl>
<dt>autofocus</dt>
<dd>この属性を"true"にすると、ユーザが別の入力をしない限り、ページをロードしたあとすぐにボタンがフォーカスされます。
ドキュメント内のform関連要素の中で1つだけがこの属性を指定できます。</dd>
<dt>form</dt>
<dd>ボタンに紐づくformを指定します。属性の値はformのid属性と一致していなければいけません。'''button'''要素をサブミットできるformデータを持ったフォームの子要素としていれば、この属性を指定せずに使用することができます。この属性によって'''form'''要素の子要素としてだけでなく、button要素をドキュメント内のどこにでも配置することができます。
<dt>formaction</dt>
<dd>formからの情報を処理するプログラムのURIを指定します。紐付いたformのaction属性を上書きます。</dd>
<dt>formmethod</dt>
<dd>formデータをサブミットするHTTP メソッドを指定します。<code>post</code>または<code>get</code>を指定できます。指定した場合、紐付いたformのmethod属性を上書きます。利用可能な値は以下のとおりです。
* <code>post</code>: formのbodyに含まれるデータをサーバに送信します。
* <code>get</code>: form属性のURIにセパレータとして”?”をつけてフォームのデータを追記し、作成されたURIをサーバに送信します。formが動的でなく、ASCII文字のみで構成されていればこのメソッドを使用できます。</dd>
<dt>formnovalidate</dt>
<dd>ボタンがサブミットボタンであれば、formの値の妥当性を確認するかどうかを指定することができます。formの持つnovalidate属性を上書きます。</dd>
<dt>formtarget</dt>
<dd>この属性は送信されたフォームを受け取るウィンドウを指定します。以下の中から一つ指定することができます。
<ul>
<li><code>_self</code>: 自身のフォームにレスポンスを表示します。これがデフォルト値となります。</li>
<li><code>_blank</code>: 名前の無いコンテキストとして新しいウインドウにレスポンスを読み込ませます。</li>
<li><code>_parent</code>: 親コンテキストにレスポンスを読み込ませます。親が存在しない場合、_selfを指定した時と同じ動作をします。</li>
<li><code>_top</code>: 一番上のコンテキストにレスポンスを読み込ませます。これは現在のコンテキストの一番祖先のコンテキストを指します。親が存在しない場合、_selfを指定した時と同じ動作をします。</li>
</ul>
</dd>
</dl>

これらの属性は<code>name</code>属性を除き、デフォルト値を持っているため、記載せずに利用することができます。
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=この例は<code>&lt;button&gt;</code>要素を使って、送信もリセットもしないクリック可能なボタンを表示しています。
|Code=<button name="myButton" type="button">クリックしてね</button>
|LiveURL=http://code.webplatform.org/gist/b08191a8d5915621a5e1
}}{{Single Example
|Language=HTML
|Description=この例ではフォームを送信するための<code>&lt;button&gt;</code>の使い方を紹介します。よくわからない場合は、form要素についてのページを読んで[[html/elements/form/ja|'''form''']]の使い方について詳細な情報を学んでください。
|Code=<form action="dataReceiverURI">
  <label for="name">氏名:</label>
  <input id="name" type="text" name="user_name">
  <button name="mySubmitButton">送信</button>
</form>
|LiveURL=http://code.webplatform.org/gist/ceb6531b1b86fb0b21d0
}}{{Single Example
|Language=HTML
|Description=<code>&lt;button=&quot;reset&quot;&gt;</code>を使ってformをリセットする例を紹介します。よくわからない場合は、form要素についてのページを読んで[[html/elements/form/ja|'''form''']]の使い方について詳細な情報を学んでください。
|Code=<form>
  <label for="name">氏名:</label>
  <input id="name" type="text" name="user_name" >
  <button name="myResetButton">リセット</button>
</form>
|LiveURL=http://code.webplatform.org/gist/c579515bcd4378bfd634
}}
}}
{{Notes_Section
|Usage=一般的に、'''button'''要素はいつでもクリック可能であるべきです。

閉じタグは必須です。

ボタンには簡単な説明文をボタン内に記載するべきです。ボタンの中のテキストが空だとｍユーザはそのボタンがどんな動きをするのかわからなくなってしまいます。

サブミットボタンを装飾するときは<button>要素を使うよりもtype属性に<code>submit</code>を指定した[[html/elements/input/ja|'''input''']]要素のほうが簡単に実装することができます。

|Notes=type属性のデフォルト値は<code>type</code>であるため、特に他の<code>type</code>を使用する必要がない場合は、<code>type</code>を省略することができます。過去のブラウザでは<code>type</code>の値がそれぞれ違いました。

Android用のFirefoxではデフォルトで<code>[[css/properties/background-image/ja|background-image]]</code>がセットされており、すべての'''button'''にグラデーションがついていました。
これは<code>background-image: none</code>を指定することで無効化することができます。

Firefoxは他のブラウザと異なり、デフォルトでbuttonの[http://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing disabledの状態がページ読み込みを挟んでも保持されます]。
autocomplete属性をoffにするとこの機能を無効にすることができます。[https://bugzilla.mozilla.org/show_bug.cgi?id=654072 Mozilla Bug #654072]をご覧ください。

===クリックとフォーカス===
ブラウザ/OS別　'''button'''をクリックした際、フォーカスが切り替わるかどうか

buttonをクリックしたときフォーカスされますか？
{{{!}} class="wikitable"
! デスクトップブラウザ
! Windows 8.1
! OS X 10.9
{{!}}-
{{!}} Firefox 30.0
{{!}} Yes
{{!}} No (even with a [[html/attributes/tabIndex|<code>tabindex</code>]])
{{!}}-
{{!}} Chrome 35
{{!}} Yes
{{!}} Yes
{{!}}-
{{!}} Safari 7.0.5
{{!}} N/A
{{!}} No (even with a [[html/attributes/tabIndex|<code>tabindex</code>]])
{{!}}-
{{!}} Internet Explorer 11
{{!}} Yes
{{!}} N/A
{{!}}-
{{!}} Presto (Opera 12)
{{!}} Yes
{{!}} ???
{{!}}}


'''button'''をタップしたときフォーカスされますか？
{{{!}} class="wikitable"
! Mobile Browsers
! iOS 7.1.2
! Android 4.4.4
{{!}}-
{{!}} Safari Mobile
{{!}} No (even with a [[html/attributes/tabIndex|<code>tabindex</code>]])
{{!}} N/A
{{!}}-
{{!}} Chrome 35
{{!}} ???
{{!}} Yes
{{!}}}
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related_Specification
|Name=HTML 5.1
|URL=http://www.w3.org/TR/html51/forms.html#the-button-element
|Status=W3C Working Draft
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 5
|URL=http://www.w3.org/TR/html5/forms.html#the-button-element
|Status=W3C Recommendation
|Relevant_changes=
}}{{Related_Specification
|Name=HTML 4.01
|URL=http://www.w3.org/TR/html401/interact/forms.html#edef-BUTTON
|Status=W3C Recommendation
|Relevant_changes=
}}
}}
{{See_Also_Section
|Topic_clusters=Document Structure, HTML
|Manual_links=* [[html/elements/input/type/button|'''input type="button"''']]
* [[html/elements/input/type/submit|'''input type="submit"''']]
|External_links=
|Manual_sections=
}}
{{Topics|HTML, UI}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=MDN, MSDN
|MDN_link=[https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button <button> on MDN]
|MSDN_link=[http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx Windows Internet Explorer API reference]
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows={{Compatibility Table Desktop Row
|Chrome_supported=Yes
|Chrome_prefixed_supported=Unknown
|Chrome_prefixed_version=
|Firefox_supported=Yes
|Firefox_prefixed_supported=Unknown
|Firefox_prefixed_version=
|Internet_explorer_supported=Yes
|Internet_explorer_prefixed_supported=Unknown
|Internet_explorer_prefixed_version=
|Opera_supported=Yes
|Opera_prefixed_supported=Unknown
|Opera_prefixed_version=
|Safari_supported=Yes
|Safari_prefixed_supported=Unknown
|Safari_prefixed_version=
}}
|Mobile_rows={{Compatibility Table Mobile Row
|Android_supported=Yes
|Android_prefixed_supported=Unknown
|Android_prefixed_version=
|Blackberry_supported=Unknown
|Blackberry_version=
|Blackberry_prefixed_supported=Unknown
|Blackberry_prefixed_version=
|Chrome_mobile_supported=Yes
|Chrome_mobile_prefixed_supported=Unknown
|Chrome_mobile_prefixed_version=
|Firefox_mobile_supported=Unknown
|Firefox_mobile_version=
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
|Safari_mobile_supported=Yes
|Safari_mobile_prefixed_supported=Unknown
|Safari_mobile_prefixed_version=
}}
|Notes_rows={{Compatibility Notes Row
|Browser=Internet Explorer
|Version=8 and later
|Note=The default value of the type attribute depends on the current document compatibility mode. In IE8 Standards mode, the default value is submit. In other compatibility modes and earlier versions of Windows Internet Explorer, the default value is button. When the BUTTON element is submitted in a form, the value depends on the current document compatibility mode. In IE8 mode, the value attribute is submitted. In other document modes and earlier versions of Internet Explorer, the innerText value is submitted.
}}
}}