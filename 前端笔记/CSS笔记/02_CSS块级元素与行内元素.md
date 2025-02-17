- [1. **块级元素（Block-Level Elements）**](#1-块级元素block-level-elements)
  - [特征：](#特征)
  - [例子：](#例子)
  - [示例效果：](#示例效果)
- [2. **行内元素（Inline Elements）**](#2-行内元素inline-elements)
  - [特征：](#特征-1)
  - [例子：](#例子-1)
  - [示例效果：](#示例效果-1)
- [3. **区别总结**](#3-区别总结)
- [4. **转变：块级与行内的转换**](#4-转变块级与行内的转换)
- [5. **应用场景**](#5-应用场景)
- [总结](#总结)

在HTML和CSS中，元素的显示类型分为 **块级元素** 和 **行内元素**。它们的主要区别在于它们的布局方式和占据空间的方式。理解这两种元素的区别对于网页布局至关重要。

### 1. **块级元素（Block-Level Elements）**

#### 特征：
- **占据整行**：块级元素默认会从新的一行开始，并占据父容器的整个宽度（除非你设置宽度）。它的后面会有换行。
- **宽度和高度**：你可以为块级元素设置宽度（`width`）和高度（`height`），它会按照这些设置占据相应的空间。
- **可以包含其他块级元素和行内元素**：块级元素可以包含其他块级元素和行内元素。
- **常见元素**：`<div>`, `<p>`, `<h1>`, `<ul>`, `<ol>`, `<li>`, `<section>`, `<article>`, `<header>`, `<footer>` 等。

#### 例子：
```html
<div>我是一个块级元素</div>
<p>这是一个段落，属于块级元素</p>
```

#### 示例效果：
- `<div>` 和 `<p>` 元素会占据父容器的整个宽度，并且在它们之前和之后会有换行。

```css
div {
    width: 80%;
    height: 100px;
    background-color: lightblue;
}
```

### 2. **行内元素（Inline Elements）**

#### 特征：
- **不占据整行**：行内元素不会强制换行，它们仅占据自身内容的宽度，也就是说，它们会与其他行内元素并排显示。
- **无法设置宽度和高度**：你无法通过CSS设置行内元素的宽度（`width`）和高度（`height`）。它们的尺寸是由内容决定的。
- **不能包含块级元素**：行内元素通常不能包含块级元素，只能包含其他行内元素或文本。
- **常见元素**：`<span>`, `<a>`, `<strong>`, `<em>`, `<img>`, `<b>`, `<i>` 等。

#### 例子：
```html
<span>这是一个行内元素</span>
<a href="#">这是一个链接</a>
```

#### 示例效果：
- `<span>` 和 `<a>` 元素不会换行，它们与其他行内元素并排显示。

```css
span {
    color: blue;
}
```

### 3. **区别总结**

| **特征**             | **块级元素**                                           | **行内元素**                                 |
| -------------------- | ------------------------------------------------------ | -------------------------------------------- |
| **显示方式**         | 占据整个父容器的宽度（默认从新的一行开始）             | 仅占据元素内容的宽度，和其他行内元素并排显示 |
| **是否换行**         | 是，前后会有换行                                       | 否，元素不会换行                             |
| **宽度与高度**       | 可以设置宽度和高度                                     | 不能设置宽度和高度，大小由内容决定           |
| **能否包含其他元素** | 可以包含其他块级元素和行内元素                         | 只能包含其他行内元素或文本                   |
| **常见标签**         | `<div>`, `<p>`, `<ul>`, `<li>`, `<header>`, `<footer>` | `<span>`, `<a>`, `<b>`, `<i>`, `<img>`       |

### 4. **转变：块级与行内的转换**

有时，我们可以通过 CSS 来改变元素的显示类型，使得一个原本是块级的元素变为行内元素，或者反过来。这是通过 `display` 属性来实现的。

- **`display: inline;`**：使块级元素变为行内元素。
  ```css
  div {
      display: inline;
  }
  ```

- **`display: block;`**：使行内元素变为块级元素。
  ```css
  span {
      display: block;
  }
  ```

- **`display: inline-block;`**：使元素既具有行内元素的特性（不会换行），又可以设置宽度和高度（像块级元素）。
  ```css
  span {
      display: inline-block;
      width: 100px;
      height: 50px;
  }
  ```

### 5. **应用场景**
- **块级元素**：常用于结构化页面，通常用作布局容器，例如`<div>` 和`<section>` 用来分组和容纳其他元素。
- **行内元素**：常用于文字和小元素的样式控制，如`<span>` 和`<a>`。它们不会破坏布局，并且可以灵活地嵌入到其他内容中。

### 总结

- **块级元素**：占据整行，能包含其他块级元素，具有宽度和高度的设置。
- **行内元素**：仅占据内容本身的宽度，不能设置宽度和高度，和其他行内元素一起并排显示。