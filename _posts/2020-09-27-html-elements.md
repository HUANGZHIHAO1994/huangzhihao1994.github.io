<div align="left">
    <img src='https://ftp.bmp.ovh/imgs/2020/08/b77a8439ea51e080.jpg' height="50" width="50" >
</div>
---
title: HTML elements
author: Zhihao HUANG 
date: 2019-08-11 00:34:00 +0800
categories: [Blogging, HTML]
tags: [HTML]
toc: false
---

1.F12中elements是网页在内存中的源码

2.说明

```
“<html>”跟标签，子标签“<head>” “<body>”, “<head>”还有子标签"<title>" “<head>”中内容不会显示在网页中，在网页标签中出现 , "<h1>"一级标题, "<h2>" 二级标题, "<p>"段落，"<img>"和"<input>"这些只有开始没有结束，自结束标签。注释："<!-- -->"
```



```html
<html>
	<head>
		<title>哈哈，我在哪出现？</title>
	</head>
	<body>
		<h1>回乡偶书（二首）</h1>  
		<h2>其一</h2>           
		<h2>贺知章</h2>
		<p>少小离家老大回</p>
		<p>乡音无改鬓毛衰</p>
		<p>儿童相见不相识</p>
		<p>笑问客从何处来</p>
        <!-- 
		HTML的注释，注释中的内容会被浏览器所忽略，不会在网页中直接显示，
			但是可以在源码中查看注释，注释用来对代码进行解释说明的
			开发中一定要养成良好的编写注释的习惯，注释要求简单明了
		
		注释还可以将一些不希望显示的内容隐藏
		
		注释不能嵌套
		
		标签一般成对出现，但是也存在一些自结束标签
		
		
		<img>
		<img />
		<input>
		<input />
		-->
	</body>
</html>
```



3.属性

```html
<html>
	<head>
		<title>标签的属性</title>
	</head>
	<body>
	
	<!-- 
		属性，在标签中（开始标签或自结束标签）还可以设置属性
			属性是一个名值对（x=y）
			属性用来设置标签中的内容如何显示
			
			属性和标签名或其他属性应该使用空格隔开
			
			属性不能瞎写，应该根据文档中的规定来编写，
				有些属性有属性值，有些没有。如果有属性值，属性值应该使用引号引起来
			<font>字体，不推荐使用，“结构”是HTML，“表现”是CSS的活儿，“行为”是js的活儿
			
	-->
        <h1>这是我的<font color="red" size='3'>第三个</font>网页！</h1>
    </body>
</html>
```



4.网页基本结构（html5），文档声明

```html
<!doctype html>
<html>
	<head>
	<!-- 可以通过meta标签来设置网页的字符集，避免乱码问题 -->
		<meta charset="utf-8">
		<title>网页的基本结构</title>
	</head>
	<body>
	
	<!-- 
		迭代d
			网页的版本
				HTML4
				XHTML2.0
				HTML5
				...
				
			文档声明（doctype）
				- 文档声明用来告诉浏览器当前网页的版本
				- html5的文档声明
				<!doctype html>
				<!Doctype HTML>
				
				
		进制：
			十进制（日常使用）
				- 特点：满10进1
				- 计数：0 1 2 3 4 5 6 7 8 9 10 11 12 13 ... 19 20
				- 单位数字：10个 （0-9）
			
			二进制（计算机底层的进制）
				- 特点：满2进1
				- 计数：0 1 10 11 100 101 110 111
				- 单位数字：2个 （0-1）
				- 扩展：
					- 所有数据在计算机底层都会以二进制的形式保存
					- 可以将内存想象为一个有多个小格子组成的容器，每一个小格子中可以存储一个1或一个0
						这一个小格子在内存中被称为1位（bit）
						
						8bit = 1byte(字节)
						1024byte = 1kb(千字节)
						1024kb = 1mb(兆字节)
						1024mb = 1gb(吉字节)
						1024gb = 1tb(特字节)
						1024tp = 1pb
			
			八进制(很少用)
				- 特点：满8进1
				- 计数： 0 1 2 3 4 5 6 7 10 11 12 ... 17 20
				- 单位数字：8个 （0-7）
			
			十六进制(一般显示一个二进制数字时，都会转换为十六进制)
				- 特点：满16进1
				- 计数：0 1 2 3 4 5 6 7 8 9 a b c d e f 10 11 12 ... 1a 1b 1c 1d 1e 1f 20 ..
				- 单位数字：16个（0-f）
				
				
		字符编码
			李立超 -> 110000110110 （编码）
			110000110110 -> 李立超 （解码）
			
			- 所有的数据在计算机中存储时都是以二进制形式存储的，文字也不例外。
				所以一段文字在存储到内存中时，都需要转换为二进制编码
				当我们读取这段文字时，计算机会将编码转换为字符，供我们阅读
				
			- 编码
				- 将字符转换为二进制码的过程称为编码
			- 解码
				- 将二进制码转换为字符的过程称为解码
			- 字符集（charset）
			    - 编码和解码所采用的规则称为字符集
			- 乱码问题：
				- 如果编码和解码所采用的字符集不同就会出现乱码问题
			- 常见的字符集：
				ASCII
				ISO88591
				GB2312
				GBK
				UTF-8，在开发时我们使用的字符集都是UTF-8
		
	-->
	

	</body>
</html>
```



