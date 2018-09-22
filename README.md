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

+ HTML文档
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
    1. 一般以名称/值对的形式出现，值通常以双引号包着
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
    2. 可包含的标签:  
    + &lt;title&gt;   
        - 定义浏览器工具栏中的标题
        - 页面被添加到收藏夹时显示的标题
        - 显示在搜索引擎结果中的页面标题  
    
    + &lt;base&gt;  
        - 为页面上的所有链接规定默认地址或默认目标
        - 如：
        &lt;base href="http://www.w3school.com.cn/images/" /&gt;  
        &lt;base target="_blank" /&gt;

    + &lt;link&gt; （外联样式表)    
        - 标签定义文档与外部资源之间的关系  
        - 最常用于链接样式表
        - 如：  
        &lt;link rel="stylesheet" type="text/css" href="mystyle.css" /&gt;  
    + &lt;meta&gt; （元数据）
        - 元数据是关于数据的信息
        - 不会显示在页面上，但是对于机器是可读的
        - 常用于规定页面的描述、关键词（用于搜索引擎)、文档的作者、最后修改时间（用于告知浏览器如何显示内容或重新加载页面）以及其他元数据  
        - 必需属性：content  
            定义与http-equiv 或那么属性相关的元信息
        - 可选属性：   
            * http-equiv   
            1）把content属性关联到HTTP头部
            2）指示服务器在向浏览器发送文档之前，先发送给浏览器的MIME文档头部
            3）可能值：  
                content-type
                expires
                refresh
                set-cookie
            4) 如：
            &lt;meta http-equiv="Content-Type" content="text/html; charset=gb2312" /&gt;

            文档重定向：  
&lt;meta http-equiv="Refresh" content="5;url=http://www.w3school.com.cn" /&gt;

            * name  
            1) 把content属性关联到一个名称  
            2) 可能值：  
                author    
                description  
                keywords  
                generator  
                revised  
                others  
            * scheme  
            1) 定义由于翻译content属性值的格式
        - 如：
        &lt;meta name="description" content="Free Web tutorials on HTML, CSS, XML" /&gt;  
        &lt;meta name="keywords" content="HTML, CSS, XML" /&gt;


    + &lt;script&gt; （javascript脚本）
    + &lt;style&gt; （内联样式）  
        - 用于为 HTML 文档定义样式信息

+ &lt;body&gt;  
    文档内容在这里编写

#### HTML5 全局属性
1. accessKey  
规定访问元素的键盘快捷键 （？在mac上不生效？）  
2. class  
    - 原生js选择：document.getElementsByClassName()
    - jQuery选择：$('.' + className)
3. dir  
    - 规定元素中<font color='#ff000'>**文字**</font>的方向
    - 两个有效值：
    1. ltr (从左到右)
    2. rtl（从右到左）
    - 常用于&lt;bdo标签&gt; [使用示例](https://hf024.github.io/html5-learning/demo/html-bdo-dir.html)
    - 运用在非&lt;bdo&gt;标签上时，与text-align的表现类似，但是又有区别，[查看](https://hf024.github.io/html5-learning/demo/html-dir.html)
4. id  
    - 元素的唯一标识符
    - 可用来定位到文档中的特定位置，如:demo.html中有一个id属性为element的元素，则可以使用example.html#elment直接定位到该元素
    - 原生JS选择：document.getElementById()
    - jQuery选择：$('#' + id)
5. lang  
    - 说明元素内容的使用语言
    - 有效值必须是ISO语言代码，常用的：en(英语)，zh(中文)
    - 常用于&lt;html&gt;标签
6. style  
    - 直接在元素上定义css样式
7. tabindex
    - HTML页面上的键盘焦点可以通过按Tab键在各元素之间切换，tabindex属性可以改变默认的切换顺序  
    - 值设置为-1的元素，在用户按下Tab键后不会被选中
    - 值设为大于0的数，值越小，被选中的优先级越高
    - [使用示例](https://hf024.github.io/html5-learning/demo/html-tabindex.html)
8. title  
    - 提供元素的额外信息，通常用于显示提示信息
    - 常用在&lt;a&gt;标签上

以下是HTML5<font color='red'>新增</font>属性
9. contenteditable
    - 让用户能够修改页面内容
    - 值设置为true时，元素可编辑
    - 值设置为false时，元素禁止编辑
    - [使用示例](https://hf024.github.io/html5-learning/demo/html5-contenteditable.html)
10. contextmenu
11. data-yourvalue
12. draggle
13. hidden
14. item  
15. itemprop  
16. spellcheck  
17. subject  




