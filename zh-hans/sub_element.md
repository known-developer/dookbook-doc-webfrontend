TOPICS: <sub>
AUTHORS: Wizard; wizardforcel@mozilla.net; mdn:wizardforcel

# `<sub>`

**HTML `<sub>` 元素**定义了一个文本区域，出于排版的原因，与主要的文本相比，应该展示得更低并且更小。

|  |  |
| :-- | :-- |
| **内容分类** | 流式内容和短语内容 |
| **允许的内容** | 短语内容 |
| **标签省略** | 不允许，开始标签和结束标签都不能省略。 |
| **允许的父元素** | 可以包含短语内容的任意元素 |
| **允许的 ARIA 角色** | 任意 |
| **DOM 接口** | HTMLElement |

## 属性

这个元素仅仅包含全局属性

## 用法注解

- 这个元素应该只用于排版目的，也就是改变文本的位置会改变含义，例如在数学中（t2，也可以考虑使用 MathML 公式）或者化学符号（`H2O`）。
- 这个元素不能用于样式上的目的，比如产品名称 LaTeX 的样式，这时应该使用 CSS 样式： `vertical-align` 属性的 `sub` 值能实现相同效果

## 示例

```html
<p>The chemical formula of water: H<sub>2</sub>O</p>
```
