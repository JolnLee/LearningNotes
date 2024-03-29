# 浮动

### 网页布局方式

> 网页的布局方式其实就是指浏览器是如何对网页中的元素进行排版的

1. 标准流\(文档流/普通流\)排版方式
   1. 其实浏览器默认的排版方式就是标准流的排版方式
   2. 在CSS中将元素分为三类, 分别是块级元素/行内元素/行内块级元素
   3. 在标准流中有两种排版方式, 一种是垂直排版, 一种是水平排版, 如果元素是块级元素, 那么就会垂直排版 , 如果元素是行内元素/行内块级元素, 那么就会水平排版
2. 浮动流排版方式
   1. 浮动流是一种"半脱离标准流"的排版方式
   2. 浮动流只有一种排版方式, 就是水平排版. 它只能设置某个元素左对齐或者右对齐

> 1. 浮动流中没有居中对齐, 也就是没有`center`这个取值 
> 2. 在浮动流中是不可以使用`margin: 0 auto;`

* 特点:
  * 在浮动流中是不区分块级元素/行内元素/行内块级元素的,所以元素都可以水平排版
  * 在浮动流中无论是块级元素/行内元素/行内块级元素都可以设置宽高
  * 综上所述, 浮动流中的元素和标准流中的行内块级元素很像

#### 定位流排版方式

{% page-ref page="position-css.md" %}

### 脱标

> 脱标: 脱离标准流
>
> 当某一个元素浮动之后, 那么这个元素看上去就像被从标准流中删除了一样, 这个就是浮动元素的脱标

* 影响:
  * 如果前面一个元素浮动了, 而后面一个元素没有浮动 , 那么前面一个元素就会盖住后面一个元素

### 排序规则

1. 相同方向上的浮动元素, 先浮动的元素会显示在前面, 后浮动的元素会显示在后面
2. 不同方向上的浮动元素, 左浮动会找左浮动, 右浮动会找右浮动
3. 浮动元素浮动之后的位置, 由浮动元素浮动之前在标准流中的位置来确定

### 贴靠现象

1. 如果父元素的宽度能够显示所有浮动元素, 那么浮动的元素会并排显示
2. 如果父元素的宽度不能显示所有浮动元素, 那么会从最后一个元开始往前贴靠
3. 如果贴靠了前面所有浮动元素之后都不能显示, 最终会贴靠到父元素的左边或者右边

### 字围现象

> 浮动元素不会挡住没有浮动元素中的文字, 没有浮动的文字会自动给浮动的元素让位置,这个就是浮动元素字围现象

### 高度问题

> 1. 在标准流中内容的高度可以撑起父元素的高度
> 2. 在浮动流中浮动的元素是不可以撑起父元素的高度的

