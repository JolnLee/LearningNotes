# 多媒体标签

### Video标签

* 作用: 播放视频
* video标签的属性
  * src: 设置需要播放的视频地址
  * autoplay: 是否需要自动播放视频
  * controls: 是否需要显示控制条
  * poster: 没有播放之前显示的占位图片
  * loop: 一般用于做广告视频, 视频播放完毕之后是否需要循环播放
  * preload: 预加载视频, 但是需要注意preload和autoplay相冲, 如果设置了autoplay属性, 那么preload属性就会失效
  * muted:静音
  * width/height: 和img标签中的一样
* 格式:
  * 第一种格式:`<video src=""></video>`
  * 第二种格式:

```text
<video>
    <source src="" type=""></source>
    <source src="" type=""></source>
</video>
```

* video标签的第二种格式存在的意义就是为了解决浏览器适配问题

{% hint style="info" %}
让所有浏览器都通过video标签播放视频的一个前提条件, 就是浏览器必须支持HTML5标签, 否则同样无法播放;
{% endhint %}

> 为了让过去的一些浏览器也能够通过video标签来播放视频,我们可以通过一个html5media的JS框架来实现;

### Audio标签

* 作用: 播放音频
* 格式:
  * 第一种格式`<audio src=""></audio>`
  * 第二种格式:

```text
<audio>
    <source src="" type="">
</audio>
```

> video中能够使用的属性在audio标签中大部分都能够使用, 并且功能都一样 只不过有3个属性不能用, height/width/poster;

### 详情和概要标签

* 作用:利用summary标签来描述概要信息, 利用details标签来描述详情信息
* 默认情况下是折叠展示, 想看见详情必须点击
* 格式:

```text
<details>
    <summary>概要信息</summary>
    详情信息
</details>
```

### Marquee标签

* 作用: 跑马灯
* 格式:`<marquee>内容</marquee>`
* 属性:
  * direction: 设置滚动方向 left/right/up/down
  * scrollamount: 设置滚动速度, 值越大就越快
  * loop: 设置滚动次数, 默认是-1, 也就是无限滚动
  * behavior: 设置滚动类型 slide滚动到边界就停止, alternate滚动到边界就弹回

{% hint style="info" %}
marquee标签不是W3C推荐的标签, 在W3C官方文档中也无法查询这个标签, 但是各大浏览器对这个标签的支持非常好;
{% endhint %}



