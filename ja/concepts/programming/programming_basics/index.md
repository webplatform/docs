---
title: プログラミングの基礎
attributions:
  - 'This content was originally published on [DevOpera](http://dev.opera.com), Opera''s Developer Network. .'
summary: "※ 本記事はまだ試験的に作成しているものである点にご注意願います。\n"
tags:
  - Guides
  - JavaScript
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - 'af/concepts/programming/programming basics'
    - 'ar/concepts/programming/programming basics'
    - 'ast/concepts/programming/programming basics'
    - 'az/concepts/programming/programming basics'
    - 'bcc/concepts/programming/programming basics'
    - 'bg/concepts/programming/programming basics'
    - 'br/concepts/programming/programming basics'
    - 'ca/concepts/programming/programming basics'
    - 'cs/concepts/programming/programming basics'
    - 'da/concepts/programming/programming basics'
    - 'de/concepts/programming/programming basics'
    - 'diq/concepts/programming/programming basics'
    - 'el/concepts/programming/programming basics'
    - 'eo/concepts/programming/programming basics'
    - 'es/concepts/programming/programming basics'
    - 'fa/concepts/programming/programming basics'
    - 'fi/concepts/programming/programming basics'
    - 'fr/concepts/programming/programming basics'
    - 'gl/concepts/programming/programming basics'
    - 'gu/concepts/programming/programming basics'
    - 'he/concepts/programming/programming basics'
    - 'hu/concepts/programming/programming basics'
    - 'hy/concepts/programming/programming basics'
    - 'id/concepts/programming/programming basics'
    - 'it/concepts/programming/programming basics'
    - 'ka/concepts/programming/programming basics'
    - 'kk/concepts/programming/programming basics'
    - 'km/concepts/programming/programming basics'
    - 'ko/concepts/programming/programming basics'
    - 'ksh/concepts/programming/programming basics'
    - 'kw/concepts/programming/programming basics'
    - 'mk/concepts/programming/programming basics'
    - 'ml/concepts/programming/programming basics'
    - 'mr/concepts/programming/programming basics'
    - 'ms/concepts/programming/programming basics'
    - 'nl/concepts/programming/programming basics'
    - 'no/concepts/programming/programming basics'
    - 'oc/concepts/programming/programming basics'
    - 'pl/concepts/programming/programming basics'
    - 'pt/concepts/programming/programming basics'
    - 'pt-br/concepts/programming/programming basics'
    - 'ro/concepts/programming/programming basics'
    - 'ru/concepts/programming/programming basics'
    - 'si/concepts/programming/programming basics'
    - 'sk/concepts/programming/programming basics'
    - 'sl/concepts/programming/programming basics'
    - 'sq/concepts/programming/programming basics'
    - 'sr/concepts/programming/programming basics'
    - 'sv/concepts/programming/programming basics'
    - 'ta/concepts/programming/programming basics'
    - 'th/concepts/programming/programming basics'
    - 'tr/concepts/programming/programming basics'
    - 'uk/concepts/programming/programming basics'
    - 'vi/concepts/programming/programming basics'
    - 'yue/concepts/programming/programming basics'
    - 'zh/concepts/programming/programming basics'
    - 'zh-hans/concepts/programming/programming basics'
    - 'zh-hant/concepts/programming/programming basics'
    - 'zh-tw/concepts/programming/programming basics'
uri: 'ja/concepts/programming/programming basics'

---
## Summary

※ 本記事はまだ試験的に作成しているものである点にご注意願います。

本記事では、JavaScriptを例として、プログラミングの基礎的な原則について述べます。

## はじめに