```html
<!-- 文档声明，声明当前网页的版本 -->
<!doctype html>

<!-- html的根标签（元素），网页中的所有内容都要写根元素的里边 -->
<html>

	<!-- head是网页的头部，head中的内容不会在网页中直接出现，主要用来帮助浏览器或搜索引擎来解析网页 -->
	<head>

		<!-- meta标签用来设置网页的元数据，这里meta用来设置网页的字符集，避免乱码问题 -->
		<meta charset="utf-8">
		
		<!-- title中的内容会显示在浏览器的标题栏，搜索引擎会主要根据title中的内容来判断网页的主要内容 -->
		<title>网页的标题</title>

	</head>

	<!-- body是html的子元素，表示网页的主体，网页中所有的可见内容都应该写在body里 -->
	<body>

		<!-- h1网页的一级标题 -->
		<h1>网页的大标题</h1>

	</body>

</html>
```



5.实体

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>实体</title>
</head>
<body>

    <!-- 
        在网页中编写的多个空格默认情况会自动被浏览器解析为一个空格

        在HTML中有些时候，我们不能直接书写一些特殊符号
            比如：多个连续的空格，比如字母两侧的大于和小于号

        如果我们需要在网页中书写这些特殊的符号，则需要使用html中的实体（转义字符）
        实体的语法：
            &实体的名字;
                &nbsp; 空格
                &gt; 大于号
                &lt; 小于号
                &copy; 版权符号


     -->
<p>
    今天&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;天气真不错！
</p>
    
<p>

    a&lt;b&gt;c
</p>

</body>
</html>
```



6.meta

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <!-- 
        meta主要用于设置网页中的一些元数据，元数据不是给用户看
            charset 指定网页的字符集
            name 指定的数据的名称
            content 指定的数据的内容

                keywords 表示网站的关键字，可以同时指定多个关键字，关键字间使用,隔开
                    <meta name="Keywords" content="网上购物,网上商城,手机,笔记本,电脑,MP3,CD,VCD,DV,相机,数码,配件,手表,存储卡,京东"/>
                    <meta name="keywords" content="网购,网上购物,在线购物,网购网站,网购商城,购物网站,网购中心,购物中心,卓越,亚马逊,卓越亚马逊,亚马逊中国,joyo,amazon">
                    
                description 用于指定网站的描述
                    <meta name="description" content="京东JD.COM-专业的综合网上购物商城,销售家电、数码通讯、电脑、家居百货、服装服饰、母婴、图书、食品等数万个品牌优质商品.便捷、诚信的服务，为您提供愉悦的网上购物体验!"/>
                    网站的描述会显示在搜索引擎的搜索的结果中

                title标签的内容会作为搜索结果的超链接上的文字显示    
     -->
     <meta name="keywords" content="HTML5,前端,CSS3">
     <meta name="description" content="这是一个非常不错的网站">
     <!--
          <meta http-equiv="refresh" content="3;url=https://www.mozilla.org"> 
        将页面重定向到另一个网站
    -->
    <!-- <meta http-equiv="refresh" content="3;url=https://www.baidu.com"> -->
    <title>Document</title>

</head>
<body>
    
</body>
</html>
```



7.语义化标签

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>

    <!-- 
        在网页中HTML专门用来负责网页的结构
            所以在使用html标签时，应该关注的是标签的语义，而不是它的样式

            标题标签：
                h1 ~ h6 一共有六级标题
                从h1~h6重要性递减，h1最重要，h6最不重要
                h1在网页中的重要性仅次于title标签，一般情况下一个页面中只会有一个h1
                一般情况下标题标签只会使用到h1~h3，h4~h6很少用

                标题标签都是块元素

            在页面中独占一行的元素称为块元素（block element）
     -->
     <h1>一级标题</h1>
     <h2>二级标题</h2>
     <h3>三级标题</h3>
     <h4>四级标题</h4>
     <h5>五级标题</h5>
     <h6>六级标题</h6>

     <!-- 
        hgroup标签用来为标题分组，可以将一组相关的标题同时放入到hgroup

      -->
      <hgroup>
            <h1>回乡偶书二首</h1>
            <h2>其一</h2>
      </hgroup>
      


     <!-- 
         p标签表示页面中的一个段落

         p也是一个块元素
      -->
      <p>在p标签中的内容就表示一个段落</p>
      <p>在p标签中的内容就表示一个段落</p>

      <!-- 
          em标签用于表示语音语调的一个加重

          在页面中不会独占一行的元素称为行内元素（inline element）
       -->
      <p>今天天气<em>真</em>不错！</p>

      <!-- 
          strong表示强调，重要内容！
       -->
      <p>你今天必须要<strong>完成作业</strong>！</p>

      鲁迅说：
      <!-- blockquote 表示一个长引用 -->
      <blockquote>
          这句话我是从来没有说过的！
      </blockquote>

      <!-- 
          q表示一个短引用
       -->
      子曰<q>学而时习之，乐呵乐呵！</q>

      <!-- 
          br标签表示页面中的换行
       -->
      <br>
      <br>

      今天天气真不错
     
    
