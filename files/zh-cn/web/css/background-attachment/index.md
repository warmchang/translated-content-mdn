---
title: background-attachment
slug: Web/CSS/background-attachment
---

**`background-attachment`** [CSS](/zh-CN/docs/Web/CSS) 属性决定背景图像的位置是在{{glossary("视口")}}内固定，或者随着包含它的区块滚动。

{{InteractiveExample("CSS Demo: background-attachment")}}

```css interactive-example-choice
background-attachment: scroll;
```

```css interactive-example-choice
background-attachment: fixed;
```

```css interactive-example-choice
background-attachment: local;
```

```css interactive-example-choice
background-attachment: local, scroll;
```

```css interactive-example-choice
background-attachment: scroll, local;
```

```html interactive-example
<section id="default-example">
  <div id="example-element">
    London. Michaelmas term lately over, and the Lord Chancellor sitting in
    Lincoln's Inn Hall. Implacable November weather. As much mud in the streets
    as if the waters had but newly retired from the face of the earth, and it
    would not be wonderful to meet a Megalosaurus, forty feet long or so,
    waddling like an elephantine lizard up Holborn Hill. London. Michaelmas term
    lately over, and the Lord Chancellor sitting in Lincoln's Inn Hall.
    Implacable November weather. As much mud in the streets as if the waters had
    but newly retired from the face of the earth, and it would not be wonderful
    to meet a Megalosaurus, forty feet long or so, waddling like an elephantine
    lizard up Holborn Hill.
  </div>
</section>
```

```css interactive-example
body {
  overflow: scroll;
}

#default-example {
  height: 600px;
}

#example-element {
  max-width: 20rem;
  height: 100%;
  background:
    url("/shared-assets/images/examples/lizard.png") right 3rem top 1rem / 15rem
      no-repeat,
    url("/shared-assets/images/examples/moon.jpg") center / 10rem;
  color: #ff5454;
  font-size: 1.5em;
  font-weight: bold;
  overflow: auto;
  padding: 20px;
  text-shadow:
    0 0 0.6rem #000,
    0 0 0.6rem #000;
}
```

## 语法

```css
/* 关键 属性值 */
background-attachment: scroll;
background-attachment: fixed;
background-attachment: local;

/* 全局 属性值 */
background-attachment: inherit;
background-attachment: initial;
background-attachment: unset;
```

### 取值

- `fixed`
  - : 此关键属性值表示背景相对于视口固定。即使一个元素拥有滚动机制，背景也不会随着元素的内容滚动。
- `local`
  - : 此关键属性值表示背景相对于元素的内容固定。如果一个元素拥有滚动机制，背景将会随着元素的内容滚动，并且背景的绘制区域和定位区域是相对于可滚动的区域而不是包含他们的边框。
- `scroll`
  - : 此关键属性值表示背景相对于元素本身固定，而不是随着它的内容滚动（对元素边框是有效的）。

### 标准语法

{{csssyntax}}

## 例子

### 简单的例子

#### CSS 样式表

```css
p {
  background-image: url("star-solid.gif");
  background-attachment: fixed;
}
```

#### HTML 源码

```html
<p>
  There were doors all round the hall, but they were all locked; and when Alice
  had been all the way down one side and up the other, trying every door, she
  walked sadly down the middle, wondering how she was ever to get out again.
</p>
```

#### 效果

{{EmbedLiveSample("简单的例子")}}

### 多背景图支持

此属性支持多张背景图片。你可以用逗号分隔来为每一张背景图片指定不同的`<attachment>属性值。`每一张背景图片顺序对应相应的 attachment 属性。

#### CSS 样式表

```css
p {
  background-image: url("star-solid.gif"), url("star-transparent.gif");
  background-attachment: fixed, scroll;
  background-repeat: no-repeat, repeat-y;
}
```

#### HTML 源码

```html
<p>
  There were doors all round the hall, but they were all locked; and when Alice
  had been all the way down one side and up the other, trying every door, she
  walked sadly down the middle, wondering how she was ever to get out again.
  Suddenly she came upon a little three-legged table, all made of solid glass;
  there was nothing on it except a tiny golden key, and Alice's first thought
  was that it might belong to one of the doors of the hall; but, alas! either
  the locks were too large, or the key was too small, but at any rate it would
  not open any of them. However, on the second time round, she came upon a low
  curtain she had not noticed before, and behind it was a little door about
  fifteen inches high: she tried the little golden key in the lock, and to her
  great delight it fitted!
</p>
```

#### 效果

{{EmbedLiveSample("多背景图支持")}}

## 规范

{{Specifications}}

{{cssinfo}}

## 浏览器兼容性

{{Compat}}

## 参见

- [更多背景图](/zh-CN/docs/Web/CSS/CSS_backgrounds_and_borders/Using_multiple_backgrounds)
