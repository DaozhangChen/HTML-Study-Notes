# 《HTML入门笔记1》
近期学习了有关HTML的一些基础知识，并做了一些笔记，以下就是笔记的主题内容，内容包含五个部分，分别为
1. HTML是谁发明的？
2. HTML的起手式应该写什么？
3. 常用的表章节标签有哪些，分别是什么意思？
4. 全局属性有哪些？
5. 常用的内容标签有哪些，分别是什么意思？
  
  本文是自己观看饥人谷方应杭老师的《前端体系课》中的所学知识内容，由于本人是初学者，其中的内容可能表达或描述不够准确与全面，望各位能够多多谅解，另外，若有错误的内容，也恳请各位大佬们批评指正，感谢各位。
## HTML是谁发明的？
HTML的发明者是来自英国的Tim Berners-Lee，此人被称为HTML之父，由于2004年英国女皇给他颁发不列颠帝国勋章的爵级司令勋章，之后的叙述中将用**李爵士**来代替。  
那么李爵士干了什么事呢？  
在上世纪80年代，李爵士在物理实验室工作时，闻到走廊旁紫丁香花丛的香气，于是就有了一个灵感：人脑可以透过互相联贯的神经传递信息，为什么不可以经由电脑文件互相连接形成"超文本"呢？  
于是在1989年，李爵士就成功开发出了世界上第一个Web服务器和Web客户机，同年12月，李爵士为他的发明定名为World Wide Web，即我们熟悉的**WWW**。  
而WWW就是URL、HTTP、HTML的集合，使用HTML，将所需要表达的信息按某种规则写成HTML文件，通过专用的浏览器来识别，并将这些HTML文件“翻译”成可以识别的信息，即我们所见到的网页。
## HTML的起手式应该写什么？
认真的说，需要写这些
```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
是不是很多东西，但是只要你有安装*emmet插件*，就只需要在编译器中输入一个！，然后加一下tab就可以自动帮你输入这一段HTML起手式。（非常好用！）  
输入效果如下图所示  
![HTML起手式](HTML%E8%B5%B7%E6%89%8B%E5%BC%8F.png)
## HTML常用的表章节的标签有哪些，分别是什么意思？
常用的表章节标签有：  
* h1~h6
* section
* article
* main
* aside  
他们的含义及用法是：  
## h1~h6
h1~h6标签为标题标签，展现了6个不同级别的标题，不同标题的字体大小不同，h1的字体最大，h6级别的字体最小。下面放图来感受一下
![标题字体大小](h1~h6.png)  
*图中少了一个`<body>`,忘记写了。。。*
## section
section表示一个通用独立章节，一般来说会在section中包含一个标题，即h1~h6一般为section的子元素。
```html
<body>
    <section>
        <h1>我是老八</h1>
        <p>嗨害嗨</p>
    </section>
</body>
```
## article
意思为文章，是HTML中的一个独立结构，其意在可成为独立分配或者可复用的结构，一般来说一个article结构中会有若干个section结构。  
```html
<body>
    <main>
      <article>
        <header>我是谁？</header>
        <h1>大家来说说我是谁？</h1>
        <section>
          <h2>我是老六</h2>
          <p>人人都是老六</p>
        </section>
        <section>
          <h2>我是老八</h2>
          <p>嗨害嗨</p>
        </section>
        <footer>奥利给</footer>
      </article>
    </main>
  </body>
```
article与section元素的区别：  
article是页面中独立的、完整的内容，除了内容部分一般还有自己的标题、头注和脚注。  
section是对页面的内容进行分块，一个section通常由内容和标题组成。  
**什么时候该用article？什么时候用section呢？**  
article注重独立性，section强调分块，通常来说，一块内容相对独立与完整的时候则推荐用article，但是如果需要把一块内容分成好几块的时候则推荐使用section。
## main
此元素呈现了HTML文档的主体部分，一般是article的父元素。
```html
<body>
    <main>
    <article>
      <section>
        <h2>我是老六</h2>
        <p>人人都是老六</p>
      </section>
      <section>
        <h2>我是老八</h2>
        <p>嗨害嗨</p>
      </section>
    </article>
    </main>
  </body>
```
## aside
与main元素相反，是表示与主体内容无关的部分，可被单独拆分出来而不会使整体受到影响。通常表现为侧边栏或者标注框。
```html
<section>
  <h2>我是老八</h2>
    <aside>老八：一个神奇的物种</aside>
  <p>嗨害嗨</p>
</section>
```
## 全局属性有哪些？
全局属性指所有标签都具备的属性。  
常见的全局属性有：  
* class
* contenteditable
* hidden
* id
* style
* tabindex
* title  
## class
表示声明，创建一个标签，用于定义该标签中的属性。
![class效果图](class.png)
图中我用class声明了两个标签middle和bordered，并使用.middle和.bordered来定义两个标签的样式。*（推荐使用加上标签的形式来定义标签，这样可以使每个标签独立出来，若下面的class中包含多个独立标签，就可以直接使用，而不需要再次定义一个全新的标签样式）*
## 