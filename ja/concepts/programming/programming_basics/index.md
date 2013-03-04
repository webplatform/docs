{{Page_Title|プログラミングの基礎}}
{{Flags}}
{{Summary_Section|※ 本記事はまだ試験的に作成しているものである点にご注意願います。

本記事では、JavaScriptを例として、プログラミングの基礎的な原則について述べます。
}}
{{Guide
|Content=== はじめに ==
<!-- サンプルコードはリンク先の実行用サンプルコードとの矛盾を防ぐために翻訳しないまま残している箇所がありますので、ご注意下さい。 -->
経験を積んだプログラマは、遅かれ早かれ、全く技術に詳しくない人々からは、まるで黒魔術でも扱っているかのごとく見られるようになっていくものです。逆の立場から見れば、技術に詳しくない人にとって、もし力を貸してくれている人がいたとしても、何をどうしているのかが伝わらないままであれば、そのうちついて行けなくなってしまいます。[http://www.w3.org/wiki/Web_Standards_Curriculum Web Standards Curriculum]は、プログラミングとは何かを簡単な言葉で説明しており、経験を積んだプログラマにも技術に詳しくない人にもどちらにもわかりやすい内容となっています。

JavaScriptプログラミングの仕方を学ぶ前には必須となる全般的なプログラミングの原則を基礎として固めておくこともまた、初心者のWeb開発者にとっては大変有益となります。一見退屈と思えるかもしれませんが、ご安心下さい。初めのうちに基礎的な原則を踏まえておけば、(ここは大きな声で)後々きっと強固で力強く、創造的な力として、あなたの身になることでしょう。プログラミングの基礎は、特定のプログラミング言語(もちろん、ここではJavaScript)を使ってみる前に習得しておくことが重要なのです。

== まずは触ってみよう ==

プログラミングの基礎を学ぶ上での第一歩は、試しにコマンドを入力して実行、その結果として何が出力されるかを見ることです。プログラミングとは数学と言語の組み合わせのように成り立っており、すなわち、コンピュータに解かせたい計算を正しい文法で順番通りに記述し、コンピュータに渡す作業であると言えます。プログラミングにおいて文法(grammar)とは、何をどういう並びで記述しなければならないといった構文(syntax)を定義するものであり、プログラミング言語によって大幅に異なっています。

例として、次のような2つの簡単なコードを示します。これらは全く同じように動作しますが、前者はJavaScript、後者はPHPで書かれています。

<source lang="javascript">
var fahrenheit = prompt('Enter temperature in Fahrenheit', 0);
var celsius = (fahrenheit - 32) * 5 / 9;
alert(celsius);
</source>

<source lang="php">
$fahrenheit = $_GET['fahrenheit'];
$celsius = ($fahrenheit - 32) * 5 / 9;
echo $celsius;
</source>

それでは、JavaScriptによる[http://dev.opera.com/articles/view/programming-the-real-basics/fahrenheit.html 華氏(℉)から摂氏(℃)への変換サンプル]を試しに動かしてみましょう。

これらのプログラミング言語がコンピュータに解釈されると、何らかの動作や結果が生じます。JavaScriptといったプログラミング言語はWebブラウザが解釈することができます。すなわち、ブラウザに「何かをさせる」には、JavaScriptでその動作をHTML文書の中に記述して、ブラウザで開けばよいのです。一方、他のプログラミング言語では、実行可能にするために一度変換(コンパイル)するといった作業が必要となります。コンピュータは深掘りすると0と1の2つを理解するだけで動作していることになりますが、様々な動作を実現するために多様なレベルの言語が存在しているのです。

== 変数 ==

プログラミングについて理解を進める第一歩は、数学の使い方に立ち返ることです。恐らく学校で学んだことを思い出してみると、次のような式を書くことから数学が始まったのではないでしょうか。

<pre>3 + 5 = 8</pre>
 
続いて、例えば次のように未知の値をxとして計算することを勉強し始めることでしょう。

<pre>3 + x = 8</pre>

この式において、xの値は次のように移項して計算することができるでしょう。
 
<pre>x = 8 - 3 
-&gt; x = 5</pre>

そして、さらに柔軟に、2個以上の変数を扱うことも可能になっていきます。
 
<pre>x + y = 8</pre>

このとき、上の式においてxとyの値を変えていくことができて、
 
<pre>x = 4
y = 4</pre>
 
としても、
 
<pre>x = 3
y = 5</pre>

としても、上の等式は成立しているわけです。

同じようにして、プログラミング言語は動作します− プログラミングにおいて、変数は、その都度変化する値を格納するコンテナの役割を果たすのです。変数はあらゆる種類の値、そして、計算結果を保持することができます。変数には名前が与えられ、等号(=)で区切ってその値を指定します。変数名はどのような文字や単語を含むことが可能ですが、利用できるプログラミング言語によって他の機能のために予約されたいくつかの単語があることによる制約があることを覚えておいて下さい。

簡単のため、本記事ではJavaScriptを例としてプログラミング言語について学んでいきます(そもそも本記事自体がJavaScriptプログラミングの記事のうちの一章であるわけですが)。次の例では2つの変数を定義し、その和を計算して、その結果を3つめの変数として定義しています。

注: <code>&lt;script&gt;</code>タグはブラウザに対してスクリプト言語として実行するよう知らせるために用います。

<source lang="javascript">
<script>
var x = 5,
    y = 6,
    result = x + y;
</script>
</source>
 
各命令がセミコロン(;)で終わるように書かれたこれらのスクリプトは、ブラウザのJavaScriptインタープリタによって逐次実行されます。セミコロンはインタープリタに対して命令の終わりであることを知らせるために書かれるもので、これは人間が扱う言語において句読点や感嘆符(!)で文章を締めくくるのと同様のものだと言えます。

<!-- 原文では英語を例にしていますが、ここでは日本語に置き換えています。 -->
これらのスクリプトを日本語で表現すると、このような感じになることでしょう:

* ここに記述するものは、HTMLではない他の何かです:
* xという変数を新たに定義し(<code>var</code>宣言によって表されます)、その値として5を割り当てて、命令を終了します。
* yという変数を新たに定義し、その値として6を割り当てて、命令を終了します。
* resultという変数を新たに定義して、xとyを加算したものをその値として割り当てて、命令を終了し、宣言全体を終了します。(ここで、インタープリタはx、yの値を確認し、その値を加算して生じる結果、すなわち11を得るという演算処理を行います。)
* HTMLとは異なる何らかの言語はここまでであり、HTMLに戻って引き続き解釈を続けます。

2つの間に演算子を追加することで、あらゆる計算を実行することが可能です。古典的なものとして、加算するのにプラス(+)記号、減算するのにマイナス(-)記号があります。ここで、積算(かけ算)ではアスタリスク(*)、除算(割り算)ではスラッシュ(/)を用いる必要があります。記述可能ないくつかの計算例を次に示します。二重スラッシュ(//)で始まるテキストはJavaScriptではコメントとして扱われることにご注意願います。JavaScriptインタープリタではそのようなコメント行を読み込んでも、同じ行内であればそれ以後は実行の対象から除外されます。すなわち、ブラウザに解釈させずに、人間に対して何かのコメントを示したいときにはこのようなコメント行を用います。

<source lang="javascript">
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
</source>

このように、計算する際に、変数を組み合わせて使ったり他の変数と同じ値にしたり、変数を固定値として用いたりすることもできます。また、本来期待される演算順に合わせるために括弧()でグループ化することも可能です。(実際の計算では、まず括弧が優先され、その後、積算と除算、加算と減算、そして数学の授業で習うとおりの計算の仕方、の順に従って実行されます。)

=== 変数の型 ===
 
ところで、電卓でできることをそのままなぞるだけでは、退屈になってくるのではないでしょうか。(もっとも、電卓で5318008と入力して逆さまにすると、(英語圏の人であれば)クスクスと笑ってしまいとは思いますが。)コンピュータはより洗練されたものであり、さらに複雑な変数を扱うことができるのです。そこで本節では変数の「型」について述べます。変数には数値以外にも様々な型があり、プログラミング言語によって異なっています。一般的な型としては次のようなものがあります。
 
* 小数型(Float): <code>1.21323</code>, <code>4</code>, <code>100004</code> もしくは <code>0.123</code>のような数値
* 整数型(Integer): <code>1</code>, <code>12</code>, <code>33</code>, <code>140</code>のような自然数であって、<code>1.233</code>のようなものではないもの
* 文字列型(String): "<code>boat</code>", "<code>象</code>" あるいは "<code>おお、あなたは背が高いね!</code>"のような一連の文字列
* ブール型(Boolean): <code>true</code> または <code>false</code> のどちらかの値を取り、それ以外の値を取らないもの
* 配列(Array): <code>1,2,3,4,'今、退屈だよ'</code>のように、複数の値を一つの集合としてまとめたもの
* オブジェクト(Object): オブジェクトを表すもの。ここで、オブジェクトとは現実世界にある対象物を、プロパティとメソッドを定義することによってモデル化して扱おうとするものです。例えば、猫を、4本の脚と一つの尻尾を持ち、茶色であるcatというオブジェクトとして定義することができるでしょう。また、<code>purr()</code>というメソッドを定義することによって、ゴロゴロと鳴くという動作をオブジェクトcatに定義したり、さらには<code>getCheeseBurger()</code>というメソッドによってチーズバーガーを欲しがる動作を定義することもできます。さらに、これらのオブジェクト定義を再利用して、色が灰色という以外は同様のプロパティを持つ猫のオブジェクトを定義することもできるのです。

JavaScriptは「型の扱いが緩やかな」プログラミング言語であり、変数に格納されているデータがどのような型であるかを明示的に宣言する必要が無いという特徴があります。変数を宣言するには<code>var</code>というキーワードを先頭に記述すればよく、どのような文脈や引用でデータの型を使おうとも、ブラウザは正しく動作するようになっています。

==== 小数と整数 ====

ここでは不思議なことや特殊なことは何もないことでしょう。変数には数値であればどのような値でも代入できます。
  
<source lang="javascript">
<script>
var fahrenheit = 123,
    celsius = (fahrenheit - 32) * 5/9,
    clue = 0.123123;
</script>
</source>

小数と整数はどのような数値演算でも計算可能です。

==== ブール型(boolean) ====

ブール型(boolean)の値は、「イエスかノーか」という単純な定義になっています。具体的には、<code>true</code>か<code>false</code>のどちらかのキーワードが値として代入されます。
 
<source lang="javascript">
<script>
var doorClosed = true,
    catCanLeave = false;
</script>
</source>

==== 文字列 ====
 
文字列は、一つないし複数の行で構成され、各行がどんな種類の文字でも含むことができます。JavaScriptでは、シングルクオート('')もしくはダブルクオート("")で囲むことで文字列を定義できます。
 
<source lang="javascript">
<script>
var surname = 'Heilmann',
    name = "Christian",
    age = '33',
    hair = 'Flickr famous';
</script>
</source>

これらの文字列は、+演算子を用いて結合することができますが、減算の要領で文字列からその一部を抜き出すことはできません。文字列を書き換えるには、使っているプログラミング言語で用意されている関数を用いる必要があります。一方、シンプルな文字列の結合は次のような簡単な形で表せます。
 
<source lang="javascript">
<script>
var surname = 'Heilmann',
    name = 'Christian',
    age = '33',
    hair = 'Flickr famous',
    message = 'Hi, I am ' + name + ' ' + surname + '. ';

message += 'I am ' + age + 'years old and my hair is ' + hair;
alert(message);
</script>
</source>
 
それでは、[http://dev.opera.com/articles/view/programming-the-real-basics/flickrfamous.html 文字列結合のデモ]を試しに動かしてみましょう。

+=演算子は、"message = message +"を短縮して書いたものです。上記の例の場合は“Hi, I am Christian Heilmann. I am 33 years old and [http://flickr.com/photos/tags/thehairofchristianheilmann/ my hair is Flickr famous]”という結果となります。
 
ここで見落とせない点は、結合するのか、値を足すのか、ということです。もし2つの値を足すのであれば、文字列ではなく数値であることを確かめる必要があります。例えば、[http://dev.opera.com/articles/view/programming-the-real-basics/concatvsadd.html 結合するのか加算なのかのデモ]では、異なる2つの結果が出力されます。“5”+“3”の結果は53であって8にはならないのです! 文字列から数値に変換する最も簡単な方法として、先ほどのデモ(のソースコード)のように、変数の前に"+"を記述する方法があります(訳注: ここでは <code>y = +y;</code> のようにしています)。
 
多くのプログラミング言語では、文字列を囲む際にシングルクオートとダブルクオートのどちらが使われているかは、組み合わせて使われない限りは区別されません。このため、文字列の終わりがどこにあるかでJavaScriptインタプリタに混乱を引き起こさないようにするためには、文字列を囲むのに使われていないクオート記号の前にバックスラッシュ(\)を置く必要があります。
 
<source lang="javascript">
<script>
// この例では、'の後に記述されているものが何であるかを、
// インタープリタが解釈できなくなり、エラーとなります。
// 文字列に代入されるのは、'Isn'となってしまいます。
var stringWithError = 'Isn't it hard to get things right?';
// 次のように記述すれば、エラーは発生しません。
var stringWithoutError = 'Isn\'t it hard to get things right?';
</script>
</source>

==== 配列 ====
 
配列は大変強力な構造を持っています。一つに配列には複数の値を代入することが可能で、それぞれが変数もしくは値を持ちます。次に例を示します。

<source lang="javascript">
<script>
var pets = new Array('Boomer','Polly','Mr.Frisky');
</script>
</source>

それぞれの値には、配列内で付与されたインデックス値である、'''配列の'''カウンタを用いてアクセスすることが可能となっており、本の章番号を見ていくような感覚で利用することができます。具体的には、<code>配列名[インデックス値]</code>のような構文となります。上の例では、<code>pets[1]</code>の値は"Polly"となります。でもちょっと待って下さい。Pollyを表すのは、'''2番目に指定された値なのだから'''、<code>pets[2]</code>であるべきでは? ...答えは'''ノー'''なのです − コンピュータは1からではなく0から数え始めるので、カウンタは2とはならない、というわけです。このことはよく混乱や勘違いを引き起こしたりします。

配列が自動的に生成する特殊な情報として、配列の要素数を表す<code>length</code>があります。上の例では、<code>pets.length</code>の値を確認すると、実際に格納されている要素の数である3となるでしょう。

配列は、何か共通の性質のあるものをまとめて扱うのに大いに役に立つものであり、どのプログラミング言語でも、配列を操作する手軽な関数 − ソート、フィルタ、検索、など − を数多く備えています。

==== オブジェクト ====
 
順番に付与される番号ではなく、より詳細な記述で個々の要素を表してまとめたい場合は、配列ではなく、オブジェクトを生成する必要があります。JavaScriptプログラミングにおいて、オブジェクトは、人々や乗り物、道具といった現実世界にある対象物を表現したりモデル化したりしたものとして構成されます。

オブジェクトは大きくて非常に賢く、そして汎用的なプログラミングの要素であり、その扱い方を詳細に説明するには、本記事で扱える範囲としては大きくなりすぎてしまいます。ここではオブジェクトをいくつかの属性(プロパティ)を持った一つのものとして扱うこととします。まずは例として人を表すpersonというオブジェクトを扱います。このとき、様々なプロパティをドット(.)と合わせてオブジェクト名の後につなげることで定義していくことができます。
 
<source lang="javascript">
<script>
var person = new Object();
person.name = 'Chris';
person.surname = 'Heilmann';
person.age = 33;
person.hair = 'Flickr famous';
</script>
</source>

プロパティの内容は、ドットに続けて記述するか(<code>person.age</code>であれば33)、大括弧([])で囲んで記述するか(<code>person['name']</code>であれば“Chris”)のいずれかの方法で取得することができます。JavaScriptオブジェクトの詳細については、本コースで後ほどより詳細に学びます。

以上が、様々な型の変数に関する概要となります。プログラミングにおけるもう一つの大きな要素として、プログラムの構造とロジックの組み立てがあります。これらについては、さらに2つのプログラミングにおける概念、条件文と繰り返しが必要となってきます。

== 条件文 ==
 
条件文は、何がどうなっているかをテストするために用いられます。この条件文は、いくつかの使い方において、プログラミングの大変重要な役割を果たします。

何よりもまず、条件文は、どのようなデータが処理中に渡されてもプログラムが動作することを保証するためにもちいられます。もしデータの内容を盲目的に信頼してしまうと、問題が発生してプログラムは誤動作を引き起こすでしょう。もしどうしたいか、および、必要な全ての情報が正しいフォーマットで得られているかどうかをテストすることができるのであれば、プログラムは遙かに安定して動作することでしょう。このように用心して進める手法は、防御的プログラミングと呼ばれています。
 
もう一つ、条件文は分岐を可能とします。例えば、申し込みフォームを提出するようなプログラムの場合、その動作が枝分かれになるような構成になるのではないでしょうか。このような場合、初歩的な対処として、条件文に合致するか否かによって、異なる分岐先のコードを実行することとなります。
 
最も簡単な条件文は<code>if</code>文で、<code>if (条件文) { 処理 … }</code>のような構文で記述します。ここでは、条件文が成立する場合に、中括弧({})で囲まれた箇所に書かれたコードが実行されます。次の例では、文字列の内容をテストして、その値に応じて別の文字列を代入します。
 
<source lang="javascript">
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
</source>
 
それでは各自で[http://dev.opera.com/articles/view/programming-the-real-basics/weather.html if文による気候を確認するサンプル]を試してみて下さい。変数countryの値を変えると異なる文章が表示されるのが確認できることでしょう。

条件文を記述する部分には、等号(=)が3個連なっていますが、これは、値だけではなく、データの型も合致しているかどうかをテストするための条件文であることを表すものです。2つの連なる等号(すなわち==)でも、条件文の内容をテストすることはできますが、この場合、<code>if (x == 5)</code>と宣言したとき、xの値が数値の5であっても文字列"5"であっても、条件文のテストの結果は合致(true)という結果になります。プログラムがどのように挙動するものであるかによって、このことは違う結果をもたらします。

条件文を用いたテストには、他には次のようなものがあります。
 
* x &gt; 0 - xは0より大きいか?
* x &lt; 0 - xは0より小さいか?
* x &lt;= 4 - xは0以下か?
* x != 'hello' - xは文字列'hello'と違っているか?
* x - 変数xは存在するか(定義済みか)?

条件文は入れ子にすることもできます。次の例では、上の例に対して、変数countryに値が代入されているかどうかを確認する場合の対処について示しています。

<source lang="javascript">
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
</source>

それでは、[http://dev.opera.com/articles/view/programming-the-real-basics/saferweather.html if文で安全に気候を確認するサンプル]を試してみて下さい。変数countryの値を変えると異なる文章が表示されるのが確認できることでしょう。

一方、先に示した(変数countryの内容をテストしない)例では、変数countryに代入された値に対する処理が定義済みであるかどうかにかかわらず、必ず何かしらの文章を表示しようとします。従って、エラーとなるか、もしくは“this is '''undefined''', the weather...”のように表示してしまいます。後者のサンプルではより安全に動作し、もし変数countryが未定義であれば何もしないようになっています。

さらに、複数の条件を"or"や"and"で組み合わせることで、どちらかの条件がtrue、もしくは両方がtrueになっているかどうかをテストすることができます。JavaScriptでは、"or"は<nowiki>||</nowiki>、"and"は&amp;&amp;で記述することができます。変数xの値が10から20までの間であるかどうかをテストするには、条件文として<code>if(x &gt; 10 &amp;&amp; x &lt; 20)</code>と記述すればよいのです。また、変数countryの値が"England"か"Germany"のどちらかであるかどうかを確かめるには、条件文として<code>if(country == 'England' <nowiki>||</nowiki> country == 'Germany')と記述すればよいことになります。

また、<code>else</code>節を記述すると、最初に記述した条件文が不成立の場合に適用される処理となります。これは、どんな値の場合でも対応しながら、ある特定の値に限って特別な対処を行いたい場合に、非常に有用です。

<pre>&lt;script type="text/javascript"&gt;
  var umbrellaMandatory;
  if(country == 'England'){
    umbrellaMandatory = true;
  } else {
    umbrellaMandatory = false;
  }
&lt;/script&gt;</pre>

条件文はとても役に立つものですが、使い道は少し限られています。もし何か繰り返して実行したい処理がある場合はどうすればよいでしょうか? 例えば配列の各要素の値に対して段落タグ(&lt;p&gt;〜&lt;/p&gt;)を付け加えたい場合はどうでしょうか? 条件文だけで対処するのであれば、次のように、異なる配列の要素数に対してそれぞれ処理を固定的に記述する羽目に陥ってしまうことでしょう。
 
<pre>&lt;script type="text/javascript"&gt;
  var names = new Array('Chris','Dion','Ben','Brendan');
  var all = names.length;
  if(all == 1){
    names[0] = '&lt;p&gt;' + names[0] + '&lt;/p&gt;';
  }
  if(all == 2){
    names[0] = '&lt;p&gt;' + names[0] + '&lt;/p&gt;';
    names[1] = '&lt;p&gt;' + names[1] + '&lt;/p&gt;';
  }
  if(all == 3){
    names[0] = '&lt;p&gt;' + names[0] + '&lt;/p&gt;';
    names[1] = '&lt;p&gt;' + names[1] + '&lt;/p&gt;';
    names[2] = '&lt;p&gt;' + names[2] + '&lt;/p&gt;';
  }
  if(all == 4){
    names[0] = '&lt;p&gt;' + names[0] + '&lt;/p&gt;';
    names[1] = '&lt;p&gt;' + names[1] + '&lt;/p&gt;';
    names[2] = '&lt;p&gt;' + names[2] + '&lt;/p&gt;';
    names[3] = '&lt;p&gt;' + names[3] + '&lt;/p&gt;';
  }
&lt;/script&gt;</pre>

これではあまりにも大変な上に柔軟性に欠けてしまいます。プログラミングとは身の回りのことをより便利にするものですし、かといって人間が同じコードを何度も繰り返し書いてしまっては間違いの原因となりかねません。よりよいプログラミングとは機械に対して退屈な作業をしなくて済むようにして、人間にとって本当に成し遂げたいことだけに集中できるようにするものであるはずです。
 
この例の場合、条件文の代わりに、どのような要素数を持っていても配列の各要素に対して同じ処理を正確に繰り返すことのできる、'''繰り返し'''処理が必要になります。次節では繰り返しを用いて上の例を作り直したものを示します − これらの2つの例を比較すると、繰り返しを用いた方がより手短になることがわかることでしょう。

== 繰り返し ==

繰り返し処理では、一つの変数の値を変化させながら、同じ条件式を繰り返し判定します。最も簡単な繰り返しとして<code>for</code>文があります。構文は<code>if</code>文に似ていますが、2つのオプションが付け加わります。
 
<pre>for(条件文;終了条件文;更新){
  // do it, do it now
}</pre>

<code>for</code>を使って繰り返し処理を行うには、通常は繰り返して実行したいコードを中括弧({})で囲みます。ここで、反復して用いる変数を定義して、繰り返し処理の中で値を変化させ続けて、その値が終了条件文に合致するまで繰り返すようにします(合致したとき、インタプリタは繰り返し処理から抜け出して、繰り返し処理の次に記述されたコードから実行するように移ります)。次に例を示します。
 
<pre>&lt;script type="text/javascript" charset="utf-8"&gt;
  for(var i = 0;i &lt; 11;i = i + 1){
    // do it, do it now
  }
&lt;/script&gt;</pre>

この例では、変数<code>i</code>の値を最初に0として、11になるまで(すなわち11より小さいうちは)その値を確かめるように処理を定義しています。更新を行う代入式 − <code>i = i + 1</code> − では、変数<code>i</code>の値を1増加させて、その上で繰り返し処理を継続して反復していきます。すなわち、これによって11回の繰り返しが行われます。もし<code>i</code>の値を2増加させるのであれば、繰り返しは6回となります。
 
<pre>&lt;script type="text/javascript"&gt;
  for(var i = 0;i &lt; 11;i = i + 2){
    // do it, do it now
  }
&lt;/script&gt;</pre>

前節で示した条件文を用いた例を 繰り返し処理に置き換えると、次のようにより短くよりシンプルなものになります。
 
<pre>&lt;script type="text/javascript"&gt;
  var names = new Array('Chris','Dion','Ben','Brendan');
  var all = names.length;
  for(var i=0;i&lt;all;i=i+1){
    names[i] = '&lt;p&gt;' + names[i] + '&lt;/p&gt;';
  }
&lt;/script&gt;</pre>

なお、ここでは変数<code>i</code>の値は繰り返し処理内で配列のカウンタとして用いています。以上が、繰り返しを用いた効果なのです − 同じことを繰り返し実行できるだけではなく、何回繰り返しが行われたかを把握するためにも利用できるのです。

}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section
|Manual_sections==== 練習問題 ===
 
* 次のコードを実行するとなぜエラーになるのですか? − <code>var x = hello world</code>
* 次のコードは正しいですか? − <code>var x = 'elephant';var y = "mouse";</code>
* 次の条件式はどのような条件をテストするものですか? <code>if(x &gt; 10 &amp;&amp; x &lt; 20 &amp;&amp; x !== 13 &amp;&amp; y &lt; 10)</code>
* 次の条件式はどのような結果となりますか? <code>if(b &lt; 10 &amp;&amp; b &gt; 20)</code>?
* 要素として“peter”,“paul”,“mary”,“paddington bear”,“mr.ben”,“zippy” そして “bagpuss” を含む配列に対して繰り返し処理を行い、これらのうち奇数番目の要素それぞれに対して、"odd"というクラス名を付与した段落タグ(&lt;p&gt;〜&lt;/p&gt;)を付与する処理を作成して下さい。 ヒント: 1個おきに要素をテストするには、モジュロ演算(割り算の剰余の計算)を<code>i % 2 == 0</code>の要領で利用します。
}}
{{Topics|JavaScript}}
{{External_Attribution
|Is_CC-BY-SA=No
|Sources=DevOpera
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{WPDLanguages}}