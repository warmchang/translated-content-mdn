---
title: CSS 流式布局
slug: Web/CSS/CSS_display/Flow_layout
---

{{CSSRef}}

"文档流"或"流式布局"是在对布局进行任何更改之前，在页面上显示"块"和"内联"元素的方式。这个"流"本质上是一系列的事物，它们都在你的布局中一起工作，并且互相了解。一旦某部分脱离了"流"，它就会独立地工作。

在文档流中，内联元素按内联方向显示，即词语在依据文件写作模式的句子中表示的方向。块元素则一个接一个地显示，就像该文档的写作模式中的段落一样。因此在英语中，内联元素从左边开始一个接一个地显示，块元素从顶部开始向下显示并移动页面。

## 示例

下面的示例演示块和内联级别框。两个带有绿色边框的段落元素是"块"级，其中一个在另一个下面显示。

第一个句子还包括一个带有蓝色背景的 span 元素。这是行内级别，因此显示在句子的适当位置。

{{EmbedGHLiveSample("css-examples/layout/normal-flow.html", '100%', 720)}}

## 参见

- [常规流中的块和内联布局](/zh-CN/docs/Web/CSS/CSS_display/Block_and_inline_layout_in_normal_flow)
- [应用或脱离流式布局](/zh-CN/docs/Web/CSS/CSS_display/In_flow_and_out_of_flow)
- [格式化上下文简介](/zh-CN/docs/Web/CSS/CSS_display/Introduction_to_formatting_contexts)
- [流式布局和书写模式](/zh-CN/docs/Web/CSS/CSS_display/Flow_layout_and_writing_modes)
- [流式布局和溢出](/zh-CN/docs/Web/CSS/CSS_display/Flow_layout_and_overflow)
