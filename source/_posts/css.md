---
title: CSS
---
# CSS

*CSS* :(*C*ascading *S*tyle *S*heets).

CSS 描述了如何在屏幕、纸张或其他媒体上显示 HTML 元素

## 语法

CSS 规则集（rule-set）由选择器和声明块组成：

![1692231577571](C:\Users\Moonykun\AppData\Roaming\Typora\typora-user-images\1692231577571.png)

- 选择器指向您需要设置样式的 HTML 元素。


- 声明块包含一条或多条用分号分隔的声明。


- 每条声明都包含一个 CSS 属性名称和一个值，以冒号分隔。


- 多条 CSS 声明用分号分隔，声明块用花括号括起来。


## CSS 选择器

- 简单选择器（根据名称、id、类来选取元素）
- [组合器选择器](https://www.w3school.com.cn/css/css_combinators.asp)（根据它们之间的特定关系来选取元素）
- [伪类选择器](https://www.w3school.com.cn/css/css_pseudo_classes.asp)（根据特定状态选取元素）
- [伪元素选择器](https://www.w3school.com.cn/css/css_pseudo_elements.asp)（选取元素的一部分并设置其样式）
- [属性选择器](https://www.w3school.com.cn/css/css_attribute_selectors.asp)（根据属性或属性值来选取元素）

### 简单选择器

#### **CSS 元素选择器：**

```css
p {
  text-align: center;
  color: red;
}
```

#### **CSS id 选择器**

id 选择器使用 HTML 元素的 id 属性来选择特定元素。

元素的 id 在页面中是唯一的，因此 id 选择器用于选择一个唯一的元素！

```css
#para1 {
  text-align: center;
  color: red;
}
```

#### **CSS 类选择器**

```css
.center {
  text-align: center;
  color: red;
}
```

特定的 HTML 元素会受类的影响

```css
p.center {
  text-align: center;
  color: red;
}
// 只有具有 class="center" 的 <p> 元素会居中对齐：
```

#### CSS 通用选择器

```css
* {
  text-align: center;
  color: blue;
}
// 通用选择器（*）选择页面上的所有的 HTML 元素。
```

#### CSS 分组选择器

```css
h1, h2, p {
  text-align: center;
  color: red;
}
// 选取所有 <h1> 元素和所有 <h2> <p>元素。
```

## 如何添加 CSS

有三种插入样式表的方法：外部 CSS,内部 CSS,行内 CSS

外部 CSS

```css
<link rel="stylesheet" type="text/css" href="mystyle.css">
// 定义在head标签内
```

内部 CSS

```css
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
} 
</style>
```

行内 CSS

```css
<h1 style="color:blue;text-align:center;">This is a heading</h1>
```

页面中的所有样式将按照以下规则“层叠”为新的“虚拟”样式表，其中第一优先级最高：

1. 行内样式（在 HTML 元素中）
2. 外部和内部样式表（在 head 部分）
3. 浏览器默认样式

注意：外部和内部样式表的优先级由其在html内定义的位置有关

## CSS颜色

指定颜色是通过使用预定义的颜色名称，或 RGB、HEX、HSL、RGBA、HSLA 值。

### RGB 值

rgb(*red*, *green*, *blue*)

值区间为0-255

### RGBA 值

RGBA 颜色值是具有 alpha 通道的 RGB 颜色值的扩展 - 它指定了颜色的不透明度。

rgba(*red*, *green*, *blue*, *alpha*)

### HEX 值

在 CSS 中，可以使用以下格式的十六进制值指定颜色：#*rrggbb*

因为红色设置为最大值（ff），其他设置为最小值（00）。

### HSL 值

hsla(*hue*, *saturation*, *lightness*)

色相（*hue*）是色轮上从 0 到 360 的度数。0 是红色，120 是绿色，240 是蓝色。

饱和度（*saturation*）是一个百分比值，0％ 表示灰色阴影，而 100％ 是全色。

亮度（*lightness*）也是百分比，0％ 是黑色，50％ 是既不明也不暗，100％是白色。

**hsl(172, 100%, 50%)**

### HSLA 值

hsla(*hue*, *saturation*, *lightness*, *alpha*)

*alpha* 参数是介于 0.0（完全透明）和 1.0（完全不透明）之间的数字：

## CSS 背景

`background-color` 属性指定元素的背景色。

`background-image` 属性指定用作元素背景的图像。(默认情况下，图像会重复，以覆盖整个元素。)

```css
body {
  background-image: url("gradient_bg.png");
  background-repeat: repeat-x;
}
```

background-repeat  repeat-x(x轴上重复)，no-repeat（只显示一次）

`background-position` 属性用于指定背景图像的位置。（right top）;

`background-attachment` 属性指定背景图像是应该滚动还是固定的（不会随页面的其余部分一起滚动） fixed 固定， scroll 随页面滚动

background - 简写属性：

```css
body {
  background: #ffffff url("tree.png") no-repeat right top;
}
```

在使用简写属性时，属性值的顺序为：

- background-color
- background-image
- background-repeat
- background-attachment
- background-position

## CSS 边框属性

`border` 属性允许您指定元素边框的样式、宽度和颜色

`border-style` 属性指定要显示的边框类型。

允许以下值：

- `dotted` - 定义点线边框
- `dashed` - 定义虚线边框
- `solid` - 定义实线边框
- `double` - 定义双边框
- `groove` - 定义 3D 坡口边框。效果取决于 border-color 值
- `ridge` - 定义 3D 脊线边框。效果取决于 border-color 值
- `inset` - 定义 3D inset 边框。效果取决于 border-color 值
- `outset` - 定义 3D outset 边框。效果取决于 border-color 值
- `none` - 定义无边框
- `hidden` - 定义隐藏边框

`border-style` 属性可以设置一到四个值（用于上边框、右边框、下边框和左边框）

`border-width` 属性指定四个边框的宽度。

```css
p.three {
  border-style: solid;
  border-width: 25px 10px 4px 35px; /* 上边框 25px，右边框 10px，下边框 4px，左边框 35px */
}
```

`border-color` 属性用于设置四个边框的颜色。

```css
p.one {
  border-style: solid;
  border-color: red green blue yellow; /* 上红、右绿、下蓝、左黄 */
}
```

`**border-radius` 属性用于向元素添加圆角边框：**

## CSS 外边距

CSS 拥有用于为元素的每一侧指定外边距的属性：

- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

所有外边距属性都可以设置以下值：

- auto - 浏览器来计算外边距
- *length* - 以 px、pt、cm 等单位指定外边距
- % - 指定以包含元素宽度的百分比计的外边距
- inherit - 指定应从父元素继承外边距

您可以将 margin 属性设置为 `auto`，以使元素在其容器中水平居中。

然后，该元素将占据指定的宽度，并且剩余空间将在左右边界之间平均分配。

外边距合并

外边距合并（叠加）是一个相当简单的概念。但是，在实践中对网页进行布局时，它会造成许多混淆。

简单地说，外边距合并指的是，当两个**垂直**外边距相遇时，它们将形成一个外边距。合并后的外边距的高度等于两个发生合并的外边距的高度中的较大者。

## CSS 内边距

## Padding - 单独的边

CSS 拥有用于为元素的每一侧指定内边距的属性：

- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`

所有内边距属性都可以设置以下值：

- *length* - 以 px、pt、cm 等单位指定内边距
- % - 指定以包含元素宽度的百分比计的内边距
- inherit - 指定应从父元素继承内边距

**提示：**不允许负值。

## CSS 框模型



## 附：

CSS 注释：

```css
/* 这是一条单行注释 */
p {
  color: red;
}
```

