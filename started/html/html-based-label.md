# HTML基础标签

### H系列标签

* 作用:用于给文本添加标题语义;
* 格式:`<h1>我是标题1</h1>;`

> H系列标签会独占一行;

{% hint style="info" %}
1. H系列标签共6个,h1~h6,多则无效;
2. 项目中慎用,尤其是h1\(有关SEO权重\);
{% endhint %}

### P标签

* 作用:用于给文本添加段落语义
* 格式:`<p>我是段落</p>`

> P系列标签会独占一行;

### Hr标签

* 作用:在网页中显示一个水平分割线
* 格式:`<hr/>`
* 由于Hr标签修改样式,所以不推荐使用

### 注释

* 什么是注释?
  * 注释用来在文档中插入注释语句。注释语句不会在浏览器中显示。
* 使用注释的原因?
  * 使用注释对代码进行解释，这样做有助于在以后的时间对代码的编辑\(提高阅读性\)。特别是代码量很大的情况下很有用。
* 格式:`<!--注释-->`

### Img标签

* 作用:在网页中插入图片
* 格式:`<img src="xxx.jpg">`

### Br标签

* 作用:让内容换行
* 格式:`<br/>`

### 绝对路径和相对路径

* 绝对路径:从电脑具体盘符寻找文件
* 相对路径:文件相对于当前文件的位置寻找

{% hint style="info" %}
绝对路径可移植性差,不建议使用;
{% endhint %}

### A标签

* 作用:为文字或者图片添加链接
* 格式:&lt;a href="xxx.xxx"&gt;这里是超链接&lt;/a&gt;
* 补充\(a标签其他用法\):
  * 假链接:`<a href="#">超链接</a>`或者是`<a href="javacript:;"></a>`
  * 跳转页面指定位置\(配合id使用\):`<a href="#slideshow"></a>`

### Base标签

* 作用:指定当前网页所有超链接打开方式
* 格式:`<base target="_block">;`

> 1. a标签内部指定的打开方式优先级要高;
> 2. base标签要放在head\(头部\)标签内;

