# html5-learning
这里记录的是我阅读《HTML5权威指南》的学习笔记  
**<font color='red'>期望</font>**：对html有更深入的了解，能够将所学到的理论知识熟练地运用到实际项目中  
***
### 打卡 -- day1
#### 前期准备  
浏览器：Chrome   
编辑器：VS code  
后台服务：node.js  
web服务器：？

#### 复习HTML 
结合[w3school](http://www.w3school.com.cn/html/html_jianjie.asp)的内容
##### 什么是HTML 
HTML 是用来描述网页的超文本标记语言（Hyper Text Markup Language）  
注：*标记语言：由标签组成*
+ HTML 标签(tag)  
    1. 由尖括号包围的关键词，比如：&lt;html&gt;
    2. 通常成对出现的,如:&lt;body&gt;&lt;/body&gt; ，其中，第一个标签为开始标签（开放标签），第二个标签为结束标签（闭合标签）

+ HTML 文档 
    1. 就是网页
    2. 由HTML元素和纯文本组成
    3. web浏览器的作用就是解析HTM文档，并以网页的形式展示出来


+ HTML 元素
    1. 从开始标签到结束标签之间的所有代码
    2. 两种表现形式 
        - 非空元素  
        <开始标签>元素内容<结束标签>
        - 空元素（元素内容为空）   
        <开始标签 />
        - 虚元素  
        规范规定不允许放置任何内容
        比如：&lt;br /&gt;、&lt;img /&gt;、&lt;hr /&gt;
    3. 大多数HTML有属性

+ HTML 属性
    1. 一般以名称/值对的形式出现，值通常以双引号包着
    2. 布尔属性不需要设定值，只需要属性名，如 disabled、checked
    3. 定义在开始标签中
    4. 多个属性之间已空格隔开
    5. 自定义属性  
    以data-开头
    
##### 创建HTML文档
+ &lt;!DOCTYPE&gt;   
    1. DOCTYPE不是html的标签，它的作用是告诉浏览器页面是用哪个版本的HTML编写的  
    2. <font color=red>为避免浏览器解析出错，DOCTYPE必须为于HTML文档的第一行</font>  
    3. HTML4.01 基于SGML，因此&lt;!DOCTYPE&gt;需要声明引用DTD(DTD规定了标记语言的规则)
    4.HTML5 不基于SGML，因此不需要引用DTD

+ &lt;html&gt; 标签  
    紧跟在&lt;!DOCTYPE&gt;之后的是&lt;html&gt;标签，告知浏览器，以下就是HTML文档的内容了。

+ &lt;head&gt; 元素 
    1. &lt;head&gt;是所有头部元素的容器
    2. 可包含的标签:  
    &lt;title&gt;  (文档标题)  
    &lt;base&gt; （）  
    &lt;link&gt; （外联样式表） 
    &lt;meta&gt; （元数据）  
    &lt;script&gt; （javascript脚本）
    &lt;style&gt; （内联样式）  


    


