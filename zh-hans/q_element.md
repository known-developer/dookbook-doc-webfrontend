TOPICS: <q>

# `<q>`

**HTML`<q>`元素** 表示所包含的文本是短内联引号。 大多数现代浏览器通过将文本用引号引起来来实现此目的。 此元素用于不需要段落分隔符的短引号； 对于长引用，请使用[`<blockquote>`](/zh-hans/webfrontend/<blockquote>)元素。

|  |  |
| :-- | :-- |
| **内容分类** | 流程内容，措辞内容，可触知内容. |
| **允许的内容** | 短语内容. |
| **标签遗漏** | 无，开始标签和结束标签都是必需的. |
| **允许的父元素** | 任何接受短语内容的元素. |
| **允许的 ARIA 角色** | 任何 |
| **DOM 接口** | `HTMLQuoteElement` |

!!! warn "Don't try this at home"
    使用说明：大多数现代浏览器都会在`<q>`元素内的文本周围自动添加引号。 在较旧的浏览器中可能需要样式规则才能添加引号。

## 属性

此元素包括[全局属性](https://wiki.developer.mozilla.org/en-US/docs/HTML/Global_attributes).

| 属性 | 描述 |
| :-- | :-- |
| `cite` | 此属性的值是一个URL，它为引用的信息指定源文档或消息。 该属性旨在指向解释上下文或引用内容的信息. |

## 示例

```html
<p>According to Mozilla's website,
  <q
  cite="https://www.mozilla.org/en-US/about/history/details/">Firefox 1.0
  was released in 2004 and became a big success.</q></p>
```
