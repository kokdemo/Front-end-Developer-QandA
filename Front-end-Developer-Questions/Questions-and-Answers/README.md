#2014年最新前端开发面试题（题目列表+答案 完整版）


## <a name='list'>目录</a>

  1. [前言](#preface)
  1. [HTML 部分](#html)
  1. [CSS  部分](#css)
  1. [JavaScript 部分](#js)
  1. [其他问题](#other) 
  1. [优质网站推荐](#web) 
 
 

## <a name='preface'>前言</a> ##

本文总结了一些优质的前端面试题（多数源于网络），初学者阅后也要用心钻研其中的原理，重要知识需要系统学习，透彻学习，形成自己的知识链。万不可投机取巧，只求面试过关是错误的！


###面试有几点需注意：(来源程劭非老师 github:@wintercn)

1. 面试题目： 根据你的等级和职位变化，入门级到专家级：范围↑、深度↑、方向↑。

1. 题目类型： 技术视野、项目细节、理论知识题，算法题，开放性题，案例题。

1. 进行追问： 可以确保问到你开始不懂或面试官开始不懂为止，这样可以大大延展题目的区分度和深度，知道你的实际能力。因为这种关联知识是长时期的学习，绝对不是临时记得住的。

1. 回答问题再棒，面试官（可能是你的直接领导面试），会考虑我要不要这个人做我的同事？所以态度很重要。（感觉更像是相亲）

1. 资深的工程师能把absolute和relative弄混，这样的人不要也罢，因为团队需要的你这个人具有可以依靠的才能（靠谱）。



**前端开发面试知识点大纲：**

	HTML&CSS：
		对Web标准的理解、浏览器内核差异、兼容性、hack、CSS基本功：布局、盒子模型、选择器优先级及使用、HTML5、CSS3、移动端适应 

	JavaScript：  
        数据类型、面向对象、继承、闭包、插件、作用域、跨域、原型链、模块化、自定义事件、内存泄漏、事件机制、异步装载回调、模板引擎、Nodejs、JSON、ajax等。

	其他：
       HTTP、安全、正则、优化、重构、响应式、移动端、团队协作、可维护、SEO、UED、架构、职业生涯 

作为一名前端工程师，**无论工作年头长短都应该必须掌握的知识点**：

此条由 王子墨 发表在 [前端随笔](http://julying.com/blog/front-end-engineers-must-master-knowledge/) 
   
		1、DOM结构 —— 两个节点之间可能存在哪些关系以及如何在节点之间任意移动。
		
		2、DOM操作  ——如何添加、移除、移动、复制、创建和查找节点等。
		
		3、事件    —— 如何使用事件，以及IE和标准DOM事件模型之间存在的差别。
		
		4、XMLHttpRequest —— 这是什么、怎样完整地执行一次GET请求、怎样检测错误。
		
		5、严格模式与混杂模式 —— 如何触发这两种模式，区分它们有何意义。
		
		6、盒模型 —— 外边距、内边距和边框之间的关系，及IE8以下版本的浏览器中的盒模型
		
		7、块级元素与行内元素 —— 怎么用CSS控制它们、以及如何合理的使用它们
		
		8、浮动元素——怎么使用它们、它们有什么问题以及怎么解决这些问题。
		
		9、HTML与XHTML——二者有什么区别，你觉得应该使用哪一个并说出理由。
		
		10、JSON  —— 作用、用途、设计结构。
			



**备注：** 

根据自己需要选择性阅读，面试题是对理论知识的总结，让自己学会应该如何表达。

资料答案不够正确和全面，**欢迎补充**答案、题目；最好是现在网上没有的。 

格式不断修改更新中。  


## <a name='html'>HTML</a>

- Doctype作用? 严格模式与混杂模式如何区分？它们有何意义? 

		（1）、<!DOCTYPE> 声明位于文档中的最前面，处于 <html> 标签之前。告知浏览器的解析器，
              用什么文档类型 规范来解析这个文档。 
		
		（2）、严格模式的排版和 JS 运作模式是  以该浏览器支持的最高标准运行。
		
		（3）、在混杂模式中，页面以宽松的向后兼容的方式显示。模拟老式浏览器的行为以防止站点无法工作。
		
		（4）、DOCTYPE不存在或格式不正确会导致文档以混杂模式呈现。
		
		-----
	
	注解：
		
	DocType如字面所示，是指文档格式，告诉浏览器应该怎么解析这个文件，在html4中，有三种解析方式Strict，Transitional，Frameset，第一种不包括弃用元素和框架，后面的两种分别对应包括启用元素和页内框架。xhtml也有这三种，意义相同。
		
	html5种只有一种声明方式<!DOCTYPE html>。
		
	严格模式与混杂模式的产生主要是因为ie5.5~ie6之间产生的巨大差异（这个具体差异在css和js中都有），m$为了解决这个问题，提出了这两种模式，如果你不写doctype（这个词对大小写不敏感），那么ie会自动按混合模式也就是照ie5.5来渲染……orz
		
	所以请不要使用混合模式……
	


- 行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？

		（1）CSS规范规定，每个元素都有display属性，确定该元素的类型，每个元素都有默认的display值，
		  比如div默认display属性值为“block”，成为“块级”元素；
		  span默认display属性值为“inline”，是“行内”元素。  

		（2）行内元素有：a b span img input select strong（强调的语气） 
		 块级元素有：div ul ol li dl dt dd h1 h2 h3 h4…p  
	
		（3）知名的空元素： 
		<br> <hr> <img> <input> <link> <meta> 
		鲜为人知的是： 
		<area> <base> <col> <command> <embed> <keygen> <param> <source> <track> <wbr>
		
	注解：
		
	首先答案中那个空元素我不知道是什么意思，至少MDN上中那些空元素一般都属于inline元素。
		
	https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elemente
		
	我个人认为其实html的本质依旧是排版，所以从排版的角度来看看这个问题。
		
	block也就是块级元素其实对应着就是排版中的块，想想一张报纸的构成：标题，小标题，段落，列表等等，这都是一个块，中间只要有字就可以撑起一个版面。值得一提的是，在html5中添加了很多语义化标签，类似header，footer，section也都是块级元素啦。
		
	而inline也就是行内元素则对应着那些并不【重要】的内容，这里当然是对排版而言啦。比如图片，文字的格式（加粗倾斜删除线这种）图片，以及html中的一些交互内容（输入，选择）这些都是行内元素，他们都是不能独占一块区域的，按照内容的多少，他们才显示多少体积，这与霸气的块级元素有所不同。
		
	在告别了table的页面设计之后，现在的前端设计主要依靠css来完成控制，因此你可以为任意的元素设置属性，因此可以让a元素独占一行，也可以让h1元素苦逼的和p元素连在一起……
		
	除了上述两种显示效果之外还有inline-block，list-item，table，以及围绕table的一系列效果。
		
	这里简短的说一些inline-block吧，之前的block是独占一行，但是block有自己的高度，为了实现又有宽度，又有高度的效果，就产生了inline-blcok效果。list-item则是让这个元素像列表那样显示。

- link 和@import 的区别是？

	
		（1）link属于XHTML标签，而@import是CSS提供的;

		（2）页面被加载的时，link会同时被加载，而@import引用的CSS会等到页面被加载完再加载;

		（3）import只在IE5以上才能识别，而link是XHTML标签，无兼容问题;

		（4）link方式的样式的权重 高于@import的权重.	
	
	注解：
		
	其实题目的意思应该是用link和@import加载css的区别。
		
	由于同源限制（同源问题自己搜搜看），如果要加载一个外部文件，必须要用一个更安全的办法，于是就使用link标签来加载一个文件，本质上是一个get的过程。
		
	因此link除了可以加载样式表css之外，还可以加载很多东西，比如icon，sidebar等等，很强大，具体看MDN上的这个表：
		
	https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types
		
	至于@import嘛，首先加载css有四种写法（感觉跟孔乙己似的……）：link，embed，行内，@import。
		
	link已经说过，行内你也知道（就是把css写到元素的style里面……），embed是html5新增的嵌入内容的标签。
		
	@import可以在css的内部加载另外一个css。值得一提的是，@import也是get方法。
		
	所以单独的使用link和import都可以并行的加载css文件，然而两种方法一旦同时使用，link就会打断import的加载，就没有并行了，这将会引起阻塞，增加了页面加载时间。此外import还会引发css乱序加载的问题。
		
	因此为了性能和效果起见，还是不要用@import来加载文件了。

- 浏览器的内核分别是什么?
	
	     * IE浏览器的内核Trident、Mozilla的Gecko、Chrome的Blink（WebKit的分支）、Opera内核原为Presto，现为Blink；
	
	注解：

	Webkit内核目前主要是Safari在使用，而国内的一系列的快速浏览器也大都是根据Chromium的再开发……所以也都是Blink内核。
	
	相比这点，夸一下傲游吧，傲游好歹是基于Webkit来进行开发的……比那些人不知高到哪里去了……


- 常见兼容性问题？

		* png24位的图片在iE6浏览器上出现背景，解决方案是做成PNG8.
	
		* 浏览器默认的margin和padding不同。解决方案是加一个全局的*{margin:0;padding:0;}来统一。
		 
		* IE6双边距bug:块属性标签float后，又有横行的margin情况下，在ie6显示margin比设置的大。 
	       
		  浮动ie产生的双倍距离 #box{ float:left; width:10px; margin:0 0 0 100px;} 
	    
	     这种情况之下IE会产生20px的距离，解决方案是在float的标签样式控制中加入 ——_display:inline;将其转化为行内属性。(_这个符号只有ie6会识别)
	
		  渐进识别的方式，从总体中逐渐排除局部。 
	  
		  首先，巧妙的使用“\9”这一标记，将IE游览器从所有情况中分离出来。 
		  接着，再次使用“+”将IE8和IE7、IE6分离开来，这样IE8已经独立识别。
         
          css
	          .bb{
	           background-color:#f1ee18;/*所有识别*/
	          .background-color:#00deff\9; /*IE6、7、8识别*/
	          +background-color:#a200ff;/*IE6、7识别*/
	          _background-color:#1e0bd1;/*IE6识别*/ 
	          } 
  
		*  IE下,可以使用获取常规属性的方法来获取自定义属性,
		   也可以使用getAttribute()获取自定义属性;
           Firefox下,只能使用getAttribute()获取自定义属性. 
           解决方法:统一通过getAttribute()获取自定义属性.
          
		* IE下,even对象有x,y属性,但是没有pageX,pageY属性; 
          Firefox下,event对象有pageX,pageY属性,但是没有x,y属性.
		  
		* 解决方法：（条件注释）缺点是在IE浏览器下可能会增加额外的HTTP请求数。
		
		* Chrome 中文界面下默认会将小于 12px 的文本强制按照 12px 显示, 
		  可通过加入 CSS 属性 -webkit-text-size-adjust: none; 解决.

		* 超链接访问过后hover样式就不出现了 被点击访问过的超链接样式不在具有hover和active了解决方法是改变CSS属性的排列顺序:
		L-V-H-A :  a:link {} a:visited {} a:hover {} a:active {}
	    
	注解：这一条内容比较多哈，我挑几个来注解一下。

	浏览器默认margin和padding，这个主要是由于每个浏览器都有一套默认的显示效果，所以都会有一些默认的属性。
		
	以Chrome为例，p元素的段前和段后都有1em的margin，其他还有很多。为了控制不同浏览器上的效果一致，会采取一种reset的办法，将页面上所有的margin，padding等都干掉。这也是没办法，希望将来的标准里可以有一个全局属性来控制这一点。
		
	其他的ie问题就不补充了，研究ie的兼容问题是所有前端的痛。


- html5有哪些新特性、移除了那些元素？如何处理HTML5新标签的浏览器兼容问题？如何区分 HTML 和 
HTML5？
	
	
		* HTML5 现在已经不是 SGML 的子集，主要是关于图像，位置，存储，多任务等功能的增加。

		* 绘画 canvas  
		  用于媒介回放的 video 和 audio 元素 
		  本地离线存储 localStorage 长期存储数据，浏览器关闭后数据不丢失；
          sessionStorage 的数据在浏览器关闭后自动删除
		  
		  语意化更好的内容元素，比如 article、footer、header、nav、section 
		  表单控件，calendar、date、time、email、url、search  
		  新的技术webworker, websockt, Geolocation

		* 移除的元素
		
		纯表现的元素：basefont，big，center，font, s，strike，tt，u；
		
		对可用性产生负面影响的元素：frame，frameset，noframes；

	    	支持HTML5新标签：
		
		* IE8/IE7/IE6支持通过document.createElement方法产生的标签，
		  可以利用这一特性让这些浏览器支持HTML5新标签，
  
          	浏览器支持新标签后，还需要添加标签默认的样式：
	   
		* 当然最好的方式是直接使用成熟的框架、使用最多的是html5shim框架
		   <!--[if lt IE 9]> 
		   <script> src="http://html5shim.googlecode.com/svn/trunk/html5.js"</script> 
		   <![endif]--> 
		如何区分： DOCTYPE声明\新增的结构元素\功能元素

	注解：
		
	按照一般的说法，html5分为8个部分，分别是：语义化标签，离线存储，设备访问，网络连接，多媒体，图形接口，css3支持，以及性能提升。
		
	语义化标签（不是语意）之前提到过，就是排版思想，不再提。
		
	离线存储主要指LocalStorage，indexedDB等，可以搜搜看，我用前者做过几个小应用。
		
	设备访问是指现在可以用浏览器来访问更高权限的东西，比如传感器，视频，音频等等。
		
	网络连接主要指webSocket这类的技术。
		
	多媒体主要是指新增的video和audio标签，终于可以告别发热超厉害的flash了啊哈哈哈哈……
		
	图形接口包括canvas，2D，3D GDI。可以搜搜WebGL看。
		
	最后两个不提。
		
	

- 语义化的理解？ 
	
		用正确的标签做正确的事情！
		html语义化就是让页面的内容结构化，便于对浏览器、搜索引擎解析；
		在没有样式CCS情况下也以一种文档格式显示，并且是容易阅读的。
		搜索引擎的爬虫依赖于标记来确定上下文和各个关键字的权重，利于 SEO。
		使阅读源代码的人对网站更容易将网站分块，便于阅读维护理解。

	注解：
		
	上一个问题也说过，我个人认为最核心还是要让html符合排版思想。

- HTML5的离线储存？

	    	* localStorage    长期存储数据，浏览器关闭后数据不丢失；
        	* sessionStorage  数据在浏览器关闭后自动删除。
        	
        注解：
        
        记得还有indexedDB，别忘了。此外答案中的两个Storage是以字符串的形式保存的。

- (写)描述一段语义的html代码吧。

	    	（HTML5中新增加的很多标签（如：<article>、<nav>、<header>和<footer>等）
		就是基于语义化设计原则）  
			< div id="header"> 
			< h1>标题< /h1> 
			< h2>专注Web前端技术< /h2> 
			< /div>

	注解：
		
	这个答案写的也太……糙了……
		
	我来一个：
		< header>
			< nav></nav>
		</header>
		< aside></aside>
		< section>
			< h1></h1>
			< p></p>
		</section>
		< footer></footer>
			

- iframe有那些缺点？ 

		*iframe会阻塞主页面的Onload事件；

		*iframe和主页面共享连接池，而浏览器对相同域的连接有限制，所以会影响页面的并行加载。
	        使用iframe之前需要考虑这两个缺点。如果需要使用iframe，最好是通过javascript
	        动态给iframe添加src属性值，这样可以可以绕开以上两个问题。
	        
	注解：
	        
	请明确一点，iframe是在一个页面里又加载了一个网页，所以渲染是按照两个页面来的……
	        
	有的github上的项目主页上会用一个iframe加载这个项目的star按钮，很好玩。

- 请描述一下 cookies，sessionStorage 和 localStorage 的区别？ 

 		cookie在浏览器和服务器间来回传递。 sessionStorage和localStorage不会
		sessionStorage和localStorage的存储空间更大；
		sessionStorage和localStorage有更多丰富易用的接口；
		sessionStorage和localStorage各自独立的存储空间；
		
	注解：
		
	sessionStorage会随着会话关闭而移除，如果页面被意外刷新，可以通过它来进行恢复，这大大提升了表单页的体验，如果你开两个网页，就视为两个会话。（这一点没有验证）
		
	另外这里说一下indexDB的特点吧，就像一个真正的数据库一样需要操作。
		
- 如何实现浏览器内多个标签页之间的通信? (阿里)
		
		调用localstorge、cookies等本地存储方式

	注解：
		
	我觉得这里应该是指web message，如HTML5 window.postMessage()和server-sent事件以及web sockets。下面这个链接讲的很好。提示一下，这些方法存在兼容性问题。
		
	http://www.36ria.com/3890  

- webSocket如何兼容低浏览器？(阿里)
		
		Adobe Flash Socket 、 ActiveX HTMLFile (IE) 、 基于 multipart 编码发送 XHR 、 基于长轮询的 XHR


## <a name='css'>CSS</a> 

- 介绍一下CSS的盒子模型？

		（1）有两种， IE 盒子模型、标准 W3C 盒子模型；IE的content部分包含了 border 和 pading;

		（2）盒模型： 内容(content)、填充(padding)、边界(margin)、 边框(border).
		
	注解：
	
	我觉得应该细说是三种盒模型，Flexible Box也即是弹性盒模型。
	
	弹性盒模型是指对父元素空间分割的一种模式，通过添加几个参数就可以简单的实现grid的效果，简直赞。
	
	https://developer.mozilla.org/zh-CN/docs/CSS/Tutorials/Using_CSS_flexible_boxes



- CSS 选择符有哪些？哪些属性可以继承？优先级算法如何计算？ CSS3新增伪类有那些？

		*   	1.id选择器（ # myid）
			2.类选择器（.myclassname）
			3.标签选择器（div, h1, p）
			4.相邻选择器（h1 + p）
			5.子选择器（ul < li）
			6.后代选择器（li a）
			7.通配符选择器（ * ）
			8.属性选择器（a[rel = "external"]）
			9.伪类选择器（a: hover, li: nth - child）
		  
		*   可继承的样式： font-size font-family color, UL LI DL DD DT;

		*   不可继承的样式：border padding margin width height ;
		  
		*   优先级就近原则，同权重情况下样式定义最近者为准;

		*   载入样式以最后载入的定位为准;

		优先级为:
		  
		   !important >  id > class > tag  
		  
		   important 比 内联优先级高
		   
	

		CSS3新增伪类举例：

		p:first-of-type	选择属于其父元素的首个 <p> 元素的每个 <p> 元素。
		p:last-of-type	选择属于其父元素的最后 <p> 元素的每个 <p> 元素。
        p:only-of-type	选择属于其父元素唯一的 <p> 元素的每个 <p> 元素。
		p:only-child	选择属于其父元素的唯一子元素的每个 <p> 元素。
		p:nth-child(2)	选择属于其父元素的第二个子元素的每个 <p> 元素。
 	    :enabled  :disabled 控制表单控件的禁用状态。
		:checked        单选框或复选框被选中。

	注解：
	
	选择器部分，子选择器中，应该是一个大于号……
	
	选择器里也有比较好玩的，比如那个相邻选择器，比如要让整个列表的前三项特殊样式。
	
	可以li,li+li,li+li+li一个样式，li+li+li+li一个样式……
	
	选择器的优先度遵循这样一个原则：范围原则，比如tag选择器的范围就很大，相对class的就少很多，id则是整个页面中唯一的。
	
	关于important，请务必记住，因为它的优先度最高，因此当整个工程量比较复杂的时候，尽可能不要使用这个，会造成混乱。
	

- 如何居中div？如何居中一个浮动元素？

	*  给div设置一个宽度，然后添加margin:0 auto属性
		 
			div{
				width:200px;
				margin:0 auto;
			 }  

			 
	*  居中一个浮动元素
  
			  确定容器的宽高 宽500 高 300 的层
			  设置层的外边距
			 
		     	.div { 
			  Width:500px ; height:300px;//高度可以不设
			  Margin: -150px 0 0 -250px;
			  position:relative;相对定位
              		  background-color:pink;//方便看效果
			  left:50%;
			  top:50%;
			} 
	
	注解：

	居中元素是老考题了，最重要的一点是需要计算子元素和父元素的位置。
	
	在父元素是有宽度的前提下，经过计算，可以得出这个效果。
	
	还有一种办法，就是给元素加一个百分比的宽度，margin-left亦然。


- 列出display的值，说明他们的作用。position的值， relative和absolute定位原点是？
 
	      1.   
	      	block 象块类型元素一样显示。
		none 缺省值。象行内元素类型一样显示。
		inline-block 象行内元素一样显示，但其内容象块类型元素一样显示。
		list-item 象块类型元素一样显示，并添加样式列表标记。
	  
	      2. 
		*absolute	
			生成绝对定位的元素，相对于 static 定位以外的第一个父元素进行定位。 
	
		*fixed （老IE不支持）
			生成绝对定位的元素，相对于浏览器窗口进行定位。 
	
		*relative	
			生成相对定位的元素，相对于其正常位置进行定位。 
	
		* static	默认值。没有定位，元素出现在正常的流中
		*（忽略 top, bottom, left, right z-index 声明）。
	
		* inherit	
		 	规定从父元素继承 position 属性的值。

	注解：
	
	display部分前文有说过。
	
	position里比较容易混的是absolute和fixed，简而言之的讲，fixed用来显示页面头部，页面脚部的固定内容，在使用fixed时候，其他的内容将会无视fixed元素的高度，所以为了正常显示，请给后面内容加一个padding-top。

	  
- CSS3有哪些新特性？

  		CSS3实现圆角（border-radius:8px），阴影（box-shadow:10px），
		对文字加特效（text-shadow、），线性渐变（gradient），旋转（transform）
          	transform:rotate(9deg) scale(0.85,0.90) translate(0px,-30px) skew(-9deg,0deg);//旋转,缩放,定位,倾斜
          	增加了更多的CSS选择器  多背景 rgba 
          	
        注解：
        
        新特性都能写好几本书了……简而言之……强化了页面的形状的变形和动画效果，增加了更多的伪类选择器，背景选项也大大增强了。
        

- 一个满屏 品 字布局 如何设计?

	注解：
	
	……这个题……
	
	三个div，第一个宽度100%，第二个和第三个浮动，宽度自定义，加起来不大于100%就行。

- 经常遇到的CSS的兼容性有哪些？原因，解决方法是什么？

	注解：
	
	css兼容性可比html的多多了……
	
	ie6的盒模型不一样，一些新属性的浏览器实现不一样，需要加私有化前缀。


- 为什么要初始化CSS样式。

		- 因为浏览器的兼容问题，不同浏览器对有些标签的默认值是不同的，如果没对CSS初始化往往会出现浏览器之间的页面显示差异。
	
		- 当然，初始化样式会对SEO有一定的影响，但鱼和熊掌不可兼得，但力求影响最小的情况下初始化。

		*最简单的初始化方法就是： * {padding: 0; margin: 0;} （不建议）
	
		淘宝的样式初始化： 
		body, h1, h2, h3, h4, h5, h6, hr, p, blockquote, dl, dt, dd, ul, ol, li, pre, form, fieldset, legend, button, input, textarea, th, td { margin:0; padding:0; }
		body, button, input, select, textarea { font:12px/1.5tahoma, arial, \5b8b\4f53; }
		h1, h2, h3, h4, h5, h6{ font-size:100%; }
		address, cite, dfn, em, var { font-style:normal; }
		code, kbd, pre, samp { font-family:couriernew, courier, monospace; }
		small{ font-size:12px; }
		ul, ol { list-style:none; }
		a { text-decoration:none; }
		a:hover { text-decoration:underline; }
		sup { vertical-align:text-top; }
		sub{ vertical-align:text-bottom; }
		legend { color:#000; }
		fieldset, img { border:0; }
		button, input, select, textarea { font-size:100%; }
		table { border-collapse:collapse; border-spacing:0; } 
		
	注解：
	
	前文提过reset，这里就是……



- absolute的containing block计算方式跟正常流有什么不同？
	
	注解：

	没看懂题……absolute的计算是按照static 定位以外的第一个父元素进行定位。
	

- position跟display、margin collapse、overflow、float这些特性相互叠加后会怎么样？

	注解：
	
	我之前还真不知道这个问题……以下是我的测试结果：
	
	http://runjs.cn/code/zjz5apom
	
	从结果中可以看出，absolute和fixed直接让一个元素变成了inline-block的元素，所以display,float是没用的，margin等是有用的。
	
	relative只是对原来元素的一个位移，所以这些属性都能用。
	
	static很生猛，直接无视了那些属性……

- 对BFC规范的理解？

		（W3C CSS 2.1 规范中的一个概念,它决定了元素如何对其内容进行定位,以及与其他元素的关 系和相互作用。）
- css定义的权重

		以下是权重的规则：标签的权重为1，class的权重为10，id的权重为100，以下例子是演示各种定义的权重值：
	 
		/*权重为1*/
		div{
		}
		/*权重为10*/
		.class1{
		}
		/*权重为100*/
		#id1{
		}
		/*权重为100+1=101*/
		#id1 div{
		}
		/*权重为10+1=11*/
		.class1 div{
		}
		/*权重为10+10+1=21*/
		.class1 .class2 div{
		} 
		
		如果权重相同，则最后定义的样式会起作用，但是应该避免这种情况出现
		
	注解：
	
	这样子算太痛苦……还是请记住范围原则。


- 解释下浮动和它的工作原理？清除浮动的技巧

	注解：
	
	工作原理其实我的观点是这样的：根据一定的规则，将浮动元素的一个属性进行排列。
	
	规则可以是左浮动，右浮动，上对齐，下对齐，左右对齐等等，对应规则提取一个属性（宽或高）进行排列。其他的无视掉……
	
	清楚浮动的技巧说两个：
	
	在子元素的浮动后面加一个空的div，对应的css是clear:both;
	
	或者直接用:after伪类。
	
	有一个好玩的事情是，float也是浮点数的意思，所以在js中改变css的时候要注意……

- 用过媒体查询，针对移动端的布局吗？
	
	注解：

	媒体查询本意是为了让html在不同的设备上效果适应，比如打印机，屏幕等等。
	
	然而因为可以通过查询一些属性如宽度和高度来区别的写css，也成为了响应式布局的方案。
	
	我个人认为这种现状需要改变。

- 使用 CSS 预处理器吗？喜欢那个？
		
		SASS 

	注解：
	
	常见的有LESS，SASS，stylus，第一个是用js写的，第二个使用ruby写的，配合compass一同使用，威力无穷！

- 如果需要手动写动画，你认为最小时间间隔是多久，为什么？（阿里）

		多数显示器默认频率是60Hz，即1秒刷新60次，所以理论上最小间隔为1/60＊1000ms ＝ 16.7ms
		
	注解：
	
	其实人眼看起来才24帧一秒，那么1/24应该也是备选答案之一。
	
	实际上很难做到1/60的动画，为了保证浏览器的性能跟得上，一般会使用降帧的办法来进行优化。


- display:inline-block 什么时候会显示间隙？(携程)

		移除空格、使用margin负值、使用font-size:0、letter-spacing、word-spacing
 


## <a name='js'>JavaScript</a>

-  JavaScript原型，原型链 ? 有什么特点？

-  eval是做什么的？ 

		它的功能是把对应的字符串解析成JS代码并运行；
		应该避免使用eval，不安全，非常耗性能（2次，一次解析成js语句，一次执行）。

-  null，undefined 的区别？

-  写一个通用的事件侦听器函数。

			// event(事件)工具集，来源：github.com/markyun
			markyun.Event = {
				// 页面加载完成后
				readyEvent : function(fn) {
					if (fn==null) {
						fn=document;
					}
					var oldonload = window.onload;
					if (typeof window.onload != 'function') {
						window.onload = fn;
					} else {
						window.onload = function() {
							oldonload();
							fn();
						};
					}
				},
				// 视能力分别使用dom0||dom2||IE方式 来绑定事件
				// 参数： 操作的元素,事件名称 ,事件处理程序
				addEvent : function(element, type, handler) {
					if (element.addEventListener) {
						//事件类型、需要执行的函数、是否捕捉
						element.addEventListener(type, handler, false);
					} else if (element.attachEvent) {
						element.attachEvent('on' + type, function() {
							handler.call(element);
						});
					} else {
						element['on' + type] = handler;
					}
				},
				// 移除事件
				removeEvent : function(element, type, handler) {
					if (element.removeEnentListener) {
						element.removeEnentListener(type, handler, false);
					} else if (element.datachEvent) {
						element.detachEvent('on' + type, handler);
					} else {
						element['on' + type] = null;
					}
				}, 
				// 阻止事件 (主要是事件冒泡，因为IE不支持事件捕获)
				stopPropagation : function(ev) {
					if (ev.stopPropagation) {
						ev.stopPropagation();
					} else {
						ev.cancelBubble = true;
					}
				},
				// 取消事件的默认行为
				preventDefault : function(event) {
					if (event.preventDefault) {
						event.preventDefault();
					} else {
						event.returnValue = false;
					}
				},
				// 获取事件目标
				getTarget : function(event) {
					return event.target || event.srcElement;
				},
				// 获取event对象的引用，取到事件的所有信息，确保随时能使用event；
				getEvent : function(e) {
					var ev = e || window.event;
					if (!ev) {
						var c = this.getEvent.caller;
						while (c) {
							ev = c.arguments[0];
							if (ev && Event == ev.constructor) {
								break;
							}
							c = c.caller;
						}
					}
					return ev;
				}
			}; 



-  Node.js的适用场景？

		高并发、聊天、实时消息推送

-  介绍js的基本数据类型。

		number,string,boolean,object,undefined
	
-  Javascript如何实现继承？

		通过原型和构造器
	
-  ["1", "2", "3"].map(parseInt) 答案是多少？

		 [1, NaN, NaN] 因为 parseInt 需要两个参数 (val, radix) 但 map 传了 3 个 (element, index, array)

-  如何创建一个对象? （画出此对象的内存图）

		  function Person(name, age) {
		    this.name = name;
		    this.age = age;
		    this.sing = function() { alert(this.name) } 
		  } 


-  谈谈This对象的理解。

		this是js的一个关键字，随着函数使用场合不同，this的值会发生变化。
	
	    但是有一个总原则，那就是this指的是调用函数的那个对象。
		
	    this一般情况下：是全局对象Global。 作为方法调用，那么this就是指这个对象	

-  事件是？IE与火狐的事件机制有什么区别？ 如何阻止冒泡？ 

		 1. 我们在网页中的某个操作（有的操作对应多个事件）。例如：当我们点击一个按钮就会产生一个事件。是可以被 JavaScript 侦测到的行为。  
		 2. 事件处理机制：IE是事件冒泡、火狐是 事件捕获；
		 3. ev.stopPropagation();

-  什么是闭包（closure），为什么要用它？


		执行say667()后,say667()闭包内部变量会存在,而闭包内部函数的内部变量不会存在.使得Javascript的垃圾回收机制GC不会收回say667()所占用的资源，因为say667()的内部函数的执行需要依赖say667()中的变量。这是对闭包作用的非常直白的描述.
  
		  function say667() {
			// Local variable that ends up within closure
			var num = 666;
			var sayAlert = function() { alert(num); }
			num++;
			return sayAlert;
		}
		 
		 var sayAlert = say667();
		 sayAlert()//执行结果应该弹出的667  


-  "use strict";是什么意思 ? 使用它的好处和坏处分别是什么？

-  如何判断一个对象是否属于某个类？


		
 		  使用instanceof （待完善）

	       if(a instanceof Person){
	           alert('yes');
	       }
-  new操作符具体干了什么呢?

			 1、创建一个空对象，并且 this 变量引用该对象，同时还继承了该函数的原型。
	  	  	 2、属性和方法被加入到 this 引用的对象中。
	 		 3、新创建的对象由 this 所引用，并且最后隐式的返回 this 。
		    
		var obj  = {};
		obj.__proto__ = Base.prototype;
		Base.call(obj); 

-  Javascript中，有一个函数，执行时对象查找时，永远不会去查找原型，这个函数是？
  
		hasOwnProperty

-  JSON 的了解？
		
		JSON(JavaScript Object Notation) 是一种轻量级的数据交换格式。
		它是基于JavaScript的一个子集。数据格式简单, 易于读写, 占用带宽小
        {'age':'12', 'name':'back'}

-  js延迟加载的方式有哪些？
		
		defer和async、动态创建DOM方式（用得最多）、按需异步载入js

		
-  ajax 是什么? 

-  同步和异步的区别?

-  如何解决跨域问题?
	 
		jsonp、 iframe、window.name、window.postMessage、服务器上设置代理页面
-  模块化怎么做？


		
	 [ 立即执行函数](http://benalman.com/news/2010/11/immediately-invoked-function-expression/),不暴露私有成员
		
		    var module1 = (function(){
		    　　　　var _count = 0;
		    　　　　var m1 = function(){
		    　　　　　　//...
		    　　　　};
		    　　　　var m2 = function(){
		    　　　　　　//...
		    　　　　};
		    　　　　return {
		    　　　　　　m1 : m1,
		    　　　　　　m2 : m2
		    　　　　};
		    　　})(); 

-  AMD（Modules/Asynchronous-Definition）、CMD（Common Module Definition）规范区别？

-  异步加载的方式有哪些？

			
	      (1) defer，只支持IE
	      
	      (2) async：
	      
	      (3) 创建script，插入到DOM中，加载完毕后callBack
	  
- documen.write和 innerHTML的区别
			  
document.write只能重绘整个页面

innerHTML可以重绘页面的一部分
		  

-  .call() 和 .apply() 的区别？

						
		  例子中用 add 来替换 sub，add.call(sub,3,1) == add(3,1) ，所以运行结果为：alert(4); 
		
		  注意：js 中的函数其实是对象，函数名是对 Function 对象的引用。
		 
			function add(a,b)
			{
			    alert(a+b);
			}
			
			function sub(a,b)
			{
			    alert(a-b);
			}
			
			add.call(sub,3,1);  

-  Jquery与jQuery UI 有啥区别？ 

			
		*jQuery是一个js库，主要提供的功能是选择器，属性修改和事件绑定等等。

		*jQuery UI则是在jQuery的基础上，利用jQuery的扩展性，设计的插件。
         提供了一些常用的界面元素，诸如对话框、拖动行为、改变大小行为等等


-  JQuery的源码看过吗？能不能简单说一下它的实现原理？

-  jquery 中如何将数组转化为json字符串，然后再转化回来？

			
jQuery中没有提供这个功能，所以你需要先编写两个jQuery的扩展：
 
		$.fn.stringifyArray = function(array) {
		    return JSON.stringify(array)
		}
		
		$.fn.parseArray = function(array) {
		    return JSON.parse(array)
		} 

		然后调用：
		$("").stringifyArray(array)


-  针对 jQuery 的优化方法？

		*基于Class的选择性的性能相对于Id选择器开销很大，因为需遍历所有DOM元素。

		*频繁操作的DOM，先缓存起来再操作。用Jquery的链式调用更好。   
         比如：var str=$("a").attr("href");

		*for (var i = size; i < arr.length; i++) {}
         for 循环每一次循环都查找了数组 (arr) 的.length 属性，在开始循环的时候设置一个变量来存储这个数字，可以让循环跑得更快： 
         for (var i = size, length = arr.length; i < length; i++) {}


-  JavaScript中的作用域与变量声明提升？ 

-  如何编写高性能的Javascript？

-  那些操作会造成内存泄漏？


			 
	    内存泄漏指任何对象在您不再拥有或需要它之后仍然存在。
        垃圾回收器定期扫描对象，并计算引用了每个对象的其他对象的数量。如果一个对象的引用数量为 0（没有其他对象引用过该对象），或对该对象的惟一引用是循环的，那么该对象的内存即可回收。

        setTimeout 的第一个参数使用字符串而非函数的话，会引发内存泄漏。
		闭包、控制台日志、循环（在两个对象彼此引用且彼此保留时，就会产生一个循环）

-  JQuery一个对象可以同时绑定多个事件，这是如何实现的？

- 如何判断当前脚本运行在浏览器还是node环境中？（阿里）
			
		通过判断Global对象是否为window，如果不为window，当前脚本没有运行在浏览器中
  

## <a name='other'>其他问题</a>


- 你遇到过比较难的技术问题是？你是如何解决的？

- 常使用的库有哪些？常用的前端开发工具？开发过什么应用或组件？

- 页面重构怎么操作？

- 列举IE 与其他浏览器不一样的特性？

- 99%的网站都需要被重构是那本书上写的？

- 什么叫优雅降级和渐进增强？

- WEB应用从服务器主动推送Data到客户端有那些方式？

- 对Node的优点和缺点提出了自己的看法？

		
		*（优点）因为Node是基于事件驱动和无阻塞的，所以非常适合处理并发请求，
          因此构建在Node上的代理服务器相比其他技术实现（如Ruby）的服务器表现要好得多。
		  此外，与Node代理服务器交互的客户端代码是由javascript语言编写的，
	      因此客户端和服务器端都用同一种语言编写，这是非常美妙的事情。

		*（缺点）Node是一个相对新的开源项目，所以不太稳定，它总是一直在变，
          而且缺少足够多的第三方库支持。看起来，就像是Ruby/Rails当年的样子。


- 你有哪些性能优化的方法？


		 （看雅虎14条性能优化原则）。
	
		  （1） 减少http请求次数：CSS Sprites, JS、CSS源码压缩、图片大小控制合适；网页Gzip，CDN托管，data缓存 ，图片服务器。
		
		  （2） 前端模板 JS+数据，减少由于HTML标签导致的带宽浪费，前端用变量保存AJAX请求结果，每次操作本地变量，不用请求，减少请求次数
		
		  （3） 用innerHTML代替DOM操作，减少DOM操作次数，优化javascript性能。
		
		  （4） 当需要设置的样式很多时设置className而不是直接操作style。
		
		  （5） 少用全局变量、缓存DOM节点查找的结果。减少IO读取操作。
		
		  （6） 避免使用CSS Expression（css表达式)又称Dynamic properties(动态属性)。
		
		  （7） 图片预加载，将样式表放在顶部，将脚本放在底部  加上时间戳。
		
		  （8） 避免在页面的主体布局中使用table，table要等其中的内容完全下载之后才会显示出来，显示比div+css布局慢。

- http状态码有那些？分别代表是什么意思？

		100-199 用于指定客户端应相应的某些动作。 
		200-299 用于表示请求成功。 
		300-399 用于已经移动的文件并且常被包含在定位头信息中指定新的地址信息。 
		400-499 用于指出客户端的错误。400	1、语义有误，当前请求无法被服务器理解。401	当前请求需要用户验证 403	服务器已经理解请求，但是拒绝执行它。
		500-599 用于支持服务器错误。 503 – 服务不可用

- 一个页面从输入 URL 到页面加载显示完成，这个过程中都发生了什么？（流程说的越详细越好）


			查找浏览器缓存 
		    DNS解析、查找该域名对应的IP地址、重定向（301）、发出第二个GET请求
		    进行HTTP协议会话
		    客户端发送报头(请求报头)
		    服务器回馈报头(响应报头)
		    html文档开始下载
		    文档树建立，根据标记请求所需指定MIME类型的文件
		    文件显示
			[
			浏览器这边做的工作大致分为以下几步：
			
			加载：根据请求的URL进行域名解析，向服务器发起请求，接收文件（HTML、JS、CSS、图象等）。
			
			解析：对加载到的资源（HTML、JS、CSS等）进行语法解析，建议相应的内部数据结构（比如HTML的DOM树，JS的（对象）属性表，CSS的样式规则等等）
			}
- 除了前端以外还了解什么其它技术么？你最最厉害的技能是什么？

- 你常用的开发工具是什么，为什么？

- 对前端界面工程师这个职位是怎么样理解的？它的前景会怎么样？

		     前端是最贴近用户的程序员，比后端、数据库、产品经理、运营、安全都近。
			1、实现界面交互
			2、提升用户体验
			3、有了Node.js，前端可以实现服务端的一些事情
			

		前端是最贴近用户的程序员，前端的能力就是能让产品从 90分进化到 100 分，甚至更好，
        
         参与项目，快速高质量完成实现效果图，精确到1px；
        
         与团队成员，UI设计，产品经理的沟通；
        
         做好的页面结构，页面重构和用户体验；
        
         处理hack，兼容、写出优美的代码格式；
        
         针对服务器的优化、拥抱最新前端技术。
- 加班的看法？


   		加班就像借钱，原则应当是------救急不救穷
	


- 平时如何管理你的项目？

				先期团队必须确定好全局样式（globe.css），编码模式(utf-8) 等；

				编写习惯必须一致（例如都是采用继承式的写法，单样式都写成一行）；
			
				标注样式编写人，各模块都及时标注（标注关键样式调用的地方）；
			
				页面进行标注（例如 页面 模块 开始和结束）；
			
				CSS跟HTML 分文件夹并行存放，命名都得统一（例如style.css）；
			
				JS 分文件夹存放 命名以该JS功能为准的英文翻译。
			
				图片采用整合的 images.png png8 格式文件使用 尽量整合在一起使用方便将来的管理
- 如何设计突发大规模并发架构？


- 说说最近最流行的一些东西吧？常去哪些网站？ 

			Node.js、Mongodb、npm、MVVM、MEAN、three.js 

- 移动端（Android IOS）怎么做好用户体验?

			清晰的视觉纵线、信息的分组、极致的减法、
			利用选择代替输入、标签及文字的排布方式、
			依靠明文确认密码、合理的键盘利用、

- 你在现在的团队处于什么样的角色，起到了什么明显的作用？

- 你认为怎样才是全端工程师（Full Stack developer）？ 


- 介绍一个你最得意的作品吧？

- 你的优点是什么？缺点是什么？

- 如何管理前端团队?


- 最近在学什么？能谈谈你未来3，5年给自己的规划吗？

- 想问公司的问题？
		
			问公司问题：
			目前关注哪些最新的Web前端技术（未来的发展方向）？
			前端团队如何工作的（实现一个产品的流程）？
			公司的薪资结构是什么样子的？


## <a name='web'>优质网站推荐</a>

1. 极客标签：		 http://www.gbtags.com/


2. 码农周刊：		 http://weekly.manong.io/issues/


3. 前端周刊：		 http://www.feweekly.com/issues


9. 极客头条： 	 http://geek.csdn.net/


3. Startup News：http://news.dbanotes.net/


4. Hacker News： https://news.ycombinator.com/news  


7. InfoQ：  		 http://www.infoq.com/ 


10. w3cplus：     http://www.w3cplus.com/


10. Stack Overflow： http://stackoverflow.com/ 


6. Atp：  		 http://atp-posts.b0.upaiyun.com/posts/ 



###the last time that refresh: 2014/4/5 15:12:43 

	爱机车、爱骑行、爱旅行、爱摄影、爱阅读的理想青年，前端开发攻城师。
		
	我的微博：http://weibo.com/920802999