</body>
</html>
```



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>

    <!-- 
        块元素（block element）
            - 在网页中一般通过块元素来对页面进行布局
        行内元素（inline element）
            - 行内元素主要用来包裹文字

            - 一般情况下会在块元素中放行内元素，而不会在行内元素中放块元素
            - 块元素中基本上什么都能放
            - p元素中不能放任何的块元素

        浏览器在解析网页时，会自动对网页中不符合规范的内容进行修正
            比如：
                标签写在了根元素的外部
                p元素中嵌套了块元素
                根元素中出现了除head和body以外的子元素
                ... ...
     -->

     <p>
         <h1>哈哈</h1>
     </p>
   
    
</body>
</html>

<h1>我就要写在html标签的外部！</h1>
```



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>
<body>
    <!-- 
        布局标签（结构化语义标签）
     -->

     <!--
		这些语义化标签目前显示效果没区别，需要css继续封装才有效果，现在只是告知目的较多
        header 表示网页的头部
        main 表示网页的主体部分(一个页面中只会有一个main)
        footer 表示网页的底部
        nav 表示网页中的导航
        aside 和主体相关的其他内容（侧边栏）
        article 表示一个独立的文章
        section 表示一个独立的区块，上边的标签都不能表示时使用section
        

		用的最多！div相当于上面所有
        div 没有语义，就用来表示一个区块，目前来讲div还是我们主要的布局元素
        span 行内元素，没有任何的语义，一般用于在网页中选中文字

      -->
     <header></header>
     <main></main>
     <footer></footer>

     <nav></nav>
     <aside></aside>
     <article></article>

     <section></section>

     <div></div>

     <span></span>
</body>
</html>
```



8.列表

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Document</title>
</head>

<body>

    <!-- 
    列表（list）
        1、铅笔
        2、尺子
        3、橡皮

    在html中也可以创建列表，html列表一共有三种：
        1、有序列表
        2、无序列表
        3、定义列表

    有序列表，使用ol标签来创建无序列表
        使用li表示列表项  
        
    无序列表，使用ul标签来创建无序列表
        使用li表示列表项

    定义列表，使用dl标签来创建一个定义列表
        使用dt来表示定义的内容
        使用dd来对内容进行解释说明

    列表之间可以互相嵌套

 -->

    <ul>
        <li>结构</li>
        <li>表现</li>
        <li>行为</li>
    </ul>

    <ol>
        <li>结构</li>
        <li>表现</li>
        <li>行为</li>
    </ol>


    <dl>
        <dt>结构</dt>
        <dd>结构表示网页的结构，结构用来规定网页中哪里是标题，哪里是段落</dd>
        <dd>结构表示网页的结构，结构用来规定网页中哪里是标题，哪里是段落</dd>
        <dd>结构表示网页的结构，结构用来规定网页中哪里是标题，哪里是段落</dd>
    </dl>

    <ul>
        <li>
            aa
            <ul>
                <li>aa-1</li>
                <li>aa-2
                    <ul>
                        <li>aa-1</li>
                        <li>aa-2</li>
                    </ul>
                </li>
            </ul>
        </li>
    </ul>


</body>

</html>
```



9.超链接

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>超链接</title>
</head>
<body>
    <!-- 
        超链接可以让我们从一个页面跳转到其他页面，
            或者是当前页面的其他的位置

        使用 a 标签来定义超链接
            属性：
                href 指定跳转的目标路径
                    - 值可以是一个外部网站的地址
                    - 也可以写一个内部页面的地址

        超链接是也是一个行内元素，在a标签中可以嵌套除它自身外的任何元素
        alt+shift+↑/↓ 向上向下复制
     -->

     <a href="https://www.baidu.com">超链接</a>
     <br><br>
     <!-- <a href="https://www.baidu123.com">超链接</a> -->
     <a href="07.列表.html">超链接2</a>
    
</body>
</html>
```



10.相对路径

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    
    <!-- 
        当我们需要跳转一个服务器内部的页面时，一般我们都会使用相对路径
            相对路径都会使用.或..开头
                ./
                ../
            ./可以省略不写，如果不写./也不写../则就相当于写了./

            ./ 表示当前文件所在的目录
                - 在这里当前页面就是 09.相对路径.html
                - ./就等于 09.相对路径.html 所在的目录 path

            ../ 表示当前文件所在目录的上一级目录

     -->
    <a href="./target.html">超链接1</a> 
    <br><br>
    <a href="../07.列表.html">超链接2</a>
    <br><br>
    <a href="./inner/target2.html">超链接3</a>
    <br><br>
    <a href="../outer/target3.html">超链接4</a>


</body>
</html>
```



