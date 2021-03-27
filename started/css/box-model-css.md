# 盒模型

### 边框

> 边框就是环绕在标签宽度和高度周围的线条

* 格式:

```text
/*连写(同时设置四条边的边框)*/
border: 边框的宽度 边框的样式 边框的颜色;
```

{% hint style="info" %}
1. 这种格式中颜色属性可以省略, 省略之后默认就是黑色;
2. 这种格式中样式不能省略, 省略之后就看不到边框了;
3. 这种格式中宽度可以省略, 省略之后还是可以看到边框;
{% endhint %}

```text
/*连写(分别设置四条边每条边的边框)*/
border-top: 边框的宽度 边框的样式 边框的颜色;
border-right: 边框的宽度 边框的样式 边框的颜色;
border-bottom: 边框的宽度 边框的样式 边框的颜色;
border-left: 边框的宽度 边框的样式 边框的颜色;
```

```text
/*连写(分别设置四条边的边框的样式)*/
border-width: 上 右 下 左;
border-style: 上 右 下 左;
border-color: 上 右 下 左;
```

> 1. 这三个属性的取值是按照顺时针来赋值, 也就是按照上右下左来赋值, 而不是按照日常生活中的上下左右 
> 2. 这三个属性的取值省略时的规律:
>    1. 左边的取值和右边的一样;
>    2. 下边的取值和上边一样;
>    3. 右下左边取值和上边一样;

```text
/*非连写(方向+要素)*/
border-left-width: 20px;
border-left-style: double;
border-left-color: pink;
```

### 内边距

> 边框和内容之间的距离就是内边距

* 格式:

```text
/*非连写*/
padding-top: ;
padding-right: ;
padding-bottom: ;
padding-left: ;
```

```text
/*连写*/
padding: 上 右 下 左;
```

* 属性省略时的取值同[边框](box-model-css.md#bian-kuang-shu-xing)一样;
* 给标签设置内边距之后, 标签占有的宽度和高度会发生变化;
* 给标签设置内边距之后, 内边距也会有背景颜色;

### 外边距

> 标签和标签之间的距离就是外边距

* 格式:

```text
/*非连写*/
margin-top: ;
margin-right: ;
margin-bottom: ;
margin-left: ;
```

```text
/*连写*/
margin: 上 右 下 左;
```

* 属性省略时的取值同[边框](box-model-css.md#bian-kuang)一样;
* 外边距的那一部分是没有背景颜色的;

#### 外边距的合并现象

> 在默认布局的垂直方向上, 默认情况下外边距是不会叠加的, 会出现合并现象, 谁的外边距比较大就听谁的

### CSS盒模型

> CSS盒模型仅仅是一个形象的比喻, HTML中所有的标签都是盒子

### 盒子模型宽度和高度

> 1. 内容的宽度和高度 就是通过width/height属性设置的宽度和高度
> 2. 元素的宽度和高度 宽度 = `left-border + left-padding + width + right-padding + right-border` 高度 同理可证
> 3. 元素空间的宽度和高度 宽度 = `left-margin + left-border+ left-padding + width +right-padding + right-border + right-margin` 高度 同理可证

### Box-sizing属性

> CSS3中新增了一个`box-sizing`属性, 这个属性可以保证我们给盒子新增`padding`和`border`之后, 盒子元素的宽度和高度不变

* `box-sizing`属性是如何保证增加`padding`和`border`之后, 盒子元素的宽度和高度不变?
  * 增加`padding`和`border`之后要想保证盒子元素的宽高不变, 那么就必须减去一部分内容的宽度和高度
* 取值:
  * `content-box:`元素的宽高 = 边框 + 内边距 + 内容宽高
  * `border-box:` 元素的宽高 = width/height的宽高

### 盒子居中和内容居中

> `text-align:center;和margin:0 auto;`

* text-align: center;
  * 设置盒子中存储的文字/图片水平居中
* margin:0 auto;
  * 让盒子自己水平居中

### 清空默认边距

> 为了更好的控制盒子的宽高和计算盒子的宽高等等, 编写代码之前第一件事情就是清空默认的边距

* 如何清空默认的边距

```text
/*格式*/
*{
            margin: 0;
            padding: 0;
}
```

{% hint style="info" %}
通配符选择器会找到\(遍历\)当前界面中所有的标签, 所以性能不好,项目中可以使用第三方库的代码进行清空,例如:[YUI](http://yui.yahooapis.com/3.18.1/build/cssreset/cssreset-min.css)
{% endhint %}

### 行高和字号

> 在CSS中所有的行都有自己的行高\(`line-height`\)

* 行高和盒子高不是同一个概念 行高指的是每行内容的高度 盒子高指的是元素的高度
* 文字在行高中默认是垂直居中的
* 要想一行文字在盒子中垂直居中, 那么只需要设置这行文字的"行高等于盒子的高"即可
* 如果一个盒子中有多行文字, 只能通过设置`padding`来让文字居中,而不能使用行高

如果一个盒子中存储的是文字, 那么一般情况下我们会以盒子左边的内边距为基准, 不会以右边的内边距为基准, 因为这个右边的内边距有误差,右边内边距的误差从何而来?

* 因为右边如果放不下一个文字, 那么文字就会换行显示, 所以文字和内边距之间的距离就有了误差
* 顶部的内边距并不是边框到文字顶部的距离, 而是边框到行高顶部的距离

### Margin传递问题

> 在父子元素中， 如果给子元素设置了margin-top， 默认会传递到父元素

解决方案:

1. 给父元素设置边框
2. 或者给父元素添加两行代码 `overflow: hidden; *zoom: 1;`

### 父子元素包裹问题

> 在其它浏览器中， 如果子元素的宽高大于父元素的宽高， 那么不会把父元素撑开 但是在IE6浏览器下， 如果子元素的宽高大于父元素的宽高，那么父元素会被子元素撑开

解决方案:

1. 项目中, 不要让子元素的宽高大于父元素的宽高

> 如果在企业开发中子元素必须要大于父元素， 那么可以添加`overflow: hidden; overflow: hidden`;含义： 将超出父元素的部分剪切掉





