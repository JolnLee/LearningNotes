# 背景相关

### 背景尺寸

> 背景尺寸属性是CSS3中新增的一个属性, 专门用于设置背景图片大小

* `background-size:    ;`
* 取值:
  * 具体像素\(宽,高\)
  * 百分比\(以元素宽高为100%\)
  * 等比拉伸\(`auto`/宽 , `auto`/高\);
  * `cover`:告诉系统图片需要等比拉伸 告诉系统图片需要拉伸到宽度**和**高度都填满元素
  * `contain`:告诉系统图片需要等比拉伸 告诉系统图片需要拉伸到宽度**或**高度都填满元素

### 背景图片定位区域

> 告诉系统背景图片从什么区域开始显示,默认情况下就是从padding区域开始显示

* `background-origin:      ;`
* 取值:
  * `padding-box` :\(从`padding`区域开始显示\)
  * `border-box`:\(从`border`开始显示\)
  * `content` :\(从内容区开始显示\)

### 背景绘制区域

> 专门用于指定从哪个区域开始绘制背景的, 默认情况下会从border区域开始绘制背景

* `background-clip:        ;`
* 取值:
  * `padding-box` :\(从`padding`区域开始绘制\)
  * `border-box`:\(从`border`开始绘制\)
  * `content` :\(从内容区开始绘制\)

### 多重背景图片

> 多张背景图片之间用逗号隔开即可

* 先添加的背景图片会盖住后添加的背景图片 建议在编写多重背景时拆开编写

### 图片相关\(补充\)

> 如果图片宽度大于父元素宽度,不能使用`margin/text-align`让图片居中?

* 解决方案:
  * 使用定位流让图片居中
  * 使用`margin: 0 -100%;`需要给父元素添加`text-align:center`



