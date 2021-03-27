# 表单标签

## 表单

* 表单就是专门用来收集用户信息的

### 表单元素

* 表单元素还是HTML中的一些标签, 只不过比较特殊, 在浏览器中所有的表单标签都有特殊的外观和默认的功能

{% hint style="info" %}
表单元素一定要写在表单中;
{% endhint %}

### 表单的格式

```text
<form>
    <表单元素>
</form>
```

### 常见的表单元素

* input标签, input标签有一个type属性, 这个属性有很多类型的取值, 取值的不同就决定了input标签的功能和外观不同
* 例如:

```text
    <!--明文输入框-->
    <input type="text" name="aa"><br>
    <!--密码输入框-->
    <input type="password" name="bb"><br>
    <!--定义一个普通按钮作用:配合JS完成一些操作-->
    <input type="button" value="我是按钮" onclick="alert('lnj')">
    <!--定义一个图片按钮作用:配合JS完成一些操作-->
    <input type="image" src="images/register.jpg" onclick="alert('lnj')">
    <!--定义重置按钮作用:清空表单中的数据
    注意点:
        重置按钮有默认的按钮标题, 默认叫做重置也可以通过value属性来修改默认标题
    -->
    <input type="reset" value="清空">
    <!--定义提交按钮
    作用:将表单中的数据提交到远程服务器
    注意点:
        要想把表单中的数据提交到远程服务器,必须满足两个条件
            1.告诉表单需要提交到哪个服务器可以通过form标签的action属性来告诉表单,
              需要提交到那个服务器
            2.告诉表单,表单中的哪些数据需要提交
    -->
    <input type="submit">
    <!--隐藏域
    作用: 用于后台的收集用户的一些数据, 隐藏域是不会出现在界面中的
    -->
    <input type="hidden" name="cc" value="it666">
    <!--单选框 单项选择-->
    <input type="radio" name="gender">
    <!--多选框-->
    <input type="checkbox" name="sport" value="basketball">
    <!--
    在单选框和多选框中,所有的项目的name必须一致
    在表单标签中,除了按钮标签以外的标签,都可以通过value来指定需要提交到服务器的数据
    -->
```

### Label标签

* 默认情况下文字和输入框是没有关联关系的, 也就是说点击文字输入框不会聚焦, 如果想点击文字时让对应的输入框聚焦, 那么就需要让文字和输入框进行绑定,所以我们可以使用Label标签

#### 绑定的格式:

* 将文字利用label标签包裹起来
* 给输入框添加一个id属性
* 在label标签中通过for属性和输入框中的id进行绑定即可

```text
<label for="account">账号:</label><input type="text" id="account">
```

### Datalist标签

* 作用: 给输入框绑定待选项

```text
<datalist>
    <option>待选项内容</option>
</datalist>
```

#### 绑定的格式:

* 一个输入框,一个datalist列表
* 给datalist列表标签添加一个id
* 给输入框添加一个list属性,将datalist的id对应的值赋值给list属性即可

```text
请输入你的车型: <input type="text" list="cars">
<datalist id="cars">
    <option>奔驰</option>
    <option>宝马</option>
    <option>奥迪</option>
    <option>路虎</option>
    <option>宾利</option>
</datalist>
```

### 表单标签-H5

```text
    <!--可以自动校验输入的内容是否符合邮箱的格式-->
    邮箱:<input type="email"><br>
    <!--可以自动校验输入的内容是否是URL地址-->
    域名:<input type="url"><br>
    <!--输入框中只能输入数字-->
    电话:<input type="number"><br>
    <!--可以通过日历来选择时间-->
    时间:<input type="date"><br>
    <!--可以通过取色板来选择颜色-->
    颜色: <input type="color"><br>
```

### Select标签

* 作用: 用于定义下拉列表
* 格式:

```text
<select>
    <optgroup label="分组名称">
        <option>列表数据</option>
    </optgroup>
</select>
```

> 1. 下拉列表不能输入内容, 但是可以直接在列表中选择内容;
> 2. 可以通过给option标签添加一个selected属性来指定列表的默认值;
> 3. 可以通过给option标签包裹一层optgroup标签来给下拉列表中的数据分类;

### Textarea标签

* 作用: 定义一个多行输入框
* 格式:`<textarea></textarea>`

> 1. 默认情况下输入框可以无限换行;
> 2. 默认情况下输入框有自己的宽度和高度;
> 3. 默认情况下输入框是可以手动拉伸的;
> 4. 可以通过cols和rows来指定输入框的宽度和高度, 但是虽然指定了列数和行数, 但是还是可以无限往下输入;