```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    
    <!-- 
        target属性，用来指定超链接打开的位置
            可选值：
                _self 默认值 在当前页面中打开超链接
                _blank 在一个新的要么中打开超链接

     -->
    <a href="07.列表.html" target="_blank">超链接</a>

    <br><br>
    <a href="#bottom">去底部</a>

    <br><br>
    <a href="#p3">去第三个自然段</a>

    <br><br>
    

    <p>在我的后园，可以看见墙外有两株树，一株是枣树，还有一株也是枣树。 这上面的夜的天空，奇怪而高，我生平没有见过这样奇怪而高的天空。他仿佛要离开人间而去，使人们仰面不再看见。然而现在却非常之蓝，闪闪地䀹着几十个星星的眼，冷眼。他的口角上现出微笑，似乎自以为大有深意，而将繁霜洒在我的园里的野花草上。 我不知道那些花草真叫什么名字，人们叫他们什么名字。我记得有一种开过极细小的粉红花，现在还开着，但是更极细小了，她在冷的夜气中，瑟缩地做梦，梦见春的到来，梦见秋的到来，梦见瘦的诗人将眼泪擦在她最末的花瓣上，告诉她秋虽然来，冬虽然来，而此后接着还是春，蝴蝶乱飞，蜜蜂都唱起春词来了。她于是一笑，虽然颜色冻得红惨惨地，仍然瑟缩着。 枣树，他们简直落尽了叶子。先前，还有一两个孩子来打他们，别人打剩的枣子，现在是一个也不剩了，连叶子也落尽了。他知道小粉红花的梦，秋后要有春；他也知道落叶的梦，春后还是秋。他简直落尽叶子，单剩干子，然而脱了当初满树是果实和叶子时候的弧形，欠伸得很舒服。但是，有几枝还低亚着，护定他从打枣的竿梢所得的皮伤，而最直最长的几枝，却已默默地铁似的直刺着奇怪而高的天空，使天空闪闪地鬼䀹眼；直刺着天空中圆满的月亮，使月亮窘得发白。 鬼䀹眼的天空越加非常之蓝，不安了，仿佛想离去人间，避开枣树，只将月亮剩下。然而月亮也暗暗地躲到东边去了。而一无所有的干子，却仍然默默地铁似的直刺着奇怪而高的天空，一意要制他的死命，不管他各式各样地䀹着许多蛊惑的眼睛。 哇的一声，夜游的恶鸟飞过了。 我忽而听到夜半的笑声，吃吃地，似乎不愿意惊动睡着的人，然而四围的空气都应和着笑。夜半，没有别的人，我即刻听出这声音就在我嘴里，我也即刻被这笑声所驱逐，回进自己的房。灯火的带子也即刻被我旋高了。 后窗的玻璃上丁丁地响，还有许多小飞虫乱撞。不多久，几个进来了，许是从窗纸的破孔进来的。他们一进来，又在玻璃的灯罩上撞得丁丁地响。一个从上面撞进去了，他于是遇到火，而且我以为这火是真的。两三个却休息在灯的纸罩上喘气。那罩是昨晚新换的罩，雪白的纸，折出波浪纹的叠痕，一角还画出一枝猩红色的栀子。 猩红的栀子开花时，枣树又要做小粉红花的梦，青葱地弯成弧形了……我又听到夜半的笑声；我赶紧砍断我的心绪，看那老在白纸罩上的小青虫，头大尾小，向日葵子似的，只有半粒小麦那么大，遍身的颜色苍翠得可爱，可怜。 我打一个呵欠，点起一支纸烟，喷出烟来，对着灯默默地敬奠这些苍翠精致的英雄们。 一九二四年九月十五日。</p>
    <p>在我的后园，可以看见墙外有两株树，一株是枣树，还有一株也是枣树。 这上面的夜的天空，奇怪而高，我生平没有见过这样奇怪而高的天空。他仿佛要离开人间而去，使人们仰面不再看见。然而现在却非常之蓝，闪闪地䀹着几十个星星的眼，冷眼。他的口角上现出微笑，似乎自以为大有深意，而将繁霜洒在我的园里的野花草上。 我不知道那些花草真叫什么名字，人们叫他们什么名字。我记得有一种开过极细小的粉红花，现在还开着，但是更极细小了，她在冷的夜气中，瑟缩地做梦，梦见春的到来，梦见秋的到来，梦见瘦的诗人将眼泪擦在她最末的花瓣上，告诉她秋虽然来，冬虽然来，而此后接着还是春，蝴蝶乱飞，蜜蜂都唱起春词来了。她于是一笑，虽然颜色冻得红惨惨地，仍然瑟缩着。 枣树，他们简直落尽了叶子。先前，还有一两个孩子来打他们，别人打剩的枣子，现在是一个也不剩了，连叶子也落尽了。他知道小粉红花的梦，秋后要有春；他也知道落叶的梦，春后还是秋。他简直落尽叶子，单剩干子，然而脱了当初满树是果实和叶子时候的弧形，欠伸得很舒服。但是，有几枝还低亚着，护定他从打枣的竿梢所得的皮伤，而最直最长的几枝，却已默默地铁似的直刺着奇怪而高的天空，使天空闪闪地鬼䀹眼；直刺着天空中圆满的月亮，使月亮窘得发白。 鬼䀹眼的天空越加非常之蓝，不安了，仿佛想离去人间，避开枣树，只将月亮剩下。然而月亮也暗暗地躲到东边去了。而一无所有的干子，却仍然默默地铁似的直刺着奇怪而高的天空，一意要制他的死命，不管他各式各样地䀹着许多蛊惑的眼睛。 哇的一声，夜游的恶鸟飞过了。 我忽而听到夜半的笑声，吃吃地，似乎不愿意惊动睡着的人，然而四围的空气都应和着笑。夜半，没有别的人，我即刻听出这声音就在我嘴里，我也即刻被这笑声所驱逐，回进自己的房。灯火的带子也即刻被我旋高了。 后窗的玻璃上丁丁地响，还有许多小飞虫乱撞。不多久，几个进来了，许是从窗纸的破孔进来的。他们一进来，又在玻璃的灯罩上撞得丁丁地响。一个从上面撞进去了，他于是遇到火，而且我以为这火是真的。两三个却休息在灯的纸罩上喘气。那罩是昨晚新换的罩，雪白的纸，折出波浪纹的叠痕，一角还画出一枝猩红色的栀子。 猩红的栀子开花时，枣树又要做小粉红花的梦，青葱地弯成弧形了……我又听到夜半的笑声；我赶紧砍断我的心绪，看那老在白纸罩上的小青虫，头大尾小，向日葵子似的，只有半粒小麦那么大，遍身的颜色苍翠得可爱，可怜。 我打一个呵欠，点起一支纸烟，喷出烟来，对着灯默默地敬奠这些苍翠精致的英雄们。 一九二四年九月十五日。</p>
    <p id="p3">在我的后园，可以看见墙外有两株树，一株是枣树，还有一株也是枣树。 这上面的夜的天空，奇怪而高，我生平没有见过这样奇怪而高的天空。他仿佛要离开人间而去，使人们仰面不再看见。然而现在却非常之蓝，闪闪地䀹着几十个星星的眼，冷眼。他的口角上现出微笑，似乎自以为大有深意，而将繁霜洒在我的园里的野花草上。 我不知道那些花草真叫什么名字，人们叫他们什么名字。我记得有一种开过极细小的粉红花，现在还开着，但是更极细小了，她在冷的夜气中，瑟缩地做梦，梦见春的到来，梦见秋的到来，梦见瘦的诗人将眼泪擦在她最末的花瓣上，告诉她秋虽然来，冬虽然来，而此后接着还是春，蝴蝶乱飞，蜜蜂都唱起春词来了。她于是一笑，虽然颜色冻得红惨惨地，仍然瑟缩着。 枣树，他们简直落尽了叶子。先前，还有一两个孩子来打他们，别人打剩的枣子，现在是一个也不剩了，连叶子也落尽了。他知道小粉红花的梦，秋后要有春；他也知道落叶的梦，春后还是秋。他简直落尽叶子，单剩干子，然而脱了当初满树是果实和叶子时候的弧形，欠伸得很舒服。但是，有几枝还低亚着，护定他从打枣的竿梢所得的皮伤，而最直最长的几枝，却已默默地铁似的直刺着奇怪而高的天空，使天空闪闪地鬼䀹眼；直刺着天空中圆满的月亮，使月亮窘得发白。 鬼䀹眼的天空越加非常之蓝，不安了，仿佛想离去人间，避开枣树，只将月亮剩下。然而月亮也暗暗地躲到东边去了。而一无所有的干子，却仍然默默地铁似的直刺着奇怪而高的天空，一意要制他的死命，不管他各式各样地䀹着许多蛊惑的眼睛。 哇的一声，夜游的恶鸟飞过了。 我忽而听到夜半的笑声，吃吃地，似乎不愿意惊动睡着的人，然而四围的空气都应和着笑。夜半，没有别的人，我即刻听出这声音就在我嘴里，我也即刻被这笑声所驱逐，回进自己的房。灯火的带子也即刻被我旋高了。 后窗的玻璃上丁丁地响，还有许多小飞虫乱撞。不多久，几个进来了，许是从窗纸的破孔进来的。他们一进来，又在玻璃的灯罩上撞得丁丁地响。一个从上面撞进去了，他于是遇到火，而且我以为这火是真的。两三个却休息在灯的纸罩上喘气。那罩是昨晚新换的罩，雪白的纸，折出波浪纹的叠痕，一角还画出一枝猩红色的栀子。 猩红的栀子开花时，枣树又要做小粉红花的梦，青葱地弯成弧形了……我又听到夜半的笑声；我赶紧砍断我的心绪，看那老在白纸罩上的小青虫，头大尾小，向日葵子似的，只有半粒小麦那么大，遍身的颜色苍翠得可爱，可怜。 我打一个呵欠，点起一支纸烟，喷出烟来，对着灯默默地敬奠这些苍翠精致的英雄们。 一九二四年九月十五日。</p>
    <p>在我的后园，可以看见墙外有两株树，一株是枣树，还有一株也是枣树。 这上面的夜的天空，奇怪而高，我生平没有见过这样奇怪而高的天空。他仿佛要离开人间而去，使人们仰面不再看见。然而现在却非常之蓝，闪闪地䀹着几十个星星的眼，冷眼。他的口角上现出微笑，似乎自以为大有深意，而将繁霜洒在我的园里的野花草上。 我不知道那些花草真叫什么名字，人们叫他们什么名字。我记得有一种开过极细小的粉红花，现在还开着，但是更极细小了，她在冷的夜气中，瑟缩地做梦，梦见春的到来，梦见秋的到来，梦见瘦的诗人将眼泪擦在她最末的花瓣上，告诉她秋虽然来，冬虽然来，而此后接着还是春，蝴蝶乱飞，蜜蜂都唱起春词来了。她于是一笑，虽然颜色冻得红惨惨地，仍然瑟缩着。 枣树，他们简直落尽了叶子。先前，还有一两个孩子来打他们，别人打剩的枣子，现在是一个也不剩了，连叶子也落尽了。他知道小粉红花的梦，秋后要有春；他也知道落叶的梦，春后还是秋。他简直落尽叶子，单剩干子，然而脱了当初满树是果实和叶子时候的弧形，欠伸得很舒服。但是，有几枝还低亚着，护定他从打枣的竿梢所得的皮伤，而最直最长的几枝，却已默默地铁似的直刺着奇怪而高的天空，使天空闪闪地鬼䀹眼；直刺着天空中圆满的月亮，使月亮窘得发白。 鬼䀹眼的天空越加非常之蓝，不安了，仿佛想离去人间，避开枣树，只将月亮剩下。然而月亮也暗暗地躲到东边去了。而一无所有的干子，却仍然默默地铁似的直刺着奇怪而高的天空，一意要制他的死命，不管他各式各样地䀹着许多蛊惑的眼睛。 哇的一声，夜游的恶鸟飞过了。 我忽而听到夜半的笑声，吃吃地，似乎不愿意惊动睡着的人，然而四围的空气都应和着笑。夜半，没有别的人，我即刻听出这声音就在我嘴里，我也即刻被这笑声所驱逐，回进自己的房。灯火的带子也即刻被我旋高了。 后窗的玻璃上丁丁地响，还有许多小飞虫乱撞。不多久，几个进来了，许是从窗纸的破孔进来的。他们一进来，又在玻璃的灯罩上撞得丁丁地响。一个从上面撞进去了，他于是遇到火，而且我以为这火是真的。两三个却休息在灯的纸罩上喘气。那罩是昨晚新换的罩，雪白的纸，折出波浪纹的叠痕，一角还画出一枝猩红色的栀子。 猩红的栀子开花时，枣树又要做小粉红花的梦，青葱地弯成弧形了……我又听到夜半的笑声；我赶紧砍断我的心绪，看那老在白纸罩上的小青虫，头大尾小，向日葵子似的，只有半粒小麦那么大，遍身的颜色苍翠得可爱，可怜。 我打一个呵欠，点起一支纸烟，喷出烟来，对着灯默默地敬奠这些苍翠精致的英雄们。 一九二四年九月十五日。</p>
    <p>在我的后园，可以看见墙外有两株树，一株是枣树，还有一株也是枣树。 这上面的夜的天空，奇怪而高，我生平没有见过这样奇怪而高的天空。他仿佛要离开人间而去，使人们仰面不再看见。然而现在却非常之蓝，闪闪地䀹着几十个星星的眼，冷眼。他的口角上现出微笑，似乎自以为大有深意，而将繁霜洒在我的园里的野花草上。 我不知道那些花草真叫什么名字，人们叫他们什么名字。我记得有一种开过极细小的粉红花，现在还开着，但是更极细小了，她在冷的夜气中，瑟缩地做梦，梦见春的到来，梦见秋的到来，梦见瘦的诗人将眼泪擦在她最末的花瓣上，告诉她秋虽然来，冬虽然来，而此后接着还是春，蝴蝶乱飞，蜜蜂都唱起春词来了。她于是一笑，虽然颜色冻得红惨惨地，仍然瑟缩着。 枣树，他们简直落尽了叶子。先前，还有一两个孩子来打他们，别人打剩的枣子，现在是一个也不剩了，连叶子也落尽了。他知道小粉红花的梦，秋后要有春；他也知道落叶的梦，春后还是秋。他简直落尽叶子，单剩干子，然而脱了当初满树是果实和叶子时候的弧形，欠伸得很舒服。但是，有几枝还低亚着，护定他从打枣的竿梢所得的皮伤，而最直最长的几枝，却已默默地铁似的直刺着奇怪而高的天空，使天空闪闪地鬼䀹眼；直刺着天空中圆满的月亮，使月亮窘得发白。 鬼䀹眼的天空越加非常之蓝，不安了，仿佛想离去人间，避开枣树，只将月亮剩下。然而月亮也暗暗地躲到东边去了。而一无所有的干子，却仍然默默地铁似的直刺着奇怪而高的天空，一意要制他的死命，不管他各式各样地䀹着许多蛊惑的眼睛。 哇的一声，夜游的恶鸟飞过了。 我忽而听到夜半的笑声，吃吃地，似乎不愿意惊动睡着的人，然而四围的空气都应和着笑。夜半，没有别的人，我即刻听出这声音就在我嘴里，我也即刻被这笑声所驱逐，回进自己的房。灯火的带子也即刻被我旋高了。 后窗的玻璃上丁丁地响，还有许多小飞虫乱撞。不多久，几个进来了，许是从窗纸的破孔进来的。他们一进来，又在玻璃的灯罩上撞得丁丁地响。一个从上面撞进去了，他于是遇到火，而且我以为这火是真的。两三个却休息在灯的纸罩上喘气。那罩是昨晚新换的罩，雪白的纸，折出波浪纹的叠痕，一角还画出一枝猩红色的栀子。 猩红的栀子开花时，枣树又要做小粉红花的梦，青葱地弯成弧形了……我又听到夜半的笑声；我赶紧砍断我的心绪，看那老在白纸罩上的小青虫，头大尾小，向日葵子似的，只有半粒小麦那么大，遍身的颜色苍翠得可爱，可怜。 我打一个呵欠，点起一支纸烟，喷出烟来，对着灯默默地敬奠这些苍翠精致的英雄们。 一九二四年九月十五日。</p>
    <p>在我的后园，可以看见墙外有两株树，一株是枣树，还有一株也是枣树。 这上面的夜的天空，奇怪而高，我生平没有见过这样奇怪而高的天空。他仿佛要离开人间而去，使人们仰面不再看见。然而现在却非常之蓝，闪闪地䀹着几十个星星的眼，冷眼。他的口角上现出微笑，似乎自以为大有深意，而将繁霜洒在我的园里的野花草上。 我不知道那些花草真叫什么名字，人们叫他们什么名字。我记得有一种开过极细小的粉红花，现在还开着，但是更极细小了，她在冷的夜气中，瑟缩地做梦，梦见春的到来，梦见秋的到来，梦见瘦的诗人将眼泪擦在她最末的花瓣上，告诉她秋虽然来，冬虽然来，而此后接着还是春，蝴蝶乱飞，蜜蜂都唱起春词来了。她于是一笑，虽然颜色冻得红惨惨地，仍然瑟缩着。 枣树，他们简直落尽了叶子。先前，还有一两个孩子来打他们，别人打剩的枣子，现在是一个也不剩了，连叶子也落尽了。他知道小粉红花的梦，秋后要有春；他也知道落叶的梦，春后还是秋。他简直落尽叶子，单剩干子，然而脱了当初满树是果实和叶子时候的弧形，欠伸得很舒服。但是，有几枝还低亚着，护定他从打枣的竿梢所得的皮伤，而最直最长的几枝，却已默默地铁似的直刺着奇怪而高的天空，使天空闪闪地鬼䀹眼；直刺着天空中圆满的月亮，使月亮窘得发白。 鬼䀹眼的天空越加非常之蓝，不安了，仿佛想离去人间，避开枣树，只将月亮剩下。然而月亮也暗暗地躲到东边去了。而一无所有的干子，却仍然默默地铁似的直刺着奇怪而高的天空，一意要制他的死命，不管他各式各样地䀹着许多蛊惑的眼睛。 哇的一声，夜游的恶鸟飞过了。 我忽而听到夜半的笑声，吃吃地，似乎不愿意惊动睡着的人，然而四围的空气都应和着笑。夜半，没有别的人，我即刻听出这声音就在我嘴里，我也即刻被这笑声所驱逐，回进自己的房。灯火的带子也即刻被我旋高了。 后窗的玻璃上丁丁地响，还有许多小飞虫乱撞。不多久，几个进来了，许是从窗纸的破孔进来的。他们一进来，又在玻璃的灯罩上撞得丁丁地响。一个从上面撞进去了，他于是遇到火，而且我以为这火是真的。两三个却休息在灯的纸罩上喘气。那罩是昨晚新换的罩，雪白的纸，折出波浪纹的叠痕，一角还画出一枝猩红色的栀子。 猩红的栀子开花时，枣树又要做小粉红花的梦，青葱地弯成弧形了……我又听到夜半的笑声；我赶紧砍断我的心绪，看那老在白纸罩上的小青虫，头大尾小，向日葵子似的，只有半粒小麦那么大，遍身的颜色苍翠得可爱，可怜。 我打一个呵欠，点起一支纸烟，喷出烟来，对着灯默默地敬奠这些苍翠精致的英雄们。 一九二四年九月十五日。</p>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quia quasi numquam quam molestias cumque eveniet ab nobis doloribus dolores. Nesciunt, distinctio tempore similique consequuntur nulla dolorem sapiente minus praesentium impedit.</p>

    <!-- 在开发中可以将#作为超链接的路径的展位符使用 -->
    <a href="#">这是一个新的超链接</a>

    <br><br>

    <!-- 可以使用 javascript:; 来作为href的属性，此时点击这个超链接什么也不会发生 -->
    <a href="javascript:;">这是一个新的超链接</a>
    <br><br>


    <!-- 
        可以直接将超链接的href属性设置为#，这样点击超链接以后
            页面不会发生跳转，而是转到当前页面的顶部的位置

        可以跳转到页面的指定位置，只需将href属性设置 #目标元素的id属性值

        id属性（唯一不重复的）
            - 每一个标签都可以添加一个id属性
            - id属性就是元素的唯一标识，同一个页面中不能出现重复的id属性    
     -->

    <a id="bottom" href="#">回到顶部</a>
</body>
</html>
```



