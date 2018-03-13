<h1 id="1markdown">1.什么是Markdown？</h1>
<pre><code>    Markdown 是一种用来写作的轻量级「标记语言」，它用简洁的语法代替排版，而不像一般我们用的字处理软件 Word 或 Pages 有大量的排版、字体设置。它使我们专心于码字，用「标记」语法，来代替常见的排版格式。
</code></pre>
<hr>
<h1 id="2markdown">2.Markdown快速入门</h1>
<h3 id="1">1.标题</h3>
<pre><code>  标题是每篇文章都需要也是最常用的格式，在 Markdown 中，如果一段文字被定义为标题，只要在这段文字前加 # 号即可。
   # 一级标题h1 
   ## 二级标题h2  
   ### 三级标题h3
   或者
   一级标题h1 
   =============
   二级标题h2  
   -------------
   或者
   # 这是 H1 #
   ## 这是 H2 ##
   ### 这是 H3 ###  
以此类推，总共六级标题，建议在井号后加一个空格，这是最标准的 Markdown 语法。如图
</code></pre>
<p><img src="http://ishare.58corp.com/uploads/image/201702/20170203154906_52117.jpg" alt="20170203154906_52117"></p>
<hr>
<h3 id="2">2.列表</h3>
<pre><code>   在html中大家都非常熟悉有序列表和无序列表 然而在Markdown 中我们只需要在文字前加上 - 或 * 即可变为无序列表，有序列表则直接在文字前加1\. 2\. 3\. 符号要和文字之间加上一个字符的空格。如图
</code></pre>
<p><img src="http://ishare.58corp.com/uploads/image/201702/20170203155557_62753.jpg" alt="20170203155557_62753"></p>
<hr>
<h3 id="3">3.区块引用</h3>
<pre><code>  一般文章开头都要缩近 我们可以在文章的开头引入 >(大于号) 就相当于在Markdown中引入区块，Markdown 也允许你偷懒只在整个段落的第一行最前面加上 > ：
 > ## 这是一个标题。
 > 
 > 1\.   这是第一行列表项。
 > 2\.   这是第二行列表项。
 > 
 > >可以进行嵌套：
 > 
</code></pre>
<hr>
<h3 id="4">4.粗体与斜体</h3>
<pre><code>  Markdown 的粗体和斜体也非常简单，用两个 * 或者两个 _ 包含一段文本就是粗体的语法，用一个 *或者一个 _ 包含一段文本就是斜体的语法。
</code></pre>
<hr>
<h3 id="5">5.表格</h3>
<pre><code>    Markdown 中的表格比较繁琐，书写起来比较麻烦
    | 总类 | 数量 | 价格 |
    | ---  |:---: | ---:|
    | 苹果 | 3个 | $100 |
    | 香蕉 | 2个 |  $12 |
    | 总计 | 5个 | $112 |
</code></pre>
<blockquote>
  <table>
  <thead>
  <tr>
  <th>总类</th>
  <th>数量</th>
  <th>价格</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>苹果</td>
  <td>3个</td>
  <td>$100</td>
  </tr>
  <tr>
  <td>香蕉</td>
  <td>2个</td>
  <td>$12</td>
  </tr>
  <tr>
  <td>总计</td>
  <td>5个</td>
  <td>$112</td>
  </tr>
  </tbody>
  </table>
  <hr>
</blockquote>
<h3 id="6">6.代码模块</h3>
<pre><code> 和程序相关的代码，通常这些区块我们并不希望它以一般段落文件的方式去排版，而是照原来的样子显示，Markdown 会用 pre 标签来把代码区块包起来。或者就用（4个空格来显示）
</code></pre>
<hr>
<h3 id="7">7.代码块</h3>
<pre><code> 在Markdown中 用` `或者code标签来显示代码块
</code></pre>
<hr>
<h3 id="8">8.链接</h3>
<pre><code>  在html 中我们提到链接第一时间想到的是a标签 但在Markdown中 我们可以用http标签来显示
</code></pre>
<hr>
<h3 id="9">9.插入图片</h3>
<pre><code>  Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。行内式的图片语法看起来像是：![title](/path/to/img.jpg)例如
</code></pre>
<p><img src="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1486124551759&di=06cab225ad6f82faeb08236ebe998502&imgtype=jpg&src=http%3A%2F%2Fimg3.imgtn.bdimg.com%2Fit%2Fu%3D278698877%2C3877982126%26fm%3D214%26gp%3D0.jpg" alt="58 同城"></p>
<hr>
<h3 id="10">10.分割线</h3>
<pre><code>  你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：
</code></pre>
<hr>
<pre><code> * * *

 ***

 *****

 - - -
</code></pre>
<hr>
<h3 id="11">11.反斜杠</h3>
<pre><code>  Markdown 可以利用反斜杠来插入一些在语法中有其它意义的符号 如 ＊ _  +  - # !
  例如  \*转义符号\*
</code></pre>
<hr>
<h1 id="3markdown">3.Markdown编辑器</h1>
<pre><code> 1.Smark 开源软件
 2.MarkdownPad 
 3.Mou
 4.MacDown 
</code></pre>