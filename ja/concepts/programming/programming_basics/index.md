{{Page_Title|プログラミングの基礎}}
{{Flags}}
{{API_Name}}
{{Languages}}
{{Summary_Section|※ 本記事はまだ試験的に作成しているものである点にご注意願います。

本記事では、JavaScriptを例として、プログラミングの基礎的な原則について述べます。
}}
{{Concept_Page
|Content=== はじめに ==

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
 


Arrays are very powerful constructs. An array is a collection of values, and each of the values can be a variable, or a real value. For example:
 
<source lang="javascript">
<script>
var pets = new Array('Boomer','Polly','Mr.Frisky');
</script>
</source>
 
You can access each of the values with the '''array''' counter, which is the index number in the array—think of it as being like looking up chapters in a book. The syntax is <code>arrayname[index]</code>. So for example <code>pets[1]</code> would give you the string “Polly”. But wait! I hear you ask—shouldn’t it be <code>pets[2]</code> for Polly, given that it is the '''second''' value in the array? '''No'''—the counter is not 2, as computers start counting at 0, not at 1! This is a very common cause of confusion and errors.
 
Arrays automatically get a special information source for you: <code>length</code>. If you check the value of <code>pets.length</code> you will get 3 as there are 3 items in this array.
 
Arrays are great for describing collections of things that have something in common, and every language comes with dozens of handy functions to manipulate them—sorting, filtering, searching and so on.
  

}}
{{Examples_Section
|Not_required=Yes
|Examples=
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{See_Also_Section}}
{{Topics}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}