11.图片

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>

    <!-- 
        图片标签用于向当前页面中引入一个外部图片
         使用img标签来引入外部图片，img标签是一个自结束标签
         img这种元素属于替换元素（块和行内元素之间，具有两种元素的特点）
         属性：
            src 属性指定的是外部图片的路径（路径规则和超链接是一样的）

            alt 图片的描述，这个描述默认情况下不会显示，有些浏览器会图片无法加载时显示
                搜索引擎会根据alt中的内容来识别图片，如果不写alt属性则图片不会被搜索引擎所收录

            width 图片的宽度 (单位是像素)
            height 图片的高度    
                - 宽度和高度中如果只修改了一个，则另一个会等比例缩放

            注意：
                一般情况在pc端，不建议修改图片的大小，需要多大的图片就裁多大
                但是在移动端，经常需要对图片进行缩放（大图缩小）


        图片的格式：
            jpeg(jpg)
                - 支持的颜色比较丰富，不支持透明效果，不支持动图
                - 一般用来显示照片
            gif
                - 支持的颜色比较少，支持简单透明，支持动图
                - 颜色单一的图片，动图
            png
                - 支持的颜色丰富，支持复杂透明，不支持动图
                - 颜色丰富，复杂透明图片（专为网页而生）
            webp
                - 这种格式是谷歌新推出的专门用来表示网页中的图片的一种格式
                - 它具备其他图片格式的所有优点，而且文件还特别的小
                - 缺点：兼容性不好

            base64 
                - 将图片使用base64编码，这样可以将图片转换为字符，通过字符的形式来引入图片    
                - 一般都是一些需要和网页一起加载的图片才会使用base64

            效果一样，用小的
            效果不一样，用效果好的



     -->

    <img src="./img/1.gif" alt="松鼠">

    <img width="200"  src="https://d2ggl082rr1mkp.cloudfront.net/category/IronMan_preview_1521810286_220_310.jpeg" alt="钢铁侠">

    <img src="data:image/jpeg;base64,/9j/4QAYRXhpZgAASUkqAAgAAAAAAAAAAAAAAP/sABFEdWNreQABAAQAAAA8AAD/4QMZaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLwA8P3hwYWNrZXQgYmVnaW49Iu+7vyIgaWQ9Ilc1TTBNcENlaGlIenJlU3pOVGN6a2M5ZCI/PiA8eDp4bXBtZXRhIHhtbG5zOng9ImFkb2JlOm5zOm1ldGEvIiB4OnhtcHRrPSJBZG9iZSBYTVAgQ29yZSA1LjMtYzAxMSA2Ni4xNDU2NjEsIDIwMTIvMDIvMDYtMTQ6NTY6MjcgICAgICAgICI+IDxyZGY6UkRGIHhtbG5zOnJkZj0iaHR0cDovL3d3dy53My5vcmcvMTk5OS8wMi8yMi1yZGYtc3ludGF4LW5zIyI+IDxyZGY6RGVzY3JpcHRpb24gcmRmOmFib3V0PSIiIHhtbG5zOnhtcE1NPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvbW0vIiB4bWxuczpzdFJlZj0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL3NUeXBlL1Jlc291cmNlUmVmIyIgeG1sbnM6eG1wPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvIiB4bXBNTTpEb2N1bWVudElEPSJ4bXAuZGlkOjJDQUQyNzAxMTY4NDExRTZBMTdEOTlBRDNBNjk4N0QzIiB4bXBNTTpJbnN0YW5jZUlEPSJ4bXAuaWlkOjJDQUQyNzAwMTY4NDExRTZBMTdEOTlBRDNBNjk4N0QzIiB4bXA6Q3JlYXRvclRvb2w9IkFkb2JlIFBob3Rvc2hvcCBDUzYgV2luZG93cyI+IDx4bXBNTTpEZXJpdmVkRnJvbSBzdFJlZjppbnN0YW5jZUlEPSIyMEIwNzYzMUNEQzQ2NkI5NzM4RUFEQjBCNTdFMUE5RiIgc3RSZWY6ZG9jdW1lbnRJRD0iMjBCMDc2MzFDREM0NjZCOTczOEVBREIwQjU3RTFBOUYiLz4gPC9yZGY6RGVzY3JpcHRpb24+IDwvcmRmOlJERj4gPC94OnhtcG1ldGE+IDw/eHBhY2tldCBlbmQ9InIiPz7/7gAOQWRvYmUAZMAAAAAB/9sAhAAGBAQEBQQGBQUGCQYFBgkLCAYGCAsMCgoLCgoMEAwMDAwMDBAM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">
    <img src="data:image/gif;base64,R0lGODlhaAFoAcQAAOfn5y0tLdfX1xQUFsbGxre3t5qamqOjpP7+/nh4efLy84SEhFNTVEhISWdnaPn5+QYGBg4OEPv7+7+/v66url1dXt/f38/Pz/b29m9vcDs7PB8fII+PkO7u7hYWGP///yH/C1hNUCBEYXRhWE1QPD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iQWRvYmUgWE1QIENvcmUgNS41LWMwMjEgNzkuMTU1NzcyLCAyMDE0LzAxLzEzLTE5OjQ0OjAwICAgICAgICAiPiA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXBNTT0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL21tLyIgeG1sbnM6c3RSZWY9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC9zVHlwZS9SZXNvdXJjZVJlZiMiIHhtbG5zOnhtcD0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wLyIgeG1wTU06RG9jdW1lbnRJRD0ieG1wLmRpZDowRjIyNzMwNDU0QkUxMUU2QkIzN0QxOUI3OUI1M0E0NSIgeG1wTU06SW5zdGFuY2VJRD0ieG1wLmlpZDowRjIyNzMwMzU0QkUxMUU2QkIzN0QxOUI3OUI1M0E0NSIgeG1wOkNyZWF0b3JUb29sPSJBZG9iZSBQaG90b3Nob3AgQ0MgMjAxNCBXaW5kb3dzIj4gPHhtcE1NOkRlcml2ZWRGcm9tIHN0UmVmOmluc3RhbmNlSUQ9IjYwMTc1QUJFMTQ5MzM2OUVCMzAyRUI2RTREQzNBMzkyIiBzdFJlZjpkb2N1bWVudElEPSI2MDE3NUFCRTE0OTMzNjlFQjMwMkVCNkU0REMzQTM5MiIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PgH//v38+/r5+Pf2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" alt="">
    
