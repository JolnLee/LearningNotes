# 动画模块

## 动画模块

### 过渡和动画的异同

* 1不同点
  * 过渡必须人为的触发才会执行动画 动画不需要人为的触发就可以执行
* 相同点
  * 过渡和动画都是用来给元素添加动画的 过渡和动画都是系统新增的一些属性
  * 过渡和动画都需要满足三要素才会有动画效果
* 三要素:
  * 告诉系统需要执行xxx动画
  * 然后我们需要自己创建一个名称叫做xxx的动画
  * 告诉系统动画持续的时长
  * 例:

```text
/*1.告诉系统需要执行哪个动画*/
animation-name: xxx;

/*3.告诉系统动画持续的时长*/
animation-duration: 3s;

/*2.告诉系统我们需要自己创建一个名称叫做xxx的动画*/
@keyframes xxx {
    from{
        margin-left: 0;
    }
    to{
        margin-left: 500px;
    }
}
```

### 其他属性

* `animation-name: sport;`动画名
* `animation-duration: 2s;`持续时长
* `animation-timing-function: linear;`动画运动曲线
* `animation-iteration-count: 3;`动画次数\(取值:infinity 无限次\)
* `animation-direction: alternate;`往返动画
  * 取值: normal, 默认的取值, 执行完一次之后回到起点继续执行下一次 alternate, 往返动画, 执行完一次之后往回执行下一次\(返回动画也算一次\);
* `animation-play-state: paused`暂停/执行\(paused/running\);
* `animation-fill-mode:both;`指定动画等待状态和结束状态的样式
  * 取值:none: 不做任何改变 forwards: 让元素结束状态保持动画最后一帧的样式 backwards: 让元素等待状态的时候显示动画第一帧的样式 both: 让元素等待状态显示动画第一帧的样式, 让元素结束状态保持动画最后一帧的样式

### 连写

* 动画模块连写格式
  * `animation:动画名称 动画时长 动画运动速度 延迟时间 执行次数 往返动画;`
* 动画模块连写格式的简写
  * `animation:动画名称 动画时长;`
* 注意点:
  * 动画中如果有和默认样式同名的属性,会覆盖默认样式的属性
  * 编写动画时,固定不变的值写在前面,需要变化的值写在后面
* 运动曲线可以传`steps(N)`方法,将动画分为N步更有节奏感.

