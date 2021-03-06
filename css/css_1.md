# 层叠样式表 (Cascading Style Sheets)

css 样式由**选择符**和**声明**组成，而**声明**又由**属性**和**值**组成

- 选择符：又称选择器，指明网页中要应用样式规则的元素

- 声明：在英文大括号 `{}` 中的的就是声明，属性和值之间用英文冒号 `:` 分隔。当有多条声明时，中间可以英文分号 `;` 分隔，如下所示：

  ```css
  p{
      font-size:12px;
      color:red;
  }
  ```



### CSS注释代码

用 `/*注释语句*/` 来标明（html中使用 `<!--注释语句-->`）



# 内联式css样式

**直接写在现有的HTML标签中，注意要写在元素的开始标签里**

```html
<p style="color:red">这里文字是红色。</p>
```

并且css样式代码要写在`style=""`双引号中，如果有多条css样式代码设置可以写在一起，中间用分号隔开

```html
<p style="color:red;font-size:12px">这里文字是红色。</p>
```



# 嵌入式css样式

**嵌入式css样式，把css样式代码写在`<style type="text/css"></style>`标签之间**

一般情况下嵌入式css样式写在`<head></head>`之间

```html
<head>
<style type="text/css">
span{
color:red;
}
</style>
</head>
```



# 外部式css样式

外部式css样式(也可称为外联式)就是把css代码写一个单独的外部文件中，这个css样式文件以“`.css`”为扩展名，在 `<head>` 内（不是在 `<style` 标签内）使用 `<link>` 标签将css样式文件链接到HTML文件内

```html
<link href="base.css" rel="stylesheet" type="text/css" />
```



# 三种方法的优先级

**就近原则（离被设置元素越近优先级别越高）并且内联式、嵌入式、外部式样式表中css样式是在的相同权值的情况下**



# 标签选择器

标签选择器其实就是html代码中的标签，如`<html>、<body>、<h1>、<p>、<img>`



# 类选择器

```css
.类选器名称{css样式代码;}
```

- 英文圆点开头
- 其中**类选器名称**可以任意起名（但不要起中文噢）

使用方法

1. 使用合适的标签把要修饰的内容标记起来，如下：

   ```html
   <span>胆小如鼠</span>
   ```

2. 使用class="类选择器名称"为标签设置一个类，如下：

   ```html
   <span class="stress">胆小如鼠</span>
   ```

3. 设置类选器css样式，如下：

   ```css
   .stress{color:red;}/*类前面要加入一个英文圆点*/
   ```



# ID选择器

- 为标签设置`id="ID名称"`
- ID选择符的前面是 `#` 号



# 类和ID选择器的区别

**相同点：**

可以应用于任何元素

**不同点：**

- ID选择器在html文档中只能使用一次，而类选择器可以使用多次
- 可以使用类选择器词列表方法为一个元素同时设置多个样式

```css
.stress{
    color:red;
}
.bigsize{
    font-size:25px;
}
```

```html
<p>到了<span class="stress bigsize">三年级</span>下学期时，我们班上了一节公开课...</p>
```



# 子选择器

一个比较有用的选择器**子选择器**，即大于符号 `>` 用于选择指定标签元素的**第一代子元素**

```css
.food>li{border:1px solid red;}
```

这行代码会使class名为`food`下的子元素`li`（水果、蔬菜）加入红色实线边框



# 包含（后代）选择器

**包含选择器**，即加入空格，用于选择指定标签元素下的**后辈元素**



# 通用选择器

使用一个 `*` 号指定，作用是匹配html中**所有**标签元素

```css
* {color:red}
```



# 伪类选择符

它允许给html不存在的标签（标签的某种状态）设置样式，比如给html中一个标签的**鼠标划过的状态**来设置字体颜色：

```css
a:hover{color:red:}
```



# 分组选择符

为html多个标签元素设置同一个样式时，使用分组选择器 `,`

```css
h1,span{color:red}
```



