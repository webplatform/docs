{{Page_Title|プログラミングの基礎}}
{{Flags}}
{{API_Name}}
{{Summary_Section|※ 本記事はまだ編集中であり、編集の都合上、未完成のまま投稿されていることにご注意願います。

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
 
You start performing calculations when you introduce an unknown, for example x below:
 
<pre>3 + x = 8</pre>
 
Shifting those around you can determine x:
 
<pre>x = 8 - 3 
-&gt; x = 5</pre>
 
When you introduce more than one you make your term more flexible - you are using variables:
 
<pre>x + y = 8</pre>
 
You can change the values of x and y and the formula can still be true:
 
<pre>x = 4
y = 4</pre>
 
or
 
<pre>x = 3
y = 5</pre>
 
The same works with programming languages—in programming, variables are containers for values that can vary. Variables can hold all kinds of values and also the results of calculations. Variables have a name and a value separated by an equals sign (=). Variable names can be any letter or word, but bear in mind that there are restrictions from language to language of what you can use, as some words are reserved for other functionality.

To keep things easy, let’s use JavaScript as an example programming language in this article (logical, since this section of the web standards curriculum is all about JavaScript programming!) The following defines two variables, calculates the result of adding the two and defines this result as a value of a third variable.
 
Note: The &lt;script
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