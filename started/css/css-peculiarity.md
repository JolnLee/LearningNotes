# CSS三大特性

### 继承性

* 给父元素设置一些属性, 子元素也可以使用, 这个我们就称之为继承性
* 应用场景: 
  * 一般用于设置网页上的一些共性信息, 例如网页的文字颜色, 字体,文字大小等内容

{% hint style="info" %}
并不是所有的属性都可以继承, 只有以`color/font-/text-/line-`开头的属性才可以继承 
{% endhint %}

> 1. 在CSS的继承中不仅仅是儿子可以继承, 只要是后代都可以继承 
> 2. 继承性中的特殊性
>    1. a标签的文字颜色和下划线是不能继承的
>    2. 标签的文字大小是不能继承的

### 层叠性

* 层叠性就是CSS处理冲突的一种能力

> 层叠性只有在多个选择器选中"同一个标签", 然后又设置了"相同的属性", 才会发生层叠性

### 优先级

* 当多个选择器选中同一个标签, 并且给同一个标签设置相同的属性时, 如何层叠就由优先级来确定
* 优先级判断的三种方式:
* 间接选中就是指继承 如果是间接选中, 那么就是采用就近原则 
* 相同选择器\(直接选中\) 如果都是直接选中, 并且都是同类型的选择器, 那么就是后面覆盖前面
* 不同选择器\(直接选中\) 如果都是直接选中, 并且不是相同类型的选择器, 那么就会按照选择器的优先级来层叠
  * id&gt;类&gt;标签&gt;通配符&gt;继承&gt;浏览器默认

#### important

* 作用: 用于提升某个直接选中标签的选择器中的某个属性的优先级的, 可以将被指定的属性的优先级提升为最高

{% hint style="info" %}
1. `!important`只能用于直接选中, 不能用于间接选中
2. 通配符选择器选中的标签也是直接选中的
3. `!important`只能提升被指定的属性的优先级, 其它的属性的优先级不会被提升
4. `!important`必须写在属性值得分号前面 
5. `!important`前面的感叹号不能省略
{% endhint %}

#### 优先级的权重

* 当多个选择器混合在一起使用时, 我们可以通过计算权重来判断谁的优先级最高
* 权重的计算规则
  * 首先先计算选择器中有多少个id, id多的选择器优先级最高
  * 如果id的个数一样, 那么再看类名的个数, 类名个数多的优先级最高
  * 如果类名的个数一样, 那么再看标签名称的个数, 标签名称个数多的优先级最高
  * 如果id个数一样, 类名个数也一样, 标签名称个数也一样, 那么此时后写覆盖先写

{% hint style="info" %}
只有选择器是直接选中标签的才需要计算权重, 否则一定会听直接选中的选择器
{% endhint %}