</body>
</html>
```



12.内联框架

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>

    <!-- 
		现在用的不多了
        内联框架，用于向当前页面中引入一个其他页面
            src 指定要引入的网页的路径
            frameborder 指定内联框架的边框

     -->
    <iframe src="https://www.qq.com" width="800" height="600" frameborder="0"></iframe>
    <h1>Hello</h1>

    
</body>
</html>
```



13.音视频

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>

    <!-- 
        audio 标签用来向页面中引入一个外部的音频文件的
            音视频文件引入时，默认情况下不允许用户自己控制播放停止

        属性：
            controls 是否允许用户控制播放
            autoplay 音频文件是否自动播放
                - 如果设置了autoplay 则音乐在打开页面时会自动播放
                    但是目前来讲大部分浏览器都不会自动对音乐进行播放 
            loop 音乐是否循环播放  
     -->
    <!-- <audio src="./source/audio.mp3" controls autoplay loop></audio> -->
    
    <!-- <audio src="./source/audio.mp3" controls></audio> -->


    <!-- 除了通过src来指定外部文件的路径以外，还可以通过source来指定文件的路径，多个source会顺序找有用的<embed>是ie8兼容-->
    <audio controls>
        <!-- 对不起，您的浏览器不支持播放音频！请升级浏览器！ -->
        <source src="./source/audio.mp3">
        <source src="./source/audio.ogg">
        <embed src="./source/audio.mp3" type="audio/mp3" width="300" height="100">
    </audio>

    <!-- 
        使用video标签来向网页中引入一个视频
            - 使用方式和audio基本上是一样的
     -->
    <video controls>
        <source src="./source/flower.webm">
        <source src="./source/flower.mp4">
        <embed src="./source/flower.mp4" type="video/mp4">
    </video>

    <iframe frameborder="0" src="https://v.qq.com/txp/iframe/player.html?vid=b00318l66nt" allowFullScreen="true" width="500" height="300"></iframe>


</body>
</html>
```