経験を積んだプログラマは、遅かれ早かれ、全く技術に詳しくない人々からは、まるで黒魔術でも扱っているかのごとく見られるようになっていくものです。逆の立場から見れば、技術に詳しくない人にとって、もし力を貸してくれている人がいたとしても、何をどうしているのかが伝わらないままであれば、そのうちついて行けなくなってしまいます。[Web Standards Curriculum](http://www.w3.org/wiki/Web_Standards_Curriculum)は、プログラミングとは何かを簡単な言葉で説明しており、経験を積んだプログラマにも技術に詳しくない人にもどちらにもわかりやすい内容となっています。

JavaScriptプログラミングの仕方を学ぶ前には必須となる全般的なプログラミングの原則を基礎として固めておくこともまた、初心者のWeb開発者にとっては大変有益となります。一見退屈と思えるかもしれませんが、ご安心下さい。初めのうちに基礎的な原則を踏まえておけば、(ここは大きな声で)後々きっと強固で力強く、創造的な力として、あなたの身になることでしょう。プログラミングの基礎は、特定のプログラミング言語(もちろん、ここではJavaScript)を使ってみる前に習得しておくことが重要なのです。

## まずは触ってみよう

プログラミングの基礎を学ぶ上での第一歩は、試しにコマンドを入力して実行、その結果として何が出力されるかを見ることです。プログラミングとは数学と言語の組み合わせのように成り立っており、すなわち、コンピュータに解かせたい計算を正しい文法で順番通りに記述し、コンピュータに渡す作業であると言えます。プログラミングにおいて文法(grammar)とは、何をどういう並びで記述しなければならないといった構文(syntax)を定義するものであり、プログラミング言語によって大幅に異なっています。

例として、次のような2つの簡単なコードを示します。これらは全く同じように動作しますが、前者はJavaScript、後者はPHPで書かれています。

``` js
var fahrenheit = prompt('Enter temperature in Fahrenheit', 0);
var celsius = (fahrenheit - 32) * 5 / 9;
alert(celsius);
```

```
$fahrenheit = $_GET['fahrenheit'];
$celsius = ($fahrenheit - 32) * 5 / 9;
echo $celsius;
```

 それでは、JavaScriptによる[華氏(℉)から摂氏(℃)への変換サンプル](http://dev.opera.com/articles/view/programming-the-real-basics/fahrenheit.html)を試しに動かしてみましょう。

これらのプログラミング言語がコンピュータに解釈されると、何らかの動作や結果が生じます。JavaScriptといったプログラミング言語はWebブラウザが解釈することができます。すなわち、ブラウザに「何かをさせる」には、JavaScriptでその動作をHTML文書の中に記述して、ブラウザで開けばよいのです。一方、他のプログラミング言語では、実行可能にするために一度変換(コンパイル)するといった作業が必要となります。コンピュータは深掘りすると0と1の2つを理解するだけで動作していることになりますが、様々な動作を実現するために多様なレベルの言語が存在しているのです。

## 変数

プログラミングについて理解を進める第一歩は、数学の使い方に立ち返ることです。恐らく学校で学んだことを思い出してみると、次のような式を書くことから数学が始まったのではないでしょうか。

    3 + 5 = 8

続いて、例えば次のように未知の値をxとして計算することを勉強し始めることでしょう。

    3 + x = 8

この式において、xの値は次のように移項して計算することができるでしょう。

    x = 8 - 3
    -> x = 5

そして、さらに柔軟に、2個以上の変数を扱うことも可能になっていきます。

    x + y = 8

このとき、上の式においてxとyの値を変えていくことができて、

    x = 4
    y = 4

としても、

    x = 3
    y = 5

としても、上の等式は成立しているわけです。

同じようにして、プログラミング言語は動作します− プログラミングにおいて、変数は、その都度変化する値を格納するコンテナの役割を果たすのです。変数はあらゆる種類の値、そして、計算結果を保持することができます。変数には名前が与えられ、等号(=)で区切ってその値を指定します。変数名はどのような文字や単語を含むことが可能ですが、利用できるプログラミング言語によって他の機能のために予約されたいくつかの単語があることによる制約があることを覚えておいて下さい。

簡単のため、本記事ではJavaScriptを例としてプログラミング言語について学んでいきます(そもそも本記事自体がJavaScriptプログラミングの記事のうちの一章であるわけですが)。次の例では2つの変数を定義し、その和を計算して、その結果を3つめの変数として定義しています。

注: `<script>`タグはブラウザに対してスクリプト言語として実行するよう知らせるために用います。

``` js
<script>
var x = 5,
    y = 6,
    result = x + y;
</script>
```

 各命令がセミコロン(;)で終わるように書かれたこれらのスクリプトは、ブラウザのJavaScriptインタープリタによって逐次実行されます。セミコロンはインタープリタに対して命令の終わりであることを知らせるために書かれるもので、これは人間が扱う言語において句読点や感嘆符(!)で文章を締めくくるのと同様のものだと言えます。

これらのスクリプトを日本語で表現すると、このような感じになることでしょう:

-   ここに記述するものは、HTMLではない他の何かです:
-   xという変数を新たに定義し(`var`宣言によって表されます)、その値として5を割り当てて、命令を終了します。
-   yという変数を新たに定義し、その値として6を割り当てて、命令を終了します。
-   resultという変数を新たに定義して、xとyを加算したものをその値として割り当てて、命令を終了し、宣言全体を終了します。(ここで、インタープリタはx、yの値を確認し、その値を加算して生じる結果、すなわち11を得るという演算処理を行います。)
-   HTMLとは異なる何らかの言語はここまでであり、HTMLに戻って引き続き解釈を続けます。

2つの間に演算子を追加することで、あらゆる計算を実行することが可能です。古典的なものとして、加算するのにプラス(+)記号、減算するのにマイナス(-)記号があります。ここで、積算(かけ算)ではアスタリスク(\*)、除算(割り算)ではスラッシュ(/)を用いる必要があります。記述可能ないくつかの計算例を次に示します。二重スラッシュ(//)で始まるテキストはJavaScriptではコメントとして扱われることにご注意願います。JavaScriptインタープリタではそのようなコメント行を読み込んでも、同じ行内であればそれ以後は実行の対象から除外されます。すなわち、ブラウザに解釈させずに、人間に対して何かのコメントを示したいときにはこのようなコメント行を用います。

``` js
<script>
var x = 5,
    y = 6,
    z = 20,
    multiply = x * y * z;

// multiplyには600が代入される
var divide = x / y;
// divideには0.8333333333333334が代入される
var addAndDivide = (x + z) / y;
// addAndDivide = 4.166666666666667
var half = (y + z) / 2;
// halfには13が代入される
</script>
```

 このように、計算する際に、変数を組み合わせて使ったり他の変数と同じ値にしたり、変数を固定値として用いたりすることもできます。また、本来期待される演算順に合わせるために括弧()でグループ化することも可能です。(実際の計算では、まず括弧が優先され、その後、積算と除算、加算と減算、そして数学の授業で習うとおりの計算の仕方、の順に従って実行されます。)

### 変数の型

ところで、電卓でできることをそのままなぞるだけでは、退屈になってくるのではないでしょうか。(もっとも、電卓で5318008と入力して逆さまにすると、(英語圏の人であれば)クスクスと笑ってしまいとは思いますが。)コンピュータはより洗練されたものであり、さらに複雑な変数を扱うことができるのです。そこで本節では変数の「型」について述べます。変数には数値以外にも様々な型があり、プログラミング言語によって異なっています。一般的な型としては次のようなものがあります。

-   小数型(Float): `1.21323`, `4`, `100004` もしくは `0.123`のような数値
-   整数型(Integer): `1`, `12`, `33`, `140`のような自然数であって、`1.233`のようなものではないもの
-   文字列型(String): "`boat`", "`象`" あるいは "`おお、あなたは背が高いね!`"のような一連の文字列
-   ブール型(Boolean): `true` または `false` のどちらかの値を取り、それ以外の値を取らないもの
-   配列(Array): `1,2,3,4,'今、退屈だよ'`のように、複数の値を一つの集合としてまとめたもの
-   オブジェクト(Object): オブジェクトを表すもの。ここで、オブジェクトとは現実世界にある対象物を、プロパティとメソッドを定義することによってモデル化して扱おうとするものです。例えば、猫を、4本の脚と一つの尻尾を持ち、茶色であるcatというオブジェクトとして定義することができるでしょう。また、`purr()`というメソッドを定義することによって、ゴロゴロと鳴くという動作をオブジェクトcatに定義したり、さらには`getCheeseBurger()`というメソッドによってチーズバーガーを欲しがる動作を定義することもできます。さらに、これらのオブジェクト定義を再利用して、色が灰色という以外は同様のプロパティを持つ猫のオブジェクトを定義することもできるのです。

JavaScriptは「型の扱いが緩やかな」プログラミング言語であり、変数に格納されているデータがどのような型であるかを明示的に宣言する必要が無いという特徴があります。変数を宣言するには`var`というキーワードを先頭に記述すればよく、どのような文脈や引用でデータの型を使おうとも、ブラウザは正しく動作するようになっています。

#### 小数と整数

ここでは不思議なことや特殊なことは何もないことでしょう。変数には数値であればどのような値でも代入できます。

``` js
<script>
var fahrenheit = 123,
    celsius = (fahrenheit - 32) * 5/9,
    clue = 0.123123;
</script>
```

 小数と整数はどのような数値演算でも計算可能です。

#### ブール型(boolean)

ブール型(boolean)の値は、「イエスかノーか」という単純な定義になっています。具体的には、`true`か`false`のどちらかのキーワードが値として代入されます。

``` js
<script>
var doorClosed = true,
    catCanLeave = false;
</script>
```

#### 文字列

文字列は、一つないし複数の行で構成され、各行がどんな種類の文字でも含むことができます。JavaScriptでは、シングルクオート(*)もしくはダブルクオート("")で囲むことで文字列を定義できます。*

``` js
<script>
var surname = 'Heilmann',
    name = "Christian",
    age = '33',
    hair = 'Flickr famous';
</script>
```

 これらの文字列は、+演算子を用いて結合することができますが、減算の要領で文字列からその一部を抜き出すことはできません。文字列を書き換えるには、使っているプログラミング言語で用意されている関数を用いる必要があります。一方、シンプルな文字列の結合は次のような簡単な形で表せます。

``` js
<script>
var surname = 'Heilmann',
    name = 'Christian',
    age = '33',
    hair = 'Flickr famous',
    message = 'Hi, I am ' + name + ' ' + surname + '. ';

message += 'I am ' + age + 'years old and my hair is ' + hair;
alert(message);
</script>
```

 それでは、[文字列結合のデモ](http://dev.opera.com/articles/view/programming-the-real-basics/flickrfamous.html)を試しに動かしてみましょう。

+=演算子は、"message = message +"を短縮して書いたものです。上記の例の場合は“Hi, I am Christian Heilmann. I am 33 years old and [my hair is Flickr famous](http://flickr.com/photos/tags/thehairofchristianheilmann/)”という結果となります。

ここで見落とせない点は、結合するのか、値を足すのか、ということです。もし2つの値を足すのであれば、文字列ではなく数値であることを確かめる必要があります。例えば、[結合するのか加算なのかのデモ](http://dev.opera.com/articles/view/programming-the-real-basics/concatvsadd.html)では、異なる2つの結果が出力されます。“5”+“3”の結果は53であって8にはならないのです! 文字列から数値に変換する最も簡単な方法として、先ほどのデモ(のソースコード)のように、変数の前に"+"を記述する方法があります(訳注: ここでは `y = +y;` のようにしています)。

多くのプログラミング言語では、文字列を囲む際にシングルクオートとダブルクオートのどちらが使われているかは、組み合わせて使われない限りは区別されません。このため、文字列の終わりがどこにあるかでJavaScriptインタプリタに混乱を引き起こさないようにするためには、文字列を囲むのに使われていないクオート記号の前にバックスラッシュ(\\)を置く必要があります。

``` js
<script>
// この例では、'の後に記述されているものが何であるかを、
// インタープリタが解釈できなくなり、エラーとなります。
// 文字列に代入されるのは、'Isn'となってしまいます。
var stringWithError = 'Isn't it hard to get things right?';
// 次のように記述すれば、エラーは発生しません。
var stringWithoutError = 'Isn\'t it hard to get things right?';
</script>
```

#### 配列

配列は大変強力な構造を持っています。一つに配列には複数の値を代入することが可能で、それぞれが変数もしくは値を持ちます。次に例を示します。

``` js
<script>
var pets = new Array('Boomer','Polly','Mr.Frisky');
</script>
```

 それぞれの値には、配列内で付与されたインデックス値である、**配列の**カウンタを用いてアクセスすることが可能となっており、本の章番号を見ていくような感覚で利用することができます。具体的には、`配列名[インデックス値]`のような構文となります。上の例では、`pets[1]`の値は"Polly"となります。でもちょっと待って下さい。Pollyを表すのは、**2番目に指定された値なのだから**、`pets[2]`であるべきでは? ...答えは**ノー**なのです − コンピュータは1からではなく0から数え始めるので、カウンタは2とはならない、というわけです。このことはよく混乱や勘違いを引き起こしたりします。

配列が自動的に生成する特殊な情報として、配列の要素数を表す`length`があります。上の例では、`pets.length`の値を確認すると、実際に格納されている要素の数である3となるでしょう。

配列は、何か共通の性質のあるものをまとめて扱うのに大いに役に立つものであり、どのプログラミング言語でも、配列を操作する手軽な関数 − ソート、フィルタ、検索、など − を数多く備えています。

#### オブジェクト

順番に付与される番号ではなく、より詳細な記述で個々の要素を表してまとめたい場合は、配列ではなく、オブジェクトを生成する必要があります。JavaScriptプログラミングにおいて、オブジェクトは、人々や乗り物、道具といった現実世界にある対象物を表現したりモデル化したりしたものとして構成されます。

オブジェクトは大きくて非常に賢く、そして汎用的なプログラミングの要素であり、その扱い方を詳細に説明するには、本記事で扱える範囲としては大きくなりすぎてしまいます。ここではオブジェクトをいくつかの属性(プロパティ)を持った一つのものとして扱うこととします。まずは例として人を表すpersonというオブジェクトを扱います。このとき、様々なプロパティをドット(.)と合わせてオブジェクト名の後につなげることで定義していくことができます。

``` js
<script>
var person = new Object();
person.name = 'Chris';
person.surname = 'Heilmann';
person.age = 33;
person.hair = 'Flickr famous';
</script>
```

 プロパティの内容は、ドットに続けて記述するか(`person.age`であれば33)、大括弧([])で囲んで記述するか(`person['name']`であれば“Chris”)のいずれかの方法で取得することができます。JavaScriptオブジェクトの詳細については、本コースで後ほどより詳細に学びます。

以上が、様々な型の変数に関する概要となります。プログラミングにおけるもう一つの大きな要素として、プログラムの構造とロジックの組み立てがあります。これらについては、さらに2つのプログラミングにおける概念、条件文と繰り返しが必要となってきます。

## 条件文

条件文は、何がどうなっているかをテストするために用いられます。この条件文は、いくつかの使い方において、プログラミングの大変重要な役割を果たします。

何よりもまず、条件文は、どのようなデータが処理中に渡されてもプログラムが動作することを保証するためにもちいられます。もしデータの内容を盲目的に信頼してしまうと、問題が発生してプログラムは誤動作を引き起こすでしょう。もしどうしたいか、および、必要な全ての情報が正しいフォーマットで得られているかどうかをテストすることができるのであれば、プログラムは遙かに安定して動作することでしょう。このように用心して進める手法は、防御的プログラミングと呼ばれています。

もう一つ、条件文は分岐を可能とします。例えば、申し込みフォームを提出するようなプログラムの場合、その動作が枝分かれになるような構成になるのではないでしょうか。このような場合、初歩的な対処として、条件文に合致するか否かによって、異なる分岐先のコードを実行することとなります。

最も簡単な条件文は`if`文で、`if (条件文) { 処理 … }`のような構文で記述します。ここでは、条件文が成立する場合に、中括弧({})で囲まれた箇所に書かれたコードが実行されます。次の例では、文字列の内容をテストして、その値に応じて別の文字列を代入します。

``` js
<script>
var country = 'France',
    weather,
    food,
    currency,
    message;

if (country === 'England') {
  weather = 'horrible';
  food = 'filling';
  currency = 'pound sterling';
}

if (country === 'France') {
  weather = 'nice';
  food = 'stunning, but hardly ever vegetarian';
  currency = 'funny, small and colourful';
}

if (country === 'Germany') {
  weather = 'average';
  food = 'wurst thing ever';
  currency = 'funny, small and colourful';
}

message = 'this is ' + country + ', the weather is ' + weather + ', the food is ' + food + ' and the ' + 'currency is ' + currency;
alert(message);
</script>
```

 それでは各自で[if文による気候を確認するサンプル](http://dev.opera.com/articles/view/programming-the-real-basics/weather.html)を試してみて下さい。変数countryの値を変えると異なる文章が表示されるのが確認できることでしょう。

条件文を記述する部分には、等号(=)が3個連なっていますが、これは、値だけではなく、データの型も合致しているかどうかをテストするための条件文であることを表すものです。2つの連なる等号(すなわち==)でも、条件文の内容をテストすることはできますが、この場合、`if (x == 5)`と宣言したとき、xの値が数値の5であっても文字列"5"であっても、条件文のテストの結果は合致(true)という結果になります。プログラムがどのように挙動するものであるかによって、このことは違う結果をもたらします。

条件文を用いたテストには、他には次のようなものがあります。

-   x \> 0 - xは0より大きいか?
-   x \< 0 - xは0より小さいか?
-   x \<= 4 - xは0以下か?
-   x != 'hello' - xは文字列'hello'と違っているか?
-   x - 変数xは存在するか(定義済みか)?

条件文は入れ子にすることもできます。次の例では、上の例に対して、変数countryに値が代入されているかどうかを確認する場合の対処について示しています。

``` js
<script>
var country = 'Germany',
    weather,
    food,
    currency,
    message;

if (country) {
    if (country == 'England') {
        weather = 'horrible';
        food = 'filling';
        currency = 'pound sterling';
    }

    if (country == 'France') {
        weather = 'nice';
        food = 'stunning, but hardly ever vegetarian';
        currency = 'funny, small and colourful';
    }

    if (country == 'Germany') {
        weather = 'average';
        food = 'wurst thing ever';
        currency = 'funny, small and colourful';
    }

    message = 'this is ' + country + ', the weather is ' + weather + ', the food is ' + food + ' and the ' + 'currency is ' + currency;
    alert(message);
}
</script>
```

 それでは、[if文で安全に気候を確認するサンプル](http://dev.opera.com/articles/view/programming-the-real-basics/saferweather.html)を試してみて下さい。変数countryの値を変えると異なる文章が表示されるのが確認できることでしょう。

一方、先に示した(変数countryの内容をテストしない)例では、変数countryに代入された値に対する処理が定義済みであるかどうかにかかわらず、必ず何かしらの文章を表示しようとします。従って、エラーとなるか、もしくは“this is **undefined**, the weather...”のように表示してしまいます。後者のサンプルではより安全に動作し、もし変数countryが未定義であれば何もしないようになっています。

さらに、複数の条件を"or"や"and"で組み合わせることで、どちらかの条件がtrue、もしくは両方がtrueになっているかどうかをテストすることができます。JavaScriptでは、"or"は||、"and"は&&で記述することができます。変数xの値が10から20までの間であるかどうかをテストするには、条件文として`if(x > 10 && x < 20)`と記述すればよいのです。また、変数countryの値が"England"か"Germany"のどちらかであるかどうかを確かめるには、条件文として`if(country == 'England' || country == 'Germany')と記述すればよいことになります。`

また、\<code\>else節を記述すると、最初に記述した条件文が不成立の場合に適用される処理となります。これは、どんな値の場合でも対応しながら、ある特定の値に限って特別な対処を行いたい場合に、非常に有用です。

    <script type="text/javascript">
      var umbrellaMandatory;
      if(country == 'England'){
        umbrellaMandatory = true;
      } else {
        umbrellaMandatory = false;
      }
    </script>

条件文はとても役に立つものですが、使い道は少し限られています。もし何か繰り返して実行したい処理がある場合はどうすればよいでしょうか? 例えば配列の各要素の値に対して段落タグ(\<p\>〜\</p\>)を付け加えたい場合はどうでしょうか? 条件文だけで対処するのであれば、次のように、異なる配列の要素数に対してそれぞれ処理を固定的に記述する羽目に陥ってしまうことでしょう。

    <script type="text/javascript">
      var names = new Array('Chris','Dion','Ben','Brendan');
      var all = names.length;
      if(all == 1){
        names[0] = '<p>' + names[0] + '</p>';
      }
      if(all == 2){
        names[0] = '<p>' + names[0] + '</p>';
        names[1] = '<p>' + names[1] + '</p>';
      }
      if(all == 3){
        names[0] = '<p>' + names[0] + '</p>';
        names[1] = '<p>' + names[1] + '</p>';
        names[2] = '<p>' + names[2] + '</p>';
      }
      if(all == 4){
        names[0] = '<p>' + names[0] + '</p>';
        names[1] = '<p>' + names[1] + '</p>';
        names[2] = '<p>' + names[2] + '</p>';
        names[3] = '<p>' + names[3] + '</p>';
      }
    </script>

これではあまりにも大変な上に柔軟性に欠けてしまいます。プログラミングとは身の回りのことをより便利にするものですし、かといって人間が同じコードを何度も繰り返し書いてしまっては間違いの原因となりかねません。よりよいプログラミングとは機械に対して退屈な作業をしなくて済むようにして、人間にとって本当に成し遂げたいことだけに集中できるようにするものであるはずです。

この例の場合、条件文の代わりに、どのような要素数を持っていても配列の各要素に対して同じ処理を正確に繰り返すことのできる、**繰り返し**処理が必要になります。次節では繰り返しを用いて上の例を作り直したものを示します − これらの2つの例を比較すると、繰り返しを用いた方がより手短になることがわかることでしょう。

## 繰り返し

繰り返し処理では、一つの変数の値を変化させながら、同じ条件式を繰り返し判定します。最も簡単な繰り返しとして`for`文があります。構文は`if`文に似ていますが、2つのオプションが付け加わります。

    for(条件文;終了条件文;更新){
      // do it, do it now
    }

`for`を使って繰り返し処理を行うには、通常は繰り返して実行したいコードを中括弧({})で囲みます。ここで、反復して用いる変数を定義して、繰り返し処理の中で値を変化させ続けて、その値が終了条件文に合致するまで繰り返すようにします(合致したとき、インタプリタは繰り返し処理から抜け出して、繰り返し処理の次に記述されたコードから実行するように移ります)。次に例を示します。

    <script type="text/javascript" charset="utf-8">
      for(var i = 0;i < 11;i = i + 1){
        // do it, do it now
      }
    </script>

この例では、変数`i`の値を最初に0として、11になるまで(すなわち11より小さいうちは)その値を確かめるように処理を定義しています。更新を行う代入式 − `i = i + 1` − では、変数`i`の値を1増加させて、その上で繰り返し処理を継続して反復していきます。すなわち、これによって11回の繰り返しが行われます。もし`i`の値を2増加させるのであれば、繰り返しは6回となります。

    <script type="text/javascript">
      for(var i = 0;i < 11;i = i + 2){
        // do it, do it now
      }
    </script>

前節で示した条件文を用いた例を 繰り返し処理に置き換えると、次のようにより短くよりシンプルなものになります。

    <script type="text/javascript">
      var names = new Array('Chris','Dion','Ben','Brendan');
      var all = names.length;
      for(var i=0;i<all;i=i+1){
        names[i] = '<p>' + names[i] + '</p>';
      }
    </script>

なお、ここでは変数`i`の値は繰り返し処理内で配列のカウンタとして用いています。以上が、繰り返しを用いた効果なのです − 同じことを繰り返し実行できるだけではなく、何回繰り返しが行われたかを把握するためにも利用できるのです。

## See also

### 練習問題

-   次のコードを実行するとなぜエラーになるのですか? − `var x = hello world`
-   次のコードは正しいですか? − `var x = 'elephant';var y = "mouse";`
-   次の条件式はどのような条件をテストするものですか? `if(x > 10 && x < 20 && x !== 13 && y < 10)`
-   次の条件式はどのような結果となりますか? `if(b < 10 && b > 20)`?
-   要素として“peter”,“paul”,“mary”,“paddington bear”,“mr.ben”,“zippy” そして “bagpuss” を含む配列に対して繰り返し処理を行い、これらのうち奇数番目の要素それぞれに対して、"odd"というクラス名を付与した段落タグ(\<p\>〜\</p\>)を付与する処理を作成して下さい。 ヒント: 1個おきに要素をテストするには、モジュロ演算(割り算の剰余の計算)を`i % 2 == 0`の要領で利用します。

<table class="nmbox {{{class}}}" style>
<tr>
<th class="mbox-image" style>
**言語:**

</th>
<td class="mbox-text">
**[English](/concepts/programming/programming_basics)** • <span lang="ja">**日本語**</span>

</td>
</tr>
</table>
